<script>
    /**
     * @type {any}
     */
    let brand;
    let model = '';
    let seller = '';
    let price = '';
    
    let display = false;

    function displayValues() {
        display = true;
    }

</script>

<input type="text" id="brand" placeholder="Brand" />
<input type="text" id="model" bind:value={model} placeholder="Model" />
<input type="text" id="seller" bind:value={seller} placeholder="Seller" />
<input type="number" id="price" bind:value={price} placeholder="Price">

<hr>

{#if brand && model && seller && price}
<button id="add" on:click={() => displayValues()}>Add</button>
{/if}

{#if  display}
{brand} {model} {seller} {price}
{/if}

<hr>