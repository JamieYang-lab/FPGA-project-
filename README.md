# FPGA-project-1
### Authors: 105321047 105321035

#### Input/Output unit:<br>
* 8x8 LED 矩陣，用來顯示閃躲遊戲畫面。下圖為對戰中的畫面。<br>
<img src="https://github.com/JamieYang-lab/FPGA-project-/blob/main/images/462556518_1376486029986701_6593770486051233512_n.jpg" width="300"/><br>
* 七段顯示器，用來顯示倒數計時。<br>
<img src="https://github.com/JamieYang-lab/FPGA-project-/blob/main/images/462567880_1102193041378006_1474330130410306633_n.jpg" width="300"/><br>
* LED 陣列，用來顯示剩餘的生命。<br>
<img src="https://github.com/JamieYang-lab/FPGA-project-/blob/main/images/462584675_916789567232196_3956865446878236999_n.jpg" width="300"/><br>

#### 功能說明:<br>
遊戲規則：輸入秒數，使用按鈕操控人物左右閃躲落下的障礙物。碰到障礙物扣一血，扣完三血失敗，倒數計時結束成功躲避所有障礙物即成功。<br>

#### 程式模組說明:<br>
module LD_final_project(
    output reg [7:0] DATA_R, DATA_G, DATA_B, //接到8*8LED矩陣，顯示畫面(紅綠藍)
    output reg [6:0] d7_1, //接到七段顯示器，顯示秒數
    output reg [2:0] COMM, Life,// 接到LED陣列，顯示生命值
    output reg [1:0] COMM_CLK, //FPGA內建時鐘，操控刷新
    output EN, //接8*8LED矩陣
    input CLK, clear, Left, Right, //接到按鈕，操控人物左右和開始遊戲
    input [7:0] SW  // 輸入秒數用的開關，接到開關
);


#### Demo video: (請將影片放到雲端空間)

<a href="https://drive.google.com/file/d/1NlwseTnhxPiVIIJlAHLIW_4pNClAuiux/view" title="Demo Video"><img src="https://github.com/JamieYang-lab/FPGA-project-/blob/main/images/462567880_1102193041378006_1474330130410306633_n.jpg" width="500"/></a>
