写在前头，求star

1. 此判题器原先是内嵌在我代码里的为了开源给单独分离出来了，且，并没有搞输入的错误判断，因为我自己用，我可以确保输入到判题器的结果是正确的（手动加狗头护体）
2. 我觉得最好玩的地方就是统计每个时间片里的不同状态的车辆数量，感觉每次全局搜索统计很浪费时间，就突发奇想在更新状态的时候顺手修改状态计数器，见updateCarState的实现，虽然简单但真的实用啊，而且代码操作方便，省心省力
3. Datas文件里的CarDatas，RoadDatas，CrossDatas为存放数据的三个核心类
4. 编译及使用,在终端运行./run.sh 即可，如果想自己编译运行可参照run.sh的内容
5. 赛题信息见:https://codecraft.huawei.com/Generaldetail
6. map存放了官方给的两个测试地图，有官方给出的正确结果，因为基本有效成绩也就是系统调度时间，所以我跳过了其他次要条件（毕竟懒嘛）
7. 复赛正式比赛的时候这玩意儿竟然和官方的结果出现巨大误差，死锁都检测不出来，（痛心，判题器啊，我那么相信你，你竟然这么搞我，不知道我旁边还有妹子的嘛，搞得我尴尬的一p，幸好当初先把复赛主要任务定位成去蹭饭拿手环的，我真是个小机灵鬼），因为我复赛训练阶段根本没见过死锁误判的时候，相差最多的也就是和官方判题器的结果差1,也就是基本一个小数点的问题，中间到底发生了什么我并不想知道了,反正主任务已完成（哈哈哈），可能还是我测试次数少了（无奈的微笑）
8. 对了运行的时候记得F11全屏，并“ctrl”+“-” 多缩小几次字体，还是挺好玩的（没有可视化之尽量还是可视化吧，谁叫我懒呢）(注，之后字体调回去可是“ctrl”+“shift”+“+”哟，队友也被搞过，但你们知道为什么要加一个shift嘛，知道答案的我，哈哈哈，笑死我了)
9. Document中俩图是官方给的判题器伪码的俩文档版本，之所以有俩图是因为当初这里训练赛的时候出现了实际程序和文档不一致的地方（看谁的眼力好，能发现俩文档不同的地方，哈哈哈），经过最后和官方确定正式应该是picture1版本，因为只有这样才可以和官方给的例子匹配，结果对得上，而picture2版本的就是跑起来俩地图竟然还有死锁的，pantiqi.cpp第925行即为当初文档争论点