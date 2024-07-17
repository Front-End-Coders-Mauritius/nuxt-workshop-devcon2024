<template>
    <main class="text-center text-gray-700 bg-gradient-to-tr from-blue-500 to-green-500">
        <div class="px-4 py-10 grid grid-cols-1 text-left gap-10 max-w-4xl mx-auto">
            <h1>Power Outages in Mauritius</h1>
            <div>
                <div class="grid gap-10">
                    <h2>Today</h2>
                    <div class="grid gap-10">
                        <slot />
                    </div>
                    <h2>Tomorrow</h2>
                    <div class="grid gap-10"></div>                    
                </div>
            </div>

        </div>
    </main>
</template>