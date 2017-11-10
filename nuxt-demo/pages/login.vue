<template>
    <Form ref="user" :model="user" :rules="ruleInline" class="login">
        <FormItem prop="user">
            <Input type="text" v-model="user.name" placeholder="Username">
                <Icon type="ios-person-outline" slot="prepend"></Icon>
            </Input>
        </FormItem>
        <FormItem prop="password">
            <Input type="password" v-model="user.password" placeholder="Password">
                <Icon type="ios-locked-outline" slot="prepend"></Icon>
            </Input>
        </FormItem>
        <FormItem>
            <Button type="primary" @click="handleSubmit('user')">Signin</Button>
        </FormItem>
    </Form>
</template>
<script>
export default {
  name: 'login',
  data () {
    return {
      user: {
        name: '',
        password: ''
      }
    }
  },
  methods: {
  }
}
</script>
<style>
.login {
    margin: 0 auto;
    margin-top: 15%;
    width: 300px;
    height: 150px;
}
</style>
