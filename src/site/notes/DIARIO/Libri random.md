---
{"dg-publish":true,"permalink":"/diario/libri-random/","dg-note-properties":{}}
---

<div class="libro-momento">

<div class="lm-item" data-quote="«la tua citazione qui»" data-title="Titolo libro 1">
![[copertina1.jpg\|copertina1.jpg]]
</div>

<div class="lm-item" data-quote="«altra citazione»" data-title="Titolo libro 2">
![[copertina2.jpg\|copertina2.jpg]]
</div>

</div>



<div class="libro-momento">

<div class="lm-item" data-quote="«la tua citazione qui»" data-title="Titolo del libro">
![[copertina1.jpg\|copertina1.jpg]]
</div>

<div class="lm-item" data-quote="«altra citazione qui»" data-title="Altro titolo">
![[copertina2.jpg\|copertina2.jpg]]
</div>

</div>

<script>
(function() {
  const items = document.querySelectorAll('.lm-item');
  if (items.length === 0) return;
  const chosen = items[Math.floor(Math.random() * items.length)];
  chosen.classList.add('lm-visible');
  const titleEl = document.createElement('p');
  titleEl.className = 'lm-title';
  titleEl.innerText = chosen.dataset.title;
  const quoteEl = document.createElement('p');
  quoteEl.className = 'lm-quote';
  quoteEl.innerText = chosen.dataset.quote;
  chosen.appendChild(titleEl);
  chosen.appendChild(quoteEl);
})();
</script>