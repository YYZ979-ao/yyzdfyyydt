# 声纹中国：非遗声音航线（作业2）

这是与 `zuoye1` 明显区分的第二版非遗音乐地图。页面采用深色声音航线布局，包含地图标记、曲目抽屉和底部独立播放器。

## 曲目构成

- 教师示例：澳门咸水歌《攞鱼歌》
- 教师示例：台湾客家山歌《老山歌》
- 新增曲目：川江号子《川江船夫号子》
- 新增曲目：维吾尔木卡姆《拉克木卡姆·散序》
- 新增曲目：昆曲《牡丹亭·皂罗袍》
- 新增曲目：花儿《上去高山望平川》
- 新增曲目：西安鼓乐《雨霖铃》

五首新增曲目均来自 `十首非遗` 文件夹中没有在 `zuoye1` 使用的 MP4 视频，并已提取为体积更适合网页播放的 MP3 文件。

## 运行方法

1. 使用 VS Code 打开 `C:\Users\admin\Desktop\zuoye2`。
2. 打开 `index.html`。
3. 点击 VS Code 右下角的 `Go Live`。
4. 在浏览器中点击左侧曲目或地图编号即可定位并播放。

## GitHub Pages 部署注意

排查过一次线上无声：`index.html` 里写的路径是 `./assets/xxx.mp3`，如果上传时只把 7 个 MP3 扔进仓库**根目录**，线上会全部 404、表现为「播放没有声音」。

- 网页端上传时，**直接拖拽整个 `assets` 文件夹**到上传区（不要只框选里面的 mp3 文件），才能保留目录结构。
- 部署后先在浏览器打开 `https://<用户名>.github.io/<仓库名>/assets/luoyuge.mp3` 自检：能下载到约 3.7MB 的音频即为正确，返回 404 说明目录没传上去。
- 现在的 `index.html` 已内置容错：若 `assets/` 下找不到音频，会自动回退到根目录同名文件，并在播放器副标题处显示失败原因。

## 文件结构

```text
zuoye2/
├── index.html
├── README.md
└── assets/
    ├── luoyuge.mp3
    ├── laushange-hsu.mp3
    ├── chuanjiang-haozi.mp3
    ├── rak-muqam.mp3
    ├── mudanting-zaoluopao.mp3
    ├── gaoshan-wang-pingchuan.mp3
    └── yulinling.mp3
```

## 提交前检查

- 地图显示 7 个编号标记。
- 左侧列表与底部播放器可以切换曲目。
- 七段音频都能正常播放。
- 上传时必须包含完整的 `assets` 文件夹。
- 使用 Live Server 或 GitHub Pages 打开，不建议直接双击 HTML。
