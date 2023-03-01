<script>
    import data from "../data.json"
</script>

<main>
    <div class="header">
        <img src={data.logo} width="160" alt="">
    </div>
    <div class="buttons">
        {#each data.links as link}
            <a href={link.url} class="links">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="7" y1="17" x2="17" y2="7"></line><polyline points="7 7 17 7 17 17"></polyline></svg>
                <p>{link.name}</p>
                <p>{link.text}</p>
            </a>
        {/each}
    </div>
</main>

<style lang="scss">
    .header {
        position: relative;
        text-align: center;
        font-size: .8rem;
        margin: 2rem;
        img {
            border-radius: 10rem;
        }
    }

    .buttons {
        display: grid;
        margin: auto;
        grid-template-columns: 1fr;
        gap: .6rem;
        max-width: 420px;
    }
    
    .links {
        padding: 1rem;
        margin: 0rem 1rem;
        color: aliceblue;
        border-radius: .2rem;
        text-decoration: none;
        background: rgb(31, 34, 39);
        border: 2px solid rgb(45, 49, 55);
        transition: all 200ms;
        &:hover {
            transform: scale(1.02);
        }
        p:nth-child(2) {
            font-size: 1rem;
            font-weight: 500;
            color: aliceblue;
        }
        p {
            color: rgb(108, 111, 115);
            font-size: .8rem;
            margin: 0;
        }
        svg {
            height: 100%;
            vertical-align: middle;
            float: right;
        }
    }
</style>