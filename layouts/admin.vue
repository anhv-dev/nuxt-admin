<template>
    <a-layout class="layout-admin">
        <a-layout-sider v-model="collapsed" :trigger="null" collapsible>
            <div class="layout-admin__logo" />
            <a-menu theme="dark" mode="inline" :default-selected-keys="['1']">
                <a-menu-item key="1">
                    <a-icon type="user" />
                    <span>nav 1</span>
                </a-menu-item>
                <a-menu-item key="2">
                    <a-icon type="video-camera" />
                    <span>nav 2</span>
                </a-menu-item>
                <a-menu-item key="3">
                    <a-icon type="upload" />
                    <span>nav 3</span>
                </a-menu-item>
            </a-menu>
        </a-layout-sider>
        <a-layout>
            <a-layout-header class="layout-admin__header">
                <a-icon
                        class="layout-admin__header--trigger"
                        :type="collapsed ? 'menu-unfold' : 'menu-fold'"
                        @click="() => (collapsed = !collapsed)"
                />
            </a-layout-header>
            <a-layout-content
                    :style="{ margin: '24px 16px', padding: '24px', background: '#fff', minHeight: 'auto' }"
            >
                <Nuxt/>
            </a-layout-content>
        </a-layout>
    </a-layout>
</template>
<script>
  export default {
    data() {
      return {
        collapsed: false,
      };
    },
  };
</script>

<style lang="scss" scoped>
    @import '@/assets/admin.scss';
</style>


