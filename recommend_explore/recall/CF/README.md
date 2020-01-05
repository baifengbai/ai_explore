#### UserCF和ItemCF的区别和应用
+ `UserCF`算法的特点：
    + 用户较少的场合，否则用户相似度矩阵计算代价太大；
    + 适合时效性较强，用户个性化兴趣不太明显的领域；
    + 对新用户不友好，对新物品友好，因为用户相似度矩阵不能实时计算；
    + 很难提供令用户信服的推荐解释；

+ `ItemCF`算法的特定：
    + 适合物品数量明显小于用户数的场合，否则物品相似度矩阵计算代价很大；
    + 适合长尾物品丰富，用户个性化需求强的领域；
    + 对新用户友好，对新物品不友好，因为物品相似度矩阵不需要很强的实时性；
    + 利用用户历史行为做推荐解释，比较令用户信服；

所以可以看出`UserCF`适用于物品增长很快，实时性较高的场合，比如新闻推荐。而在图书、电子商务和电影领域`ItemCF`则更合适,比如京东、天猫、优酷等这些网站，用户的兴趣是比较固定和持久的，而且这些网站的物品更新速度不会特别快，一天更新也是可以忍受的；

对于使用userCF的系统，需要解决用户冷启动问题 和如何让一个新物品被第一个用户发现
对于只用itemCF的系统，需要解决物品冷启动问题
