### Определение максимально привлекательного товара на основе нормализованных характеристик

#### Введение
Выбор оптимального товара для покупки, особенно в условиях обширного ассортимента, требует детального анализа и сравнения различных характеристик. В данном исследовании рассматривается подход к оценке привлекательности товаров с использованием нормализации их параметров и последующего расчета на основе этих нормализованных данных. Мы рассмотрим модели электрических самокатов, с учетом их грузоподъемности, максимальной скорости, запаса хода и стоимости.

#### Методология

##### Шаг 1: Сбор данных
Для анализа были выбраны модели электрических самокатов с различными характеристиками, такими как грузоподъемность, максимальная скорость, запас хода и цена. [Таблица 1](table_01.md)

##### Шаг 2: Нормализация параметров
Для нормализация всех характеристик с использованием метода Min-Max нормализации. Нормализованное значение каждого параметра рассчитывается по формуле:

$$
X'_ i = \frac{X_i - X_{\text{min}}}{X_{\text{max}} - X_{\text{min}}}
$$

где:

- $X'_i$ — нормализованное значение критерия,
- $X_i$ — значение критерия,
- $X_{\text{min}}$ и $X_{\text{max}}$ — минимальные и максимальные значения критерия в наборе данных.

При нормализации цены методом min-max мы стремимся минимизировать значение цены. Нормализованная цена рассчитывается по формуле:

$$
P'_ i = 1 - \frac{X_i - X_{\text{min}}}{X_{\text{max}} - X_{\text{min}}}
$$

Таким образом, при нормализации мы получаем значение, близкое к 1 для минимальной цены, что отражает нашу цель оптимизировать цену. [Таблица 2](table_02.md)

##### Шаг 3: Вычисление агрегированного показателя
Для объединенеия нормализованных критериев (Грузоподъемность, Максимальная скорость, Запас хода) вычислим агрегированный показатель по формуле:

$$
A_i = \sqrt{\sum_{i=1}^{n} (X'_i)^2}
$$

где $A_i$ — агрегированный показатель криетриев, $X'_i$ — нормализованное значение критерия.

##### Шаг 4: Нормализация агрегированного показателя
Нормализация агрегированного показателя необходима для корректного вычисления Евклидовой нормы, чтобы привести все значения к единой шкале, по формуле:

$$
A'_ i = \sqrt{\sum_{i=1}^{n} (A_i)^2}
$$

где $A_i$ — нормализованный агрегированный показатель, а $A_i$ — агрегированный показатель. [Таблица 3](table_03.md)

##### Шаг 5: Вычисление Евклидовой нормы

На заключительном этапе рассчитывается Евклидова норма по формуле:

$$
E_i = \sqrt{(P'_i)^2 + (A'_i)^2}
$$

Расчеты в [Таблице 4](table_04.md).

#### Результаты и обсуждение
На основе проведенного анализа, наиболее привлекательными моделями по совокупности параметров и стоимости оказались модели **f30** **e22** и **f40a**. Они демонстрируют высокую привлекательность по отношению к их цене, что делает их оптимальными вариантами для покупки. Модели с высшими техническими характеристиками, такие как  **gt2** **gt1** и **p100su**, хоть и имеют высокие показатели по отдельным параметрам, уступают по привлекательности из-за значительной стоимости.

#### Заключение
Приведенная методология позволяет объективно оценить и сравнить различные модели товаров на основе совокупности их характеристик и цены. Такой подход можно использовать для принятия более обоснованных решений при выборе товара, особенно когда выбор основывается на нескольких ключевых параметрах. [Таблица 5](table_05.md)
