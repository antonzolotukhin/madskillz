# skills

Скиллы для Claude Code.

| Скилл | Что делает |
|---|---|
| [neuroslop](skills/neuroslop/SKILL.md) | Находит и правит нейрослоп в русском тексте: кальки, хвостовые деепричастия, тире-паузы, шаблонную риторику. Механический прогон — `scripts/detect.py`. |

## Установка

Через marketplace:

```
/plugin marketplace add antonzolotukhin/madskillz
/plugin install neuroslop@azmadskillz
```

Или симлинком, чтобы правки в репе сразу подхватывались:

```bash
ln -s "$PWD/skills/neuroslop" ~/.claude/skills/neuroslop
```

Для точного поиска оборотов `detect.py` нужен pymorphy3: `pipx install pymorphy3`. Без него скрипт работает по суффиксам.

## Новый скилл

Каталог `skills/<имя>/` с `SKILL.md` (frontmatter `name` и `description`), плюс запись в `.claude-plugin/marketplace.json`.
