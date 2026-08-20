---
name: sncr_ccir-mcp
description: Skill da REST API do SNCR: Emissão do Certificado de Cadastro do Imóvel Rural (CCIR) na MCP.AI: 1 endpoint em /api/sncr_ccir. SNCR: Emissão do Certificado de Cadastro do Imóvel Rural (CCIR), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# SNCR: Emissão do Certificado de Cadastro do Imóvel Rural (CCIR) — REST API skill

Você tem acesso à **SNCR: Emissão do Certificado de Cadastro do Imóvel Rural (CCIR)** REST API na MCP.AI.

> SNCR: Emissão do Certificado de Cadastro do Imóvel Rural (CCIR), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/sncr_ccir
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/sncr_ccir/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"codigo_imovel":"...","uf_sede":"...","municipio_sede":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/sncr_ccir/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `sncr_ccir_consultar`

SNCR: Emissão do Certificado de Cadastro do Imóvel Rural (CCIR), consulta em fonte oficial. _(POST /api/sncr_ccir/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `codigo_imovel` | string | Sim | Parâmetro de consulta "codigo_imovel". |
| `uf_sede` | string | Sim | Parâmetro de consulta "uf_sede". |
| `municipio_sede` | string | Sim | Parâmetro de consulta "municipio_sede". |
| `cpf_titular` | string | Não | Parâmetro de consulta "cpf_titular". |
| `cnpj_titular` | string | Não | Parâmetro de consulta "cnpj_titular". |
| `natureza_juridica` | string | Não | Parâmetro de consulta "natureza_juridica". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_sncr_ccir` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
