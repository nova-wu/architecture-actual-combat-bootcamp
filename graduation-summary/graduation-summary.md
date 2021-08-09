# 毕业总结

## 面向复杂度的架构设计方法论理解

### 什么是架构？（4R）

- 软件架构指系统的顶层结构，它定义了系统由哪些角色组成，角色之间的关系和运作规则。可以用4R的方式来理解。
- Rank 顶层结构
- Role 组成角色
- Relation 角色之间的关系
- Rule 运作规则

### 为什么要做架构设计？（降低复杂度）

- 软件系统规模增长，数据结构和算法不再是主要问题，整个系统的结构成为首要问题，需要通过架构设计来降低整个系统的复杂度

### 什么是面向复杂度的架构设计？（本质、思路、模式、套路）

- 本质：架构设计是为了降低软件系统的复杂度
- 思路(怎么做架构设计)：通过分析系统需求找到系统复杂的地方，然后设计方案
- 模式(有哪些复杂度)：复杂度来源：高性能、高可用、可扩展、安全、成本...
- 套路(怎么降低复杂度)：分库分表、缓存、集群、分片、微服务、DDD、异地多活...

### 如何开展面向复杂度的架构设计？（架构设计四阶段）

- ![](https://remnote-user-data.s3.amazonaws.com/9VBuren14m3mOwlHuUML11fb2L4pR51WK-sbCbH8q8xUi-zYECrrlY0mDa-KsWBZzUmAXA1RkvZI7Jinu8qcirN1lTKRI0me6N_sVNwuaBU0T4gcdxxJp6UKPzqgc0x5.png)
- ![](https://remnote-user-data.s3.amazonaws.com/hqsUp7ygqr7G0oJQLyO1NXeRR5LrqcmrT-ZBtS5-vTgu1fOG1-BvOfiNXePVwVFa63id7PLxGn7govZucJU7RJirTCpZkhALfYoTIAsYN3ZxXdUnF0pqbe7mw-b_LaUU.png)

#### 架构设计前期

- 主要任务
  - 澄清不确定性
    - 明确利益干系人的诉求
    - 消除冲突的诉求
    - 诉求优先级排序
  - 识别复杂度
    - 识别核心场景
    - 明确或者预估质量需求
    - 识别复杂度（见下文 复杂度有哪些？各种复杂度的应对思路是什么？）

- 工作模式
  - 与业务方交流
  - 与利益干系人交流

- 关键输出
  - 总体业务架构图
  - 核心场景流程

#### 架构设计中期

- 主要任务
  - 设计备选方案
    - 头脑风暴
    - 筛选方案
    - 设计备选方案（见下文 架构设计模式）
  - 选择备选方案
    - 360度评估
    - 明确选择标准
    - 选择最终方案，并汇报

- 工作模式
  - 架构小组讨论
  - 架构小组写文档
  - 向利益干系人汇报

- 关键输出
  - 备选方案
  - 方案评估结论
  - 方案汇报结论

#### 架构设计后期

- 主要任务
  - 细化架构
    - 按照4R架构定义来细化架构
  - 完善架构
    - 可维护性、可测试性、可观测性、成本、安全

- 工作模式
  - 写架构设计文档（见 [架构实战营详细架构设计文档模板](https://xie.infoq.cn/article/a1c01e8f55c81b36a787f9f5b)）
  - 给技术团队宣讲架构

- 关键输出
  - 完整的架构设计方案

#### 架构设计验证阶段（贯穿项目全流程）

- 主要任务
  - 收集架构意见
    - 开发人员意见
    - 测试人员意见
    - 运维人员意见
  - 跟进架构落地效果
    - 性能测试结果
    - 压力测试结构
    - 线上运维情况

- 工作模式
  - 总结复盘
  - 收集吐槽

- 关键输出
  - 架构优化建议
  - 架构迭代计划

### 如何判断架构设计的好坏？（三原则）

- 合适原则：合适优于业界领先（制约：资源、时间、业务变化）
- 简单原则：简单优于复杂（越复杂越不可靠、越难扩展、越难处理故障）
- 演化原则：演化优于一步到位（满足当前业务，与业务一起发展）

### 复杂度有哪些？各种复杂度的应对思路是什么？

- 架构设计复杂度模型
  - ![](https://remnote-user-data.s3.amazonaws.com/zz0mhubcc2znfaqlvdt7glahhd_phra7jowhybyjllyxdgxntnpu8njkoijjismnkairnoiyonsphvpi-p1kpfvo-03esiiqds6tj_yo2cmsfkylkbcj1y1ccezobuj6.png)
- 架构设计复杂度应对之道
  - ![](https://remnote-user-data.s3.amazonaws.com/iy1wk-drdsczhq2y_8-fl1axdk6lvzq41qz9soq5wifrz6i433ysobdhhng1u7hnw5vtto_oeognis40bugj7i9w72s9gnjuuvh7izcf-ireu7gv36fim-etehpm5gtg.png)
- 可扩展复杂度模型
  - 可扩展性：extensibility，指系统适应变化的能力，包含可理解和可复用两个部分
  - ![](https://remnote-user-data.s3.amazonaws.com/ddt3n_j69oain0gc3guvra-odyo_pu9mjyt-digw6h4kjkza6ti1quwi0one-dpvgsm_6jhooghlolcsnf8aju6xisoqyjzfbjnffj2s0arxfpq1lnvqaxjoxrwpiugl.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/mvnp_zdni4mku71c1ciqqkmtxr_ggmltzzsjgomaipyax2eevqpeb6v-iocjauommqduq3evuvp8fdjshomwxsn03hhu4ybcq8o_eeg5s3z3iwclp6-a2ykqdz0k9_sv.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/jnex_08erlp8ae48jnvu7h73_kymfgx_umf_4zhsua9j6qqzb3lo1ukzqfwqvhzajxsgdann7wlue0zcx053pbzhju1v7owcbxekus3y5vpgbzccat0mjqqndvvr1wno.png)
  - 封装的技巧：规则引擎、微内核、抽象层、设计模式
- 高性能复杂度模型
  - ![](https://remnote-user-data.s3.amazonaws.com/xjb2w98ysgx9-5krs3coucxmpkad5svhbziowsmhnxp0oajvcgq-kwpjrsfkxuv7oru1fxzaovekpkoqvpyjs3rnz2mvxxau7d7nt9mnoxkvvwc08mkhdtw_wkmevq0u.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/ue-t09ahsreqaansfojjkwqobeulzxsw9b7ttmaixyoceu1vhygeh099kk28vtxcvp1917fhu20uoe1goirad5nuhzeg5_ub7vzk7sjo8kulc9j_znymvf9io-xjcy0p.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/p9h4qng-nb8-hmzhlqnlnouzcwqjw6dvny16o0dx4zkvzbntm699epylbqspwve0pikzovjp1jzitnwuk9mbyd7ylhrg0h0pck5d_nfxvfmhqlsd4vpimi5bhvtmvi5v.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/qfbfiiwf9jz8hceklf-r0nwkwl7zzx1fj16tqc3hhf1-exy8hp70bmvthiluywbiqbf2oh7ewxmhm5xng1ejrihqim-p1wd6po3s7mebf7ymjfl7bhtfn7ivlrvnjbhh.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/nwhgebplsqzili5gjfgstu7gnwok1nfwnk37kt_dpmvwlyhyslyyjbghzhm394lqz7ospo5ekiac28prrmj-n9ot3l7klnxizwj0pr6hvwq0pjvgd0sprrfa4hccp6v0.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/pe8f0nxlr9a4-vouka2tb5qcgxs2mngmgn_nxlxztvqvwk9okgcnmznqs2qa1yomsudokut5tlte4ttmumbdepuscf9jr_63tb6yoteo8lt6c80fnnhr4s_yrgnhg2nk.png)
- 高可用复杂度模型
  - ![](https://remnote-user-data.s3.amazonaws.com/w0rirqwcxircivbn1i2o5fzzcjf5blxnft4g_xcxf5jgdbplruskyoj-xce9a4vu9cujubwaervfu1hhdhwzjma5bvll-ojpmqqqjch9yljnmpw9k_ohlkgrz6sa18bq.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/cqj70tksnz0cgyw756im4ytdxpbajpyd85y7ovzwqjv4ny1po4jls5iicj7mc1g79fgcjub-1wjkbg3tqizyir4i_x-rwxfwm60a9hyclb7sacps1qfy36n3xlyvogdo.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/zrsb-wptqdgqjeeisu8lkdk31ginncyqbdghrkdexvomc_4hpm-rvazcqr3w8wjb80cztazb98jmpjcjgx5ks1rum7kd2nzsh2lglvljtlsxgena-yrqwmgbw42r0ec3.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/f_nzmc1if4pkt_ago1klmf62qcer_hozgnsuydusotavh6swdeddatoygfansmslyhhmwytregtgrw3pi7z1janeiawylym-xu2puxx5cplfsfs2_e_qb8v2gmtqbdqd.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/qfd20f6jjtjem-yxrxu2xjphrkcwserdasgqhtw_fvssvuv6qzbd_hqxhtc59fltpkzrkoecuxm6nm_ra2hyap1zodnpwblwmonrhrdih39kjl0pnqcqp0d93vws84al.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/1r06gg3m9forok0rj5kjvenmmkj9c8xadiyrr-ojlqrbnarfflc9-3ppifsjfgldguuabzxn_7h7q7qcxzlqagq8a1p0zfizx-cbuftqvpmw5nepkd-dyv3h_gryjpjv.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/ilmc5lvipw8nrhjgmdfy_lx1byvtwdkvdsfpr4yae-qkuo2as_mrogejbknivbwi3djjhx1wmym8jvzi-syjnpfroukbc-68lhwq6xymc-ouitdjv20r5fzzw9al6k2t.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/tilyjtn_ozeo7s4eyliw3bowasbucjoyidh8xp19lbiws0sri546z-b3u1kvckaqwqhuvarbgs5rzijq6sdx6fkqsoroabrcelw7rurnuuehrh9b_nil_6o2hlhuthao.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/axavemi7yr1iv5etnzq9tcf5s_gwgkmfm-4x5zu7wamordvnsajciwoxlihggnwak-fqcgiksz6ukiujcby-xts7oq8xtle0wctfsupcci8f1kmash5gcnfe6m9n_y8g.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/lhlajh28sw2n7wfq-xdej5mf5fl4zxuflcywf-_xffsheawpjc5pt7vunixsqjqskq8srse1ylypbzdpgbkrflq4rlb16kw8jd6mndcq895b3ptnzfmq1ht05x3ex7vh.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/if0jkeu9kkkvwu2gxt98jvdfuq7w8qiel9pl1mmx86wj_uaxci8ka4o3dcilwa9yn3yxicnujhcvoasz_mc3vgf--wl2r50_h5_neds9ms76rakfo2fytdbxtl4qqt5j.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/luvhreavcojfocon_umoxouh0dzuy7chqcihghoye8crfjmap6rsiuxfcla5wito0y-ghiefzkqw9pi1awr21yniovbnpy2fx_znoaqzjza-fxzfyq8tstjczhjiuqcj.png)
- 低成本复杂度本质
  - ![](https://remnote-user-data.s3.amazonaws.com/dz7_wl8l_zblw26pe4h84jwinorehtjfmm50autkxyt22kgpe9gosbjdlxkfqzfm-8ju7bfbbtiat2nhwnrib5zblvgcgxdxklfj6bgde_uqqpxyeogiskyhtxiy-p5k.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/ieogky3rzwuoqgidpdfz2fvyp7jp3yvoh0fb7me9lycv1l7d5oi26nrvmqurqj5czwrhkaiw599adxa4wrm4hx_dgxgtl5kx9dfdjia4ldyw0mcf-qde_ozyu3mtkmd5.png)
- 安全性复杂度本质
  - ![](https://remnote-user-data.s3.amazonaws.com/nxmdmsi_t2-pxfmc8wy582hgdzmmcpj09ldyhc_rad_bpnmp3v-0lzmvlwnxdxb1rvy5tvrewkx_gmx1l_xmewgmozqeo6twowdbr5nird8fl_xcqkhb6ydhja7btraz.png)
  - ![](https://remnote-user-data.s3.amazonaws.com/ehkf5pydqn-3wia1yrc6ct23jretxr_zfm2r1mayrdol-hkebnzom1uvxg5y8ftsej391xgbzad7kjksopfpbesdp8ourzbite-lsblji0qnmaymxehig81iv3hzgkxp.png)
- 可测试性复杂度本质
  - 可测试性：软件系统在测试环境下能否方便的支持测试各种场景的能力
  - ![](https://remnote-user-data.s3.amazonaws.com/n7zr0ed1djoqps4tj7izu5vwxdxxehlqs7-75lnuhvnkzs5yjubiegvt84mobmhzur8v9upt8fxdp6bpksqtel5s17jpaximqsjf7hfzy0a9jgcmnchxua2fk_lxmulv.png)
- 可维护性复杂度本质
  - 可维护性：软件系统支持定位问题、修复问题的能力
  - ![](https://remnote-user-data.s3.amazonaws.com/ik-ymaj5ez0leujzzbohc7kji5m1k_f8aqjjl9gmucrbsqjg65z2rlxzsqjtlya2vszgcerkurp6hzwmymh0o99-aihz2o_89ydww_w-qz_b-1odgessihi1o9uwcuzb.png)
- 可观测性复杂度本质
  - 可观测性：软件系统对外展现内部状态的能力
  - 可观测性是可测试性、可维护性的基础
  - ![](https://remnote-user-data.s3.amazonaws.com/ni_lp0-7rkxa1dtndt6jepwirjd_kuwt9qfuypqm8lt2befrdzrsycpcg3rsuddkp9xsszier62p3zz-j8qmjqagjfydowujjnrnq2epd6u2o2t5okvctry5f6bhjxkr.png)

### 架构设计有哪些常用的模式？（三高一扩展的应对套路）

- 高并发架构模式
  - 异步
  - 缓存

- 高性能架构模式
  - 存储高性能
    - 读写分离
    - 分库分表
    - NoSQL
    - 缓存
  - 计算高性能
    - 单机高性能
      - PPC/preforked
      - TPC/prethreaded
      - Reactor
      - Proactor
    - 集群高性能
      - 负载均衡

- 高可用架构模式
  - 高可用理论支持
    - CAP理论
    - FMEA方法，排除架构可用性隐患的利器
  - 存储高可用
    - 双机
      - 主备复制/主从复制/主主复制
      - 主备切换/主从切换
    - 集群
      - 数据复制集群（例如Redis sentinel集群）
      - 数据分片集群（例如Redis cluster）
    - 数据分区
  - 计算高可用
    - 主备/主从
    - 对称集群（负载均衡集群）
    - 非对称集群（例如ZooKeeper集群）
  - 业务高可用
    - 接口级别高可用
      - 降级
      - 熔断
      - 限流
      - 排队
    - 地理级别高可用
      - 同城多机房
      - 跨城多机房
      - 跨国数据中心

- 可扩展架构模式
  - 分层
  - SOA
  - 微服务
  - 微内核

## 课程收获

- 华仔善于总结，是个宝藏老师，自己多年工作经验，有想法，但不成体系，华仔梳理出了体系
- 高手视野，存储、计算、三高一扩展
- 很实战，拿来即用 设计文档 存储架构设计
- 方法论的方法论 如何学存储系统
- 全面 架构设计的方方面面



