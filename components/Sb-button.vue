<template>
    <div>
        <slot 
          name="Mainbtn"
          :size="size"
          :theme="theme"
          :block="block"
          :squared="squared"
          :pill="pill"
          :disabled="disabled"
          :icon="icon"
          :btn_title="btn_title"
          :toolkit_title="toolkit_title"
        ></slot>
    </div>
</template>
<script>
export default {
    data(){
        return{
            size:{
            default:'md',
            lg: 'lg',
            sm: 'sm',
            md: 'md'
        },
        theme:{
            default:'secondary',
            success: 'success',
            secondary: 'secondary',
            primary: 'primary',
            info: 'info',
            danger: 'danger',
            warning: 'warning',
            link:'link'
        }
        }
    },
    props:{
        icon:{
            type:String,
            default:''
        },
        btn_title:{
            type:String,
            default:''
        },
        toolkit_title:{
            type:String,
            default:''
        },
        block:{
            type:String,
            default: 'block'
        },
        squared:{
            type:String,
            default:'squared'
        },
        pill:{
            type:String,
            default:'pill'
        },
        disabled:{
            type:Boolean,
            default:true
        },
        active:{
            type:Boolean,
            default:true
        }

    }
}
</script>