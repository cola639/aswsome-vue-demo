<template>
  <div class="home-viewport">
    <el-upload
      class="upload-wrap"
      drag
      action="https://jsonplaceholder.typicode.com/posts/"
      multiple
      :data="params"
      :before-upload="beforeUpload"
      :on-success="onsucess"
      :file-list="fileList"
    >
      <i class="el-icon-upload"></i>
      <div class="el-upload__text">将文件拖到此处，或<em>点击上传</em></div>
      <div class="el-upload__tip">支持扩展名: .rar .zip .doc .docx .pdf .jpg...</div>
    </el-upload>
  </div>
</template>
<script>
export default {
  name: 'Home',
  components: {},
  data() {
    return {
      params: { id: 'test', key: 'key1' },
      fileList: []
    }
  },
  props: {},
  created() {},
  mounted() {},
  beforeDestroy() {},
  computed: {},
  watch: {},
  methods: {
    beforeUpload(params) {
      console.log('🚀TCL: >> beforeUpload >> params', params)
    },
    onsucess(response, file, fileList) {
      console.log('🚀TCL: >> ,onsucess >> response', response)
    }
  }
}
</script>
<style lang="scss" scoped>
.home-viewport {
  width: 600px;
  height: 600px;
  margin: 20px auto;
}

.el-icon-upload {
  color: #4388e2;
}
.el-upload__tip {
  font-size: 12px;
  margin-top: 10px;
  color: #999;
}
</style>
