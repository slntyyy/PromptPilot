<template>
  <div class="app-shell">
    <Sidebar />
    <main>
      <header class="topbar">
        <div></div>
        <div class="header-actions">
          <button class="login-button">登录</button>
          <button class="register-button">注册</button>
        </div>
      </header>

      <section class="home-content">
        <div class="welcome-wrap">
          <h1>Hi，欢迎使用 <span>PromptPilot</span><i class="title-spark">✦</i></h1>
          <div class="prompt-menu">
            <div class="menu-caption"><i>✦</i><span>我能帮你做点什么？</span><i>✦</i></div>
            <button class="menu-card" @click="startCreate">
              <span class="card-label"><i class="spark-icon">✧</i> 帮我生成一个 Prompt</span>
              <b>→</b>
            </button>
            <button class="menu-card" @click="startOptimize">
              <span class="card-label"><i class="flask-icon">♙</i> 优化我的 Prompt</span>
              <b>→</b>
            </button>
            <button class="menu-card" @click="showApiTip">
              <span class="card-label"><i class="key-icon">⚿</i> 获取 API Key</span>
              <b>→</b>
            </button>
          </div>
        </div>
        <p class="manual-link"><a href="#">使用手册</a></p>
      </section>

      <button class="assistant-button" aria-label="打开助手"><span>▤</span></button>
      <div class="floating-tools">
        <button aria-label="活动">♙</button>
        <button aria-label="客服">♧</button>
      </div>
    </main>
  </div>
</template>
<script>
import Sidebar from '../components/Sidebar.vue'
export default {
  components: { Sidebar },
  methods: {
    startCreate () { this.$router.push({ path: '/', query: { action: 'create' } }) },
    startOptimize () { this.$router.push({ path: '/', query: { action: 'optimize' } }) },
    showApiTip () { window.alert('API Key 获取入口即将上线') }
  }
}
</script>
<style scoped>
.app-shell{min-height:100vh}.app-shell main{margin-left:224px;min-height:100vh}header{height:72px;background:#fff;border-bottom:1px solid #edf0f5;display:flex;align-items:center;justify-content:space-between;padding:0 28px;position:sticky;top:0;z-index:3}.panel-toggle,.icon-button{border:0;background:transparent;color:#73798a}.panel-toggle{font-size:20px}.header-actions{display:flex;align-items:center;gap:18px}.icon-button{height:32px}.user-button{border:0;background:#f4f5ff;color:#5a60d8;border-radius:18px;padding:8px 16px}.workspace{max-width:1120px;margin:auto;padding:30px 34px 50px}.welcome{height:172px;border-radius:16px;background:linear-gradient(110deg,#edf2ff 0%,#f5f1ff 58%,#eef7ff 100%);padding:34px 38px;display:flex;justify-content:space-between;overflow:hidden}.eyebrow{font-size:12px;color:#6269dd;font-weight:600;margin-bottom:10px}.welcome h1{font-size:27px;margin:0;color:#263151}.welcome p{font-size:14px;color:#747e99;margin:12px 0}.hero-art{position:relative;width:180px}.hero-art>span{position:absolute;color:#77b7ff;font-size:32px;right:110px;top:20px}.spark-card{width:110px;height:110px;border-radius:28px;background:linear-gradient(145deg,#747af5,#a6d1ff);position:absolute;right:10px;top:-10px;transform:rotate(12deg);box-shadow:0 18px 35px #8c9bf04a;display:grid;place-items:center;color:white}.spark-card .icon{width:54px;height:54px}.creator,.result-card{background:white;border-radius:14px;border:1px solid #edf0f5;margin-top:18px;box-shadow:0 4px 18px rgba(39,49,84,.035)}.creator{padding:24px}.creator-head{display:flex;justify-content:space-between}.creator-head h2{font-size:18px;margin:0}.creator-head p{font-size:13px;color:#999ead;margin:7px 0 18px}.template{height:34px;border:1px solid #e4e6ee;background:white;border-radius:7px;color:#686f80}.type-tabs{display:flex;border-bottom:1px solid #eceef4;margin-bottom:22px}.type-tabs button{border:0;background:none;padding:0 4px 12px;margin-right:26px;color:#969baa}.type-tabs button.selected{color:#555bd9;border-bottom:2px solid #6267dd}.prompt-label{font-size:13px;font-weight:600}.editor{border:1px solid #dfe2eb;border-radius:10px;margin-top:8px;overflow:hidden;transition:.2s}.editor:focus-within{border-color:#777ce8;box-shadow:0 0 0 3px #777ce817}.editor textarea{width:100%;height:116px;border:0;resize:none;outline:0;padding:16px}.editor-tools{height:38px;background:#fafbfc;border-top:1px solid #f1f2f5;padding:5px 10px}.editor-tools button{border:0;background:white;color:#777e90;height:28px;border-radius:6px;margin-right:7px}.quick-prompts{height:44px;display:flex;align-items:center;gap:8px;font-size:12px;color:#999daa}.quick-prompts button{border:1px solid #eaecf2;background:white;border-radius:14px;color:#777d8d;padding:5px 10px}.generate-row{display:flex;justify-content:flex-end;align-items:center;margin-top:8px}.model-select{height:42px;border-right:1px solid #e6e8ef;padding:0 18px;margin-right:18px;display:flex;align-items:center;gap:8px}.model-select small{font-size:10px;color:#aaaebe;display:block}.model-select strong{font-size:13px}.status-dot{width:7px;height:7px;border-radius:50%;background:#50ca9a}.generate{height:42px;border:0;border-radius:8px;padding:0 22px;background:linear-gradient(100deg,#6265df,#7771ed);color:white;font-weight:600;box-shadow:0 6px 14px #6265df30;display:flex;align-items:center;gap:7px}.generate:disabled{opacity:.45;cursor:not-allowed}.generate .icon{width:18px}.result-card{padding:20px 24px}.result-title{display:flex;justify-content:space-between;align-items:center}.result-title h3{margin:0}.result-title button{border:0;background:#f1f1ff;color:#6267db;border-radius:6px;padding:7px 12px}.result-card pre{white-space:pre-wrap;font-family:inherit;font-size:13px;line-height:1.8;color:#555e73;background:#f7f8fb;padding:16px;border-radius:8px}.feature-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:18px}.feature-grid article{background:white;border:1px solid #edf0f5;border-radius:12px;padding:20px}.feature-icon{width:38px;height:38px;border-radius:10px;display:grid;place-items:center;color:white}.purple{background:#7976e9}.blue{background:#56a8e9}.orange{background:#f1a468}.feature-grid h3{font-size:15px;margin:14px 0 6px}.feature-grid p{font-size:12px;color:#9297a5;line-height:1.7;height:40px}.feature-grid a{font-size:12px;color:#6267db}
@media(max-width:760px){.app-shell main{margin-left:64px}.workspace{padding:18px 14px}.welcome{padding:24px;height:150px}.welcome h1{font-size:20px}.hero-art{display:none}.feature-grid{grid-template-columns:1fr}.generate-row{justify-content:space-between}.model-select{display:none}.quick-prompts button:nth-last-child(1){display:none}}

.app-shell{background:#fff}.app-shell main{position:relative;margin-left:224px;min-height:100vh;background:#fff}.topbar{height:72px;padding:0 24px;border:0;box-shadow:none}.header-actions{gap:10px}.login-button,.register-button{height:32px;border-radius:6px;padding:0 16px;font-size:14px}.login-button{color:#fff;border:0;background:#4f46e5;box-shadow:0 4px 10px rgba(79,70,229,.18)}.register-button{color:#34384a;border:1px solid transparent;background:#fff}.home-content{position:relative;height:calc(100vh - 72px);min-height:590px}.welcome-wrap{position:absolute;left:50%;top:74px;width:min(520px,calc(100% - 40px));transform:translateX(-50%);text-align:center}.welcome-wrap h1{margin:0;font-size:30px;font-weight:700;letter-spacing:.2px;color:#111827;white-space:nowrap}.welcome-wrap h1 span{color:#5c61f2}.title-spark{position:absolute;margin-left:6px;margin-top:-8px;color:#6baaf6;font-size:18px;font-style:normal}.prompt-menu{width:480px;max-width:100%;margin:46px auto 0}.menu-caption{height:30px;margin-bottom:12px;color:#72798c;font-size:13px}.menu-caption i{color:#6da8f5;margin:0 10px;font-style:normal;font-size:15px}.menu-card{width:100%;height:53px;margin-top:12px;padding:0 22px;border:1px solid #e9eaef;border-radius:5px;background:#fff;display:flex;align-items:center;justify-content:space-between;color:#111827;box-shadow:0 1px 2px rgba(20,25,40,.02);font-size:14px;transition:.2s}.menu-card:hover{border-color:#c9caf8;box-shadow:0 7px 18px rgba(71,75,150,.08);transform:translateY(-1px)}.card-label{font-weight:600}.card-label i{display:inline-block;width:24px;color:#111827;font-style:normal;text-align:left;font-size:19px}.spark-icon{color:#111827!important}.flask-icon{transform:rotate(180deg)}.key-icon{font-size:16px!important}.menu-card b{font-size:18px;font-weight:400}.manual-link{position:absolute;bottom:32px;left:50%;transform:translateX(-50%);margin:0;font-size:12px}.manual-link a{color:#73798c;text-decoration:none}.assistant-button{position:absolute;right:16px;bottom:16px;width:44px;height:44px;border:0;border-radius:50%;background:#5b55eb;color:white;box-shadow:0 7px 18px rgba(91,85,235,.25);font-size:20px}.assistant-button span{transform:rotate(180deg);display:inline-block}.floating-tools{position:absolute;right:16px;top:50%;display:flex;flex-direction:column;gap:12px}.floating-tools button{width:38px;height:38px;border:0;border-radius:50%;background:#fff;color:#7b76e9;box-shadow:0 4px 14px rgba(40,44,80,.14);font-size:18px}.floating-tools button:last-child{color:#e87979}@media(max-width:760px){.app-shell main{margin-left:64px}.welcome-wrap{top:70px}.welcome-wrap h1{font-size:22px}.prompt-menu{width:min(390px,100%)}.floating-tools{display:none}}
</style>
