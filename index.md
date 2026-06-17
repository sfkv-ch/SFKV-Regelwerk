Willkommen im Regelwerk der SFKV
Diese Plattform ist in Arbeit. Aktuell sind die hier publizierten Regeln inoffiziell.

**Die gültigen Dokumente sind auf** **[www.sfkv.ch](https://www.sfkv.ch/archiv/richtlinien)** **publiziert.**

---

{% assign groups = "Leitbild,Statuten,Reglemente,Richtlinien" | split: "," %}

{% for group in groups %}

## {{ group }}

{% assign docs = site.docs
| where: "group", group
| sort: "title" %}

{% for doc in docs %}

- [{{ doc.shorttitle | default: doc.title }}]({{ site.baseurl }}{{ doc.url }})  
  {{ doc.description }}

{% endfor %}

{% endfor %}

---

## ℹ️ Debug / Tests

### 📦 Anzahl Docs in Collection
{{ site.docs | size }}

---

### 📄 Alle Docs URLs
{% for doc in site.docs %}
- {{ doc.name }} → {{ doc.url }}
{% endfor %}

---

### 🧪 Rohdaten (wichtige Felder)
{% for doc in site.docs %}
- title: {{ doc.title }}
  group: {{ doc.group }}
  path: {{ doc.path }}
{% endfor %}

---

## ℹ️ Hinweis

Alle Dokumente werden zentral gepflegt und automatisch aus dem internen Repository synchronisiert.

Die jeweils aktuelle Version ist verbindlich.
