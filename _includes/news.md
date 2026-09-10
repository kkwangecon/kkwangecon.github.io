<h1 id="news"></h1>

<h2 style="margin: 30px 0px 10px;">Upcoming</h2>

<ul id="upcoming-list">
  <li data-until="2026-10-08">
    <strong>[Oct. 8]</strong>
    <a href="https://sites.google.com/view/hitotsubashi-trade-urban-econ/">Hitotsubashi Trade/Urban Economics Workshop</a>, Tokyo
  </li>
  <li data-until="2026-10-05">
    <strong>[Oct. 5]</strong>
    <a href="https://sites.google.com/view/j-tree/english">Japan-Tokyo Resource and Environmental Economics(J-TREE) International Workshop</a>, Tokyo
  </li>
  <li data-until="2026-09-26">
    <strong>[Sep. 25&ndash;26]</strong>
    <a href="https://urbaneconomics.org/meetings/uea2026/">20th North American Meeting of the Urban Economics Association</a>, Chicago
  </li>
</ul>

<script>
// Each item carries data-until="YYYY-MM-DD", the last day of the event.
// Past that date the item hides itself; when none are left, so does the section.
(function () {
  var list = document.getElementById('upcoming-list');
  if (!list) return;
  var today = new Date().toISOString().slice(0, 10);
  var live = 0;
  Array.prototype.forEach.call(list.querySelectorAll('li[data-until]'), function (li) {
    if (li.getAttribute('data-until') < today) { li.style.display = 'none'; } else { live++; }
  });
  if (live === 0) {
    list.style.display = 'none';
    var h = list.previousElementSibling;
    if (h && h.tagName === 'H2') h.style.display = 'none';
  }
})();
</script>
