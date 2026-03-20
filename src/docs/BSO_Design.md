# БСО: технический проект конфигурации 1С 8.3

## Объекты метаданных
- Справочники: `BSOTypes`, `BSOItems`, `ResponsiblePersons`, `Counterparties`.
- Перечисления: `BSOStatus`, `WriteOffReason`, `InventoryResult`.
- Регистры накопления: `BSOBalances`, `BSOParties`.
- Регистр сведений: `BSOSerialNumberRegistry`.

## Ключевые реквизиты
- В `BSOItems`:
  - `BSOType` (обязательный),
  - `HasSeriesNumber`,
  - `Series`,
  - `Number`,
  - `ExternalBlankCode` (обязательный, уникальный глобально).
- В регистрах партий:
  - `Price` = `Число(15,4)`,
  - `Amount` = `Число(15,2)`.

## Индексы и уникальность
- `BSOItems.ExternalBlankCode` — уникальный индекс.
- `BSOItems(BSOType, Series, Number)` — поиск и контроль дублей.
- `BSOSerialNumberRegistry(BSOType, Series, Number)` — уникальный индекс.

## Правила идентификации
- Для нумеруемых БСО: ключ `BSOType + Series + Number`.
- Для ненумеруемых БСО: ключ `BSOType + ExternalBlankCode + PartyDocument`.
