<template>
<section class="container">
   <form class="container" onchange="produtoController.validRequired()">
        <div class="form-group">
            <label for="nome" class="form-label">Nome</label>
            <input type="text" class="form-control required" id="nome" name="quant" placeholder="">
            <span class="textErro">Nome em branco!</span>
        </div>

        <div class="form-group">
            <label for="descricao" class="form-label">Descricao</label>
            <textarea class="form-control required" id="descricao" name="descricao" rows="3"></textarea>
            <span class="textErro">Descrição em branco!</span>
        </div>

        <div class="form-group">
            <label for="quant" class="form-label">Quantidade</label>
            <input type="number" class="form-control required" id="quant" name="quant" min="0" placeholder="">
            <span class="textErro">Quantidade em branco!</span>
        </div>

        <div class="form-group">
            <label for="valor" class="form-label">Valor</label>
            <input type="number" class="form-control required" id="valor" name="valor" min="0" step="0.01"
                placeholder="">
            <span class="textErro">Valor em branco!</span>
        </div>

        <div class="form-group">
            <label for="foto" class="form-label">Foto</label>
            <input type="file" class="form-control" id="foto" name="foto" placeholder="">
        </div>

        <div class="my-3">
            <button type="button" class="btn btn-primary" id="btnSalve" onclick="produtoController.addProduto()"
                disabled>Adicionar</button>
            <button type="button" class="btn btn-danger">Cancelar</button>
            <button type="button" class="btn btn-danger" onclick="produtoController.getAllProduto()">Listar
                Produtos</button>
        </div>
    </form>
</section>
</template>

<script>
export default {
    name:"ProdutoFormComponent"
}
</script>

<style scoped>
.textErro{
    display: none;
    color: #f00;
    font-weight: bold;
    padding: 0 0 0 20px;
}
</style>