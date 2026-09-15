<img width="4080" height="3072" alt="3c81e4ee5e98adc0c07c7acacd37e049" src="https://github.com/user-attachments/assets/d6646431-6e7f-4963-b793-306fa4409146" />
<img width="3072" height="4096" alt="8bbe1dfb1d18deaa911b5974a34ad534" src="https://github.com/user-attachments/assets/849cd9c6-0928-4adb-9e36-da97b8e7c498" />

输出波形纹波电压
<img width="320" height="234" alt="77" src="https://github.com/user-attachments/assets/611bc255-f769-4552-a197-2cfdf13d0095" />

<img width="630" height="777" alt="1" src="https://github.com/user-attachments/assets/0b6d7910-053e-4270-8eaf-2d902787ec3b" />
<img width="1048" height="223" alt="2" src="https://github.com/user-attachments/assets/f9b7f727-0c51-43ed-b872-c87b2b9032f5" />
<img width="1122" height="679" alt="3" src="https://github.com/user-attachments/assets/95a24192-1561-4c04-a926-7f83e2ed4f9c" />


交流电压滤波整流

<img width="1048" height="223" alt="2" src="https://github.com/user-attachments/assets/1a623ad8-40ce-4701-9bc6-93d263c9f05a" />

F1提供过流保护
RV1当电网浪涌（如雷击、尖峰）超过阈值时，压敏电阻迅速导通，将浪涌能量泄放到零线 R1断电后泄放电容存储的电荷
L1与 X1 电容组成 LC 滤波网络，抑制差模干扰
X1与 L1 配合滤除差模干扰
Y1 Y2提供共模干扰的泄放路径
G1整流
C1和C2率高低频滤波

芯片驱动模块

<img width="503" height="513" alt="4" src="https://github.com/user-attachments/assets/51c1c861-0db7-4a33-a7bf-85e991bf6239" />

R2和R3初始启动电流在芯片工作区间
R9控制芯片工作频率
R6 C3 D1构成RCD吸收电路，吸收变压器的漏感电压和Q1的D极的寄生电感和电容产生的尖峰电压
在GATE 信号控制下Q1高速导通和关断，驱动变压器 T1 的初级绕组
D2加速 MOSFET 关断，保证断开时电压直接接地快速降压
R4大电阻防止导通时电流流向地 R5小电阻驱动mos管
R10电流采样电阻，将初级绕组电流转换为电压信号，送入 U1 的 SENSE 引脚，实现逐周期电流限制和过流保护
R8 C4RC 滤波网络，对 SENSE 信号进行滤波，防止噪声误触发保护
D3 R7 C5反向电压吸收
![330f85eb1c4f01dc9461e41689df4684](https://github.com/user-attachments/assets/b8be322a-f5e0-47a6-9197-7eeb3ad459ce)
![f701f6e1744d6a31fc3d42bbc55a7c49](https://github.com/user-attachments/assets/1a119bca-357f-4e87-9ee3-a0365430ade6)

<img width="816" height="647" alt="5" src="https://github.com/user-attachments/assets/03975702-695d-4bcc-ae79-72b661e7ddad" />

C6 R11 R12组成RC 网络，对光耦次级输出的 FB 信号进行滤波和补偿
光耦PC817C 隔离原副边，PC817C初级发光二极管由 TL431 驱动，次级光敏三极管的导通程度反映输出电压误差，调节初级 FB 引脚电压
R15 R16 和CJ431-G内部 2.5V 基准，稳压5V
C7和R18RC滤波提升环路稳定性，防止振荡
R14为光耦发光二极管提供稳定的偏置电流
R13分流，避免过大导致光耦进入饱和区，为补偿电容 C7 提供放电路径
R17 C8 D4截至反向电压，将这部分尖峰能量转移到C8 R17滤波电路中
![8b4666993e26de2c5ca9c1897bf96ae4](https://github.com/user-attachments/assets/067593a9-d122-4431-9038-88844a74e532)


C9 C10 C11输出滤波

