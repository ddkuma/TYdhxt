```markdown
# 通用导航系统

![Preview](https://www.dkewl.com/upFiles/images/202004/202004301555085687.png)

一个现代化的个人导航页面，集成动态背景、音乐播放和视觉特效，适合作为浏览器起始页或个人门户网站。

## 功能特性

- 🌄 **动态背景系统**：10+ 精美壁纸自动轮换（10秒/张）
- 🎵 **背景音乐播放**：支持自动循环播放音乐
- 🌀 **交互式LOGO**：鼠标悬停触发LOGO旋转效果
- ❄️ **雪花飘落特效**：全屏动态雪花飘落动画
- 🎨 **现代化按钮设计**：圆角半透明导航按钮样式
- 📱 **响应式布局**：适配各种屏幕尺寸设备
- 🛠️ **易定制架构**：模块化CSS和可配置JS参数
- ⏲️ **智能预加载**：图片资源预加载保证流畅切换

## 使用说明

### 快速部署
1. 克隆仓库到Web服务器
2. 修改`images/`目录下的资源文件
3. 配置`index.html`中的导航链接
4. 部署到支持静态托管的服务器

### 自定义配置
```html
<!-- 修改导航按钮 -->
<a href="YOUR_LINK" 
   class="button button-rounded button-plain button-small-caps button-border" 
   target="_blank">按钮文字</a>

<!-- 更换背景音乐 -->
<audio src="YOUR_MUSIC_URL"></audio>

<!-- 调整背景切换间隔（单位：毫秒） -->
window.setTimeout(function(){change()},15000); 

<!-- 控制雪花参数（数量/图片路径） -->
createSnow('src/', 60);
```

## 技术栈

![HTML5](https://img.shields.io/badge/-HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/-CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?logo=javascript&logoColor=black)

- **UI框架**: buttons.css
- **特效库**: snow.min.js
- **音频支持**: HTML5 Audio API
- **响应式设计**: Media Queries

## 目录结构

```
/通用导航系统
│  index.html
│  README.md
├─css/
│  │  buttons.css
│  │  showcase.css
│  └─ style.css  
├─js/
│  │  player.js
│  └─ snow.min.js  
└─images/
   │  toptitle01.png
   │  tx2.png
   └─ tx2_hover.png
```

## 配置说明

### 背景图片
1. 修改`bodyBgs`数组中的图片URL
2. 推荐尺寸：1920x1080 或更高分辨率
3. 支持JPG/PNG格式

```javascript
// 在change()函数中替换图片链接
bodyBgs[1] = "YOUR_IMAGE_URL";
```

### LOGO配置
- 默认LOGO: `/images/tx2.png`
- Hover状态LOGO: `/images/tx2_hover.png`
- 推荐尺寸：200x200像素

```javascript
function mouseOver(){
    document.getElementById("mainimg").src="HOVER_IMAGE_PATH";
}
```

## 自定义选项

### 样式修改
```css
/* 修改按钮样式 */
.button {
    transition: all 0.3s ease;
    opacity: 0.9;
}

/* 调整LOGO尺寸 */
#top_logo img {
    max-width: 220px;
}

/* 修改雪花颜色 */
.snowflake {
    filter: brightness(150%);
}
```

### 扩展功能
1. 添加搜索框：
```html
<div class="search-container">
    <input type="text" placeholder="全网搜索...">
</div>
```

2. 集成天气组件：
```javascript
// 添加天气API调用代码
```

## 许可证
本项目采用 [MIT License](LICENSE)，请遵守相关使用规范。

## 特别鸣谢
- 背景图片来源：彼岸桌面
- 按钮样式库：buttons.css
- 音频播放解决方案：KW音乐API

> **注意事项**：实际部署时请替换测试用备案号和外部资源链接，推荐使用自有版权内容。
```