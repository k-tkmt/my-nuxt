<template>
  <div>
    <h1>Todo リスト</h1>
    <table>
      <tr><th>内容</th><th>完了</th><th>追加日</th></tr>
      <tr v-for="(todo, i) in todos" :key="i">
        <td>{{i + 1}}</td>
        <td>{{todo.title}}</td>
        <td>{{todo.done}}</td>
        <td>{{todo.created_at}}</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      todos: [
        { title: '歯磨き', done: false, created_at: new Date() },
        { title: '宿題', done: false, created_at: new Date() },
      ]
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
