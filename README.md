# Team9AYS17
For our CS154 Project, we developed a theoretical computer using a turing machine. This includes an assembly language to written on an input tape to perform computation.

All values after = within the tests show the resulting a register. 

## Compound Tests

* #IA#LDV$111#ID#IC#AC#SD#H = -11
* #IA#LDV$111#ID#IC#AC#SD#LBV$11#SB#H = -1111
* #11ID#J111#111LDV$1111#SD#H = -1111
* #11ID#J1111#111LDV$1111#SD#H = -1

## Load Tests
### LAV

<table>
    <tr>
        <th></th><th>A</th><th>B</th><th>C</th><th>D</th><th>V</th>
        <th>LD A, Y</th><td>-</td><td>LAB</td><td>LAC</td><td>LAD</td><td>LAV</td>
        <th>LD B, Y</th><td>LBA</td><td>-</td><td>LBC</td><td>LBD</td><td>LBV</td>
        <th>LD C, Y</th><td>LCA</td><td>LCB</td><td>-</td><td>LCD</td><td>LCV</td>
        <th>LD D, Y</th><td>LDA</td><td>LDB</td><td>LDC</td><td>-</td><td>LDV</td>
    </tr>
</table>

* #LAV$111#LBA#LAB#H = 111
* #LAV$111#LCA#LAC#H = 111
* #LAV$111#LDA#LAD#H = 111
* #LAV$-11#LBA#LAB#H = -11
* #LAV$-11#LCA#LAC#H = -11
* #LAV$-11#LDA#LAD#H = -11

* #LBV$111#LCB#LDC#LAD = 111
* #LDV$111#LBD#LCB#LAC = 111
* #LCV$111#LDC#LBD#LAB = 111
* #LDV$111#LCD#LBC#LAB = 111 
* #LBV$-11#LCB#LDC#LAD = -11
* #LDV$-11#LBD#LCB#LAC = -11
* #LCV$-11#LDC#LBD#LAB = -11
* #LDV$-11#LCD#LBC#LAB = -11

### Arithmetic Tests

* #IA#IB#IC#ID#AB#AC#AD#AV$111#H = 1111111
* #DA#DB#DC#DD#AB#AC#AD#AV$-111#H = -1111111
* #IA#IB#IC#ID#SB#SC#SD#SV$111#H = -11111
* #DA#DB#DC#DD#SB#SC#SD#SV$-111#H = 11111
