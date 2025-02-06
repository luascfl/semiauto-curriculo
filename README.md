# semiauto-curriculo  

Este projeto fornece uma ferramenta de geração de currículo semiautomática. Ele utiliza um formulário web para criar uma representação JSON do seu currículo e, em seguida, usa um prompt do ChatGPT para refinar o JSON com base na descrição do trabalho desejado. Por fim, o JSON pode ser importado para o Reactive Resume para personalização e exportação em PDF.  

## Principais Recursos  

* **Formulário Web Interativo:** Insira facilmente suas informações de currículo por meio de um formulário HTML intuitivo.  
* **Geração de Currículo em JSON:** O formulário gera um JSON estruturado do seu currículo.  
* **Integração com ChatGPT (Prompt):** Um prompt estruturado guia o ChatGPT para aprimorar seu currículo com base em uma descrição de vaga. Isso inclui a atualização do cargo, objetivo profissional e palavras-chave/habilidades.  
* **Compatibilidade com Reactive Resume:** O JSON gerado pode ser importado diretamente para o Reactive Resume para edições adicionais e exportação em PDF.  
* **Tratamento de Erros (Saída Parcial do ChatGPT):** Inclui um mecanismo para lidar com casos em que o ChatGPT não gera um JSON completo, permitindo correção manual e download.  

## Tecnologias Utilizadas  

* HTML
* Reactive Resume (para geração final do currículo e exportação em PDF)  

## Passo a passo

1. **Acesse o Formulário Web:**
[Clique aqui para começar: semiauto-curriculo](https://curriculorr.tiiny.site/)

2. **Preencha o Formulário:** Complete todas as seções com suas informações profissionais.  

3. **Gere o JSON:** Clique no botão "Gerar JSON" para criar a versão JSON do seu currículo.  

4. É criado uma estrutura do ChatGPT com este currículo.
* A estrutura tem o objetivo de fazer com que o ChatGPT reescreva e reenvie o currículo com as seções de **cargo**, **objetivo profissional** e **habilidades** de acordo com as funções/descrições de vagas que você enviar posteriormente.

5. **Prepare o Prompt para ChatGPT:** Copie o texto da seção "Estrutura do ChatGPT" (obtido ao clicar no botão correspondente).  

6. **Use o ChatGPT:** Cole o texto copiado no ChatGPT e depois forneça a função/descrição da vaga que deseja fazer o currículo desejada. Exemplo: "Jovem aprendiz"

7. **Baixe o JSON Refinado**: o ChatGPT deverá te enviar um link para baixar o currículo JSON.
* Caso a saída do ChatGPT não esteja completa, utilize o botão "Não deu certo?" para corrigir e baixar a versão ajustada.  

8. **Importe no Reactive Resume:** Com este currículo JSON em mãos, iremos ao Reactive Resume, um poderoso site que além de fazer currículos altamente customizáveis, aceita a importação e exportação de currículos no formato JSON. Faça o upload do JSON no Reactive Resume, realize ajustes finais e exporte o currículo em PDF.  
* Você poderá usar essa estrutura para outras funções. Nas próximas mensagens, afirme de novo a função/descrição da vaga.

8.1 Faça seu registro https://rxresu.me/auth/login
Caso já possua registro > https://rxresu.me/dashboard/resumes
8.2. Clique em "Importe um currículo...", deixe o tipo do arquivo padrão (Reactive Resume .json), escolha o arquivo
8.3. Clique em confirmar. Deverá aparecer um sinal verde escrito "Validado".
Caso houver algum erro, observe o erro e cheque manualmente seu arquivo json se o ChatGPT (ou a IA utilizada) escreveu até a última linha ou acabou alucinando.
Poderá repassar o erro para a ia e pedir para que ela conserte.
8.4. Clique em Importar.
8.5. Pronto, abra seu currículo.
8.6. Vamos exportar, o botão de download está na direita da tela ou desça até achar. Exporte em PDF
* Opcionalmente, renomeie seu currículo e ative o compartilhamento público do currículo. Dessa forma, você terá um link permanente de visualização do seu currículo.

## Estrutura do Projeto  

* `Gerador de modelo de currículo RR.html`: Arquivo HTML principal com o formulário web.  
* `README.md`: Este arquivo.  


## Mensagens de Erro  

* **"Erro ao analisar o JSON: ..."**: Ocorre se o JSON importado for inválido. Verifique a sintaxe.  
* **"Erro no JSON: Por favor, cole um JSON válido."**: Aparece se o JSON corrigido na seção "Não deu certo?" ainda for inválido.  
* **Erros Relacionados ao ChatGPT:** As respostas do ChatGPT podem ser inconsistentes. Pode haver casos em que o JSON gerado esteja incompleto ou incorreto. Nesses casos, revise manualmente o JSON, corrija os erros e use o botão "Baixar JSON Corrigido" ou tente novamente no ChatGPT. Alternativamente, teste outros modelos de IA caso esse problema ocorra com frequência.  