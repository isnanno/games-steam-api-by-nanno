# 🚀 Upload para GitHub com Git LFS

Script completo para fazer upload de arquivos grandes para o GitHub usando Git LFS.

## 📋 Pré-requisitos

1. **Git instalado** - https://git-scm.com/downloads
2. **Git LFS instalado** - https://git-lfs.github.com/
3. **Python 3.6+** instalado

## 🔧 Instalação do Git LFS

1. Baixe o Git LFS em: https://git-lfs.github.com/
2. Execute o instalador
3. Verifique a instalação:
   ```powershell
   git lfs version
   ```

## 🚀 Como Usar

1. **Abra o PowerShell** na pasta do projeto:
   ```powershell
   cd "C:\Users\Nanno\Downloads\games-steam-api-by-nanno"
   ```

2. **Execute o script**:
   ```powershell
   python upload_com_git_lfs.py
   ```

3. **O script irá**:
   - ✅ Verificar se Git LFS está instalado
   - ✅ Configurar repositório Git (do zero se necessário)
   - ✅ Configurar Git LFS para arquivos .zip
   - ✅ Fazer commits incrementais (20 arquivos por commit)
   - ✅ Fazer push a cada 10 commits
   - ✅ Continuar de onde parou se interrompido

## ⚙️ Configurações

Você pode ajustar no início do arquivo `upload_com_git_lfs.py`:

```python
FILES_PER_COMMIT = 20      # Arquivos por commit (padrão: 20)
COMMITS_PER_PUSH = 10     # Commits antes de fazer push (padrão: 10)
```

## 🔐 Autenticação GitHub

Quando o Git pedir credenciais:
- **Username**: `isnanno`
- **Password**: Seu Personal Access Token (não sua senha)

Para criar um token:
1. Acesse: https://github.com/settings/tokens
2. Clique em "Generate new token (classic)"
3. Selecione a permissão `repo`
4. Copie o token gerado

## 📊 O que o Git LFS faz?

O Git LFS (Large File Storage) armazena arquivos grandes separadamente, mantendo apenas referências no repositório Git. Isso resolve problemas de:
- ✅ Tamanho de push (limite de 2GB)
- ✅ Arquivos individuais grandes (>100MB)
- ✅ Performance do repositório

## ⚠️ Notas Importantes

- O script pode recomeçar do zero se você quiser (apaga histórico Git existente)
- Os arquivos .zip serão automaticamente rastreados pelo Git LFS
- O processo pode levar várias horas com muitos arquivos
- Você pode interromper (Ctrl+C) e continuar depois

## 📧 Contato

Email: nannortx@gmail.com

