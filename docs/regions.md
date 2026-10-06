# Regions

## Configure regions

Regioner används för att begränsa spridning av flood meddelanden, endast repeaters med regionen angiven skickar meddelandet vidare. * innebär meddelanden utan region angiven, dessa är begränsade till 4 hopp enligt de rekommenderade inställningarna i [Inställningar för repeater](docs/repeater-settings.md)

Det är rekommenderat att lägga in angränsande läns regioner för att underlätta spridning av deras meddelanden, detta är speciellt önskvärt för närliggande län.

| Region | Område | Användning |
|---|---|---|
| `*` | Globalt | Tillåter trafik utan region |
| `europe` | Europa | |
| `eu` | EU | |
| `se` | Sverige | |
| `se07` | Kronobergs | |
| `se10` | Blekinge län | |
| `se12` | Skåne län | |
| `se13` | Hallands län | |
| `oresund` | Öresundsregionen | Kan vara bara att ha på backbone repeaters |
| `dk` | Danmark | Danskarna önskar att vi har denna i alla fall på backbone repeaters för att underlätta deras kommunikation till Bornholm |
| `offgrid` | Experimentiell | Använd på noder som kan drivas på batteri under längre tid. Möjliggör tester av hur meddelande kommer kunna skickas vid strömavbrott |

```text
region allowf *
region put europe *
region put eu *
region put se eu
region put se07 se
region put se10 se
region put se12 se
region put se13 se
region put oresund eu
region put dk eu
region put offgrid eu
region save
```

## Region hierarchy

```text
*
├── europe
└── eu
    ├── se
    │   ├── se07
    │   ├── se10
    │   ├── se12
    │   └── se13
    ├── oresund
    ├── dk
    └── offgrid
```

## Region reference

Mer information om regioner kan du läsa om här.

[MeshCore regions – meshat.se](https://meshat.se/meshcore/regioner)

---

[← Tillbaka till förstasidan](../README.md)
