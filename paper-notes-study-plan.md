# Paper Notes 仓库解读 & 学习计划

## 📊 仓库概览

你当前的论文笔记覆盖 **三大领域**，共约 **46 篇论文**：

| 领域 | 论文数 | 来源 |
|------|--------|------|
| 数据库内核 (DB) | 27 | CMU 15-721 |
| 分布式系统 (Distribute) | 14 | MIT 6.824 |
| 图计算/GNN (HPC) | 5 | 自选 |

笔记质量不错：有中文转述理解、有个人疑问标注、有架构图引用。这说明你不是在搬运，是真正在读。

---

## 📁 现有论文分类梳理

### 🔹 数据库内核 — 已读 27 篇

**并发控制 (Concurrency Control)** — 你的主力方向

| 论文 | 关键词 | 读懂程度 |
|------|--------|----------|
| An Evaluation of CC with One Thousand Cores | 多核并发评测 | ✅ 有笔记 |
| An Empirical Evaluation of In-Memory MVCC | MVCC 实验对比 | ✅ 有笔记 |
| An Analysis of CC Protocols (CCBench) | 并发协议基准 | ✅ 有笔记 |
| Fast Serializable MVCC (Neumann) | 串行化 MVCC | ✅ 有笔记 |
| Serializable Snapshot Isolation in PG | PG 的 SSI | ✅ 有笔记 |
| High Performance CC for Main-Memory DBs | 内存库并发 | ✅ 有笔记 |
| TicToc: Time Traveling OCC | 乐观并发 | ✅ 有笔记 |
| ERMIA | 异构负载并发 | ✅ 有笔记 |
| Opportunities for Optimism in Contended Multicore | 乐观锁争用 | ✅ 有笔记 |

**存储引擎**

| 论文 | 关键词 | 读懂程度 |
|------|--------|----------|
| LLAMA | Cache/Storage for Modern HW | ✅ 有笔记 |
| Magma | Couchbase 存储引擎 | ⚠️ 只有 PDF，无笔记 |
| ArkDB | KV 引擎 | ✅ 有笔记 |
| Optimal Column Layout for Hybrid Workloads | 列存布局 | ✅ 有笔记 |
| Integrating Compression and Execution (C-Store) | 压缩+列存 | ✅ 有笔记 |
| Bw-Tree (CMU) + Bw-Tree (MS) | 无锁 B+Tree | ✅ 有笔记 |

**查询执行 & 优化**

| 论文 | 关键词 | 读懂程度 |
|------|--------|----------|
| Efficiently Compiling Efficient Query Plans (HyPer) | JIT 编译 | ✅ 有笔记 |
| Access Path Selection in Main Memory | 内存扫描 vs 探测 | ✅ 有笔记 |
| Morsel-Driven Parallelism | NUMA 并行 | ✅ 有笔记 |
| Adaptive Radix Trees vs Hash Tables | ART 索引 | ✅ 有笔记 |

**恢复 & 事务**

| 论文 | 关键词 | 读懂程度 |
|------|--------|----------|
| ARIES | 经典恢复算法 | ✅ 有笔记 |
| ARIES:IM | 内存恢复 | ✅ 有笔记 |
| Constant Time Recovery in Azure SQL | 快速恢复 | ✅ 有笔记 |
| A Critique of Snapshot Isolation | SI 批判 | ⚠️ 只有 PDF，无笔记 |

**系统 & 综述**

| 论文 | 关键词 | 读懂程度 |
|------|--------|----------|
| Architecture of a Database System | 数据库架构综述 | ✅ 有笔记（含中文版） |
| HTAP Tutorial | HTAP 数据库 | ✅ 有笔记 |
| What Goes Around (Stonebraker) | 数据模型综述 | ⚠️ 只有 PDF，无笔记 |
| CockroachDB | 分布式 SQL | ✅ 有笔记 |
| Amazon Aurora | 云原生数据库 | ⚠️ 只有 PDF，无笔记 |
| Don't Hold My Data Hostage | 客户端协议 | ✅ 有笔记 |
| High-Performance Transactions in Deuteronomy | 事务架构 | ⚠️ 只有 PDF，无笔记 |
| Scalable GC for In-Memory MVCC | MVCC 垃圾回收 | ✅ 有笔记 |

---

### 🔹 分布式系统 — 已读 14 篇

| 论文 | 所在课程 | 读懂程度 |
|------|----------|----------|
| Time, Clocks and Ordering of Events (Lamport) | MIT 6.824 | ✅ 有笔记 |
| MapReduce | MIT 6.824 | ✅ 有笔记 |
| GFS | MIT 6.824 | ✅ 有笔记 |
| Raft | MIT 6.824 | ✅ 有笔记 |
| Bigtable | MIT 6.824 | ✅ 有笔记 |
| Chubby | MIT 6.824 | ✅ 有笔记 |
| Percolator | MIT 6.824 | ✅ 有笔记 |
| More-Raft | 进阶 | ✅ 有笔记 |
| More-GFS | 进阶 | ✅ 有笔记 |
| GentleRain (Causal Consistency) | 自选 | ✅ 有笔记 |
| Session Guarantees for Weakly Consistent Data | 自选 | ✅ 有笔记 |

---

### 🔹 图计算 / GNN 训练系统 — 已读 5 篇

| 论文 | 关键词 | 读懂程度 |
|------|--------|----------|
| Pregel | 图计算框架 | ✅ 有笔记 |
| Gemini | 分布式图处理 | ✅ 有笔记 |
| NeuGraph | GNN on GPU | ✅ 有笔记 |
| NTS | 神经训练系统 | ✅ 有笔记 |
| MLSys ROC | GNN 训练系统 | ✅ 有笔记 |

---

## ⚠️ 存在的问题

根据笔记内容判断，有几个明显的缺陷需要补：

1. **部分论文只有 PDF，没有写笔记**：
   - Magma、A Critique of Snapshot Isolation、What Goes Around、Aurora、Deuteronomy、bw-tree-ms — 这几篇要么读了一半要么存了没读
   
2. **笔记质量不均衡**：ARIES 那篇笔记较完整，但有些只有摘要式的几个要点

3. **分布式方向缺关键论文**：MIT 6.824 后半程的 FaRM、Spanner、Argos、Pegasus 等现代系统都还没读

4. **HPC 方向太浅**：只有 5 篇，更像试水

5. **缺乏输出**：笔记在本地，没有形成博客、分享或总结性输出

---

## 🗓️ 三周学习计划

### Week 1 · 扫尾 + 深挖并发控制

| 天 | 任务 | 
|----|------|
| **Day 1** | 补笔记：A Critique of Snapshot Isolation（SI 的缺陷，理解什么情况下 SI 会异常） |
| **Day 2** | 补笔记：What Goes Around（Stonebraker 综述，理解数据模型的演进） |
| **Day 3** | 重读 + 深挖：Fast Serializable MVCC + Serializable Snapshot Isolation in PG，串起来理解 —— 从理论到 PG 的实现 |
| **Day 4** | 串读并发控制链：One Thousand Cores → CCBench → ERMIA → TicToc，画一张并发控制家族图谱（2PL / OCC / MVCC / 混合） |
| **Day 5** | 补笔记：Magma + High-Performance Transactions in Deuteronomy |
| **Day 6** | 重读：Architecture of a Database System，对照你已有的知识点看哪些还没覆盖 |
| **Day 7** | 本周输出：写一篇博客/总结：「现代数据库并发控制的演进」1500 字 |

---

### Week 2 · 云原生 & 存储 + 分布式进阶

| 天 | 任务 |
|----|------|
| **Day 1** | 补笔记 + 深读：Amazon Aurora（云原生数据库的存储计算分离是里程碑） |
| **Day 2** | 串读存储链：LLAMA → C-Store（压缩执行）→ Optimal Column Layout → ArkDB，理解存储引擎的设计取舍 |
| **Day 3** | 新论文：Spanner (Google's Globally-Distributed Database) —— 分布式 DB 的巅峰之作，TrueTime API 是神设计 |
| **Day 4** | 串读分布链：Lamport Clock → Raft → Bigtable → Percolator → CockroachDB，画一条从理论到工程的线 |
| **Day 5** | 新论文：FaRM (Fast Remote Memory) —— RDMA + 分布式事务 |
| **Day 6** | 新论文：Dynamo (Amazon) 或 Cassandra —— 对比你已有的强一致性论文，理解最终一致性 |
| **Day 7** | 本周输出：写一篇：「从单机到分布式——数据库的扩展之路」 |

---

### Week 3 · 高级专题 + 体系化整理

| 天 | 任务 |
|----|------|
| **Day 1** | 重读 Bw-Tree (CMU + MS 两篇对照) + ARIES:IM，理解无锁数据结构和内存恢复 |
| **Day 2** | 重读 Query Compilation (HyPer) + Access Path Selection，理解 JIT 编译查询 |
| **Day 3** | 新论文：Spark SQL 或 Flink —— 从 OLTP 走向大数据/流处理 |
| **Day 4** | 读一篇你感兴趣但还没碰的方向：比如 Learned Index (SageDB)、Paxos 变体、或者 Calcite（查询优化器框架） |
| **Day 5** | 整理所有笔记：统一格式，补齐遗漏，把图床检查一遍 |
| **Day 6** | 建立知识图谱：画思维导图，把 46 篇论文之间的关系连起来 |
| **Day 7** | 最终输出：仓库 README 加入完整的学习路线图 + 分类索引，考虑建一个 GitHub Pages 展示 |

---

## 📚 补缺推荐（高优先级待读论文）

| 论文 | 理由 | 优先级 |
|------|------|--------|
| **Spanner (Google, 2012)** | TrueTime、全球分布式事务，分布式 DB 必读 | 🔴 必读 |
| **Dynamo (Amazon, 2007)** | 最终一致性、一致性哈希、面向可用性的设计哲学 | 🔴 必读 |
| **Bigtable** (已读) → **Megastore** → **Spanner** | Google 存储栈三部曲 | 🟡 建议 |
| **Calcite (Apache)** | 工业级查询优化器框架 | 🟡 建议 |
| **FoundationDB** | 确定性模拟测试，事务系统的另一种思路 | 🟡 建议 |
| **SageDB / Learned Index** | ML + 数据库，了解前沿方向 | 🟢 可选 |
| **Paxos Made Simple** | 共识算法基础，Raft 读完应该回头看 | 🟢 可选 |
| **ZooKeeper (2010)** | 分布式协调服务，Chubby 读完的工业对照 | 🟢 可选 |

---

## 🎯 总体建议

1. **笔记模板化**：建议每篇笔记统一结构——背景/动机 → 核心设计 → 实验结论 → 个人思考/疑问。现在的笔记偏散
2. **串读 > 单读**：你已经有了很好的基础，现在应该把论文连线，理解整个领域的演进逻辑
3. **输出倒逼输入**：每周一篇总结博客，哪怕是博客园/GitHub Issues 都行
4. **动手验证**：部分想法可以写代码验证（比如自己实现一个 MVCC 小 demo），会比纯读论文理解深很多
5. **参与社区**：TiDB/CockroachDB/Greenplum 社区都很活跃，可以看看他们的 RFC/设计文档，对照论文理解工程实践

---

*注：本计划基于你仓库当前 46 篇论文设计，每周建议投入 12-15 小时。*
