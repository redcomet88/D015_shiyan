# D015 vue+django知识图谱问答系统电子实验物理实验工科方向的neo4j数据库+LTP模型

> 完整项目收费，可联系QQ: 81040295 微信: mmdsj186011 注明从git来的，谢谢！
也可以关注我的B站： 麦麦大数据 https://space.bilibili.com/1583208775
> 

up主B站：  **麦麦大数据**
关注B站，有好处！
编号:  D015
## 视频

[video(video-HARyehaT-1761049128880)(type-bilibili)(url-https://player.bilibili.com/player.html?aid=115409512570807)(image-https://i-blog.csdnimg.cn/img_convert/1d4a1e507a1807b594fca64d397f5ac1.jpeg)(title-D015 vue+django 物理电子实验与仪器知识图谱可视化智能问答系统)]

## 1 系统简介
系统简介：本系统是一个基于Vue+Django+Neo4j+MySQL构建的大学物理电子实验知识服务平台，旨在为学生和教师提供一个高效、直观的知识查询和学习平台。系统的核心功能包括大学物理实验知识图谱的构建与可视化、智能问答服务、以及用户信息管理四大模块。主要功能如下：首先通过知识图谱模块，将大学物理实验相关的知识（如实验步骤、仪器设备、实验现象等）以可视化的方式呈现，并支持关键词检索功能；其次，智能问答模块能够自动解答用户关于实验操作、仪器使用等问题；最后，用户管理模块提供个人信息修改、头像上传、密码修改，以及登录注册功能，确保用户的个性化体验和系统的安全性。
## 2 功能设计
该系统采用典型的B/S（浏览器/服务器）架构模式。用户通过浏览器访问Vue前端界面，该前端由HTML、CSS、JavaScript以及Vue.js生态系统中的Vuex（用于状态管理）、Vue Router（用于路由导航）和Echarts或其他可视化库（用于知识图谱展示）等组件构建。前端通过API请求与Django后端进行数据交互，Django后端则负责业务逻辑处理，并与MySQL数据库进行持久化数据存储，用于存储用户信息、实验数据等结构化数据。此外，系统还集成了Neo4j图数据库，用于存储和查询实验与仪器的知识图谱关系数据，为智能问答和可视化功能提供支撑。

在智能问答模块中，系统结合自然语言处理（NLP）技术和图数据库的查询能力，能够自动解析用户提出的问题并从知识图谱中检索相关信息，提供准确的答案。知识图谱的构建包括实验与仪器的关系模型，涵盖实验的基本信息、实验步骤、所需仪器设备以及仪器的使用方法等内容。

用户管理模块不仅支持基本的登录和注册功能，还允许用户修改个人信息、更换头像（用于页面右上角显示及问答交互中的个人标识）以及修改密码，确保用户信息的安全和系统的个性化体验。
### 2.1系统架构图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/bb6dffafc8dc4ef78dd9b8198084339c.png)
### 2.2 功能模块图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/110226f2202849c3b6781ae8b1bb6281.png)
## 3 功能展示
### 3.1 登录 & 注册
登录界面背景是一个视频，展示和本文系统主题相匹配的内容，登录和注册界面在一个界面下，通过按钮来切换，注册界面输入用户名和密码，会检查这个用户是否存在，登录界面则要检查用户名是否存在以及用户名密码是否正确：  
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7098c76d413c47c195a7e25b9a824c6e.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4017c1319b5e4f4bb7125c595d3be5cc.png)
### 3.2 主页
如果通过校验，则可以进入主页，在主页是一个左侧菜单，右侧操作面板的布局，右上角是登录用户的头像和退出按钮：
### 3.3 知识图谱
neo4j 界面展示知识图谱：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/acc690f1fd6148ff8df555d508ca7694.png)
本利用echarts实现的知识图谱可视化：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/195cb49c27c34462a7ee2b513cdb1a0e.png)
支持输入关键词进行知识图谱的检索，从而展示子图：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6aa19997466c4177bb8881559dda6a58.png)
### 3.4 智能问答
基于LTP+neo4j知识图谱的问答功能，可以咨询实验相关的各类知识：
比如可以咨询实验怎么做啊？ 需要用到的仪器？仪器使用的注意事项等，可以点击回复内容打开查看详情。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9d91629cf2e44b9494384d54458e616e.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/fc20d8ac41e442dcbada2716a90facec.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4e64e957d1d04196915dcbbfb7d411c8.png)
### 3.5 个人设置
个人设置方面包含了**用户信息修改**、**密码修改**功能。
用户信息修改中可以上传头像，完成用户的头像个性化设置，也可以修改用户其他信息。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/934e0a8aab284974b1a24e99eb5e8fb0.png)
修改密码需要输入用户旧密码和新密码，验证旧密码成功后，就可以完成密码修改。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/e5362c4ee5c7464796e9e8155b876faa.png)

## 4程序代码
### 4.1 代码说明
代码介绍：本项目旨在实现电子物理实验知识图谱的可视化，通过读取Neo4j数据库中的数据，构建并展示知识图谱。知识图谱能够直观地展示实验中概念、实体及其关联关系，帮助学生和研究人员更好地理解实验内容。本项目包括以下主要功能：
从Neo4j数据库中读取实验相关的节点和关系数据
使用echarts库构建实验知识图谱
利用可视化工具生成并展示知识图谱
### 4.2 流程图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/04a6028adeb9497da9a19114b9cdf112.png)
### 4.3 代码实例
```python
# -*- coding: UTF-8 -*-
import matplotlib.pyplot as plt
import networkx as nx
from neo4j import GraphDatabase

def load_data_from_neo4j(uri, auth):
    """
    从Neo4j数据库中读取电子物理实验数据
    """
    driver = GraphDatabase.driver(uri, auth=auth)
    query = """
        MATCH (n) 
        RETURN n
    """
    results = driver.run(query)
    nodes = []
    for result in results:
        nodes.append(result["n"])
    driver.close()
    return nodes

def build_knowledge_graph(nodes):
    """
    构建知识图谱
    """
    G = nx.Graph()
    # 为每个节点添加到图中
    for node in nodes:
        G.add_node(node)
    return G

def visualize_graph(G):
    """
    使用NetworkX和Matplotlib绘制图表
    """
    pos = nx.spring_layout(G)
    nx.draw(G, pos, with_labels=True, node_color='skyblue', node_size=1500, edge_color='black', linewidths=1, font_size=12)
    plt.show()

def main():
    # 配置Neo4j连接信息
    NEO4J_URI = "bolt://localhost:7687"
    NEO4J_AUTH = ("neo4j", "password")
    
    # 从Neo4j加载数据
    data = load_data_from_neo4j(NEO4J_URI, NEO4J_AUTH)
    
    # 构建知识图
    G = build_knowledge_graph(data)
    
    # 绘制图表
    visualize_graph(G)

if __name__ == "__main__":
    main()

```
---
## 联系方式
