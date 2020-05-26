## Endpoint

##### Modelo veículo

```json
{
  "id": "1",
  "plate": "ABC-1234",
  "model": "Class C 1.1 Avantgarde Turbo Flex ",
  "manufacturer": "Mercedes-Benz",
  "color": "black",
  "status": true
}
``` 

### Api completa

`/vehicle?page=1&limit=10` Lista veiculos paginados

`/vehicle?filter=ABC4852` Busca veículo pela placa

`/vehicle?filter=true` Lista veículos pelo status

`/vehicle/:id` Busca um veículo específico

`/vehicle` Cria um novo veículo

`/vehicle/:id` Atualiza um veículo

`/vehicle/:id` Remove um veículo

### Regras de negócio

- A busca por placa `/vehicle?filter=ABC4852` não pode conter caracteres especiais (hífen, ponto, etc...)
- A criação de um novo veículo deve validar se placa já existe
- A atualização do veículo NÃO deve atualizar a placa, o ideal é que sejá feita a validação no front(bloqueando o campo) e no back(devolvendo erro)
- Use os VERBOS que achar adequado para o endpoint