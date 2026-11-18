# COI Campo – Apontamento e despacho das equipes

## Arquivos
| Arquivo | Para quê |
|---|---|
| `index.html` | Página inicial com os dois acessos |
| `campo.html` | App da equipe (celular). Pode ser instalado na tela inicial |
| `backoffice.html` | Backoffice dos programadores (computador) |
| `manifest.json`, `sw.js`, `icone-*.png` | Instalação como app e funcionamento sem sinal |

Os dados ficam no Supabase "Analise Ordem de Servico", em tabelas próprias com prefixo `ap_`. Os painéis atuais não foram alterados.

## Publicar no GitHub Pages (uma vez, cerca de 10 min)
1. Crie uma conta em github.com (pode ser com o e-mail corporativo).
2. Clique em **New repository**. Nome: `coi-campo`. Marque **Public** e clique em **Create repository**.
3. Clique em **uploading an existing file**, arraste **todos** os arquivos desta pasta e clique em **Commit changes**.
4. Vá em **Settings → Pages**. Em *Branch*, escolha `main` e `/ (root)` e clique em **Save**.
5. Em 1–2 minutos aparece o endereço: `https://SEU-USUARIO.github.io/coi-campo/`.
   - App da equipe: `.../coi-campo/campo.html`
   - Backoffice: `.../coi-campo/backoffice.html`

Para atualizar depois, envie os arquivos novos no mesmo repositório. Os celulares pegam a versão nova sozinhos.

> O repositório público expõe só o código das páginas. Os dados ficam protegidos no Supabase: tudo passa por funções que exigem o login da equipe ou do portal COI.

## Primeiro uso
1. **Backoffice:** entre com o login do portal COI. O e-mail do Adriel já está habilitado como programador.
2. **Cadastros → + Nova equipe:** código (ex.: `HJ-01`), nome, tipo, unidade, placa e senha da equipe.
3. **Cadastros → Programadores que editam:** com a senha de administrador do portal, marque quem pode despachar e ajustar.
4. **No celular do veículo:** abra o link do app, escolha a equipe e digite a senha.
   - **Android/Chrome:** menu ⋮ → **Adicionar à tela inicial**.
   - **iPhone/Safari:** Compartilhar → **Adicionar à Tela de Início**.
5. Aceite a permissão de **localização** quando o celular pedir.

## Como a equipe usa (resumo para o DDS)
- **Início do turno:** confirmar integrantes, placa e km.
- **Durante o dia:** tocar no que a equipe está fazendo agora. Ao tocar numa atividade nova, a anterior fecha sozinha. Não precisa "parar" uma para começar outra.
- **Tarefa do COI:** Aceitar → Iniciar deslocamento → Cheguei, iniciar serviço → Concluir serviço.
- **Sem sinal:** pode continuar apontando normalmente. O app guarda e envia quando o sinal voltar (aparece "Sem sinal · N").
- **Fim do turno:** Meu dia → Encerrar turno.
- **Dica:** no menu ⋮, use **Manter tela ligada** quando o celular estiver no suporte do veículo. Assim o GPS segue atualizando o mapa.

## Limites conhecidos
- Um app web só envia GPS com o app aberto na tela. Com a tela apagada, o mapa mostra a última posição e marca "sem sinal" depois de 10 minutos.
- O mapa usa OpenStreetMap e precisa de internet no computador do backoffice.
- As posições de GPS crescem cerca de 1 MB por equipe por mês. Revise a retenção depois de alguns meses.
