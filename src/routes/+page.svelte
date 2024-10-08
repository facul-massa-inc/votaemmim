<script lang="ts">
    let candidatos: Candidato[] = [
        { nome: "Arthur", partido: "FODA", frase: "é foda", numero: 21 },
        { nome: "Igor", partido: "FODA", frase: "é foda", numero: 21 },
        { nome: "Richard", partido: "FODA", frase: "é foda", numero: 21 },
        { nome: "Heitor", partido: "FODA", frase: "é foda", numero: 21 },
        { nome: "Marcelo", partido: "FODA", frase: "é foda", numero: 21 },
        { nome: "Milson", partido: "FODA", frase: "é foda", numero: 21 },
    ];
</script>
<style>
    :global(body) {
        justify-content: center;
        align-items: center;
    }
    .candidato {
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
        margin-right: 5px;
    }
</style>
{#each candidatos as candidato}
    <div class="candidato">
        <img src={candidato.foto ?? "default.jpg"} width=100 height=100 alt="">
        <p>{candidato.nome}</p>
        <q>{candidato.frase}</q>
        <div>
            <span>{candidato.partido}</span>
            <span>({candidato.numero})</span>
        </div>
        <button>VOTAR</button>
    </div>
{/each}