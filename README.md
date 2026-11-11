# Rebeca Oliveira · Massoterapeuta

Aplicativo web profissional, instalável no celular, para controlar agenda, clientes, anotações e carteira financeira da Rebeca Oliveira.

## Como executar com Live Server

1. Abra esta pasta no VS Code.
2. Clique com o botão direito em `index.html`.
3. Escolha **Open with Live Server**.
4. Acesse o endereço local exibido pelo VS Code.

Não abra o arquivo com duplo clique (`file://`), porque PWA e armazenamento local funcionam corretamente em `localhost`/Live Server ou HTTPS.

## Funcionalidades

- **Agenda como tela principal:** calendário mensal, horários, clientes, valor, tipo de massagem, anotações do atendimento e status concluído.
- **Clientes:** cadastro de nome, telefone e anotações permanentes; a ficha pode ser editada e permanece salva no aparelho.
- **Ranking:** lista automática das clientes que mais visitam o salão, baseada no número de atendimentos.
- **Carteira separada:** fica em sua própria tela e só aparece ao clicar em Carteira; registra entradas e saídas e calcula o saldo do mês. Ao marcar um atendimento como concluído, o valor é lançado automaticamente como entrada no faturamento e na carteira. Ao reabrir, o lançamento automático é removido sem duplicar valores.
- **PWA:** possui botão visível “Instalar no celular”, pode ser instalado na tela inicial do Android/iPhone e possui cache offline. No iPhone, use Compartilhar → Adicionar à Tela de Início.
- **Migração automática:** os agendamentos da versão anterior são convertidos em clientes automaticamente na primeira abertura da versão nova.

## Publicar no GitHub Pages

```bash
git init
git add .
git commit -m "feat: agenda profissional da Rebeca Oliveira"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
git push -u origin main
```

Depois, no GitHub, abra **Settings > Pages**, escolha **Deploy from a branch**, selecione `main` e `/ (root)`, e salve.

## Observações sobre os dados

O banco de dados é local ao navegador usando `localStorage`. Isso significa que as informações não são enviadas para um servidor e não sincronizam entre aparelhos. Os dados ficam preservados enquanto o armazenamento do navegador não for apagado. Para ter sincronização, login e backup em nuvem, será necessário conectar um banco online em uma próxima etapa.
