<template>
    <div id="app">
        <div>Monibuca v1.0.2</div>
        <Menu
            mode="horizontal"
            :active-name="selectedMenu"
            style="position: absolute;top: 0;right: 0;"
        >
            <MenuItem name="home" to="/">首页</MenuItem>
            <MenuItem name="docs" to="/docs" target="_blank">文档</MenuItem>
            <MenuItem name="console" to="http://monibuca.com:8081" target="_blank">演示</MenuItem>
            <Submenu name="plugins">
                <template slot="title">常用插件</template>
                <MenuItem name="gateway" target="_blank" to="/docs/plugins.html#网关插件">网关</MenuItem>
                <MenuItem name="jessica" target="_blank" to="/docs/plugins.html#jessica插件">Jessica</MenuItem>
                <MenuItem name="cluster" target="_blank" to="/docs/plugins.html#cluster插件">集群</MenuItem>
                <MenuItem name="rtmp" target="_blank" to="/docs/plugins.html#rtmp插件">RTMP</MenuItem>
                <MenuItem name="logrotate" target="_blank" to="/docs/plugins.html#日志分割插件">日志分割</MenuItem>
            </Submenu>
            <MenuItem name="4" to="https://plugins.monibuca.com" target="_blank">插件市场</MenuItem>
            <MenuItem name="5" to="about">支持</MenuItem>
        </Menu>
        <router-view class="content"></router-view>
        <div>Copyright © 2019-2020 dexter 苏ICP备20001212号</div>
    </div>
</template>

<script>
export default {
    name: "app",
    data() {
        return {
            selectedMenu: "home"
        };
    }
};
</script>

<style>
body,
html {
    height: 100%;
}
#app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #184c18;
    position: relative;
    height: 100%;
}

#app > div:first-child {
    position: absolute;
    top: 10px;
    left: 30px;
    font-size: x-large;
}
.content {
    padding-top: 60px;
}
</style>
