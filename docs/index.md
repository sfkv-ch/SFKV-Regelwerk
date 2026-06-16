Willkommen im Regelwerk der SFKV.

Diese Plattform ist in Arbeit. Aktuell sind die hier publizierten Regeln inoffiziell.

**Die gültigen Dokumente sind auf [www.sfkv.ch](https://www.sfkv.ch/archiv/richtlinien) publiziert.**

{{ site.time }}

---

{% assign groups = "Leitbild,Statuten,Reglemente,Richtlinien" | split: "," %}

{% for group in groups %}

{{ group }}

{% assign docs = site.pages
| where: "groupe", group
| sort: "title" %}

{% for doc in docs %}

[{{ doc.shorttitle | default: doc.title }}]({{ doc.url }})
{{ doc.description }}
{% endfor %}

{% endfor %}

---

## ℹ️ Hinweis

Alle Dokumente werden zentral gepflegt und automatisch aus dem internen Repository synchronisiert.

Die jeweils aktuelle Version ist verbindlich.
