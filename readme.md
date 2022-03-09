# ARO LPDA Array

## RF chain

### Antenna and first stage
```mermaid
flowchart LR

  style RF fill:#ffffff,stroke:#000000,stroke-width:4px
  classDef rf fill:#ffffff,stroke:#000000,stroke-width:2px

  classDef power fill:#ffffff,stroke:#000000,stroke-width:2px,stroke-dasharray: 5 5

  A0 --> A1
  A1 --> A2

  subgraph RF [Box 1]

  M1([DC-reg])
    A2 --?--> A3
    A3 --?--> A4
    A4 --?--> M0
    M0 --?--> A5
    A5 --?--> A6
    M0 -.DC-unreg.-> M1
    M1 -.DC-5V.-> A3
  end

  A6 --> A7


  A0[\Antenna/]
  A1([Coax. cable 1])
  A2([Bulk-head 1])
  A3([LNA 1])
  A4([LPF])
  A5([HPF])
  M0([Bias-T])
  A6([Bulk-head 2])
  A7([Coax. cable 2])




```

### Second stage

### Coax to basement

### Basement rack unit
* 400-800 MHz filter.
* Bias-T to inject power.
* Voltaje regulators.
* Power supply.
* Third stage amplifiers.



## Suppliers
* Antenna - ???
* (8) LNA 1 - 
  [Mini-Circuits.com](https://www.minicircuits.com/WebStore/dashboard.html?model=ZX60-P33ULN%2B)
* (16) LNA 2&3 -
  [Amazon.ca - Noeelec Lana Barebones](https://www.amazon.ca/dp/B07XNH6QW6/)
* (8) Band Pass Filter - ZABP-598-S+ - 410-785 MHz) -
  [Mini-Circuits.com](https://www.minicircuits.com/WebStore/dashboard.html?model=ZABP-598-S%2B)


## Resources
* Antenna - Y42400WB [Datasheet](datasheets/Y42400WB-Spec-Sheet.pdf)
* LNA 1 - ZX60-P33ULN+ [Datasheet](datasheets/ZX60-P33ULN+.pdf)
* LNA 2&3 - Noeelec Lana Barebones [Datasheet](datasheets/lana_datasheet_revision_1.pdf)
* Band Pass Filter - ZABP-598-S+ - 410-758 MHz [Datasheet](datasheets/ZABP-598-S+.pdf)
