# Шаблоны запросов отчетов

## 1. Остатки БСО на дату
- Источник: `РегистрНакопления.BSOBalances.Остатки`.
- Поля: `BSOType`, `BSOItem`, `ExternalBlankCode`, `ResponsiblePerson`, `PartyDocument`, `Quantity`.

## 2. Движение БСО за период
- Источник: `РегистрНакопления.BSOBalances.Обороты`.
- Поля: `Период`, `Регистратор`, `Операция`, `BSOItem`, `ExternalBlankCode`, `ResponsiblePerson`, `PartyDocument`, `QuantityIn`, `QuantityOut`.

## 3. Акт списания за месяц по МОЛ
- Источник: `Документ.BSOWriteOff` + ТЧ `Items`.
- Поля: `Дата`, `Номер`, `МОЛ`, `BSOItem`, `ExternalBlankCode`, `PartyDocument`, `Quantity`, `Price`, `Amount`, `WriteOffReason`.

## 4. Акт инвентаризации по МОЛ
- Источник: `Документ.BSOInventory` + ТЧ `Items`.
- Поля: `BSOItem`, `ExternalBlankCode`, `PartyDocument`, `BookQty`, `FactQty`, `DiffQty`, `Price`, `DiffAmount`, `InventoryResult`.
