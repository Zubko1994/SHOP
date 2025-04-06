<script>
import { ref } from "vue";

export default {
    name: "btn",
    props: {
        title: {
            type: String,
            default: "Перейти к выбору товара",
        },
        kind: {
            type: String,
            default: "",
        },
    },
    data() {
        return {};
    },
    method: {
        click() {
            this.$emit("click");
        },
    },
};
</script>

<template>
    <div :class="['btn', `btn_${kind}`, `btn_${borderBtn}`]" @click="click">
        <span>{{ title }}</span>
    </div>
</template>

<style lang="scss">
.btn {
    color: var(--text-default);
    font-family: "SFProText";
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
    text-align: center;
    padding: 8px 16px;
    border: var(--border-default);
    cursor: pointer;
    margin-bottom: 10px;
    background: var(--white);
    display: inline-block;
    &:hover {
        background-color: var(--default-hover);
    }
    &_primary {
        background-color: var(--highlight);
        box-shadow: 0px -1px 0px 0px #00000033 inset;
        box-shadow: 0px 1px 0px 0px #00000014;
        color: var(--white);
        padding: 12px 24px;
        border: none;
        display: inline-block;
        &:hover {
            background-color: var(--highlight-hover);
        }
    }
    &_buying {
        border: var(--border-highlight);
    }
    &_quantity {
        background: var(--surface-neutral);
        color: var(--text-default);
        padding: 2px 8px;
        display: inline-block;
        &:hover {
            background: var(--default-hover);
        }
    }
    &_quantity-active {
        background: var(--highlight-active);
        color: var(--white);
        padding: 2px 8px;
        display: inline-block;
    }
    &_basket {
        border: 1px solid;
        border-image-source: var(--gradient-button);
        padding: 8px 14px;
        background-image: url("/src/assets/image/basket.png");
        width: 60px;
        height: 36px;
        background-repeat: no-repeat;
        background-position: center;
        border: 1px solid #babfc3;
        border-radius: 4px;
        margin-right: 10px;
    }
    &_basket-adding {
        border-radius: 5px;
        border: 1px solid;
        border-image-source: var(--gradient-button);
        padding: 5px 12px;
        background-image: url("/src/assets/image/basketadding.png");
        width: 54px;
        height: 30px;
        background-repeat: no-repeat;
        background-position: center;
        border: 1px solid #babfc3;
        box-shadow: 0px 1px 0px 0px #0000000d;
        margin-right: 10px;
    }

    &_indicator-left {
        width: 40px;
        height: 40px;
        border-radius: 40px;
        padding: 10px;
        background-image: url("/src/assets/image/Primaryfillleft.svg");
        background-repeat: no-repeat;
        background-position: center;
        margin-right: 10px;
        background-color: var(--bg-button);
    }
    &_indicator-right {
        width: 40px;
        height: 40px;
        border-radius: 40px;
        padding: 10px;
        background-image: url("/src/assets/image/Primaryfill.svg");
        background-repeat: no-repeat;
        background-position: center;
        margin-right: 10px;
        background-color: var(--bg-button);
    }
}
</style>
