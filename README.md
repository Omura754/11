>> % 自動車の電流分流様相モデルの作成

% 電池（Battery）電圧 (V) （通常自動車に搭載されているバッテリーの電圧は12 V）
V_battery = 12;

% 電気機器の抵抗 (Ω) （接触抵抗の値は仮定している）
R_headlights = 5;
R_radio = 3;
R_other = 2;

% 各電気機器の電流 (A)（オームの法則を使い計算する）
I_headlights = V_battery / R_headlights;
I_radio = V_battery / R_radio;
I_other = V_battery / R_other;

% 合計電流（3つの機器の電流を足す）
I_total = I_headlights + I_radio + I_other;

% 各電気機器の電力 (W)（電力＝電流×電圧）
P_headlights = I_headlights * V_battery;
P_radio = I_radio * V_battery;
P_other = I_other * V_battery;

% 合計電力（3つの機器の電力を足す）
P_total = P_headlights + P_radio + P_other;

% 結果の表示（display関数を用い，それぞれの値を出力する）
disp('電流分流様相の結果:');
disp(['合計電流: ', num2str(I_total), ' A']);
disp(['合計電力: ', num2str(P_total), ' W']);
disp(['ヘッドライトの電力: ', num2str(P_headlights), ' W']);
disp(['ラジオの電力: ', num2str(P_radio), ' W']);
disp(['その他の電気機器の電力: ', num2str(P_other), ' W']);
電流分流様相の結果:
合計電流: 12.4 A
合計電力: 148.8 W
ヘッドライトの電力: 28.8 W
ラジオの電力: 48 W
その他の電気機器の電力: 72 W
>> 
