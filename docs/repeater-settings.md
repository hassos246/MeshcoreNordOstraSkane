# Repeater settings

## Radio

```text
set radio 869.6179809,62.5,8,8
set radio.rxgain on
```

## Routing and acknowledgements

Ställer in radion att använda 3 bytes för att identifiera sig och mer robust bekräftelse av direktmeddelande.

```text
set path.hash.mode 2
set multi.acks 1
set loop.detect moderate
```

## Advertisements and flooding

Skicka advert till repeaters grannar var fjärde timme och advert över hela meshet var 47e timme. Begränsar flood meddelanden utan region till 4 hopp, detta för att avlasta nätet från väldig långväga trafik utan att försvåra för nya användare.

```text
set advert.interval 240
set flood.advert.interval 47
set flood.max.unscoped 4
```

## Duty cycle

Enligt lag är det inte tillåtet att sända mer än 10% av tiden.

```text
set dutycycle 10
```

## AGC

```text
set agc.reset.interval 4
```

## Guest access

Lämna detta tomt. Kommandot behöver inte köras.

```text
set guest.password
```

## Power saving

Aktivera detta vid batteridrift.

```text
powersaving on
```

## Reboot

Starta om efter att alla inställningar angetts.

```text
reboot
```

---

[← Tillbaka till förstasidan](../README.md)
