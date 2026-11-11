# 🐾 Vet & Pet API - Gestão de Animais

API RESTful para registo, consulta e gestão de animais em clínicas veterinárias e centros de adoção.

## 📸 Animais Registados

| Lhasa Apso | Rato | 
| ----- | ----- | 
| <img src="https://purina.com.br/artigos/cuidado-bem-estar/quais-as-principais-caracteristicas-do-filhote-lhasa-apso" width="200"/> | <img src="https://www.amazon.com.br/Bandeira-careca-quatro-ilh%C3%B3s-lat%C3%A3o/dp/B0DNTKM2P9" width="200"/> | 
| **Porte:** Pequeno \| **Personalidade:** Legal | **Porte:** Médio \| **Personalidade:** Retardado | 

## 📌 Modelo de Dados (Schema JSON)

Cada objeto de animal retornado ou enviado para a API segue esta estrutura:

| Campo | Tipo | Obrigatório | Descrição | 
| ----- | ----- | ----- | ----- | 
| `nome` | `string` | Não | Nome atribuído ao animal (ex: *"Rato"*) | 
| `especie` | `string` | **Sim** | Espécie do animal (ex: *"Cachorro"*, *"Gato"*, *"Outro"*) | 
| `raca` | `string` | **Sim** | Raça do animal (ex: *"Lhasa Apso"*, *"Seboso"*) | 
| `idade` | `number` | **Sim** | Idade estimada do animal em anos | 
| `sexo` | `string` | **Sim** | Sexo do animal (`"Macho"` ou `"Fêmea"`) | 
| `porte` | `string` | **Sim** | Porte físico (`"Pequeno"`, `"Médio"`, `"Grande"`) | 
| `personalidade` | `string` | **Sim** | Descrição simples do comportamento | 
| `foto` | `string` | **Sim** | URL de imagem representativa do animal | 
| `disponivel` | `boolean` | **Sim** | Status para atendimento/adoção (`true` / `false`) | 

## 📡 Endpoints Principais

### `GET /pets`

Retorna a lista completa de animais registados no sistema.

**Exemplo de Resposta (`200 OK`):**

```json
[
  {
    "especie": "Cachorro",
    "raca": "Lhasa Apso",
    "idade": 10,
    "sexo": "Macho",
    "porte": "Pequeno",
    "personalidade": "legal",
    "foto": "https://purina.com.br/artigos/cuidado-bem-estar/quais-as-principais-caracteristicas-do-filhote-lhasa-apso",
    "disponivel": true
  },
  {
    "nome": "Rato",
    "especie": "Outro",
    "raca": "Seboso",
    "idade": 20,
    "sexo": "Macho",
    "porte": "Médio",
    "personalidade": "Retardado",
    "foto": "https://www.amazon.com.br/Bandeira-careca-quatro-ilh%C3%B3s-lat%C3%A3o/dp/B0DNTKM2P9",
    "disponivel": true
  }
]
```

## 💻 Como Executar o Projeto

1. **Clonar o repositório:**
   ```bash
   git clone https://github.com/teu-usuario/vet-api.git
   cd vet-api
   ```

2. **Instalar as dependências:**
   ```bash
   npm install
   ```

3. **Iniciar o servidor:**
   ```bash
   npm start
   ```