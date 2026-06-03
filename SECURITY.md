# Política de Segurança 🔐

## Versões Suportadas

O **Desapega Senac** é um projeto acadêmico em desenvolvimento ativo. Atualmente, apenas a versão mais recente recebe correções de segurança.

| Versão | Suportada |
|--------|-----------|
| 1.0.x (atual) | ✅ |
| < 1.0 | ❌ |

---

## Reportando uma Vulnerabilidade

Se você identificou uma vulnerabilidade de segurança no **Desapega Senac**, pedimos que siga as orientações abaixo antes de divulgar publicamente.

### Como reportar

**Não abra uma issue pública** para relatar vulnerabilidades. Entre em contato de forma privada pelo e-mail:

📧 **[contato@email.com](mailto:contato@email.com)**

Inclua no e-mail as seguintes informações:

- Descrição clara da vulnerabilidade encontrada
- Passos para reproduzir o problema
- Impacto potencial (ex: acesso não autorizado a dados, bypass de autenticação)
- Ambiente em que foi identificada (versão do PHP, sistema operacional, etc.)

### O que esperar após o reporte

| Etapa | Prazo estimado |
|-------|----------------|
| Confirmação de recebimento | Até 3 dias úteis |
| Avaliação inicial da vulnerabilidade | Até 7 dias úteis |
| Retorno com posicionamento (aceita ou recusada) | Até 14 dias úteis |
| Correção aplicada (se confirmada) | Até 30 dias úteis |

### Após a análise

- **Vulnerabilidade confirmada:** será corrigida na próxima versão e você será creditado na release, se desejar.
- **Vulnerabilidade recusada:** você receberá uma explicação detalhada do motivo.

---

## Boas Práticas Adotadas no Projeto

- Todas as queries ao banco utilizam **PDO com Prepared Statements**, prevenindo SQL Injection.
- A API possui configuração de **CORS** para restringir origens não autorizadas.
- Senhas são tratadas com funções seguras de hash antes de serem armazenadas.
- Operações sensíveis exigem **autenticação válida** antes de serem executadas.

---

> Este projeto foi desenvolvido com fins acadêmicos no Senac. Agradecemos qualquer contribuição que ajude a torná-lo mais seguro. 🙏
