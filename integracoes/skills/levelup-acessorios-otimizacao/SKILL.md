---
name: levelup-acessorios-otimizacao
description: Otimizar acessórios do Studio Up para o catálogo e para celulares fracos: triângulos, número de peças, CSG, textura e tamanho, sem perder a silhueta.
---

# Otimizar acessórios (catálogo e celular)

Use sempre que modelar, corrigir ou revisar um acessório (chapéu, cabelo, óculos, colar, mochila, asas...). Leia junto levelup-acessorios. A validação do editor mostra avisos; a resposta só está boa quando não sobra nenhum aviso evitável.

## Metas que a validação confere

| Item | Ideal | Máximo aceito |
|---|---|---|
| Triângulos do acessório inteiro | até 2.000 | 4.000 (acima disso o envio é recusado) |
| Peças antes de preparar a textura | até 12 | 24 |
| Textura PNG (6 vistas) | Normal (célula 256) | 2048 px no lado maior |
| Caixa do item | dentro da caixa do ponto (a validação mostra) | — |

Ao publicar, todas as peças viram UMA malha só com UMA textura PNG. Peças demais não somem: viram triângulos.

## Onde os triângulos estão

- Bloco e cunha: 12 triângulos. Use para tudo que for reto.
- Cilindro: ~64 triângulos; esfera: ~200 ou mais. Use só onde a curva aparece de longe.
- CSG (unir/negar): cada recorte soma os triângulos das peças e cria faces novas. Um furo redondo num bloco pode passar de 150 triângulos.
- Detalhe menor que 0,1 stud quase não aparece no celular: desenhe na textura em vez de modelar.

## Regras de otimização

1. **Silhueta primeiro**: 3 a 8 volumes grandes que já lembram o objeto de longe. Só depois detalhes.
2. **Detalhe pequeno vai para a textura** (botões, costuras, logos, listras, olhos de bichinho): pinte no PNG; não modele.
3. **Curvas só onde importam**: copa de chapéu redonda sim; parafusos, rebites e bordas finas não.
4. **Recortes com moderação**: use negate só para furos que se veem (lente de óculos, aro). Junte cortes vizinhos num só cortador.
5. **Nada escondido**: peça dentro de outra peça ou encostada no corpo, que nunca aparece, deve ser apagada.
6. **Simetria**: modele um lado e espelhe; não duplique detalhes que ficam atrás do corpo.
7. **Handle**: se o Handle não faz parte do visual, deixe-o pequeno (0,2 stud) e dentro da peça principal. Peças com Transparency 1 não entram na malha nem na textura, mas continuam valendo para o encaixe.
8. **Cores planejadas**: poucas cores lisas por peça; a pintura fina é feita depois, na aba Textura.
9. **Escala certa**: o item deve caber na caixa do ponto de fixação (a validação avisa). Item grande demais atrapalha a câmera e os outros jogadores.

## Ao terminar (escreva no resumo)

- Contagem estimada de peças e triângulos e o que foi simplificado.
- O que ficou para pintar na textura.
- Próximos passos do usuário: Textura → Preparar textura → pintar/conferir as 6 vistas → Validar → Testar andando → Publicar.
