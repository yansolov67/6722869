Mermaid: примеры блок-схем, графиков и диаграмм
Каждый пример — отдельный блок ```mermaid. Файл открывается в GitHub, GitLab, Obsidian, VS Code (с расширением Markdown Preview Mermaid Support) и на mermaid.live.

Оглавление
Блок-схемы (flowchart)
Диаграмма последовательности (sequence)
Диаграмма классов (class)
Диаграмма состояний (state)
ER-диаграмма
Пользовательский путь (journey)
Диаграмма Ганта
Круговая диаграмма (pie)
Квадрантная диаграмма
Диаграмма требований
Git-граф
Ментальная карта (mindmap)
Временная шкала (timeline)
Sankey
XY-график (столбцы и линии)
Блочная диаграмма
Пакетная диаграмма
Канбан
Архитектурная диаграмма
C4-диаграмма
1. Блок-схемы (flowchart)
1.1. Базовая схема

1.2. Направления: LR, RL, TB, BT

1.3. Все формы узлов

1.4. Типы связей

1.5. Подграфы (subgraph)

1.6. Стилизация

1.7. Алгоритм: чётное или нечётное

1.8. Цикл

2. Диаграмма последовательности (sequence)

3. Диаграмма классов (class)

4. Диаграмма состояний (state)

5. ER-диаграмма

6. Пользовательский путь (journey)

7. Диаграмма Ганта

8. Круговая диаграмма (pie)

9. Квадрантная диаграмма

10. Диаграмма требований
Unable to render rich display

Lexical error on line 4. Unrecognized text.
...id: 1 text: Пользователь должен
----------------------^

For more information, see https://docs.github.com/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams#creating-mermaid-diagrams

requirementDiagram
    requirement login_req {
        id: 1
        text: Пользователь должен входить по логину и паролю
        risk: high
        verifymethod: test
    }
    functionalRequirement session_req {
        id: 1.1
        text: Сессия истекает через 30 минут
        risk: medium
        verifymethod: inspection
    }
    element auth_module {
        type: module
        docref: auth.md
    }

    login_req - contains -> session_req
    auth_module - satisfies -> login_req
11. Git-граф

12. Ментальная карта (mindmap)

13. Временная шкала (timeline)

14. Sankey
Unable to render rich display

Parse error on line 2:
sankey-betaЗарплата,Аренда,30З
-----------^
Expecting 'NEWLINE', 'EOF', 'COMMA', got 'NON_ESCAPED_TEXT'

For more information, see https://docs.github.com/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams#creating-mermaid-diagrams

sankey-beta

Зарплата,Аренда,30
Зарплата,Еда,25
Зарплата,Транспорт,10
Зарплата,Накопления,20
Зарплата,Развлечения,15
15. XY-график (столбцы и линия)
Unable to render rich display

Lexical error on line 3. Unrecognized text.
...есяцам" x-axis [янв, фев, мар, апр,
----------------------^

For more information, see https://docs.github.com/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams#creating-mermaid-diagrams

xychart-beta
    title "Продажи по месяцам"
    x-axis [янв, фев, мар, апр, май, июн]
    y-axis "Тыс. руб." 0 --> 100
    bar [20, 35, 50, 45, 70, 90]
    line [20, 35, 50, 45, 70, 90]
16. Блочная диаграмма

17. Пакетная диаграмма

18. Канбан

19. Архитектурная диаграмма

20. C4-диаграмма

