# A2VISSION
## Equipo de cuantificación

Equipo de subagentes de Claude Code para análisis cuantitativo, definido en [`.claude/agents/`](.claude/agents/):

| Agente | Rol |
|---|---|
| `quant-lead` | Coordina al equipo, revisa críticamente y redacta el informe final. |
| `quant-data-engineer` | Obtiene, limpia y valida los datos (point-in-time, sin survivorship bias). |
| `quant-researcher` | Hipótesis, señales/factores y análisis estadístico. |
| `quant-backtester` | Backtests realistas con costes y validación fuera de muestra. |
| `quant-risk-manager` | Métricas de riesgo, stress tests, sizing y límites. |

### Uso
Pide a Claude Code, por ejemplo:

> Usa el agente quant-lead para evaluar una estrategia de momentum 12-1 sobre las acciones del S&P 500.

El `quant-lead` delegará en el resto y dejará el informe en `reports/`.

### Estructura de trabajo
```
data/raw/          datos crudos
data/processed/    datos limpios (Parquet)
quant/             código (data, research, backtest, risk)
reports/           informes y figuras
tests/             tests (incluido detección de look-ahead)
```

> Aviso: análisis con fines educativos y de investigación; no constituye asesoramiento financiero.
