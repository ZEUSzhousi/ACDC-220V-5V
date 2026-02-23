![8f06c317682cab9bc97a687a0bc5720d](https://github.com/user-attachments/assets/e8ce3d27-8047-44d4-a575-7ebe4737edbe)# ACDC-220V-5V
<img width="432" height="624" alt="image" src="https://github.com/user-attachments/assets/745aee76-b1f5-40e0-bfa9-5ae48fabe2ab" />

<img width="953" height="220" alt="image" src="https://github.com/user-attachments/assets/d87aa429-6cd2-4f4e-9084-9a5dd76ec85f" />
<img width="926" height="630" alt="image" src="https://github.com/user-attachments/assets/6770eed8-93de-4293-a615-439d5af2da54" />

交流电压滤波整流

<img width="865" height="232" alt="image" src="https://github.com/user-attachments/assets/0c7dc41e-46b9-4bcc-8ab9-dd8b31aef38b" />

F1提供过流保护
RV1当电网浪涌（如雷击、尖峰）超过阈值时，压敏电阻迅速导通，将浪涌能量泄放到零线 R1断电后泄放电容存储的电荷
L1与 X1 电容组成 LC 滤波网络，抑制差模干扰
X1与 L1 配合滤除差模干扰
Y1 Y2提供共模干扰的泄放路径
G1整流
C1和C2率高低频滤波

芯片驱动模块

<img width="633" height="613" alt="image" src="https://github.com/user-attachments/assets/524364f9-8966-42b1-9096-a67837eec8cf" />

R2和R3初始启动电流在芯片工作区间
R9控制芯片工作频率
R6 C3 D1构成RCD吸收电路，吸收变压器的漏感电压和Q1的D极的寄生电感和电容产生的尖峰电压
在GATE 信号控制下Q1高速导通和关断，驱动变压器 T1 的初级绕组
D2加速 MOSFET 关断，保证断开时电压直接接地快速降压
R4大电阻防止导通时电流流向地 R5小电阻驱动mos管
R10电流采样电阻，将初级绕组电流转换为电压信号，送入 U1 的 SENSE 引脚，实现逐周期电流限制和过流保护
R8 C4RC 滤波网络，对 SENSE 信号进行滤波，防止噪声误触发保护
D3 R7 C5反向电压吸收

<img width="865" height="740" alt="image" src="https://github.com/user-attachments/assets/0ce6ab87-6f5a-4558-9aa3-87a53f23ba46" />

C6 R11 R12组成RC 网络，对光耦次级输出的 FB 信号进行滤波和补偿
光耦PC817C 隔离原副边，PC817C初级发光二极管由 TL431 驱动，次级光敏三极管的导通程度反映输出电压误差，调节初级 FB 引脚电压
R15 R16 和CJ431-G内部 2.5V 基准，稳压5V
C7和R18RC滤波提升环路稳定性，防止振荡
R14为光耦发光二极管提供稳定的偏置电流
R13分流，避免过大导致光耦进入饱和区，为补偿电容 C7 提供放电路径
R17 C8 D4截至反向电压，将这部分尖峰能量转移到C8 R17滤波电路中
C9 C10 C11输出滤波

