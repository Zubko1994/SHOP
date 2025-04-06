<script>
import btn from "./components/btn.vue";

export default {
    name: "app",
    components: {
        btn,
    },
    data() {
        return {};
    },
    methods: {
        clickBtn() {
            console.log("juhgfd");
        },
    },
};
</script>

<template>
    <div id="app">
        <div class="line">
            <btn @click="clickBtn" />
            <btn title="Выбрать товар" kind="primary" />
            <btn title="Купить в 1 клик" kind="buying" />
            <btn title="Смотреть больше товаров" kind="primary" />
            <btn title="Смотреть больше брендов" kind="primary" />
        </div>
    </div>
    <div class="line">
        <btn title="6 л." kind="quantity" />
        <btn title="18 л." kind="quantity" />
        <btn title="30 л." kind="quantity" />
        <btn title="12 л." kind="quantity-active" />
        <btn title="85 г." kind="quantity-active" />
        <btn title="1 шт." kind="quantity-active" />
        <btn title="0,2 кг." kind="quantity" />
        <btn title="1,2 кг." kind="quantity" />
        <btn title="2 кг." kind="quantity" />
        <btn title="4 кг." kind="quantity" />
        <btn title="10 кг." kind="quantity" />
        <btn title="Задать вес" kind="quantity" />
        <btn title="0,4 кг." kind="quantity-active"/>
    </div>
    <btn title="" @click="clickBtn" kind="basket"/>
    <btn title="" @click="clickBtn" kind="basket-adding"/>
    <btn title="" @click="clickBtn" kind="indicator-left"/>
    <btn title="" @click="clickBtn" kind="indicator-right"/>
</template>

<style>
:root {
    --white: #ffffff;
    --default-hover: #dad0d0a9;
    --text-default: #202223;
    --highlight: #00a0ac;
    --highlight-hover: #087b83;
    --highlight-active: #449da7;
    --surface-neutral: #e4e5e7;
    --border-default: 1px solid #8c9196;
    --border-highlight: 1px solid #00a0ac;
    --gradient-button: linear-gradient(
            180deg,
            #babfc3 86.46%,
            #bbbfc3 100%);
    --bg-button: #F6F6F7;

}
#app {
    font-family: "SFProText";
    font-weight: 400;
    color: var(--color-text-default);
}

.line {
    display: flex;
    flex-direction: row;
    gap: 5px;
    align-items: center;
}
</style>
