# Hi there 👋, I'm Daniel Costa dos Santos

* 🌎 **Location:** Natal/RN – Brazil
* 💡 **I am a dedicated technology enthusiast with a strong passion for automation and data analysis. I enjoy acquiring proficiency in new tools and translating complex challenges into intelligent, actionable solutions.**
* 🔍 **Python, Selenium, Pytest e Web Scraping.**

<div align="left">

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=DanielCostadosSantos\&layout=compact\&theme=tokyonight)

</div>

### Skills

<p align="left">
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="45" height="45"/>
  <img src="https://upload.wikimedia.org/wikipedia/commons/d/d5/Selenium_Logo.png" alt="selenium" width="45" height="45"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pytest/pytest-original.svg" alt="pytest" width="45" height="45"/>
  <img src="https://cdn.jsdelivr.net/gh/simple-icons/simple-icons/icons/microsoftoffice.svg" alt="microsoft office" width="45" height="45"/>
  <img src="https://upload.wikimedia.org/wikipedia/commons/c/cf/New_Power_BI_Logo.svg" alt="power bi" width="45" height="45"/>
  <!-- Added HTML and CSS logos -->
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg" alt="html5" width="45" height="45"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg" alt="css3" width="45" height="45"/>
</p>

---

### 🌐 Connect with me

<p align="left">
  <a href="https://www.linkedin.com/in/danielcsnts/" target="_blank">
    <img align="center" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" alt="LinkedIn" height="40" width="40" />
  </a>
  <a href="mailto:danielcsnts.contato@gmail.com">
    <img align="center" src="https://cdn-icons-png.flaticon.com/512/281/281769.png" alt="Email" height="40" width="40" />
  </a>
</p>

From [Daniel Costa dos Santos](https://github.com/DanielCostadosSantos)

---

## Que foi alterado

* Adicionei as logos de **HTML5** e **CSS3** na seção de Skills (ícones SVG públicos).
* Mantive o badge `Top Langs` que já mostra as linguagens do seu repositório automaticamente.

## Mostrar percentuais de HTML e CSS do seu repositório

O badge `Top Langs` ([https://github-readme-stats.vercel.app](https://github-readme-stats.vercel.app)) mostra um gráfico compacto das linguagens, mas se você quer exibir explicitamente os percentuais de **HTML** e **CSS** no próprio README (por exemplo: `HTML — 12.3% | CSS — 5.8%`), você pode usar a GitHub Languages API e gerar automaticamente um fragmento Markdown.

Abaixo segue um pequeno script Python que busca os dados de linguagens do seu repositório e imprime um bloco Markdown com ícones e percentuais. Copie e rode no seu ambiente (ou configure como workflow do GitHub Actions para atualizar automaticamente).

```python
# requirements: requests
# pip install requests

import requests
from urllib.parse import quote

OWNER = "DanielCostadosSantos"
REPO = "<nome-do-repositorio>"  # substitua pelo repo alvo

url = f"https://api.github.com/repos/{OWNER}/{REPO}/languages"
resp = requests.get(url)
resp.raise_for_status()
langs = resp.json()  # dicionário: {"Python": 12345, "HTML": 6789, ...}

total = sum(langs.values()) or 1
percent = {k: (v / total) * 100 for k, v in langs.items()}

# Pegar HTML e CSS (0 se não existir)
html_pct = percent.get('HTML', 0.0)
css_pct = percent.get('CSS', 0.0)

md = (
    f"### Language breakdown for `{OWNER}/{REPO}`\n\n"
    f"<img src=\"https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg\" alt=\"html5\" width=\"20\"/>"
    f" **HTML** — {html_pct:.1f}%  \n"
    f"<img src=\"https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg\" alt=\"css3\" width=\"20\"/>"
    f" **CSS** — {css_pct:.1f}%  \n"
)

print(md)
```

**Exemplo de saída (fictício):**

```
### Language breakdown for `DanielCostadosSantos/meu-repo`

<img src=".../html5-original.svg" alt="html5" width="20"/> **HTML** — 12.3%  
<img src=".../css3-original.svg" alt="css3" width="20"/> **CSS** — 5.8%  
```

### Automatizar (opcional)

* Você pode transformar esse script em um GitHub Action que atualiza um arquivo `_LANGS.md` no repositório a cada push — dessa forma o README pode incluir `<!-- include: _LANGS.md -->` (ou você pode copiar o conteúdo gerado para o README diretamente).

---

Se quiser, eu posso:

* Gerar o fragmento pronto usando um repo específico (me diga o nome do repo) — eu já te mostro o texto pronto para colar no README.
* Criar o GitHub Action completo que atualiza automaticamente o breakdown no repo.

