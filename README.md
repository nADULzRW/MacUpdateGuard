# MacUpdateGuard 使用指南  
**三步掌控 macOS 系统更新**  

---

## 一、下载安装  
### 方法① 一键安装（推荐）  
复制粘贴到终端执行：  
```bash  
cd ~ && \  
curl -O https://raw.githubusercontent.com/ArdANANG/MacUpdateGuard/main/MacUpdateGuard.sh && \  
chmod +x MacUpdateGuard.sh && \  
sudo ./MacUpdateGuard.sh  
```  

### 方法② 手动安装  
1. **下载文件**  
   - 访问 [项目主页](https://github.com/ArdANANG/MacUpdateGuard)  
   - 点击绿色 `Code` 按钮 → `Download ZIP`  

2. **解压移动**  
   ```bash  
   # 打开终端（应用程序→实用工具→终端）  
   mv ~/Downloads/MacUpdateGuard-main/MacUpdateGuard.sh ~/  
   ```  

3. **授权运行**  
   ```bash  
   chmod +x ~/MacUpdateGuard.sh  # 添加执行权限  
   ```

---

## 二、首次配置  
1. 启动工具：  
   ```bash  
   sudo ~/MacUpdateGuard.sh  # 需要输入密码  
   ```  

2. 选择安装选项：  
   ```  
   [提示] 选择操作：  
   1. 自动安装到用户目录并启动（推荐）→ 按 1  
   2. 继续在当前目录执行  
   3. 退出  
   ```  

> 💡 选择 **1** 将自动完成最终配置  

---

## 三、日常使用  
### 主菜单功能：  
```  
1. 禁用系统自动更新  🚫  
2. 恢复系统自动更新  🔄  
3. 检查更新状态      📊  
4. 显示版本信息      ℹ️  
5. 退出              👋  
```  

### 快捷操作：  
```bash  
# 创建快捷命令（添加到 ~/.zshrc）  
alias updateguard="sudo ~/MacUpdateGuard.sh"  

# 以后只需输入：  
updateguard  
```  

---

## 四、注意事项  
1. **操作后建议重启**  
   - 禁用/恢复更新后，选择"立即重启"使设置完全生效  

2. **更新到最新版**  
   ```bash  
   cd ~  
   rm MacUpdateGuard.sh  
   curl -O https://raw.githubusercontent.com/ArdANANG/MacUpdateGuard/main/MacUpdateGuard.sh  
   chmod +x MacUpdateGuard.sh  
   ```  

3. **查看状态**  
   - 定期使用选项 3 检查系统更新状态  
   - 打开 `系统设置 > 通用 > 软件更新` 验证  

---

**开发者**：bili_25396444320  
**最新版本**：v3.9  
**更新日期**：2025年7月13日  

> 🌟 提示：首次运行后脚本将永久保存在您的主目录  
> 随时通过 `sudo ~/MacUpdateGuard.sh` 管理系统更新！  
