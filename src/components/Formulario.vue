
<script setup>
    const props = defineProps(["getNumber1", "getNumber2", "getOperador", "resultado"]);
</script>

<template>
    <form class="text-center">
        <div class="row">
            <div class="col">
            <input required type="number" placeholder="PRIMEIRO NUMERO" class="form-control mb-4" @keyup="props.getNumber1"/> 
            </div>
            <div class="col-md-2 mb-4 text-center">
            <select class="form-control text-center" @change="props.getOperador">
                <option class="text-center" disabled selected value="">SELECIONE A OPERAÇÃO</option>
                <option class="subtrair text-center" value="subtrair">-</option>
                <option class="somar text-center" selected value="somar">+</option>
                <option class="dividir text-center" value="dividir">÷</option>
                <option class="multiplicar text-center" value="multiplicar">x</option>
            </select>
            </div>
            <div class="col">
            <input required type="number" placeholder="SEGUNDO NUMERO" class="form-control mb-4" @keyup="props.getNumber2"/>
            </div>
        </div>
        <div class="row">
            <div class="col">
            <h3 class="black-text">Resultado</h3>
            </div>
        </div>
        <div class="row">
            <div class="col">
            <h2 class="black-text fs-1 fw-bold ps-2 mb-2">{{ props.resultado }}</h2>
            </div>
        </div>
    </form>
</template>

<style scoped>
    .black-text {
        color: black;
    }

    input[type=number]::-webkit-inner-spin-button,
    input[type=number]::-webkit-outer-spin-button {
        -webkit-appearance: none;
        margin: 0;
}

@media screen and (max-width: 768px) {
    .form-control {
        text-align: center;
    }

    select {
        padding-left: 48%;
        padding-right: 48%;
    }
}
</style>
