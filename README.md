# Verilog-layer-08.03-2DEND

![image](https://github.com/YunJoongChul/Verilog-layer-08.03-2DEND/assets/86291432/4bbd956c-a030-41b8-969e-18f69bb71731)


#### input : 32x32, 1~1024의 숫자, weights : 5x5, 1의 숫자, bias : 10, output : 28 x 28 마지막 주소 값 : 29350 + 10 
1. cnt 사용의 필요성
2. cnt_ram_ctrl 이라는 cnt를 이용하여 ram의 address, state done, ram_inputdata, wea 조절
3. ram_row_ctrl 로 row stride 조절
4. delay로 인한 ram 쪽 데이터 넣는 부분 conv2 state에서 제어 , 원래 구상은 conv5였음
5. ram address 에 대한 이해가 필요함. 기존에는 그냥 했는데 이번에는 cnt를 통해 56까지 0을 가져갔다가 그 이후로 증가하게함.
6. ram에 저장되는 시점 wea신호 명확하게 잡기.
