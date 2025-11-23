# Site Yolds

Site institucional da **Yolds** - Jovens de Espírito, Sábios de Experiência.

Plataforma digital voltada para o público 60+ no Brasil, oferecendo dicas, eventos, cursos e serviços para quem vive a maturidade com energia.

## 🎨 Identidade Visual

- **Cores**: Azul Petróleo (#008080), Terracota (#E2725B), Dourado (#FFD700)
- **Logo**: Mosaico colorido (Conceito 3)
- **Estilo**: Orgânico e humano, combinando acolhimento com energia

## 📄 Páginas

- **Home**: Apresentação da Yolds e destaques
- **Sobre**: História e missão da plataforma
- **Blog**: Posts com dicas, notícias e inspiração
- **Contato**: Formulário e informações de contato

## 🚀 Deploy no Vercel

### Pré-requisitos

1. Conta no [Vercel](https://vercel.com) (gratuita)
2. Conta no [GitHub](https://github.com) (gratuita)
3. Domínio já registrado no registro.br

### Passo a Passo

#### 1. Criar Repositório no GitHub

1. Acesse [GitHub](https://github.com) e faça login
2. Clique em **"New repository"** (ou **"Novo repositório"**)
3. Preencha:
   - **Repository name**: `yolds-website`
   - **Description**: "Site institucional da Yolds"
   - **Visibility**: Public (ou Private, se preferir)
4. Clique em **"Create repository"**

#### 2. Fazer Upload dos Arquivos

**Opção A - Via Interface Web (mais fácil):**

1. No repositório criado, clique em **"uploading an existing file"**
2. Arraste TODOS os arquivos e pastas do site para a área de upload
3. Escreva uma mensagem: "Primeira versão do site Yolds"
4. Clique em **"Commit changes"**

**Opção B - Via Git (se você tem Git instalado):**

```bash
cd yolds-website
git init
git add .
git commit -m "Primeira versão do site Yolds"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/yolds-website.git
git push -u origin main
```

#### 3. Conectar ao Vercel

1. Acesse [Vercel](https://vercel.com) e faça login
2. Clique em **"Add New..."** → **"Project"**
3. Clique em **"Import Git Repository"**
4. Selecione o repositório **yolds-website**
5. Mantenha as configurações padrão:
   - **Framework Preset**: Other
   - **Root Directory**: ./
   - **Build Command**: (deixe vazio)
   - **Output Directory**: (deixe vazio)
6. Clique em **"Deploy"**

Aguarde alguns minutos. O Vercel irá gerar um link temporário como `yolds-website.vercel.app`.

#### 4. Configurar Domínio Personalizado

1. No painel do Vercel, vá em **Settings** → **Domains**
2. Digite seu domínio: `yolds.com.br`
3. Clique em **"Add"**
4. O Vercel mostrará os registros DNS necessários

#### 5. Configurar DNS no Registro.br

1. Acesse [Registro.br](https://registro.br) e faça login
2. Vá em **"Meus Domínios"** → selecione **yolds.com.br**
3. Clique em **"Editar Zona"** ou **"DNS"**
4. Adicione os registros fornecidos pelo Vercel:

**Para domínio raiz (yolds.com.br):**
```
Tipo: A
Nome: @
Valor: 76.76.21.21
```

**Para www (www.yolds.com.br):**
```
Tipo: CNAME
Nome: www
Valor: cname.vercel-dns.com
```

5. Salve as alterações
6. Aguarde até 48 horas para propagação (geralmente leva 1-2 horas)

#### 6. Configurar Formulário de Contato

O formulário de contato usa o serviço [Formspree](https://formspree.io) (gratuito):

1. Acesse [Formspree](https://formspree.io) e crie uma conta
2. Clique em **"New Form"**
3. Digite o email de destino: `yolds@yolds.com.br`
4. Copie o **Form ID** gerado (exemplo: `abc123xyz`)
5. Edite o arquivo `contato.html` e substitua:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
   Por:
   ```html
   <form action="https://formspree.io/f/abc123xyz" method="POST">
   ```
6. Faça commit e push das alterações no GitHub
7. O Vercel fará deploy automático da atualização

## 📧 Contato

- **Email**: yolds@yolds.com.br
- **Instagram**: [@yolds60](https://instagram.com/yolds60)
- **Facebook**: [/yolds](https://facebook.com/yolds)

## 🔄 Atualizações Futuras

Para adicionar novos posts ao blog ou fazer alterações no site:

1. Edite os arquivos localmente
2. Faça commit e push para o GitHub
3. O Vercel fará deploy automático em alguns minutos

---

**© 2025 Yolds. Todos os direitos reservados.**

