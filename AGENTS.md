# 最终源码仓库协作约定

- 本目录为用户明确指定的最终源码仓库，远程 origin 为 https://github.com/shiyirong0128/DS_WORK_FINAL.git。
- 本次交付源于 DS_WORK2 的 07_Skill审查与修复，来源提交记录在 SOURCE.json。正式入口为 index.html，保留单文件离线能力。
- 维护源文件 src/ 和 scripts/build.mjs，运行 node scripts/build.mjs 重新生成 HTML；不要只改生成后的页面。
- 本仓库仅保存最终方向的页面、源码、依赖与相关测试，不导入旧仓库或其他方案历史。
- 提交本轮相关文件，保留历史，不强制推送；使用用户提供的步骤名称作为提交说明。如新代码修改轮次未提供名称，先完成可开展的工作，再询问名称。
- 完成后报告提交标识和推送结果；不要把本地提交称为已上传。
- 已按用户要求开源并发布到 GitHub Pages，公开地址为 https://shiyirong0128.github.io/DS_WORK_FINAL/；发布源为 main 分支根目录，保留 .nojekyll。
- 项目代码使用 MIT License；VT323 字体仍使用 assets/fonts/terminal-OFL.txt 中的 SIL OFL 1.1，不将第三方字体改为 MIT。
- 更新玩法或样式后重新构建并验证，再提交生成的 HTML。涉及在线发布时核对远端构建结果和匿名访问，不把尚未发布的页面称为已上线。
