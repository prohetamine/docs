---
noIndex: true
---

# Создание сервера {{ metastore-name }}

{% list tabs %}

- Консоль управления

  1. В [консоли управления]({{ link-console-main }}) выберите каталог, в котором нужно создать сервер.
  1. Нажмите кнопку **{{ ui-key.yacloud.iam.folder.dashboard.button_add }}** и выберите ![image](../../../_assets/data-proc/data-proc.svg) **{{ ui-key.yacloud.iam.folder.dashboard.label_data-proc }}** в выпадающем списке.
  1. На левой панели нажмите на значок ![image](../../../_assets/data-proc/metastore.svg) **Metastore-сервер**.
  1. Нажмите кнопку **{{ ui-key.yacloud.mdb.clusters.button_create }}**.
  1. Введите имя сервера в поле **{{ ui-key.yacloud.mdb.forms.base_field_name }}**. Имя должно быть уникальным в рамках каталога.
  1. (Опционально) Добавьте описание сервера.
  1. В блоке **{{ ui-key.yacloud.mdb.forms.section_network-settings }}** выберите сеть и подсеть, в которых будет размещен сервер {{ metastore-name }}.
  1. Если в облачной сети используются [группы безопасности](../../../vpc/concepts/security-groups.md), настройте группу безопасности по умолчанию на работу с {{ metastore-name }}. Для этого [добавьте](../../../vpc/operations/security-group-add-rule.md) в нее следующие правила:

      * Для входящего трафика от клиентов:

        * Диапазон портов — `30000-32767`.
        * Протокол — `Любой` (`Any`).
        * Источник — `CIDR`.
        * CIDR блоки — `0.0.0.0/0`.

      * Для входящего трафика от балансировщика:

        * Диапазон портов — `10256`.
        * Протокол — `Любой` (`Any`).
        * Источник — `Проверки состояния балансировщика`.

  1. При необходимости активируйте защиту сервера от непреднамеренного удаления пользователем.

      Включенная защита не помешает подключиться к серверу вручную и удалить данные.

  1. Нажмите кнопку **{{ ui-key.yacloud.common.create }}**.

{% endlist %}
