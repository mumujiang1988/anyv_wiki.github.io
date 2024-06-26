# 成本

## 成本模块系统操作

成本模块是高格ERP系统中用于管理企业成本核算的重要组成部分，涉及进货费用分摊、生产成本分摊等关键财务活动。


## 存货核算

1. 进货费用分摊单:对进货成本进行分摊处理，确保成本的准确性。
2. 暂估核算
3. 入库价格维护

## 工艺成本

## 生产成本

1. 生成成本分摊：对生产过程中的各项费用进行合理分摊，包括直接材料、直接人工和制造费用等。
2. 在制品初始化
3. 工单成本调整
4. 入库成本重整
  
- **操作**
  - 在生产成本分摊界面录入要分摊的各项费用。
  - 选择生产成本分摊对应的入库明细。
  - 选择适合的分摊模式，如材料金额、数量、辅助数量等。

## 3. 成本参数配置

- **路径**：`基本` -> `系统初始化` -> `成本参数设定`
  
- **操作**：
  - 设置启用成本核算，选择启用。
  - 配置成本计算方式，如标准成本、移动平均、月加权等。
  - 对于批次成本，需要在库存参数里启用批次成本，并在产品资料中勾选启用批号管理和批次成本。

## 4. 材料成本核算

- **操作**：
  
  - 核算领用的材料成本，通过成本数量重整进行成本核算。
  - 提供采购大表，核对材料采购明细。

## 6. 在制品成本处理

- **操作**：
  
  - 检查在制品成本情况，对已结案的成品产品进行排查。
  - 在工单成本调整里进行成本处理，修正成品材料金额。

## 7. 异常成本排查

- **操作**：
  
  - 使用收发存汇总表、入库成本汇总表等报表，查看异常数据。
  - 对异常数据进行调整，确保成本数据的准确性。

## 8. 成本结转

- **操作**：
  
  - 对调整后的异常数据进行处理。
  - 使用成本数量重整功能，结转成本至下一期。

## 9. 上线准备

- **操作**：
  
  - 提供工艺成本、存货核算、在制品管理、生产成本等期初数据。
  - 根据操作要求，准备标准成本级、材料级等不同层级的数据。

## 10. 库存期初处理

- **操作**：
  
  - 录入产品库存初始化数据。
  - 对中途启用模式进行成本数量重整和结转。

## 11. 在制品期初处理

- **操作**：

  - 登记开账时已领料未入库的产品。
  - 进行领料明细的登记，自动回写在制品初始化。

## 成本异常汇总

### 库存调整

存货调整单 先负数清空 然后正数加入   单独调整某列 都会导致数据异常
必须 列数据 产品代码，仓库代码，批号，结存数量，结存金额
仓库代码 勾选了特定仓库  无法更改

### 异常库存情况调整

领料单价大于库存单价  导致库存金额 负数  调整月加权

库存| 金额 |单价|处理|
---|---|---|---|
负数/0|负数|正数   | 调整相同正数量/0 正金额 调整  重算后续月份 |
正数/0|负数|负数|   调整相同负数量/0 正金额 清零  导入原来正数量 重算后续月份  |
0|0|负数  |          |

## 成本核算

直接费用  <font color="red">产品的直接成本</font>分配归集：如直接材料、直接人工可直接计入产品成本

制造费用   <font color="red">多个产品的共同成本</font>按方法分配：一般按照一定的分配标准，如生产工时、机器工时、直接人工成本等，将制造费用分配到各个产品或生产批次上

## 直接费用包含

1. 直接材料：构成产品实体的原材料、辅助材料等。
2. 直接人工：直接从事产品生产的工人的工资、福利费等。

## 制造费用包含

1.间接材料：如生产过程中消耗的各种辅料等。
2.间接人工：如车间管理人员的工资、福利费等。
3.折旧费：车间使用的固定资产的折旧费。
4.修理费：车间固定资产的修理费用。
5.水电费：车间消耗的水电费用。
6.机物料消耗：车间消耗的各种低值易耗品等。
7.劳动保护费：车间发生的劳动保护方面的费用。
8.低值易耗品摊销：车间使用的低值易耗品的摊销费用。
9.租赁费：车间租赁设备等的费用。
10.运输费：车间内部运输物品等的费用。
11.试验检验费：车间进行试验、检验等的费用。
12.停工损失：车间因停工而发生的各种损失。
13.其他制造费用：不能归入以上各类的其他制造费用。
