<template >
    <div>
    <Menu class="menu" mode="horizontal" :theme="theme1" active-name="index">  
        <MenuItem to="/home" name="/home">
            <Icon size="25" type="ios-home-outline" />
            首页
        </MenuItem>
        <Submenu name="carfile">
            <template slot="title">
                <Icon size="25" type="ios-folder-outline" />
                汽车档案
            </template>
            <MenuGroup title="档案操作">
                <MenuItem to="/carfiles" name="/carfiles">档案首页</MenuItem>
                <MenuItem to="/newcar" name="/newcar">创建新的档案</MenuItem>
            </MenuGroup>
        </Submenu>
        <Submenu name="warehouse">
            <template slot="title">
                <Icon size="25" type="ios-cube-outline" />
                配件仓库
            </template>
            <MenuGroup title="配件操作">
                <MenuItem to="/warehouse" name="/warehouse">仓库首页</MenuItem>
                <MenuItem to="/newfittings" name="/newfittings">配件入库</MenuItem>
            </MenuGroup>
        </Submenu>
        <Submenu name="worker">
            <template slot="title">
                <Icon size="25" type="ios-contact-outline" />
                员工管理
            </template>
            <MenuGroup title="员工操作">
                <MenuItem to="/workers" name="/workers">员工首页</MenuItem>
                <MenuItem to="/newworkers" name="/newworkers">添加员工信息</MenuItem>
            </MenuGroup>
        </Submenu>
        <Submenu name="member">
            <template slot="title">
                <Icon size="25" type="ios-contacts-outline" />
                会员管理
            </template>
            <MenuGroup title="会员操作">
                <MenuItem to="/members" name="/members">会员首页</MenuItem>
            </MenuGroup>
        </Submenu>
    </Menu>
    </div>
</template>
<script>
    export default {
        data () {
            return {
                theme1: 'dark',
                value1: false,
                color:['#f56a00', '#7265e6', '#ffbf00', '#00a2ae'],
                user:'James'
            }
        },
    }
</script>
<style>
    .menu{
        position: absolute;
    }
</style>
