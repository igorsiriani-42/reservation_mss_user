Olá Igor, sou o Leo diretor do back na Dev.

Estou correndo atrás do erro que estão tendo do cors. Esse erro não me parece ser especificamente de Cors, visto 
que os nossos projetos em todos os nossos domínios, mesmo usando Cors aberto, nunca levantou problema por conta disso.

O problema como foi descrito na reposta de vocês pelo canal de comunicação pode ser referente ao authorizer não retornando 
o header cors sim, mas isso pode não ser a origem do erro.

Todos os 3 repositórios do backend usam variáveis de ambiente do github actions para comunicar com serviços externos ou
entre si. Uma variável crítica que precisa ser setada para o devido funcionamento do authorizer é o endpoint graph da
microsoft. O authorizer usa essa variável, que na verdade é um link, para verificar se o usuário existe no banco 
microsoft e pegar as infomações dele.

Vocês setaram essas variáveis antes de deployarem para nuvem? Caso não tenham, isso com certeza é a causa do problema. 
Por via de praticidade, o Lucas conversou com um de voces da GTI para marcar uma reunião de debug. Para evitarmos contra-
tempos como esses, precisamos de acesso a conta AWS de vocês com pelo menos uma permissão de visualização.

Obrigado pela atenção, abraço
