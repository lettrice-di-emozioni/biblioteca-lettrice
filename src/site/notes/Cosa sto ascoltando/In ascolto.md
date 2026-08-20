---
{"dg-publish":true,"permalink":"/cosa-sto-ascoltando/in-ascolto/","dg-note-properties":{}}
---

![Cosa sto ascoltando/Sophisticated Header Design with Moon and Stars (1) 1.png](/img/user/Cosa%20sto%20ascoltando/Sophisticated%20Header%20Design%20with%20Moon%20and%20Stars%20(1)%201.png)

```dataviewjs
const audiolibri = [
  dv.page("Cosa sto ascoltando/audiolibro Theo da Golden e la forma della felicità")
  // aggiungi qui altri con dv.page("audiolibri/nome nota")
];

for (let libro of audiolibri) {
  if (!libro) continue;
  const perc = Number(libro.percentuale_ascolto) || 0;
  const piene = Math.round(perc / 10);
  const barra = "█".repeat(piene) + "░".repeat(10 - piene);
  const finito = perc >= 100 ? " ✅" : "";

  dv.header(2, libro.Titolo ?? libro.titolo ?? libro.file.name);
  dv.paragraph(`🎧 ${barra} ${perc}%${finito}`);
  dv.paragraph("---");
}