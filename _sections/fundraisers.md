---
title: Fundraisers
order: 4
---

<div class="text-left">
{% assign model = site.data.api.fundraisers %}
{% for endpoint in model.endpoints %}
  <div class="endpoint">
    <div class="descriptions">
      <h3>{{ endpoint.header }}</h3>
      <p class="endpoint-description">{{ endpoint.description }}</p>

      <div class="argument-list">
        <h5>Arguments</h5>
        {% if endpoint.args %}
        <table>
          {% for arg in endpoint.args %}
            <tr>
              <td class="text-right">
                <p>{{ arg.name }}</p>
                <code class="arg-type">{{ arg.type }}</code>
              </td>
              <td>{{ arg.description }}</td>
            </tr>
          {% endfor %}
        </table>
        {% else %}
        No Arguments
        {% endif %}
      </div>
    </div>
    <div class="code">
      <h4>Example request</h4>
      <pre>{{ endpoint.example_request }}</pre>

      <h4>Example response</h4>
      <pre>
{{ endpoint.example_response }}
      </pre>
    </div>
  </div>
{% endfor %}
</div>
