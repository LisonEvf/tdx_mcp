# tdx-mcp

基于通达信行情服务器的 MCP Server，为 Claude、Cursor 等 AI 助手提供实时股票数据接口。

底层依赖 [opentdx](https://github.com/LisonEvf/opentdx)（子模块）

> **声明**：本项目为个人学习项目，连接通达信公开行情服务器，严禁用于商业用途，严禁滥用接口。

## MCP Server 一键配置

支持 Claude、Cursor、OpenClaw 等 AI 助手直接调用股票数据。

### 方式一：uvx（推荐）

```json
{
  "mcpServers": {
    "tdx": {
      "command": "uvx",
      "args": ["--from", "tdx-mcp", "tdx-mcp"]
    }
  }
}
```

### 方式二：pip 安装后直接运行

```json
{
  "mcpServers": {
    "tdx": {
      "command": "tdx-mcp"
    }
  }
}
```

## 支持的数据

| 类别 | 说明 |
|------|------|
| A股行情 | 沪深北交所、创业板、科创板 |
| 扩展行情 | 期货、港股、美股、期权 |
| K线 | 多周期（1分/5分/日线/周线等），支持前/后复权 |
| 分时 | 实时/历史分时数据 |
| 排行榜 | 涨跌幅、振幅、换手率、量比等 |
| 异动监控 | 主力监控精灵 |
| F10 | 公司基本信息、财报 |
| 技术指标 | MA、EMA、MACD、RSI、KDJ、BOLL、ATR |

## MCP Tools 一览

### 股票数据

| Tool | 说明 |
|------|------|
| `get_index_overview` | 指数概况（上证/深证/北证/创业/科创/沪深300） |
| `stock_kline` | K线数据，支持复权 |
| `stock_quotes` | 个股/批量报价 |
| `stock_quotes_list` | 板块行情列表，支持排序过滤 |
| `stock_tick_chart` | 分时图 |
| `stock_top_board` | 涨跌/振幅/量比等排行榜 |
| `stock_transaction` | 历史成交 |
| `stock_auction` | 竞价数据 |
| `stock_unusual` | 异动监控 |
| `stock_f10` | F10 公司信息 |

### 扩展行情

| Tool | 说明 |
|------|------|
| `goods_kline` | 期货/港股/美股 K线 |
| `goods_quotes` | 扩展行情报价 |
| `goods_quotes_list` | 扩展行情列表 |
| `goods_tick_chart` | 商品分时图 |
| `goods_history_transaction` | 商品历史成交 |

### 技术指标

| Tool | 说明 |
|------|------|
| `indicator_ma` | 移动平均线 |
| `indicator_ema` | 指数移动平均 |
| `indicator_macd` | MACD |
| `indicator_rsi` | RSI |
| `indicator_kdj` | KDJ |
| `indicator_boll` | 布林带 |
| `indicator_atr` | 真实波动幅度 |
| `indicator_vol_ma` | 成交量均线 |

---

[![Star History Chart](https://api.star-history.com/svg?repos=LisonEvf/tdx_mcp&type=Date)](https://star-history.com/#LisonEvf/tdx_mcp&Date)
