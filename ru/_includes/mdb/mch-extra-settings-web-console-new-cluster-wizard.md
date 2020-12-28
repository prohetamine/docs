- **Начало резервного копирования (UTC)** — время по UTC, когда требуется начать [резервное копирование](../../managed-clickhouse/operations/cluster-backups.md) кластера (в 24-часовом формате). Если время не задано, резервное копирование начнется в 22:00 UTC.

- **Окно обслуживания** — настройки окна технического обслуживания. С их помощью вы можете указать предпочтительное время начала проведения операций по техническому обслуживанию хостов кластера (например, можно выбрать время, когда кластер наименее нагружен запросами): 
  - Чтобы указать предпочтительное время начала окна технического обслуживания, выберите пункт **по расписанию** и задайте нужные день недели и час дня в UTC (Coordinated Universal Time), выбрав значения из выпадающих списков.
  - Чтобы разрешить проведение операций технического обслуживания в любое время, выберите пункт **произвольное**.  

  Операции по техническому обслуживанию могут включать в себя: обновление версии СУБД, применение патчей и так далее. 

- **Гибридное хранилище** — включите эту опцию и выберите один из типов сетевого хранилища в разделе **Хранилище**, чтобы создать кластер, который будет использовать [гибридное хранилище](../../managed-clickhouse/concepts/storage.md#hybrid-storage-features). 

  {% note warning %}
  
  Эту опцию невозможно выключить после создания кластера.
  
  {% endnote %}
  
- **Доступ из {{ datalens-name }}** — включите эту опцию, чтобы получить возможность анализировать данные из кластера в сервисе [{{ datalens-full-name }}](../../datalens/concepts/index.md). Подробнее о настройке подключения см. в разделе [Подключение к {{ datalens-name }}](../../managed-clickhouse/operations/datalens-connect.md).
  
- **Доступ из консоли управления** — включите эту опцию, чтобы получить возможность [выполнять SQL-запросы](../../managed-clickhouse/operations/web-sql-query.md) к базам кластера из консоли управления {{ yandex-cloud }}.

- **Доступ из Метрики и AppMetrica** — включите эту опцию, чтобы получить возможность [импортировать данные из AppMetrica](https://appmetrica.yandex.ru/docs/cloud/index.html) в кластер.