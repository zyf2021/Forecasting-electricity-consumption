# Forecasting-electricity-consumption
Рассмотрен временной ряд данных о потреблении электроэнергии, чтобы построить модель для прогноза на основе предыдущих значений.

### Описание датасета:
Этот набор данных включает измерения электрической мощности, сделанные в одном доме в течение четырех лет (с 2006 по 2010 год). Данные включают различные метрики, такие как активная мощность, реактивная мощность, напряжение и интенсивность, которые регистрировались каждую минуту.

**Основные переменные:**
- `Date`: Дата в формате `dd/mm/yyyy`.
- `Time`: Время измерения в формате `hh:mm:ss`.
- `Global_active_power`: Суммарное потребление активной мощности (в киловатт).
- `Global_reactive_power`: Суммарное потребление реактивной мощности (в киловатт).
- `Voltage`: Напряжение (в вольтах).
- `Global_intensity`: Общая интенсивность (в амперах).
- `Sub_metering_1`: Энергия, потребляемая в зоне 1 (кухня) (в ватт-часах).
- `Sub_metering_2`: Энергия, потребляемая в зоне 2 (стирка, холодильник, осветительные приборы).
- `Sub_metering_3`: Энергия, потребляемая в зоне 3 (тепловой насос, кондиционер).

Датасет можно скачать с [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption).

---

### Шаги работы с данным проектом:

#### 1. **Загрузка и предобработка данных:**
   - Загрузить данные в pandas DataFrame.
   - Обработать пропуски, преобразовать временные данные, создать единую колонку `Datetime` из полей `Date` и `Time`.
   - Преобразовать строки в числовые значения, заменив некорректные данные.
   - Масштабировать данные Sub_metering

#### 2. **Исследовательский анализ данных (EDA):**
   - Построить график временного ряда потребления активной мощности (`Global_active_power`).
   - Построить график временного ряда потребления реактивной мощности (`Global_reactive_power`).
   - Построить график временного ряда общей интенсивности (`Global_intensity`).
   - Построить график временного ряда напряжения (`Voltage`).
   - Выявить сезонные тренды и пики (например, в зависимости от времени суток, дня недели).
   - Взять в срезе одной недели данные и посмотреть изменения потребления энергии по подкатегориям

#### 3. **Разложение на тренды и сезонность:**
   - Разложить временной ряд на тренд, сезонную и остаточную компоненты с помощью `seasonal_decompose`.

#### 4. **Построение модели прогноза:**
   - Применить модель временных рядов для прогноза потребления электроэнергии (например, ARIMA, SARIMA, Prophet).

#### 5. **Оценка и оптимизация модели:**
   - Разделить данные на тренировочные и тестовые, провести оценку качества модели с помощью метрик (MSE, MAE, RMSE).
   - Подбор гиперпараметров для оптимизации модели.

---

Этот проект будет полезен для изучения временных рядов и методов прогнозирования, а также для практики с реальными энергетическими данными. Если тебе нужны дополнительные шаги по работе с конкретными моделями или визуализациями, можешь задать вопросы на каждом этапе!
