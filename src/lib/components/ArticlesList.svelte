<script>
    import { Button } from "flowbite-svelte";
    import ArticleCard from "./ArticleCard.svelte";

    let { posts } = $props();
</script>

<section class="max-w-[1200px] mx-auto">
    <div class="container mx-auto px-4 mt-10">
        <h2 id="noticias" class="text-lg font-black my-5">Últimas notícias</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-0 md:gap-3">
            {#each posts as post, index}
                <ArticleCard {...post} {index}></ArticleCard>
            {/each}
        </div>
    </div>
</section>
