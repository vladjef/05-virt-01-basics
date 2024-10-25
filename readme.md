# Задача 2
Выберите один из вариантов платформы в зависимости от задачи. Здесь нет однозначно верного ответа так как все зависит от конкретных условий: финансирование, компетенции специалистов, удобство использования, надежность, требования ИБ и законодательства, фазы луны.

Тип платформы:

физические сервера;
паравиртуализация;
виртуализация уровня ОС;

Задачи:
высоконагруженная база данных MySql, критичная к отказу;
различные web-приложения;
Windows-системы для использования бухгалтерским отделом;
системы, выполняющие высокопроизводительные расчёты на GPU.
Объясните критерии выбора платформы в каждом случае.

## Ответ
### высоконагруженная база данных MySql, критичная к отказу;
Физические сервера. Настроен на задачи хранения данных и непрерывное выполнение определенных задач. Обеспечение высокого уровня безопасности.

### различные web-приложения;
Виртуализация уровня ОС. Быстро разворачиваются контейнеры с приложением. Возможность использовать подход IaaC. Хорошая масштабируемость.

### Windows-системы для использования бухгалтерским отделом;
Физические сервера или паравиртуализация. Стабильность, поддержка продуктов Microsoft, наличие физической машины у каждого сотрудника.

### системы, выполняющие высокопроизводительные расчёты на GPU.
Паравиртуализация. У Citrix Xen есть "продвинутые возможности по предоставлению внутри виртуальной машины 3D аппаратной акселерации GPU".

---

# Задача 3
Выберите подходящую систему управления виртуализацией для предложенного сценария. Опишите ваш выбор.

Сценарии:

100 виртуальных машин на базе Linux и Windows, общие задачи, нет особых требований. Преимущественно Windows based-инфраструктура, требуется реализация программных балансировщиков нагрузки, репликации данных и автоматизированного механизма создания резервных копий.
Требуется наиболее производительное бесплатное open source-решение для виртуализации небольшой (20-30 серверов) инфраструктуры на базе Linux и Windows виртуальных машин.
Необходимо бесплатное, максимально совместимое и производительное решение для виртуализации Windows-инфраструктуры.
Необходимо рабочее окружение для тестирования программного продукта на нескольких дистрибутивах Linux.

## Ответ
### 100 виртуальных машин на базе Linux и Windows, общие задачи, нет особых требований. Преимущественно Windows based-инфраструктура, требуется реализация программных балансировщиков нагрузки, репликации данных и автоматизированного механизма создания резервных копий.
Необходима аппаратная виртуализация (создание VM с различными ОС). Подойдет Xen с открытым исходным кодом, поддержка Windows, Linux ОС, с возможностью функции миграции.
### Требуется наиболее производительное бесплатное open source-решение для виртуализации небольшой (20-30 серверов) инфраструктуры на базе Linux и Windows виртуальных машин.
Необходима аппаратная виртуализация (создание VM с различными ОС). Подойдет Xen с открытым исходным кодом, поддержка Windows, Linux ОС, с возможностью функции миграции.
### Необходимо бесплатное, максимально совместимое и производительное решение для виртуализации Windows-инфраструктуры.
Hyper-V Server "заточен" для продуктов Microsoft и безплатный.
### Необходимо рабочее окружение для тестирования программного продукта на нескольких дистрибутивах Linux.
Выбор среди вариантов для ядер Linux - KVM. Преимущество к производительности. Поддержка большинства Linux платформ.

---

# Задача 4
Опишите возможные проблемы и недостатки гетерогенной среды виртуализации (использования нескольких систем управления виртуализацией одновременно) и что необходимо сделать для минимизации этих рисков и проблем. Если бы у вас был выбор, создавали бы вы гетерогенную среду или нет?

## Ответ
### возможные проблемы и недостатки гетерогенной среды виртуализации
Сложность в управлении.
Неэффективность использование ресурсов.
Необходим большой штат сотрудников для поддержки.
Сложность переноса данных между разными средами
### что необходимо сделать для минимизации этих рисков и проблем
"необходимо использовать комплексные решения, которые смогут функционировать как в физической, так и в виртуальной среде"
"нужно максимально снизить вероятность несовместимости технологий и упростить управление инфраструктурой"
Необходима универсальная платформа.
### Если бы у вас был выбор, создавали бы вы гетерогенную среду или нет?
Скорее всего, нет.
