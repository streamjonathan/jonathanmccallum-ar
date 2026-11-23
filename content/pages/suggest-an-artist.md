---
title: "اقترح فنانًا"
slug: suggest-an-artist
---

يسعدني كثيرًا أن أسمع عن موسيقيين وفنانين يتبعون يسوع. إذا كنت تعرف شخصًا تريد أن أكتب عنه أو أجري معه مقابلة أو أصوّر فيديو تفاعليًا عنه، فأخبرني هنا.

الاسم ورابط يكفيان — وبضع كلمات عن السبب. أقرأ كل ما يصلني. شكرًا جزيلًا.

هل تعرف أحد هؤلاء؟ المس الصورة وسيُملأ النموذج تلقائيًا — ثم أضف بضع كلمات عن السبب وأرسل.

<div class="suggest-carousel" role="list" aria-label="موسيقيون وفنانون يمكنك اقتراحهم">
{% for artist in suggest_carousel %}
  <button type="button" class="suggest-pick" role="listitem" data-artist="{{ artist.name }}" data-link="{{ artist.profile }}" title="اقترح {{ artist.name }}">
    <img src="{{ artist.img }}" alt="{{ artist.name }}" loading="lazy" width="150" height="150">
    <span class="suggest-pick__name">{{ artist.name }}</span>
    <span class="suggest-pick__note">{{ artist.note }}</span>
  </button>
{% endfor %}
</div>

<p class="suggest-carousel__more">أو اقترح شخصًا جديدًا أدناه — أي شخص تظن أن عليّ أن أسمع عنه.</p>

هذا الموقع ليس لمن هم دون سن الثامنة عشرة.

<form id="suggest-form" class="suggest-form">
  <label for="suggest-artist">اسم الفنان</label>
  <input id="suggest-artist" name="artist" type="text" maxlength="200" placeholder="من الذي عليّ أن أطّلع عليه؟" required>

  <label for="suggest-link">رابط الملف الشخصي على وسائل التواصل الاجتماعي</label>
  <input id="suggest-link" name="link" type="url" maxlength="500" placeholder="https://www.instagram.com/…" required>

  <fieldset class="suggest-kinds">
    <legend>ماذا أفعل معهم؟</legend>
    <label><input type="checkbox" name="kind" value="write"> أكتب عنه</label>
    <label><input type="checkbox" name="kind" value="interview"> أجري مقابلة معه</label>
    <label><input type="checkbox" name="kind" value="reaction"> أصوّر فيديو تفاعليًا عنه</label>
  </fieldset>

  <label for="suggest-why">لماذا هو؟</label>
  <textarea id="suggest-why" name="why" rows="3" maxlength="500" placeholder="بضع كلمات تكفي…"></textarea>

  <label for="suggest-name">اسمك <span class="optional">(اختياري)</span></label>
  <input id="suggest-name" name="fromName" type="text" maxlength="100" placeholder="لكي أتمكن من شكرك">

  <label for="suggest-from-link">رابط ملفك الشخصي على وسائل التواصل الاجتماعي <span class="optional">(اختياري)</span></label>
  <input id="suggest-from-link" name="fromLink" type="url" maxlength="500" placeholder="https://www.instagram.com/…">

  <button id="suggest-button" type="button">أرسل الاقتراح</button>

  <p id="suggest-result" aria-live="polite"></p>
</form>
