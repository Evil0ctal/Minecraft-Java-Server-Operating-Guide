# 🚀 Minecraft-Java-Server-Operating-Guide 

> 本指南是一个全面的Minecraft服务器搭建指南，适用于初学者和有经验的服务器管理员。我们将从基本的准备工作到复杂的服务器优化，一步步引导你如何科学地搭建一个Minecraft Java服务器。
> 
> 🎥 本指南配有视频教程，带你手把手操作。
> 
> - [中文]：[Bilibili](https://space.bilibili.com/12505756/video)
>
> 🩷 也欢迎大家来我的Minecraft服务器游玩
> 
>  网站：[https://boba.cat/](https://boba.cat/)
> 
>  服务器版本: 1.20.1
> 
>  服务器位置：旧金山湾区
> 
>  服主微信：Evil0ctal
> 
>  服务器Discord：[https://discord.gg/shNgKgsgNs](https://discord.gg/shNgKgsgNs)  

## 📋 开服前的准备

在搭建服务器之前，需要做好充分的准备。以下是搭建Minecraft服务器之前需要考虑的几个要点：

- **Java版本**：Minecraft服务器运行在Java平台上，所以你需要安装合适的Java版本。通常情况下，Minecraft服务器需要Java 8或更高版本，2022年以后，大多需要Java17才能运行，所以请优先使用Java17，但具体需要哪个版本，取决于你选择的服务器后端。
- **服务器后端的选择**：有几种不同的服务器后端可供选择，包括Bukkit、Spigot、PaperMC、Forge、Fabric和Sponge等。每种后端都有其特点和优势，不同的后端在性能、兼容性和可定制性方面有所不同。你应该根据你的服务器的需求和预期的玩家数量来选择合适的后端。
- **游戏版本选择**：你需要选择一个Minecraft的游戏版本。同时，你可以使用特定的工具和插件（如ViaVersion, ViaBackwards, ViaRewind）来允许不同版本的客户端连接到你的服务器。
- **插件服与Mod服区别**：
  
  - **插件服**：通常使用Bukkit, Spigot或PaperMC等后端，允许你安装插件来增加游戏功能或改变游戏机制。插件不会修改游戏的核心代码，因此对客户端没有要求。
  - **Mod服**：需要特定的服务器软件（如Forge或Fabric），并且客户端也需要安装相同的Mods才能连接。Mods可以深度修改游戏内容和机制。
- **服务器的配置选择**：服务器配置取决于你预计的玩家数量和服务器类型。至少需要一个四核CPU和4GB以上的RAM。对于大型服务器或公共服务器，可能需要更高配置的服务器和专业的网络设置。
- **服务器环境**：你可以选择在Windows或Linux环境下运行你的服务器。Linux通常被认为在运行服务器时更加高效和稳定，但是如果你对Linux的指令感到陌生，请使用Windows进行操作。
- **服务器网络环境**：如果你没有公网IP，你可能需要使用内网穿透工具（如FRP）来公开你的服务器。同时，确保你的服务器网络安全，防止未经授权的访问。

## 💻 服务器后端的选择及其GitHub链接

在选择Minecraft服务器后端时，了解每个选项的特性和优势是非常重要的。这不仅影响服务器的性能，还影响着可用的特性和插件或Mods的兼容性。下面是一些流行的Minecraft服务器后端，并附上了它们的GitHub链接，以便于读者获取更多的开发信息和社区支持。

1. **Spigot**
   
   - **介绍**：Spigot 是Bukkit的一个分支，专注于提高性能和减少延迟。它提供了许多优化选项，可以通过配置文件调整，这使得服务器管理员能够根据自己的需求来优化服务器。
   - **GitHub链接**：[SpigotMC/Spigot](https://github.com/SpigotMC/Spigot) 🌐
2. **PaperMC**
   
   - **介绍**：PaperMC 是Spigot的一个分支，旨在进一步提高性能和响应速度。PaperMC 提供了更多的配置选项和性能优化，同时保持对Bukkit插件的高度兼容性。
   - **GitHub链接**：[PaperMC/Paper](https://github.com/PaperMC/Paper) 🌐
3. **CraftBukkit**
   
   - **介绍**：CraftBukkit 是Minecraft服务器的早期形式，提供了基础的服务器功能和插件支持。虽然现在多数被Spigot和PaperMC所取代，但仍有一些服务器选择使用CraftBukkit。
   - **GitHub链接**：[Bukkit/CraftBukkit](https://github.com/Bukkit/CraftBukkit) 🌐
4. **Forge**
   
   - **介绍**：Forge 是专注于Mod的服务器后端，提供了强大的Mod加载和兼容性支持。它允许服务器运行专门为Forge开发的Mods，非常适合那些想要彻底改变游戏玩法的服务器。
   - **GitHub链接**：[MinecraftForge/MinecraftForge](https://github.com/MinecraftForge/MinecraftForge) 🌐
5. **Fabric**
   
   - **介绍**：Fabric 是一个轻量级的模组加载器和API。它旨在提供基于Minecraft 1.14及之后版本的Mods和插件的最低限度的覆盖。Fabric 的目标是允许更多实验性的Mods的产生，同时保持它们自己的独立性。
   - **GitHub链接**：[FabricMC/fabric](https://github.com/FabricMC/fabric) 🌐
6. **Sponge**
   
   - **介绍**：Sponge 是一个开源项目，旨在创建一个插件开发框架。它工作在Minecraft Forge之上，并提供了一种兼容Forge Mods的方式来添加插件功能。
   - **GitHub链接**：[SpongePowered/Sponge](https://github.com/SpongePowered/Sponge) 🌐

在选择服务器后端时，需要考虑服务器的需求、预期的玩家数量、以及你希望服务器能够提供的功能。不同的后端在性能、兼容性和可定制性方面各有优劣。例如，如果你需要运行大量Mods，Forge或Fabric可能是最好的选择。如果你关注服务器的性能和响应速度，Spigot或PaperMC可能更合适。而对于那些希望有广泛插件支持的服务器，Sponge也是一个不错的选择。

选择适合自己的服务器后端后，你可以访问其GitHub页面来获取安装指南、配置说明以及社区的支持和贡献指南。这些资源将帮助你更好地管理和优化你的Minecraft服务器。

## 🚀 开启你的第一个服务器

> 相信当你阅读完上面的介绍后，对Minecraft服务器已经有了一定的认知，在下面我们将带你开启你的第一个Minecraft服务器，并且安装一些插件，然后使用PaperMC作为后端支持，运行在Windows上，随后使用FRP安全的将服务器暴露在互联网中。

### 1️⃣ 安装Microsoft OpenJDK 17

Minecraft服务器需要Java运行环境。我们推荐使用Microsoft OpenJDK 17，它是一个免费且经过优化的JDK版本。访问[Microsoft OpenJDK官网](https://www.microsoft.com/openjdk)下载适用于你的操作系统的安装包。

- 下载完成后，运行安装程序并按照指示完成安装。
- 安装完成后，打开命令提示符（Windows）或终端（Linux/macOS），输入 `java -version` 确认安装成功。你应该看到版本号为17的相关信息。

### 2️⃣ 下载PaperMC

PaperMC 是一个高性能的Minecraft服务器，提供了更好的性能和更多的配置选项。访问 [PaperMC官网](https://papermc.io/)，选择适合你的Minecraft版本的PaperMC。

- 下载 `.jar` 文件后，选择一个适合的位置创建一个文件夹，例如 `C:\MinecraftServer` 或 `/home/user/minecraftserver`。
- 将下载的 `.jar` 文件放入这个文件夹。

### 3️⃣ 运行服务器

打开命令提示符或终端，导航到你的服务器文件夹，使用以下命令启动服务器：

```bash
java -Xms1024M -Xmx2048M -jar paper-xxx.jar nogui
```
* `-Xms1024M` 和`-Xmx2048M` 分别是服务器的最小和最大内存限制。根据你的服务器硬件配置，你可能需要调整这些值。
* 如果是首次运行，服务器将要求你接受Minecraft的最终用户许可协议（EULA）。打开生成的`eula.txt` 文件，将`eula=false` 改为`eula=true`。

### 4️⃣ 配置服务器

服务器首次运行后，会生成 `server.properties` 文件，你可以在这里配置服务器的基本设置：

* `server-port`: 修改服务器监听的端口，默认是25565。
* `max-players`: 设置服务器允许连接的最大玩家数。
* `level-name`: 设置世界的名称，决定服务器使用哪个文件夹作为世界数据。

PaperMC 和 Spigot 提供了 `paper.yml` 和 `spigot.yml` 配置文件，你可以在这里进行更详细的设置，比如调整视距、实体数量和区块加载等，以优化服务器性能。

### 5️⃣ 安装和配置插件

PaperMC 支持 Bukkit 和 Spigot 插件，可以极大地扩展服务器的功能。

* 从网站如[SpigotMC]() 和[Bukkit]() 下载插件。
* 将`.jar` 文件放入`plugins` 文件夹。
* 重启服务器，插件将被加载。

**基本插件推荐**：

* **EssentialsX**: 提供基本功能，如家园、传送和私聊。
* **WorldEdit**: 强大的地图编辑工具。
* **PermissionsEx**: 权限管理插件，管理玩家权限。
* **Vault**: 提供各种经济系统的支持。

插件的配置文件通常会在首次加载时生成在 `plugins` 文件夹的相应插件子文件夹内。它们通常是YAML或JSON格式，可以用文本编辑器进行修改。

对于插件的调试和管理，你可以使用 **PlugMan** 插件来动态加载和卸载插件，这在测试时非常有用。选择插件时，请考虑插件的更新频率、社区反馈和是否适合你的服务器设定。

### 6️⃣ 使用FRP进行内网穿透

如果你没有公网IP，可以使用FRP将你的服务器暴露在互联网中。FRP是一个使用Go语言编写的专注于内网穿透的高性能的反向代理应用，支持 TCP、UDP、HTTP、HTTPS 等多种协议。可以将内网服务以安全、便捷的方式通过具有公网 IP 节点的中转暴露到公网。你需要一台具有公网IP的VPS作为入口。首先，在VPS上安装并配置FRP服务端（frps），然后在你的Minecraft服务器上安装并配置FRP客户端（frpc）。

* 下载FRP至你的电脑:
  * Windows和Linux请下载对应的版本。
  * 下载地址：[https://github.com/fatedier/frp/releases](https://github.com/fatedier/frp/releases)
* 配置FRP:
  * 服务端-拥有公网IP的机器（frps）:
    * 服务端只需要配置端口以及设置一个安全的连接密钥供客户端连接。
    * 标准的`frps.toml` 配置文件如下：
      ```toml
      bindPort = 7000
      auth.token = "REPLACE_YOUR_TOKEN（换成你的密钥）"
      ```
    * 在服务器或者云服务器面板中放行`bindPort` 和 frpc配置文件中`remotePort` 指定的端口，如默认的7000和下面演示的25566端口，不要忘记修改auth.token。
    * 使用以下命令启动frps服务：`./frps -c ./frps.toml`。
    * 如果需要在后台长期运行，建议结合其他工具，如[systemd](https://gofrp.org/zh-cn/docs/setup/systemd/) 和`supervisor`。
  * 客户端-运行Minecraft服务器的机器（frpc）:
    * 客户端需要填写与服务端一样的端口和auth.token
    * 标准的`frpc.toml` 配置文件如下：
      ```toml
      serverAddr = "REPLACE_YOUR_SERVER_IP（换成你的服务端IP）"
      serverPort = 7000
      auth.token = "REPLACE_YOUR_TOKEN（换成你的密钥）"
      
      [[proxies]]
      name = "Minecraft-Server-TCP-25566"
      type = "tcp"
      localIP = "127.0.0.1"
      localPort = 25565
      remotePort = 25566
      ```
    * 使用以下命令启动客户端：`frpc.exe -c ./frpc.toml`。
* 配置好FRPS和FRPC后，确保在VPS上设置好防火墙规则，只允许必要的端口（例如 Minecraft 端口和 FRP 端口）。
* 访问[FRP的GitHub页面](https://github.com/fatedier/frp) 获取详细的安装和配置指南。
* 现在只需要在客户端的多人游戏中输入运行frps（服务端）的IP地址以及25566端口即可进入服务器游玩。
* 格式如:`123.456.789.0:25566`

### 7️⃣ 备份服务器和权限控制

**备份**：定期备份你的服务器数据非常重要。你可以使用如 **eBackupPlugin** 插件自动备份，或者手动复制整个Minecraft服务器文件夹到安全的位置。

**权限控制**：使用权限插件如 **PermissionsEx** 或 **LuckPerms** 来管理玩家权限。合理的权限设置可以防止插件指令滥用，并确保玩家有良好的游戏体验。

通过上述步骤，你可以成功地搭建并运行一个高效、安全且功能丰富的Minecraft服务器。记得定期维护服务器，更新插件和服务器软件，以及与你的社区保持互动。祝你的Minecraft服务器旅程顺利！
