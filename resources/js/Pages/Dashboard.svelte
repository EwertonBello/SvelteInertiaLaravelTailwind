<script>
    let count = 0;

    function handleClick() {
        count += 1;
    }
</script>

<div class="mx-auto md:flex md:flex-flow-col md:grid-cols-3 md:grid-rows-3 gap-6 px-6">

    <div class="mx-auto text-center mt-10">
        <h2 class="text-2xl mb-4 text-gray-700 font-bold">Dashboard</h2>
        <hr class="bg-gray-500 w-full h-0.25 mb-5"/>
        <!-- button -->
        <div class="mb-4">
            <button 
            type="button" 
            class='flex max-w-sm w-full bg-gradient-to-r from-green-500 to-blue-500 hover:from-green-600 hover:to-blue-600 focus:outline-none text-white text-2xl uppercase font-bold shadow-md rounded-full mx-auto p-5'
            on:click={handleClick}
            >
                <div class="flex sm:flex-cols-12 gap-2">
                    <div class="col-span-1">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M15 13l-3 3m0 0l-3-3m3 3V8m0 13a9 9 0 110-18 9 9 0 010 18z" />
                        </svg>
                    </div>
                    <div class="col-span-2 pt-2">
                    	Deu {count} {count < 2 ? 'click' : 'clicks'}
                    </div>
                </div>    
            </button>
        </div>
    </div>

</div>
