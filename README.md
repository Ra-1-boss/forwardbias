# forwardbias
% Parameters
Is = 1e-12; % Reverse saturation current (A)
Vt = 0.025; % Thermal voltage (V) at room temperature (25 mV)
n = 1;      % Ideality factor
V = 0:0.01:0.8; % Voltage range for forward bias (0 to 0.8V)

% Diode current calculation using Shockley equation
I = Is * (exp(V / (n * Vt)) - 1);

% Plotting
figure;
plot(V, I, 'b', 'LineWidth', 2);
grid on;
title('Diode I-V Characteristics (Forward Bias)');
xlabel('Voltage (V)');
ylabel('Current (A)');
