<template>
    <div>
        <SomeComponent>{{ someValue }}</SomeComponent>
        <SomeComponent2>{{ someValue2 }}</SomeComponent2>
    </div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';
    import SomeComponent from 'some-component.vue';
    import {someValue} from './some-value';

    @Component({
        components: {
            SomeComponent2: SomeComponent,
            SomeComponent,
        }
    })
    export default class AppRootComponent extends Vue {
        someValue2 = someValue;
        someValue = someValue;
    }
</script>
