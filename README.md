# 课题组项目展示

这是一个示例页面，展示了如何使用 HTML 和 CSS 在 Markdown 中创建分区域的布局。

<style>
/* 全局样式：可选，为了让页面更干净 */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 20px;
    color: #333;
}

/* 定义容器，使用 CSS Grid 创建两行两列的网格 */
.grid-container {
    display: grid;
    grid-template-columns: 1fr 1fr; /* 两列，每列等宽 */
    grid-template-rows: auto auto; /* 两行，高度自适应 */
    gap: 20px; /* 区域之间的间距 */
    margin-top: 30px;
}

/* 每个项目区域的样式 */
.project-card {
    background-color: #f9f9f9; /* 轻微的背景色，模拟无分割线 */
    padding: 20px;
    border-radius: 8px; /* 圆角边框 */
    box-shadow: 0 2px 4px rgba(0,0,0,0.1); /* 轻微的阴影，增加立体感 */
    display: flex; /* 内部使用 Flexbox 布局 */
    flex-direction: column; /* 元素垂直堆叠 */
    position: relative; /* 用于定位右上角的标题 */
}

/* 项目标题的样式 */
.project-title {
    position: absolute; /* 绝对定位 */
    top: 15px; /* 距离顶部15px */
    right: 20px; /* 距离右侧20px */
    font-size: 1.2em;
    font-weight: bold;
    color: #0056b3; /* 链接颜色 */
    text-decoration: none; /* 默认无下划线 */
}

.project-title:hover {
    text-decoration: underline; /* 鼠标悬停时显示下划线 */
}

/* 项目图片容器的样式 */
.project-image-container {
    float: left; /* 让图片浮动到左侧 */
    margin-right: 15px; /* 图片右侧留出间距 */
    margin-bottom: 10px; /* 图片下方留出间距 */
    width: 100px; /* 控制图片宽度 */
    height: 100px; /* 控制图片高度 */
    overflow: hidden; /* 确保图片不超出容器 */
    border-radius: 4px; /* 图片也带一点圆角 */
}

.project-image-container img {
    width: 100%;
    height: 100%;
    object-fit: cover; /* 裁剪图片以填充容器，保持比例 */
    display: block; /* 移除图片底部空白 */
}

/* 清除浮动，确保内容在图片下方正常排列 */
.project-description::after {
    content: "";
    display: table;
    clear: both;
}

</style>

<div class="grid-container">


    # 第N实验室
    
    <div style="text-align: right; margin-bottom: 20px;">
      <a href="./team.html" style="font-weight: bold; font-size: 1.2em; margin-right: 20px;">Team</a>
      <a href="./projects.html" style="font-weight: bold; font-size: 1.2em;">Projects</a>
    </div>
    
    ---
    
    欢迎来到 **第N实验室** 课题组主页！
    
    <style>
    /* 全局样式：可选，为了让页面更干净 */
    body {
        font-family: Arial, sans-serif;
        line-height: 1.6;
        margin: 20px;
        color: #333;
    }
    
    /* 定义容器，使用 CSS Grid 创建两行两列的网格 */
    .grid-container {
        display: grid;
        grid-template-columns: 1fr 1fr; /* 两列，每列等宽 */
        grid-template-rows: auto auto; /* 两行，高度自适应 */
        gap: 20px; /* 区域之间的间距 */
        margin-top: 30px;
    }
    
    /* 每个项目区域的样式 */
    .project-card {
        background-color: #f9f9f9; /* 轻微的背景色，模拟无分割线 */
        padding: 20px;
        border-radius: 8px; /* 圆角边框 */
        box-shadow: 0 2px 4px rgba(0,0,0,0.1); /* 轻微的阴影，增加立体感 */
        display: flex; /* 内部使用 Flexbox 布局 */
        flex-direction: column; /* 元素垂直堆叠 */
        position: relative; /* 用于定位右上角的标题 */
    }
    
    /* 项目标题的样式 */
    .project-title {
        position: absolute; /* 绝对定位 */
        top: 15px; /* 距离顶部15px */
        right: 20px; /* 距离右侧20px */
        font-size: 1.2em;
        font-weight: bold;
        color: #0056b3; /* 链接颜色 */
        text-decoration: none; /* 默认无下划线 */
    }
    
    .project-title:hover {
        text-decoration: underline; /* 鼠标悬停时显示下划线 */
    }
    
    /* 项目图片容器的样式 */
    .project-image-container {
        float: left; /* 让图片浮动到左侧 */
        margin-right: 15px; /* 图片右侧留出间距 */
        margin-bottom: 10px; /* 图片下方留出间距 */
        width: 100px; /* 控制图片宽度 */
        height: 100px; /* 控制图片高度 */
        overflow: hidden; /* 确保图片不超出容器 */
        border-radius: 4px; /* 图片也带一点圆角 */
    }
    
    .project-image-container img {
        width: 100%;
        height: 100%;
        object-fit: cover; /* 裁剪图片以填充容器，保持比例 */
        display: block; /* 移除图片底部空白 */
    }
    
    /* 清除浮动，确保内容在图片下方正常排列 */
    .project-description::after {
        content: "";
        display: table;
        clear: both;
    }
    
    /* 媒体查询：在小屏幕（例如手机）上，布局变为单列 */
    @media (max-width: 768px) {
        .grid-container {
            grid-template-columns: 1fr; /* 单列布局 */
        }
        .project-title {
            position: static; /* 取消绝对定位 */
            text-align: left; /* 标题左对齐 */
            margin-bottom: 10px; /* 标题下方增加间距 */
            margin-right: 0;
        }
        .project-image-container {
            float: none; /* 取消浮动 */
            margin-right: 0;
            margin-bottom: 15px;
            width: 100%; /* 图片宽度自适应 */
            height: auto; /* 高度自适应 */
        }
        .project-image-container img {
            height: auto;
        }
    }
    
    </style>
    
    <div class="grid-container">
    
        <div class="project-card">
            <a href="https://your-project1-link.com" class="project-title">项目一标题</a>
            <div class="project-image-container">
                <img src="./A.jpg" alt="项目A照片">
            </div>
            <div class="project-description">
                <p>这是项目一的详细文字说明，关于无线电方向的某个具体课题。你可以详细描述项目的目标、方法、实现过程和最终成果。确保文字内容能够充分解释图片所代表的项目。</p>
                <p>这里可以包含项目的主要功能、技术亮点和应用前景。</p>
            </div>
        </div>
    
        <div class="project-card">
            <a href="https://your-project2-link.com" class="project-title">项目二标题</a>
            <div class="project-image-container">
                <img src="./B.jpg" alt="项目B照片">
            </div>
            <div class="project-description">
                <p>这是项目二的详细文字说明，可能聚焦于无人机技术在某个特定场景的应用，例如智能巡检或自动配送。这里可以补充更多关于项目二的信息，比如其在课题组中的重要性，或取得的关键进展。</p>
                <p>你可以调整图片大小和文字排版，以适应不同的内容长度。</p>
            </div>
        </div>
    
        <div class="project-card">
            <a href="https://your-project3-link.com" class="project-title">项目三标题</a>
            <div class="project-image-container">
                <img src="./C.jpg" alt="项目C照片">
            </div>
            <div class="project-description">
                <p>这是项目三的详细文字说明，可能涉及测向小车在复杂环境下的高精度定位与导航技术。这个布局非常灵活，你可以根据实际需求修改每个区域的内容。</p>
                <p>记得将 `src` 属性中的图片路径替换为你的实际图片路径，`href` 属性中的链接替换为你的项目链接。</p>
            </div>
        </div>
    
        <div class="project-card">
            <a href="https://your-project4-link.com" class="project-title">项目四标题</a>
            <div class="project-image-container">
                <img src="./D.jpg" alt="项目D照片">
            </div>
            <div class="project-description">
                <p>这是项目四的详细文字说明，可能是一个跨学科融合的项目，结合了无线电、无人机和测向技术。确保图片和文字能够和谐地组合在一起，清晰地传达项目信息。</p>
                <p>如果需要更多区域，只需复制并修改 `project-card` 的 div 即可。</p>
            </div>
        </div>
    
    </div>
    
    我们致力于 **[无线电，无人机，测向小车]** 等前沿领域的研究。我们的口号是 **[我们永远不满足于现有方案，我们永远在探索更好、更优的第N种可能]**。
    
    如果您对我们的工作感兴趣，欢迎随时联系我们。

</div>
