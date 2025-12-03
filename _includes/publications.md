<h2 id="publications" style="margin: 2px 0 -10px;">Publications</h2>

<ol class="publications-list">
{% for link in site.data.publications.main %}
  <li>
    <div class="pub-row">
      <div class="title">
        <a href="{{ link.pdf }}">{{ link.title }}</a>
        {% if link.notes %}
          <span class="notes">({{ link.notes }})</span>
        {% endif %}
      </div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>
      <div class="links">
        {% if link.pdf %}
        <a href="{{ link.pdf }}" class="btn" target="_blank">PDF</a>
        {% endif %}
        {% if link.code %}
        <a href="{{ link.code }}" class="btn" target="_blank">Code</a>
        {% endif %}
        {% if link.page %}
        <a href="{{ link.page }}" class="btn" target="_blank">Project Page</a>
        {% endif %}
        {% if link.bibtex %}
        <a href="{{ link.bibtex }}" class="btn" target="_blank">BibTex</a>
        {% endif %}
      </div>
    </div>
  </li>
{% endfor %}
</ol>
