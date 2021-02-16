# **01-gates**

## *Link na môj GitHub*

https://github.com/SimonJaraby/Digital-electronics-1

## Overenie si De Morganových zákonov

### *Funkcie*

![Equations](Images/equations.png)

### Implementácia v VHDL

```vhdl
architecture dataflow of gates is
begin
    f_o  <= ((not b_i) and a_i) or ((not c_i) and (not b_i));
    fnand_o <= not (not (not b_i and a_i) and not(not b_i and not c_i));
    fnor_o <= (not (b_i or not a_i)) or (not (c_i or b_i));

end architecture dataflow;
```

### Taluľka logických hodnôt

| **c** | **b** |**a** | **f(c,b,a)** |
| :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 0 |

### Zobrazenie v čase 

![Waveforms](Images/waveforms.png)

### EDA Playground link

https://www.edaplayground.com/x/8Q97

## Verification of Distributive laws

### Funkcie

![Distributives](Images/distributives.png)

### Implementácia v VHDL

```vhdl
architecture dataflow of gates is
begin
   	f1_o <= (a_i and b_i)or(a_i and c_i);
	f2_o <= a_i and (b_i or c_i);
	f3_o <= (a_i or b_i) and (a_i or c_i);
	f4_o <= a_i or (b_i and c_i);

end architecture dataflow;
```

### Zobrazenie v čase 

![Waveforms 2](Images/waveforms2.png)

### EDA Playground link

https://www.edaplayground.com/x/cvK3
