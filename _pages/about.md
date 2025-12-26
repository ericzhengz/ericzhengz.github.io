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
  gap: 25px; /* 间距加大到 30px，增加呼吸感 */
  margin-bottom: 35px; /* 每一条之间的距离拉大 */
  align-items: flex-start; /* 顶部对齐，这样文字多了也不会拉伸图片 */
  border: none; /* 去掉底部分割线，参考图是没线的，更干净 */
}

/* === 手机端适配 === */
@media (max-width: 768px) {
  .paper-box {
    flex-direction: column;
    gap: 15px;
    margin-bottom: 30px;
    border-bottom: 1px solid #eee; /* 手机上加个线区分一下 */
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
  flex: 0 0 220px; 
  width: 220px;
  height: 130px;   /* 高度稍微改扁一点，更符合视觉比例 */
  position: relative;
  overflow: hidden;
  border-radius: 8px; /* 圆角稍微收一点，太圆了像手机APP图标 */
  box-shadow: 0 4px 10px rgba(0,0,0,0.12); /* 阴影 */
  margin-top: 5px; /* 让图片稍微往下一点，对齐文字的第一行视觉重心 */
}

.paper-box-image img {
  width: 100%;
  height: 100%;
  object-fit: cover; 
  object-position: center top;
  display: block;
  transition: transform 0.3s ease;
}

.paper-box-image:hover img {
  transform: scale(1.05);
}

/* === 徽章样式 (Times New Roman) === */
.paper-badge {
  position: absolute;
  top: 10px;
  left: -2px; /* 贴左边，或者 left: 10px 悬浮 */
  background-color: #003399; 
  color: white;
  font-family: "Times New Roman", Times, serif; 
  font-weight: bold;
  font-size: 13px; /* 字号微调 */
  letter-spacing: 0.5px;
  padding: 3px 8px;
  border-radius: 0 3px 3px 0; /* 变成左侧贴边的标签样式，参考图有时候是贴边的 */
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
  font-size: 17px; /* 从很大的20+px降到18px，精致感来源 */
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
  font-size: 14px; 
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
  font-size: 12px;
  font-family: "Times New Roman", serif;
}
.paper-links a {
  display: inline-block;
  text-decoration: none;
  color: #428bca; /* 链接蓝 */
  margin-right: 12px;
  font-weight: bold;
}
.paper-links a:hover {
  text-decoration: underline;
  color: #2a6496;
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
      <!-- <a href="#">[Code]</a> -->
    </div>
  </div>
  
</div>





Like many other Jekyll-based GitHub Pages templates, Academic Pages makes you separate the website's content from its form. The content & metadata of your website are in structured Markdown files, while various other files constitute the theme, specifying how to transform that content & metadata into HTML pages. You keep these various Markdown (.md), YAML (.yml), HTML, and CSS files in a public GitHub repository. Each time you commit and push an update to the repository, the [GitHub pages](https://pages.github.com/) service creates static HTML pages based on these files, which are hosted on GitHub's servers free of charge.

Many of the features of dynamic content management systems (like Wordpress) can be achieved in this fashion, using a fraction of the computational resources and with far less vulnerability to hacking and DDoSing. You can also modify the theme to your heart's content without touching the content of your site. If you get to a point where you've broken something in Jekyll/HTML/CSS beyond repair, your Markdown files describing your talks, publications, etc. are safe. You can rollback the changes or even delete the repository and start over - just be sure to save the Markdown files! You can also write scripts that process the structured data on the site, such as [this one](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb) that analyzes metadata in pages about talks to display [a map of every location you've given a talk](https://academicpages.github.io/talkmap.html).

For those users that need more advanced functionality, the template also supports the following popular tools:
- [MathJax](https://www.mathjax.org/) for mathematical equations
- [Mermaid](https://mermaid.js.org/) for diagraming
- [Plotly](https://plotly.com/javascript/) for plotting

Getting started
======
1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Fork [this template](https://github.com/academicpages/academicpages.github.io) by clicking the "Use this template" button in the top right. 
1. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and create content & metadata (see below -- also see [this set of diffs](https://archive.is/3TPas) showing what files were changed to set up [an example site](https://getorg-testacct.github.io) for a user with the username "getorg-testacct")
1. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section

Site-wide configuration
------
The main configuration file for the site is in the base directory in [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml), which defines the content in the sidebars and other site-wide features. You will need to replace the default variables with ones about yourself and your site's github repository. The configuration file for the top menu is in [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). For example, if you don't have a portfolio or blog posts, you can remove those items from that navigation.yml file to remove them from the header. 

Create content & metadata
------
For site content, there is one Markdown file for each type of content, which are stored in directories like _publications, _talks, _posts, _teaching, or _pages. For example, each talk is a Markdown file in the [_talks directory](https://github.com/academicpages/academicpages.github.io/tree/master/_talks). At the top of each Markdown file is structured data in YAML about the talk, which the theme will parse to do lots of cool stuff. The same structured data about a talk is used to generate the list of talks on the [Talks page](https://academicpages.github.io/talks), each [individual page](https://academicpages.github.io/talks/2012-03-01-talk-1) for specific talks, the talks section for the [CV page](https://academicpages.github.io/cv), and the [map of places you've given a talk](https://academicpages.github.io/talkmap.html) (if you run this [python file](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py) or [Jupyter notebook](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb), which creates the HTML for the map based on the contents of the _talks directory).

**Markdown generator**

The repository includes [a set of Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator
) that converts a CSV containing structured data about talks or presentations into individual Markdown files that will be properly formatted for the Academic Pages template. The sample CSVs in that directory are the ones I used to create my own personal website at stuartgeiger.com. My usual workflow is that I keep a spreadsheet of my publications and talks, then run the code in these notebooks to generate the Markdown files, then commit and push them to the GitHub repository.

How to edit your site's GitHub repository
------
Many people use a git client to create files on their local computer and then push them to GitHub's servers. If you are not familiar with git, you can directly edit these configuration and Markdown files directly in the github.com interface. Navigate to a file (like [this one](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md) and click the pencil icon in the top right of the content preview (to the right of the "Raw | Blame | History" buttons). You can delete a file by clicking the trashcan icon to the right of the pencil icon. You can also create new files or upload files by navigating to a directory and clicking the "Create new file" or "Upload files" buttons. 

Example: editing a Markdown file for a talk
![Editing a Markdown file for a talk](/images/editing-talk.png)

For more info
------
More info about configuring Academic Pages can be found in [the guide](https://academicpages.github.io/markdown/), the [growing wiki](https://github.com/academicpages/academicpages.github.io/wiki), and you can always [ask a question on GitHub](https://github.com/academicpages/academicpages.github.io/discussions). The [guides for the Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (which this theme was forked from) might also be helpful.
