# LMbench

<!-- vim-markdown-toc GFM -->

* [參數](#參數)
    - [系統](#系統)
    - [目標](#目標)
* [環境](#環境)
    - [cross compiler](#cross-compiler)
* [LMbench](#lmbench)
    - [下載](#下載)
    - [構建](#構建)
    - [執行](#執行)

<!-- vim-markdown-toc -->

---

## 參數

### 系統

-   Ubuntu 18.04（WSL）

### 目標

-   arm64

## 環境

### cross compiler

```zsh
sudo apt install -y gcc-aarch64-linux-gnu
```

## LMbench

### 下載

```zsh
wget https://downloads.sourceforge.net/project/lmbench/development/lmbench-3.0-a9/lmbench-3.0-a9.tgz
tar xvfz lmbench-3.0-a9.tgz
```

### 構建

```zsh
cd lmbench-3.0-a9

make OS=aarch64 CC="aarch64-linux-gnu-gcc -static"
```

### 執行

```
./bin/aarch64/bw_mem 512m [執行檔]
```
