# Release Notes

## v1.1.0

### Added
- Спеціальний тариф доставки для Києва: базова ставка 80.0.
- Явний параметр ставки податку `tax_rate` (значення за замовчуванням 0.20).

### Changed
- Коефіцієнт доставки за вагу збільшено з 12.0 до 15.0.
- Виконано перехід до Data Coupling: функції приймають лише необхідні примітивні дані.

### Breaking Changes
- Змінено сигнатури функцій розрахунку: `calculate_delivery_cost(city, weight_kg)` замість `calculate_delivery_cost(customer, weight_kg)`.
- Видалено глобальну змінну `GLOBAL_TAX_RATE`.
- Видалено прапорець `mode_flag`; функцію `process_invoice` замінено на `process_standard_invoice` і `process_tax_exempt_invoice`.
