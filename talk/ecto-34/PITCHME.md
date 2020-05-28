---?color=#69B739

@snap[midpoint span-100 h1-white]
# Ecto v3.4
@snapend

---

@snap[north span-100]
### Ecto v3.4
@snapend

@ul
- Built-in support to MSSQL via TDS<br>Thanks to the massive effort from @mjaric
- Query language now supports JSON/embed expressions:
- from u in User, where: u.settings["panel_enabled"]
- from u in User, where: u.settings.panel_enabled
@ulend

