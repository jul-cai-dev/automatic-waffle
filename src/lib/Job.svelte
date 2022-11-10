<script>
    export /**
            * @type {{ primary: string[]; secondary: string[]; }}
            */
     let skills;
</script>

<div class="flex flex-col bg-slate-200 rounded-md p-4 border-box">
    <div class="flex w-full flex-row justify-between space-x-4 sm:space-x-0">
        <div class="flex flex-col">
            <div class="text-2xl">
                <slot name="Company Name">
                    Company Name
                </slot>
            </div>
            <div class="text-l text-slate-600">
                <slot name="Position">
                    Position
                </slot>
            </div>
        </div>
        <div class="text-md text-slate-600">
            <slot name="Duration">
                Mar 2021 - Sep 2022
            </slot>
        </div>
    </div>
    <div class="mt-8">
        <p>
            <slot name="Description">
               Job Description
            </slot>
        </p>
    </div>
    <div class="flex mt-6">
        <div class="flex flex-wrap">
            {#each skills.primary as primary}
                <span class="bg-yellow-300 text-yellow-800 text-xs font-semibold mt-2 mr-2 px-2.5 py-0.5 rounded">{primary}</span>
            {/each}
            {#each skills.secondary as secondary}
                <span class="bg-zinc-300 text-zinc-800 text-xs font-semibold mt-2 mr-2 px-2.5 py-0.5 rounded">{secondary}</span>
            {/each}
        </div>
    </div>
</div>