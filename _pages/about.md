---
permalink: /
title: #"Academic Pages is a ready-to-fork GitHub Pages template for academic personal websites"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
Hello! My name is **Zheng Zhang**(张政), an undergraduate student in Foundations of Mathematical Science at [Dalian University of Technology](https://www.dlut.edu.cn/). My research interests include machine learning and its applications in computer vision, currently focusing on Continual Learning and Brain-Inspired AI. I have previously worked on image insertion & harmonization, image recognition, and AI for Science.


Research
======

<style>
/* === 全局容器 === */
.paper-box {
  display: flex;
  flex-direction: row;
  gap: 20px; /* 间距加大到 30px，增加呼吸感 */
  margin-bottom: 17px; /* 每一条之间的距离拉大 */
  align-items: flex-start; /* 顶部对齐，这样文字多了也不会拉伸图片 */
  border: none; /* 去掉底部分割线，参考图是没线的，更干净 */
}

/* === 手机端适配 === */
@media (max-width: 768px) {
  .paper-box {
    flex-direction: column;
    gap: 15px;
    margin-bottom: 20px;
    padding-bottom: 20px;
  }
  .paper-box-image {
    width: 100% !important;
    max-width: 100% !important;
    height: auto !important;
    flex: none !important;
  }
  .paper-box-image img {
    height: auto !important; 
    object-fit: unset !important;
  }
}

/* === 图片卡片区域 === */
.paper-box-image {
  flex: 0 0 192px; 
  width: 192px;
  height: 120px;   /* 高度稍微改扁一点，更符合视觉比例 */
  position: relative;
  overflow: visible !important;
  border-radius: 8px; /* 圆角稍微收一点，太圆了像手机APP图标 */
  box-shadow: 
    /* 第一层：深色、紧贴、用于勾勒轮廓 (Key Shadow) */
    0 2px 5px rgba(0, 0, 0, 0.25),
    /* 第二层：浅色、扩散大、用于制造悬浮氛围 (Ambient Shadow) */
    0 10px 20px rgba(0, 0, 0, 0.35); 
  transition: all 0.3s ease
  margin-top: 5px; /* 让图片稍微往下一点，对齐文字的第一行视觉重心 */
}

.paper-box-image img {
  width: 100%;
  height: 100%;
  object-fit: cover; 
  object-position: center;
  display: block;
  border-radius: 8px;
  transition: transform 0.3s ease;
}

.paper-box-image:hover img {
  transform: scale(1.05);
}

.paper-box-image:hover {
  transform: translateY(-2px); /* 物理上浮 2px */
  box-shadow: 
    0 4px 8px rgba(0, 0, 0, 0.2),
    0 15px 30px rgba(0, 0, 0, 0.3);
}

/* === 徽章样式 (Times New Roman) === */
.paper-badge {
  position: absolute;
  top: 8px;
  left: -5px; /* 贴左边，或者 left: 10px 悬浮 */
  background-color: #003399; 
  color: white;
  font-family: "Times New Roman", Times, serif; 
  font-weight: bold;
  font-size: 12px; /* 字号微调 */
  letter-spacing: 0.5px;
  padding: 3px 10px;
  border-radius: 4px; 
  box-shadow: 2px 2px 5px rgba(0,0,0,0.3); 
  z-index: 10;
  pointer-events: none;
}

/* === 文字内容区域 (核心修改部分) === */
.paper-box-text {
  flex: 1;
  font-family: "Times New Roman", serif; 
}

/* 1. 标题：不再是链接，颜色深灰，字号适中 */
.paper-title {
  font-size: 16px !important; /* 从很大的20+px降到18px，精致感来源 */
  font-weight: bold; /* 粗体 */
  color: #444;      /* 不是纯黑，是深灰 */
  line-height: 1.4;
  margin-bottom: 8px; /* 标题下方留白 */
}

/* 2. 作者：字号更小，颜色稍微浅一点 */
.paper-authors {
  font-size: 14px !important;  /* 正文字号 */
  color: #555;      /* 中灰 */
  line-height: 1.5;
  margin-bottom: 6px;
}

/* 3. 会议：斜体，字号最小 */
.paper-venue {
  font-size: 14px !important; 
  font-style: italic;
  color: #666;
  margin-bottom: 10px;
}

.venue-bold {
  color: #428bca; /* 蓝色高亮 */
  font-weight: bold;
  font-style: italic; /* 年份通常不需要斜体，突出显示 */
}

/* 4. 底部链接 */
.paper-links {
  font-size: 14px !important;
  font-family: Georgia, "Bitstream Charter", "Times New Roman", serif;
}
.paper-links a {
  display: inline-block;
  text-decoration: none;
  color: #428bca; /* 链接蓝 */
  margin-right: 10px;
  font-weight: bold;
}
.paper-links a:hover {
  text-decoration: underline;
  color: #2a6496;
}

/* === 新增：专门用于项目奖项列表的样式 === */
.project-awards {
  font-family: "Times New Roman", serif; /* 保持学术字体 */
  font-size: 13px;      /* 字号适中 */
  color: #444;          /* 深灰色，比纯黑柔和 */
  line-height: 1.3;     /* 行高拉大一点，防止多行拥挤 */
  margin-top: 8px;      /* 距离上面的 Leader 拉开一点距离 */
  margin-bottom: 10px;
}

/* 列表容器样式：去掉默认的大缩进 */
.project-awards ul {
  margin: 0;
  padding-left: 18px; /* 稍微缩进一点，让圆点对齐文字 */
  list-style-type: disc; /* 实心圆点 */
}

/* 单个奖项样式 */
.project-awards li {
  margin-bottom: 3px; /* 每个奖项之间留点空隙 */
}
  
</style>


<!-- 内容展示 Block -->
<div class="paper-box">
  
  <div class="paper-box-image">
    <div class="paper-badge">AAAI</div>
    <img src="/images/themes/Pworkflow.png" alt="Paper Thumbnail">
  </div>

  <div class="paper-box-text">
    <!-- 标题：现在是纯文本，移除了 <a href...> -->
    <div class="paper-title">
      SinBasis Networks: Matrix‑Equivalent Feature Extraction for Wave‑Like Optical Spectrograms
    </div>
    
    <div class="paper-authors">
      Yuzhou Zhu, <strong>Zheng Zhang</strong>, Ruyi Zhang, Liang Zhou
    </div>
    
    <div class="paper-venue">
      AAAI Conference on Artificial Intelligence. <span class="venue-bold">AAAI 2026</span>
    </div>
    
    <div class="paper-links">
      <a href="https://arxiv.org/abs/2505.06275">[Paper]</a>
    </div>
  </div>
  
</div>


<div class="paper-box">
  
  <div class="paper-box-image">
    <img src="/images/themes/STAGE.png" alt="Paper Thumbnail">
  </div>

  <div class="paper-box-text">
    <!-- 标题：现在是纯文本，移除了 <a href...> -->
    <div class="paper-title">
      When Classes Evolve: A Benchmark and Framework for Stage-Aware Class-Incremental Learning
    </div>
    
    <div class="paper-authors">
      First Author
    </div>
    
    <div class="paper-venue">
      CVPR under review. 
    </div>
    
    <div class="paper-links">
      <a href="https://doi.org/10.13140/RG.2.2.35822.27205">[An Early Version]</a>
      <!-- <a href="#">[Code]</a> -->
    </div>
  </div>
  
</div>



<div class="paper-box">
  
  <div class="paper-box-image">
    <img src="/images/themes/simpleBTSP.png" alt="Paper Thumbnail">
  </div>

  <div class="paper-box-text">
    <!-- 标题：现在是纯文本，移除了 <a href...> -->
    <div class="paper-title">
      Learning at Behavioral Timescales: A Sparse Statistical Framework for Zero-Gradient Class-Incremental Learning
    </div>
    
    <div class="paper-authors">
      First Author
    </div>
    
    <div class="paper-venue">
      target submission ICML. 
    </div>
    
  </div>
  
</div>

Projects
======
<div class="paper-box">
  
  <div class="paper-box-image">
    <img src="/images/themes/linggong.png" alt="Paper Thumbnail">
  </div>

  <div class="paper-box-text">
    <!-- 标题：现在是纯文本，移除了 <a href...> -->
    <div class="paper-title">
      Linggong IntelliVision: Pioneer in Multifunctional AI Imaging Platform
    </div>
    
    <div class="paper-authors">
      <strong>Leader</strong>
    </div>
    
    <div class="project-awards">
      <ul>
        <li><strong>National Second Prize</strong>, The 18th International Contest of innovAtioN (iCAN), 2024</li>
        <li><strong>National Third Prize</strong>, Global Campus Artificial Intelligence Algorithm Elite Competition, 2025</li>
        <li><strong>National Third Prize</strong>, China Collegiate Computing Contest (C4) – AIGC Innovation Contest, 2025</li>
        <li><strong>Gold Award</strong>, China International College Students' Innovation Competition (DUT Campus Selection), 2025</li>
      </ul>
    </div>
    
  </div>
  
</div>


<div class="paper-box">
  
  <div class="paper-box-image">
    <img src="/images/themes/echoforest.png" alt="Paper Thumbnail">
  </div>

  <div class="paper-box-text">
    <!-- 标题：现在是纯文本，移除了 <a href...> -->
    <div class="paper-title">
      EchoForest——World's First Pixelated Spatial Audio Sound System
    </div>
    
    <div class="paper-authors">
      Third Member, Algorithm & Software Lead
    </div>
    
    <div class="project-awards">
      <ul>
        <li><strong>Bronze Award</strong>, China International College Students' Innovation Competition, 2025</li>
        <li><strong>Provincial First Prize</strong>, "Challenge Cup" Liaoning College Students' Entrepreneurship Competition, 2024</li>
        <li><strong>First Prize</strong>, DUT "Pandeng Cup" Innovation and Entrepreneurship Competition, 2024</li>
      </ul>
    </div>
    
  </div>
  
</div>



<div class="paper-box">
  
  <div class="paper-box-image">
    <img src="/images/themes/chem.png" alt="Paper Thumbnail">
  </div>

  <div class="paper-box-text">
    <!-- 标题：现在是纯文本，移除了 <a href...> -->
    <div class="paper-title">
      Intelligent Chemical Titration Analysis Device Based on Pruned YOLOv8
    </div>
    
    <div class="paper-authors">
      <strong>Leader</strong>
    </div>
    
    <div class="project-awards">
      <ul>
        <li><strong>National First Prize</strong>, Intelligent Chemistry Experiment Challenge, 2024</li>
        <li><strong>First Prize (Ranked 1st)</strong>, DUT Intelligent Chemistry Experiment Challenge, 2024</li>
      </ul>
    </div>
    
  </div>
  
</div>


Academic Services
======
*  Conference Reviewer: AAAI.
*  Journal Reviewer: KBS.
