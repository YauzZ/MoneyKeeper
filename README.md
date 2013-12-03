MoneyKeeper
===========

守财奴记账软件维护网页

## 功能需求

1. 每日记账流水. ✓
2. 账户统计功能. ✓
3. 多科目统计. ✓
4. 支持多币种.(暂缓)
5. 指定币种统计功能.(暂缓)
6. 多种图表显示.
7. 跨账户跨币种转账支持.(暂缓)
8. 支持数据备份与恢复.
9. 支持多借多贷的会计分录生成. ✓

## 业务逻辑详细设计

1. CoreData本地数据建模,采用复式记账法,支持复杂会计分录编制.
1.1	流水表(日期,金额(借,贷),币种,科目ID,描诉,分录ID)
1.2	科目表(科目ID,科目名,描述,期初余额,期初日期)

2. 科目表管理类业务逻辑
-2.1 初始化原始科目表.-
-2.2 查增改科目记录.(科目记录只增不删)-
-2.3 返回(所有,资产,负债,收入,支出,投资损益类)科目纪录.-
2.1 三级科目体系
2.1.1 五种一级科目(资产,负债,收入,支出,损益),不可变更修改.
2.1.2 在五种一级科目下,有若干二级科目,可以查删增改.
3.1.3 三级科目在二级科目之下.


3. 流水表管理类业务逻辑
3.1 查增删改一笔(收入,支出,资产间划转,投资损益).
3.1.1 通过分录ID查询到相关的所有记录,然后进行修改和删除工作.
3.1.2 返回指定时间范围内的所有分录.
3.2 返回指定日期内的科目相关所有记录.
3.3 返回科目指定日期内的余额.

## 用户交互设计
1. 基本简单交互.

## 图表展示
1. 支持趋势图,二维线图.
2. 支持分科目饼图.
3. 支持表格.


