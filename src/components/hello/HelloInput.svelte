<script lang="ts">
    let name: string =  ''
    const handleFormSubmit = () => {
        location.href = `/hello/${encodeURIComponent(name)}`
    }
</script>

<form on:submit|preventDefault={handleFormSubmit}>
    <input type="text" bind:value={name} placeholder="Enter your name" />
</form>
