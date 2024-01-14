---
cssclasses:
  - dashboard
banner: "![[banner1.jpg]]"
banner_y: 0.274
banner_x: 0.5
---

```start-multi-column
ID: ID_8tp4
Number of Columns: 2
Largest Column: standard
border: off
```

> [!todo]+ Today's Tasks
> ```tasks
> not done
> sort by priority
> due today
> hide due date
> hide backlink
> ```

--- column-end ---
> [!warning]+ Overdue
> ```tasks
> not done
> due before today
> ```

=== end-multi-column

```dataviewjs
await dv.view("Dashboard", {pages: "", view: "month", firstDayOfWeek: "1", options: "style1"})
```


# <span class = "color: blue"> All Tasks</span>

```tasks
not done
sort by path
sort by priority
hide due date
hide backlink
```

# <span class = "color: blue">Recent file updates</span>

 `$=dv.list(dv.pages('').sort(f=>f.file.mtime.ts,"desc").limit(5).file.link)`

# <span class = "color: blue">Stats</span>

- File Count: `$=dv.pages().length`


