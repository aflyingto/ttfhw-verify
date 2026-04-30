# ttfhw-verify

TTFHW (Time To First Hello World) 仓库编译验证 Skill。

验证仓库能否成功编译和运行单元测试，输出 JSON 格式的客观指标报告。

## 安装

使用 skills CLI 安装：

```bash
npx skills add aflyingto/ttfhw-verify
```

安装后可在 Claude Code 中使用 `/ttfhw-verify` 命令。

## 功能

- 克隆仓库并检查文档完整性
- 自动选择合适的 Docker 镜像
- 尪环尝试解决构建依赖问题（不修改源码）
- 运行单元测试
- 生成 JSON 验证报告

## 使用

```bash
/ttfhw-verify                  # 交互式验证
/ttfhw-verify example-repo     # 直接验证指定仓库
/ttfhw-verify --remote IP      # 指定远端服务器
```

## 输出

验证完成后生成 `build-verification/<repo>/verification_report.json`，包含：

- 构建状态和产物
- UT 通过/失败数量
- 各阶段时长统计
- 所有尝试记录日志

## 许可证

MIT License