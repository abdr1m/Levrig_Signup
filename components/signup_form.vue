<template> 
    <!-- signup form -->
    <div class="signup_form_container"> 
        <div class="signup_form">
            <form action="#" method="POST">
                <div>
                    <v-text-field
                        label="الإسم الكامل - Nom et prénom"
                        filled
                        hide-details
                  ></v-text-field>
                </div>
                <div>
                    <v-text-field
                        class="centered-input"
                        label="البريد لاكتروني - Adresse courriel"
                        filled
                        hide-details
                  ></v-text-field>
                </div>
                <div>
                    <v-text-field
                        label="رقم الهاتف - Numéro de téléphone"
                        filled
                        hide-details
                        small
                  ></v-text-field>
                </div>
                <div class="select">
                    <div>
                        <v-select
                            :items="items"
                            label="مجالات التطوع"
                            chips
                            multiple
                            clearable
                            deletable-chips
                            solo
                        ></v-select>
                    </div>
                     <div>
                        <v-btn 
                            type="submit"
                            style="color: white; margin-right: 14px;"
                            class="p-4"
                            color="#dd4814"
                            background="#000"
                            elevation="2"
                            x-large
                            tile
                        >مشاركة</v-btn>
                    </div>
                </div>
            </form>
        </div>
    </div>
    <!-- signup form end -->
</template>
<script>
    export default {
        name: "signup",
        data: () => ({
            items: ['أمن المعلومات', 'البرمجة', 'الشبكات', 'التصميم', 'العتاد', 'الذكاء لاصطناعي', 'التسويق', 'العتادالتسويق'], 
        }),
        components: {},
    }
</script>
<style scope>
   .signup_form div {
        margin-bottom: 10px;
    } 
    .v-input__slot:before, .v-input__slot:after {
        border-color: #dd4814 !important;
    } 
    .v-text-field .v-label {
        right: 0 !important;
        left: auto !important;
    } 
    .v-select__slot {
        margin: 0 !important;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .v-input__append-inner, .v-input__append-inner > * {
        margin: 0 !important;
    }
    .v-menu {
        display: block !important;
    }
</style>
