# Encontrar valores duplicados em uma coluna

A fórmula abaixo retorna uma lista de valores que estão duplicados em uma coluna. 
Para usar basta definir a referência de células para a variável "valores".

=LET(
    valores;A1:A5;
    valores_distintos;ÚNICO(valores);
    valores_unicos;ÚNICO(valores;;VERDADEIRO);
    criterio;CONT.SE(valores;valores_distintos)>1;
    FILTRO(valores_distintos;criterio;"nenhum item duplicado")
)
