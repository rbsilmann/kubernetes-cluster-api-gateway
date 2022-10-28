# Objetivo
Criar um cluster kubernetes para microsserviços utilizando o Kong como API Gateway e Proxy Reverso.

## Ordem de execução
Inicialmente você deve aplicar as configurações na seguinte ordem:
1. kubectl apply -f configmaps/
2. kubectl apply -f secrets/
3. kubectl apply -f services/
4. kubectl apply -f statefulsets/
5. Aplicar os jobs 01, 02, 03 e 04
6. kubectl apply -f deployments/
7. kubectl apply -f horizontalpodautoscalings/
8. Aplicar os jobs 05 e 06
9. Após isso você já tera a API Admin a sua disposição no endpoint /admin-api, caso queira adicionar a segurança via key-auth siga as orientações no diretório admin-api-key-auth.