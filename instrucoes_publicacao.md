# Instruções para Publicação do Site B2F Digital no GitHub

Este documento contém instruções detalhadas para publicar o site da B2F Digital no GitHub Pages e conectá-lo ao seu domínio personalizado.

## Pré-requisitos

- Uma conta no GitHub (gratuita)
- Acesso ao painel de controle do seu domínio (b2fdigital.com)
- Os arquivos do site (fornecidos neste pacote)

## Passo 1: Criar um Repositório no GitHub

1. Acesse [GitHub](https://github.com/) e faça login na sua conta
2. Clique no botão "+" no canto superior direito e selecione "New repository"
3. Nomeie o repositório como `b2fdigital.github.io` (ou outro nome de sua preferência)
4. Deixe o repositório como "Public"
5. Marque a opção "Add a README file" (opcional)
6. Clique em "Create repository"

## Passo 2: Fazer Upload dos Arquivos do Site

### Opção 1: Usando a Interface Web do GitHub

1. No seu repositório, clique no botão "Add file" e selecione "Upload files"
2. Arraste todos os arquivos e pastas do site para a área de upload
3. Adicione uma mensagem de commit como "Initial website upload"
4. Clique em "Commit changes"

### Opção 2: Usando Git (para usuários avançados)

1. Clone o repositório para sua máquina local:
   ```
   git clone https://github.com/seu-usuario/b2fdigital.github.io.git
   ```
2. Copie todos os arquivos do site para a pasta do repositório
3. Adicione, faça commit e push dos arquivos:
   ```
   git add .
   git commit -m "Initial website upload"
   git push origin main
   ```

## Passo 3: Configurar o GitHub Pages

1. No seu repositório, vá para "Settings" (aba de configurações)
2. No menu lateral esquerdo, clique em "Pages"
3. Em "Source", selecione "Deploy from a branch"
4. Em "Branch", selecione "main" e "/root" e clique em "Save"
5. Aguarde alguns minutos para que o site seja publicado

## Passo 4: Configurar o Domínio Personalizado

### No GitHub:

1. Ainda na seção "Pages" das configurações do repositório
2. Em "Custom domain", digite `b2fdigital.com` e clique em "Save"
3. Marque a opção "Enforce HTTPS" (recomendado para segurança)

### No seu Provedor de Domínio:

1. Acesse o painel de controle do seu domínio
2. Vá para a seção de gerenciamento de DNS
3. Configure os seguintes registros:

   **Opção A: Usando registros A**
   
   Adicione quatro registros A apontando para os IPs do GitHub Pages:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
   
   **Opção B: Usando registro CNAME**
   
   Adicione um registro CNAME:
   - Nome: www
   - Valor: seu-usuario.github.io
   
   E um redirecionamento do domínio raiz para www.b2fdigital.com

4. Aguarde a propagação do DNS (pode levar até 48 horas)

## Passo 5: Verificar a Publicação

1. Após a propagação do DNS, acesse `b2fdigital.com` no navegador
2. Verifique se o site está funcionando corretamente
3. Teste a navegação entre as páginas e o formulário de contato

## Solução de Problemas

- **Site não aparece após configuração**: Aguarde a propagação do DNS (até 48 horas)
- **Erro 404**: Verifique se os arquivos foram carregados corretamente no repositório
- **Problemas com HTTPS**: Certifique-se de que a opção "Enforce HTTPS" está marcada nas configurações do GitHub Pages

## Manutenção do Site

Para atualizar o site no futuro:

1. Faça as alterações necessárias nos arquivos
2. Faça upload das alterações para o repositório (usando a interface web ou Git)
3. O GitHub Pages atualizará automaticamente o site em alguns minutos

## Suporte

Se precisar de ajuda adicional, consulte a [documentação oficial do GitHub Pages](https://docs.github.com/en/pages) ou entre em contato com o suporte do seu provedor de domínio para questões relacionadas à configuração de DNS.
