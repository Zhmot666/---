# Структуры документов БСО

## Документы
- `BSOReceipt`
- `BSOIssue`
- `BSOUsage`
- `BSOReturn`
- `BSOWriteOff`
- `BSOInventory`

## Общая структура ТЧ для движения стоимости
- `BSOItem`
- `PartyDocument` (для расходных — обязательно)
- `Quantity` (15,3)
- `Price` (15,4)
- `Amount` (15,2)

## Доп. поля диапазонов (для `BSOReceipt`, `BSOUsage`, `BSOWriteOff`)
- `SeriesFrom`, `NumberFrom`
- `SeriesTo`, `NumberTo`

## Инвентаризация (`BSOInventory.Items`)
- `BSOItem`
- `PartyDocument`
- `BookQty`
- `FactQty`
- `DiffQty`
- `Price`
- `DiffAmount`
- `InventoryResult`
