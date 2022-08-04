<template>
    <Painel titulo="Parametros" vermelho>
        <div class="parametros">
            <span>
                <strong>Quantidade Padrao: </strong>
                <input type="number" v-model="quantidade">
            </span>
            <span>
                <strong>Preco Padrao: </strong>
                <input type="number" v-model="preco">
            </span>
        </div>
    </Painel>
</template>

<script>
    export default {
        computed: {
            quantidade: {
                get() {
                    return this.$store.state.parametros.quantidade
                },
                set(valor) {
                    this.$store.commit('setQuantidade', valor)
                }
            },
            preco: {
                get() {
                    return this.$store.state.parametros.preco
                },
                set(valor) {
                    this.$store.commit('setPreco', valor)
                }
            }
        }
    }
</script>

<style>
    .parametros {
        display: flex;
        justify-content: space-around;
    }
</style>