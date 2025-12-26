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

<!-- 直接嵌入样式 (Style Block) -->
<style>
/* 容器样式 */
.paper-box {
  display: flex;
  flex-wrap: wrap;
  gap: 25px;
  margin-bottom: 30px;
  align-items: flex-start;
  border-bottom: 1px solid #e0e0e0;
  padding-bottom: 20px;
}

/* 图片区域 */
.paper-box-image {
  position: relative;
  width: 100%;
  max-width: 260px;
  flex-shrink: 0;
}
.paper-box-image img {
  width: 100%;
  border-radius: 4px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.15);
  display: block;
}

/* 徽章样式 (修正了定位问题) */
.paper-badge {
  position: absolute;
  top: 15px;
  left: -8px; /* 悬挂在左侧 */
  background-color: #003399;
  color: white;
  padding: 4px 10px;
  font-weight: bold;
  font-size: 14px;
  box-shadow: 2px 2px 4px rgba(0,0,0,0.3);
  z-index: 10;
  border-radius: 0 2px 2px 0;
}

/* 文字区域 */
.paper-box-text {
  flex-grow: 1;
  min-width: 300px;
}
.paper-box-text h4 {
  font-size: 1.2em;
  font-weight: bold;
  margin-top: 0;
  margin-bottom: 8px;
  color: #333;
}
.paper-authors {
  color: #555;
  margin-bottom: 8px;
  font-size: 1em;
}
.paper-venue {
  font-style: italic;
  color: #666;
  margin-bottom: 12px;
}
.venue-bold {
  color: #428bca;
  font-weight: bold;
}
.paper-links a {
  text-decoration: none;
  color: #428bca;
  margin-right: 12px;
  font-weight: 500;
}
.paper-links a:hover {
  text-decoration: underline;
}
</style>

<!-- 内容部分 -->
<div class="paper-box">
  
  <!-- 左侧图 + 徽章 -->
  <div class="paper-box-image">
    <div class="paper-badge">AAAI</div>
    <!-- 请确认图片路径正确，如果不显示请检查文件名大小写 -->
    <img src="/images/themes/Pworkflow.png" alt="Paper Thumbnail">
  </div>

  <!-- 右侧文字 -->
  <div class="paper-box-text">
    <h4>SinBasis Networks: Matrix‑Equivalent Feature Extraction for Wave‑Like Optical Spectrograms</h4>
    
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
