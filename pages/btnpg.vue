<template>
    <div class="main-con">
        <sb-button>
            <template #Mainbtn={theme,size,block,squared,icon,btn_title,toolkit_title}>
            <h1>Reusable Button</h1>
 

                <b-button 
                 :variant="theme.success"
                 :size="size.md"
                 :block="block"
                 :squared="squared"
                >
                {{ btn_title + 'update'}}
                <b-icon :icon="icon +'cart-plus'"></b-icon>
                </b-button>

                <br>
                <br>

                <b-button 
                 :variant="theme.danger"
                 :size="size.sm"
                 :squared="squared"
                 :title="toolkit_title +'Delete Account'"
                 v-b-tooltip.hover
                >
                <b-icon :icon="icon +'trash'"></b-icon>
                {{ btn_title + ''}}
                </b-button>

        <br>
        <br>
        <!-- toolbar -->

                <div>
                    <b-button-toolbar key-nav aria-label="Toolbar with button groups">
                        <b-button-group class="mx-1">
                        <b-button :variant="theme.warning">&laquo;</b-button>
                        <b-button>&lsaquo;</b-button>
                        </b-button-group>
                        <b-button-group class="mx-1">
                        <b-button>{{ btn_title + 'Edit'}}</b-button>
                        <b-button>{{ btn_title + 'undo'}}</b-button>
                        <b-button>{{ btn_title + 'Redo'}}</b-button>
                        <b-button><b-icon :icon="icon +'search'"></b-icon></b-button>
                        <b-button><b-icon :icon="icon +'grid'"></b-icon></b-button>
                        </b-button-group>
                        <b-button-group class="mx-1">
                        <b-button>&rsaquo;</b-button>
                        <b-button :variant="theme.warning">&raquo;</b-button>
                        </b-button-group>
                    </b-button-toolbar>
                    </div>
       
        <!-- toolbar -->
        </template>
        </sb-button>
    </div>
</template>
<script>
import SbButton from '../components/Sb-button.vue'
export default {
  components: { SbButton },
    name:'ButtonPage'
}
</script>

<style scoped>
.main-con{
    padding:20px 20px 20px 20px;
}
</style>
