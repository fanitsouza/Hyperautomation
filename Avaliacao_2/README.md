# Automação de Processamento e Triagem de Solicitações

## Descrição do Projeto
Este projeto consiste em um robô (RPA) desenvolvido para automatizar o fluxo de recebimento, triagem, extração de dados e encaminhamento de solicitações que chegam via e-mail. A automação cobre de ponta a ponta o processo de validação documental, comunicação com o cliente e atualização de bases de dados, garantindo rastreabilidade e padronização.

## Objetivo da Automação
Eliminar o processamento manual de caixas de entrada e a conferência primária de documentos. O sistema visa garantir que apenas cadastros validados e registrados sejam encaminhados ao próximo setor, ao mesmo tempo em que informa os clientes de forma imediata e autônoma sobre eventuais pendências em suas solicitações, reduzindo o tempo de resposta e erros operacionais.

## Fluxo de Trabalho (Pipeline)
O processo segue as seguintes etapas rigorosamente:
1. **Monitoramento:** Acessa automaticamente a caixa de e-mail e identifica novas solicitações.
2. **Download:** Realiza o download automático dos documentos anexados no e-mail.
3. **Validação de Regras:** Verifica e cruza os dados essenciais (Nome, CPF, Data de Nascimento e Endereço) conforme as regras de negócio definidas.
4. **Classificação:** Organiza os arquivos nos diretórios locais `Documentos_OK` ou `Documentos_Pendentes`.
5. **Extração de Dados:** Captura automaticamente as informações da ficha de cadastro.
6. **Registro de Dados:** Preenche e atualiza a planilha mestra com os dados extraídos da etapa anterior.
7. **Arquivamento:** Salva e organiza os documentos estruturados em suas respectivas pastas.
8. **Comunicação Automática:** Responde ao e-mail do cliente enviando o resultado positivo da solicitação ou detalhando o motivo da pendência documental.
9. **Encaminhamento:** Envia os casos validados para o próximo setor e move o documento correspondente para a pasta `Encaminhados`.

## Tecnologias Utilizadas
*   **Python:** Linguagem principal da automação.
*   **BotCity / Selenium:** Para orquestração da automação e interação com interfaces/sistemas web.
*   **Pandas:** Para manipulação de dados e preenchimento da planilha mestra.
*   **IMAP/SMTP (ou API do provedor):** Para leitura, monitoramento e envio de e-mails.

## Instruções Básicas para Execução

### Pré-requisitos
*   Python 3.8+ instalado na máquina.
*   Acesso liberado às credenciais da caixa de e-mail monitorada.
*   Mapeamento correto dos diretórios locais ou de rede utilizados no processo.

### Configuração do Ambiente
1. Clone este repositório para sua máquina local:
   ```bash
   git clone <https://github.com/fanitsouza/Hyperautomation/tree/main/Avaliacao_2>
