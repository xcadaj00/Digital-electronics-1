# Lab 01-gates

[https://github.com/xcadaj00/Digital-electronics-1/](https://github.com/xcadaj00/Digital-electronics-1/)

## De Morgan's laws simulation

### Source code

```vhdl
architecture dataflow of gates is
begin
    f_o     <= ((not b_i) and a_i) or ((not c_i) and (not b_i));
    fnand_o <= ((b_i nand b_i) nand (a_i)) nand ((c_i nand c_i) nand (b_i nand b_i));
    fnor_o  <= (((b_i) nor (a_i nor a_i)) nor ((c_i) nor (b_i))) nor (((b_i) nor (a_i nor a_i)) nor ((c_i) nor (b_i)));
end architecture dataflow;
```

### Graph

![Simulation De Morgan's laws](images/demorgangraph.png)

### EDA playground link

[https://www.edaplayground.com/x/a_5b](https://www.edaplayground.com/x/a_5b)

### Table

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

## Verification of Distributive laws

### Source code

```vhdl
architecture dataflow of gates is
begin
    f1_o  <= (x_i and y_i) or (x_i and z_i);
    f2_o  <= x_i and (y_i or z_i);
    g1_o  <= (x_i or y_i) and (x_i or z_i);
    g2_o  <= x_i or (y_i and z_i);
end architecture dataflow;
```

### Graph

![Simulation of Distributive laws](images/distributivelawsgraph.png)

### EDA playground link

[https://www.edaplayground.com/x/pEA4](https://www.edaplayground.com/x/pEA4)
