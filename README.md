# Altium Designer
## 1.General参数设置

1.设置按钮（Preferences）-system-General-Startup里，取消勾选Reopen last workspace可以提高打开软件和加载文件的速度

2.PCB鼠标悬停高亮：Perference-PCB Editor-Board Insight Display-Live Highlighting-取消enable下面的那个复选框

![image](https://github.com/Code-30/EDA-Learning-Notes/blob/main/Images/PCB%E9%BC%A0%E6%A0%87%E6%82%AC%E5%81%9C%E9%AB%98%E4%BA%AE.jpg)

## 2.工程的创建及管理

### 2.1完整工程文件的组成

1.工程文件，后缀名为.PrjPCB。

2.原理图文件，后缀名为.SchDoc。

3.原理图库文件，后缀名为.SCHLIB。

4.PCB文件，后缀名为.PcbDoc。

5.PCB元件库文件，后缀名为.PcbLib。

提示：ad软件采用工程文件管理所有的设计文件，因此设计文件应当都保存在工程文件中，单独的设计文件则称为“Free Documents”。

### 2.2快速查询文件保存路径

在工程目录上右击，执行Explore命令。

## 3.元件库的创建和加载

### 3.1元件的命名规范及归类
1.原理图库分类及命名
<table>
	<tr>
	    <th>元件库</th>
	    <th>元件种类</th>
	    <th>简称</th>
        <th>元件名（Lib Ref）</th>
	</tr>
	<tr>
	    <td rowspan="11">RCL.LIB（电阻、电容、电感库）</td>
	    <td>普通电阻类，包括SMD、碳膜、金膜、氧化膜、绕线、水泥、玻璃釉等</td>
	    <td>R</td>
        <td>R</td>
	</tr>
	<tr>
	    <td>康铜丝类，包括各种规格康铜丝电阻</td>
	    <td>RK</td>
        <td>RK</td>
	</tr>
	<tr>
	    <td>排阻</td>
	    <td>RA</td>
        <td>RA + 电阻数-PIN距</td>
	</tr>
	<tr>
	    <td>热敏电阻类，包括各种规格热敏电阻</td>
	    <td>RT</td>
        <td>RT</td>
	</tr>
	<tr>
	    <td>压敏电阻类，包括各种规格压敏电阻</td>
	    <td>RZ</td>
	    <td>RZ</td>
	</tr>
    <tr>
	    <td>光敏电阻类，包括各种规格光敏电阻</td>
	    <td>RL</td>
	    <td>RL</td>
	</tr>
    <tr>
	    <td>可调电阻类，包括各种规格单路可调电阻</td>
	    <td>VR</td>
	    <td>VR-型号</td>
	</tr>
    <tr>
	    <td>无极性电容类，包括各种规格无极性电容</td>
	    <td>C</td>
	    <td>CAP</td>
	</tr>
    <tr>
	    <td>有极性电容类，包括各种规格有极性电容</td>
	    <td>C</td>
	    <td>CAE</td>
	</tr>
    <tr>
	    <td>电感类</td>
	    <td>L</td>
	    <td>L+电感数-型号</td>
	</tr>
    <tr>
	    <td>变压器类</td>
	    <td>T</td>
	    <td>T-型号</td>
	</tr>
    <tr>
	    <td rowspan="10">DQ.LIB（二极管、晶体管库）</td>
	    <td>普通二极管类</td>
	    <td>D</td>
        <td>D</td>
	</tr>
    <tr>
	    <td>稳压二极管类</td>
	    <td>DW</td>
        <td>DW</td>
	</tr>
    <tr>
	    <td>双向触发二极管类</td>
	    <td>D</td>
        <td>D-型号</td>
	</tr>
     <tr>
	    <td>双二极管类，包括BAV99</td>
	    <td>Q</td>
        <td>D2</td>
	</tr>
     <tr>
	    <td>桥式整流器类</td>
	    <td>BG</td>
        <td>BG</td>
	</tr>
     <tr>
	    <td>三极管类</td>
	    <td>Q</td>
        <td>Q-类型</td>
	</tr>
    <tr>
	    <td>MOS管类</td>
	    <td>Q</td>
        <td>Q-类型</td>
	</tr>
    <tr>
	    <td>IGBT类</td>
	    <td>Q</td>
        <td>IGBT</td>
	</tr>
    <tr>
	    <td>单向可控硅（晶闸管）类</td>
	    <td>SCR</td>
        <td>SCR-型号</td>
	</tr>
    <tr>
	    <td>双向可控硅（晶闸管）类</td>
	    <td>BCR</td>
        <td>BCR-型号</td>
	</tr>
    <tr>
	    <td rowspan="3">IC.LIB（集成电路库）</td>
	    <td>三端稳压IC类，包括78系列三端稳压IC</td>
        <td>U</td>
        <td>U-型号</td>
	</tr>
    <tr>
	    <td>光电耦合器类</td>
        <td>U</td>
        <td>U-型号</td>
	</tr>
    <tr>
	    <td>IC</td>
        <td>U</td>
        <td>U-型号</td>
	</tr>
     <tr>
	    <td rowspan="3">CON.LIB（接插件库）</td>
	    <td>端子排座，包括导电插片、四脚端子等</td>
        <td>CON</td>
        <td>CON+PIN数</td>
	</tr>
    <tr>
	    <td>排线</td>
        <td>CN</td>
        <td>CN+PIN数</td>
	</tr>
    <tr>
	    <td>其他连接器</td>
        <td>CON</td>
        <td>CON-型号</td>
	</tr>
    <tr>
	    <td rowspan="6">DISPLAY.LIB（光电元件库）</td>
	    <td>发光二极管</td>
        <td>LED</td>
        <td>LED</td>
	</tr>
    <tr>
	    <td>双发光二极管</td>
        <td>LED</td>
        <td>LED2</td>
	</tr>
    <tr>
	    <td>数码管</td>
        <td>LED</td>
        <td>LED+位数-型号</td>
	</tr>
    <tr>
	    <td>数码屏</td>
        <td>LED</td>
        <td>LED-型号</td>
	</tr>
    <tr>
	    <td>背光板</td>
        <td>BL</td>
        <td>BL-型号</td>
	</tr>
    <tr>
	    <td>LCD</td>
        <td>LCD</td>
        <td>LCD-型号</td>
	</tr>
    <tr>
	    <td rowspan="8">OTHER.LIB（其他元器件库）</td>
	    <td>按键开关</td>
        <td>SW</td>
        <td>SW-型号</td>
	</tr>
     <tr>
	    <td>触摸按键</td>
        <td>MO</td>
        <td>MO</td>
	</tr>
    <tr>
	    <td>晶振</td>
        <td>Y</td>
        <td>Y-型号</td>
	</tr>
     <tr>
	    <td>保险管</td>
        <td>F</td>
        <td>FUSE</td>
	</tr>
     <tr>
	    <td>蜂鸣器</td>
        <td>BZ</td>
        <td>BUZ</td>
	</tr>
     <tr>
	    <td>继电器</td>
        <td>K</td>
        <td>K</td>
	</tr>
     <tr>
	    <td>电池</td>
        <td>BAT</td>
        <td>BAT</td>
	</tr>
     <tr>
	    <td>模块</td>
        <td>—</td>
        <td>—</td>
	</tr>
</table>
2.原理图中元件值标注规则
<table>
	<tr>
	    <th>元件</th>
	    <th colspan="2">标注规则</th>
	</tr>
    <tr>
	    <td rowspan="7">电阻</td>
	    <td>≤1Ω</td>
        <td>以小数表示，而不以毫欧表示，可表示为0RXX，例如：0R47（0.47Ω）、0R033（0.33Ω）</td>
	</tr>
    <tr>
	    <td>≤999Ω</td>
	    <td>整数表示为XXR，例如：100R（100Ω）、470R</td>
	</tr>
     <tr>
	    <td>≤999kΩ</td>
	    <td>整数表示为XXK，例如：100K（100kΩ）、470k</td>
	</tr>
    <tr>
	    <td>≤999kΩ（包含小数）</td>
	    <td>整数表示为XKX，例如：4K7（4.7kΩ）、4k99、49k9</td>
	</tr>
    <tr>
	    <td>≥1MΩ</td>
	    <td>整数表示为XXM，例如：1M（1MΩ）、10M</td>
	</tr>
    <tr>
	    <td>≥1MΩ（包含小鼠）</td>
	    <td>整数表示为XMX，例如：4M7（4.7MΩ）、2M2</td>
	</tr>
    <tr>
	    <td colspan="2">电阻如只标数值，则代表其功率低于1/4W；如果其功率大于1/4W，则需要标明实际功率。默认定义为“精度 5±5%”。为区别电阻种类，可在其后标明种类：CF（碳膜）、MF（金属膜）、PF（氧化膜）、FS（熔断）、CE（瓷壳）。</td>
	</tr>
    <tr>
	    <td rowspan="8">电容</td>
	    <td>≤1pF</td>
        <td>以小数加p表示，例如：0p47（0.47pF）</td>
	</tr>
    <tr>
	    <td>≤100pF</td>
        <td>整数表示为XXp，例如：100p（100pF）</td>
	</tr>
    <tr>
	    <td>≥100pF</td>
        <td>采用指数表示，例如：10³pF（1000pF）</td>
	</tr>
    <tr>
	    <td>≤999pF（包含小数）</td>
        <td>表示为XpX，例如：4p7（0.47pF）、6p8</td>
	</tr>
    <tr>
	    <td>接近1μF</td>
        <td>可用0.XXμ表示，例如：0.1μ、0.22μ</td>
	</tr>
    <tr>
	    <td>≥1μF</td>
        <td>整数表示为XXμF/耐压值，例如：100μF/25V、470μF/16V</td>
	</tr>
    <tr>
	    <td>≥1μF（包含小数）</td>
        <td>表示为X.X/耐压值，例如：2.2μF/400V</td>
	</tr>
    <tr>
	    <td colspan="2">电容值后标明耐压值，以“/”与电容值隔开。电解电容必须标明耐压值，其他介质电容如不标明耐压值，则默认定义耐压值为50V。</td>
	</tr>
    <tr>
	    <td>电感</td>
        <td colspan="2">同电容标法</td>
	</tr>
    <tr>
	    <td>变压器</td>
        <td colspan="2">按实际型号</td>
	</tr>
    <tr>
	    <td>二极管</td>
        <td colspan="2">按实际型号</td>
	</tr>
    <tr>
	    <td>三极管</td>
        <td colspan="2">按实际型号</td>
	</tr>
    <tr>
	    <td>集成电路</td>
        <td colspan="2">按实际型号</td>
	</tr>
    <tr>
	    <td>接插件</td>
        <td colspan="2">标明管脚数</td>
	</tr>
    <tr>
	    <td>光电器件</td>
        <td colspan="2">按实际型号</td>
	</tr>
    <tr>
	    <td>其他元件</td>
        <td colspan="2">按实际型号</td>
	</tr>
</table>
