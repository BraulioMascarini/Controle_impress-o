Sistema de Controle de Serviços de Impressão
Este projeto é um sistema de controle de serviços de impressão com interface gráfica usando Tkinter em Python. Ele permite registrar diferentes tipos de serviços de impressão, calcular totais, gerar um relatório diário, e realizar backup dos dados. Ao final de cada sessão diária, o sistema também captura um print da tela de finalização e copia o resumo do relatório para a área de transferência, para que possa ser facilmente colado em outro lugar.

Funcionalidades
Registro de vários tipos de serviços de impressão (Impressão Colorida, Preto e Branco, A3, Fotos, etc.).
Armazenamento das quantidades e valores de cada serviço em um arquivo JSON.
Cálculo e exibição automática do "Total de Impressão Contadores" e "Desperdício" (diferença entre os contadores e os serviços realizados).
Relatório de finalização diária que exibe:
Total de serviços realizados.
Valor total dos serviços.
Total de Impressão Contadores.
Desperdício.
Copia automaticamente o resumo do relatório para a área de transferência.
Captura um print da tela da finalização diária.
Possibilidade de criar backups e restaurar dados de backups anteriores.
Geração de gráficos comparativos dos serviços ao longo dos dias.
Pré-requisitos
Antes de executar o código, certifique-se de que você tenha os seguintes pacotes instalados:

Python 3.x
Tkinter (geralmente incluído nas instalações do Python)
pyautogui para captura de tela:
bash
Copiar código
pip install pyautogui
pyperclip para copiar o texto para a área de transferência:
bash
Copiar código
pip install pyperclip
matplotlib para a geração de gráficos:
bash
Copiar código
pip install matplotlib
Como Executar
Clone ou baixe este repositório no seu ambiente local.
Instale os pré-requisitos listados acima.
Execute o arquivo Python principal (aquele que contém o código fornecido).
bash
Copiar código
python nome_do_arquivo.py
Interface de Usuário
Tela Principal
A tela principal contém várias opções para inserir as quantidades e valores de diferentes tipos de serviços de impressão.
Para adicionar um serviço, insira a quantidade e o valor e clique em Adicionar.
O campo "Total de Impressão Contadores" é calculado automaticamente com base nos valores inseridos para cada serviço.
Finalização Diária
Quando clicar no botão Finalização Diária, o sistema exibe um relatório com os seguintes dados:
Resumo de todas as quantidades e valores de serviços realizados no dia.
Total de serviços.
Valor total dos serviços.
Total de Impressão Contadores (baseado nos contadores das impressoras).
Desperdício (a diferença entre os contadores e o total de serviços).
Funcionalidades Extras
Captura de Tela: Após a exibição do relatório diário, o sistema tira automaticamente um print da tela e o salva como finalizacao_diaria.png.
Cópia de Resumo: O resumo do relatório é automaticamente copiado para a área de transferência, facilitando a colagem em outro documento.
Backup e Restauração: O sistema permite criar backups dos dados diários e restaurar backups anteriores.
Gráficos Comparativos
Através da opção Gerar Gráfico Comparativo, o sistema gera gráficos mostrando o comparativo das quantidades de serviços realizados ao longo dos dias, utilizando os dados armazenados em arquivos JSON.
Estrutura do Código
Principais Componentes
ImpressaoApp: A classe principal que controla a lógica do aplicativo.
create_widgets: Método responsável por construir a interface gráfica.
add_servico: Método que adiciona os serviços e seus valores à base de dados.
finalizar_pedido: Método que gera o relatório diário, captura a tela e copia o resumo para a área de transferência.
gerar_grafico_comparativo: Método que gera gráficos comparativos com base nos dados diários armazenados.
backup e restaurar_backup: Funções responsáveis por criar e restaurar backups dos dados.
Personalizações Futuras
Este sistema pode ser personalizado de várias maneiras, incluindo:

Adicionar novos tipos de serviços.
Implementar diferentes métodos de análise de dados.
Customizar a interface gráfica para um visual mais moderno.
Implementar relatórios em formato PDF ou Excel.
Contribuição
Sinta-se à vontade para contribuir com melhorias neste projeto. Para contribuir:

Faça um fork do projeto.
Crie uma nova branch para suas alterações.
Envie um pull request quando suas alterações estiverem prontas.
Licença
Este projeto está sob a licença MIT - consulte o arquivo LICENSE.md para obter mais informações.
