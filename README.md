# Teste-Unit-rio-Jest

## O que preciso saber
Para trabalhar com testes unitários usando Jest, você precisa ter conhecimento básico em JavaScript e compreender os conceitos de testes unitários em geral. Além disso, você precisa saber:

Instalação e configuração do Jest em seu projeto.

Escrita de testes: Jest fornece vários métodos, como describe, it, test, expect, etc., para escrever e executar seus testes.

Asserções: você precisa saber como usar a biblioteca expect para fazer asserções sobre o resultado dos testes.

Mocks: Jest permite que você crie "mocks" para funções externas, o que é útil para testar funções isoladas sem depender de seus componentes externos.

Snapshots: Jest permite que você crie "snapshots" de seus componentes, que podem ser usados para testar se sua saída é consistente.

Execução de testes: você precisa saber como executar seus testes usando o Jest, incluindo como gerar relatórios e cobertura de código.

Em geral, a familiaridade com Jest e a prática de escrever testes irão ajudá-lo a se tornar proficiente em testes unitários com Jest.

Os métodos mais comuns:
describe: usado para agrupar testes relacionados em blocos lógicos. Cada describe pode conter vários it ou test para descrever comportamentos específicos.

it: usado para descrever um comportamento específico que você está testando. É equivalente ao test.

test: usado para descrever um comportamento específico que você está testando. É equivalente ao it.

beforeEach e afterEach: usados para executar código antes ou depois de cada teste. É útil para inicializar ou limpar dados antes ou depois de cada teste.

expect: usado para fazer asserções sobre o resultado dos testes. É a biblioteca central do Jest para verificar se seus testes estão passando ou falhando.

jest.fn: usado para criar mocks de funções. É útil para testar funções isoladas sem depender de seus componentes externos.

Asserções
Aqui estão alguns exemplos de asserções com Jest usando o método expect:

Verificar se um valor é igual a um determinado valor:

test('should return the correct value', () => {
  const result = 2 + 2;
  expect(result).toBe(4);
});
Verificar se um valor é verdadeiro:

test('should return true', () => {
  const result = true;
  expect(result).toBeTruthy();
});
Verificar se um valor é falso:

test('should return false', () => {
  const result = false;
  expect(result).toBeFalsy();
});
Verificar se um valor é null:

test('should return null', () => {
  const result = null;
  expect(result).toBeNull();
});
Verificar se um valor é undefined:

test('should return undefined', () => {
  let result;
  expect(result).toBeUndefined();
});
Verificar se um valor é um determinado tipo:

test('should return a string', () => {
  const result = 'hello, world';
  expect(typeof result).toBe('string');
});
Estes são apenas alguns exemplos básicos de asserções com Jest. Existem muitos outros métodos expect disponíveis, incluindo comparações de objetos, arrays e expressões regulares.

Mocks
Mocks são versões simuladas de objetos, funções ou módulos que você pode usar em seus testes para controlar e prever o comportamento de seu código. Em vez de depender de componentes externos, você pode criar mocks para substituir esses componentes durante os testes.

Aqui está um exemplo de como você pode escrever um mock de uma função usando o Jest:

test('should call the mock function', () => {
  const mockFunction = jest.fn();
  mockFunction();
  expect(mockFunction).toHaveBeenCalled();
});
Neste exemplo, estamos criando uma função mock usando jest.fn() e chamando essa função. Em seguida, usamos expect para verificar se a função mock foi realmente chamada.

Você também pode configurar a função mock para retornar um valor específico quando chamada:

test('should call the mock function with the correct arguments', () => {
  const mockFunction = jest.fn();
  mockFunction.mockReturnValueOnce(42);
  const result = mockFunction();
  expect(result).toBe(42);
  expect(mockFunction).toHaveBeenCalled();
});
