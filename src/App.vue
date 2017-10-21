<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
<!--
               <button @click="selectedComponent='appQuote'">Quote</button>
               <button @click="selectedComponent='appAuthor'">Author</button>
               <button @click="selectedComponent='appNew'">New</button>
               <hr>
               <p>{{ selectedComponent }}</p>
               <keep-alive>
                    <component :is="selectedComponent">
                       <p>Default Content</p>
                    </component>
               </keep-alive>
-->
              
               
<!--
                <app-quote>
                    <h2 slot="title">{{ quoteTitle }}</h2>
                    <p slot="content">A wonderful Quote</p>
                    <p>A wonderful Quote</p>
                </app-quote>
-->
                
                <br>
                <button 
                    class="btn btn-primary"
                    @click="selectedColorComponent='appBlue'">Load Blue Template</button>
                <button 
                    class="btn btn-primary"
                    @click="selectedColorComponent='appGreen'">Load Green Template</button>
                <button 
                    class="btn btn-primary"
                    @click="selectedColorComponent='appRed'">Load Red Template</button>
                <hr>
                <component :is="selectedColorComponent">
                    <p>This is the Content</p>
                </component>
<!--
                <app-blue>
                    <p>This is the blue content</p>
                </app-blue>
                <app-green>
                    <p>This is the green content</p>
                </app-green>
                <app-red>
                    <p>This is the red content</p>
                </app-red>
-->
            </div>
        </div>
    </div>

</template>

<script>
    import Quote from './components/Quote.vue';
    import Author from './components/Author.vue';
    import New from './components/New.vue';
    import Blue from './components/Blue.vue';
    import Green from './components/Green.vue';
    import Red from './components/Red.vue';
    export default {
        data:function(){
            return {
                quoteTitle: 'The Quote',
                selectedComponent: 'Quote',
                selectedColorComponent: 'appBlue'
            };
        },
        components: {
            appQuote: Quote,
            appAuthor: Author,
            appNew: New,
            appBlue: Blue,
            appGreen: Green,
            appRed: Red
        }
    }
</script>

<style>

</style>
