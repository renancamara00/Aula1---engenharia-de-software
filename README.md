```mermaid
 sequenceDiagram
  participant U as Usuário
  participant A as APP
  participant B as BackEnd
  participant D as Banco de dados

  U->>A: Endereço
  A->>A: GPS(Coordenadas)
  A->>+B: Endereço(cook, userID)
  B->>+D: Buscar 10 ruas e números userID
  D-->>B: Endereços
  Note over B: Calcula distancia
  B-->>A: Lista de endereço mais distancia
  A-->>U: Exibe lista de endereços com km
  
