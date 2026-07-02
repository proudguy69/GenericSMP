<template>
    <UHeader>
        <template #title>
            <div class="flex gap-2 items-center">
                <img src="https://mc-heads.net/avatar/f97fd1713e7149528e4ecb8f85cb262f" class=" h-8">
                <span>GenericSMP</span>
            </div>
        </template>

        <template #right>
            <UButton class="bg-[#5865F2] hover:bg-[#E0E3FF] hover:cursor-pointer" icon="ic:baseline-discord" to="https://discord.gg/GASyt8p4jw">Discord</UButton>
        </template>
    </UHeader>

    <UPage>
        <UPageBody>
            <UContainer>
                <div class="flex flex-col gap-4">
                    <UCard title="Info/Rules">
                        <div class="flex flex-col gap-2">
                            <div class="flex flex-col">
                                <span>PVP: <span class="text-green-500">Allowed</span></span>
                                <span>Stealing: <span class="text-green-500">Allowed</span></span>
                                <span>Griefing: <span class="text-red-500">Not Allowed</span></span>
                                <span>Hacking: <span class="text-red-500">Not Allowed</span></span>
                                <span>Combat Logging: <span class="text-red-500">Not Allowed</span></span>
                            </div>
                            <USeparator/>
                            <div>
                                You can shift + right click a villager to pick them up / place them down <br>
                                You can use <a class="text-blue-600 underline" href="https://modrinth.com/mod/reroll-trades">Reroll Trades</a> mod to be able to reroll villager trades
                                <br>You can dupe string in your inventory 1 string -> 64 string
                                <br>You can trade with villagers unlimited
                                <br>Netherite crafting receipies are disabled (for now)
                                <br>End Dimension is disabled (until the end of the server)
                                <br>You can get tier-ranked (S, A, B, C, D, F) Just ask any S Tier rank to test you
                            </div>
                        </div>
                        
                    </UCard>

                    <UCard title="Commands">
                        <div class="flex flex-col gap-2">
                            <Command command="tpa", action="Teleport to another player"/>
                            <Command command="tpahere", action="Teleport another player to you"/>
                            <Command command="tpaccept", action="Accept another players teleport request"/>
                            <Command command="home", action="commands to manage homes to be able to teleport to"/>
                            <Command command="warp", action="warp to preset locations like tiertest arena"/>
                            <Command command="workbench", action="open up crafting table"/>
                            <Command command="enderchest", action="open up echest"/>
                        </div>
                    </UCard>

                    <UCard title="Join Now! v26.2">
                        <UFieldGroup>
                            <UInput disabled model-value="smp.orangegreencat.com"/>
                            <UButton icon="i-lucide-copy" @click="copy">Copy</UButton>
                        </UFieldGroup>
                    </UCard>
                </div>
                
            </UContainer>
        </UPageBody>
    </UPage>
</template>

<script setup>
const desc = "Java 26.2 Generic SMP is a chill casual SMP that allows pvp and stealing! Join the new refreshing SMP that ISNT owned by ross! GenericSMP is NOT wannabeSMP and it also isnt trash"
useSeoMeta({
    title: 'GenericSMP',
    description: desc,
    ogTitle: 'GenericSMP',
    ogDescription: desc,
    themeColor: '#eb4034',
    ogUrl: 'https://smp.orangegreencat.com'
})

import Command from '~/components/Command.vue';
const toast = useToast()

function copy() {
    navigator.clipboard.writeText('smp.orangegreencat.com')
    toast.add({title:'Copied to clipboard!'})
}

</script>