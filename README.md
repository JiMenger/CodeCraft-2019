1. 此判题器原先是内嵌在我代码里的为了开源给单独分离出来了，且，并没有搞输入的错误判断，因为我自己用，我可以确保输入到判题器的结果是正确的（微笑）
2. 我觉得最好玩的地方就是统计每个时间片里的不同状态的车辆数量，感觉每次全局搜索统计很浪费时间，就突发奇想在更新状态的时候顺手修改状态计数器，见updateCarState的实现，虽然简单但真的实用啊，而且代码操作方便，省心省力
3. Datas文件里的CarDatas，RoadDatas，CrossDatas为存放数据的三个核心类
4. 使用及编译 运行./run.sh 即可，如果想自己编译可参照run.sh的第一行
5. 赛题信息见:https://codecraft.huawei.com/Generaldetail
6. map存放了官方给的两个测试地图，txt里是官方给出的正确结果，因为基本有效成绩也就是系统调度时间，所以我跳过了其他次要条件，毕竟懒嘛
7. 复赛正式比赛的时候这玩意儿竟然和官方的死锁冲突，简直晴天霹雳，因为我复赛训练阶段根本没见过死锁误判的时候，相差最多的也就是和官方判题器的结果差1,也就是基本一个小数点的问题，中间到底发生了什么我并不想知道了，可能还是我测试次数少了（又一个微笑）