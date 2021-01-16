# Genshin Impact Wish History Utility
原神祈愿（抽卡）历史记录导出工具

## 效果图

![效果](https://github.com/Masterain98/GenshinImpactWishHistoryUtility/blob/main/example/screenshot.png?raw=true) 

Bilibili演示视频：[AV713675798](https://www.bilibili.com/video/bv14X4y1K7zu)

## 为什么有这个小工具

1. 非洲人需要算保底，需要比较完整且查询方便的抽卡历史记录 (main reason)
2. 离谱的一页只有6条记录的设计。也许手机端会有不错的体验，但在PC端，给你这么大一个屏幕你却只给这么点信息是在是愚蠢的设计。
3. 基于第一点的情况下，米哈游还不做一个网页版的查询页面
4. 原神国服API的海外节点只有香港，在远离亚洲的地方很容易长时间不出结果（但为什么更新检查API就有美国服务器？）
5. 适合不会抓包用API的用户，通过API可以直接从原神服务器获取到抽卡历史记录，对于有网络知识的人而言会更简单

## 如何使用 

1. 打开原神，进入祈愿中的历史记录页面
2. 手动复制表格中的内容到程序根目录下的对应TXT文件中，一行一条信息（出货类型/出货名称/时间），三行为一次抽卡记录
   - ```Novice.txt``` 为新手祈愿
   - ```Permanent.txt``` 为常驻祈愿
   - ```CharacterEvent.txt``` 为角色活动UP祈愿
   - ```WeaponEvent.txt``` 为武器活动UP祈愿
3. 打开主程序，按照提示输入需要导出的数据（序号即可，以空格作为间隔）
4. 导出完成后，导出数据位于程序根目录下的```GenshinInpactWishHistory.xlsx``` 文件中

## 拓展性 

1. 程序基于Python，使用的库主要是```openpyxl```  和 ```pandas```  ，本质是一个简单的脚本
2. 数据从TXT读取后导入Excel使用的是pandas DataFrame，所以实际上导出成sql之类的数据库文件都是可以的
3. 这个方案我认为是在不直接请求原神API情况下可适用性最强的，除非PM看到这个玩意后把网页给改了。最早时是想拿截图OA的，这种小规模的中文OA价格挺便宜的而且使用时可以偷懒很多，但想到海外API那延迟就算了
4. 开源基于GPL协议

## 语言

|          | CMDUI语言 | 数据导出 | 高亮出货数据 |
| -------- | --------- | -------- | ------------ |
| 简体中文 | ✅         | ✅        | ✅            |
| 繁體中文 | ❌         | ✅        | ❗（未测试）  |
| English  | ❌         | ✅        | ❌            |
| 日本語   | ❌         | ✅        | ❌            |

