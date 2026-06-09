# Guia de Contribuição

Obrigado por contribuir com o **IA Mentor de Carreira**.

## 1. Faça um fork

1. Acesse o repositório no GitHub.
2. Clique em **Fork** para criar uma cópia na sua conta.
3. Clone seu fork localmente:
   ```bash
   git clone git@github.com:SEU-USUARIO/ia-mentor-carreira.git
   cd ia-mentor-carreira
   ```

## 2. Crie uma branch

Crie uma branch descritiva a partir da `main`:
```bash
git checkout main
git pull origin main
git checkout -b feat/nome-da-mudanca
```

## 3. Faça commits objetivos

Use mensagens no padrão Conventional Commits:
```text
feat: adiciona roadmap de 90 dias
fix: corrige seção de pré-entrevista
docs: melhora instruções de uso
```

## 4. Envie para seu fork

```bash
git add .
git commit -m "feat: sua alteração"
git push -u origin feat/nome-da-mudanca
```

## 5. Abra um Pull Request

1. Vá ao seu fork no GitHub.
2. Clique em **Compare & pull request**.
3. Explique o contexto, mudanças e como validar.
4. Aguarde revisão.

## Boas práticas

- Faça mudanças pequenas e focadas.
- Atualize documentação quando necessário.
- Evite commits com arquivos temporários ou segredos.
- Garanta que o conteúdo esteja claro e em português.

