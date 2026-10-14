**ESPECIFICAÇÃO DE REQUISITOS**

**Projeto Mãos Solidárias**

Documento de requisitos funcionais e não funcionais

| **Campo**           | **Informação**                        |
| ------------------- | ------------------------------------- |
| Versão do documento | 1.0                                   |
| Data de elaboração  | 14/10/2026                            |
| Responsável         | \_**\_**\_**\_**\_**\_**\_**\_**\____ |
| Aprovado por        | \_**\_**\_**\_**\_**\_**\_**\_**\____ |

# 1\. Apresentação

Este documento organiza os requisitos fornecidos para o projeto Mãos Solidárias. Os requisitos funcionais descrevem os serviços e comportamentos esperados do sistema; os requisitos não funcionais estabelecem atributos de qualidade e restrições. Os itens estão preservados conforme a base informada e podem ser refinados durante a validação com as partes interessadas.

# 2\. Requisitos Funcionais

## Gestão de Usuários

| **ID** | **Requisito**                                                              |
| ------ | -------------------------------------------------------------------------- |
| RF01   | O sistema deve permitir cadastro de usuários individuais.                  |
| RF02   | O sistema deve permitir cadastro de instituições de caridade.              |
| RF03   | O sistema deve exigir autenticação para instituições editarem seus perfis. |
| RF04   | O sistema deve permitir recuperação de senha por e-mail.                   |

## Verificação de Instituições

| **ID** | **Requisito**                                                                                                           |
| ------ | ----------------------------------------------------------------------------------------------------------------------- |
| RF05   | O sistema deve solicitar documentos comprovatórios (CNPJ, certificado de utilidade pública) no cadastro da instituição. |
| RF06   | O sistema deve ter um fluxo de aprovação antes de publicar a instituição.                                               |
| RF07   | O sistema deve indicar visualmente quais instituições foram verificadas.                                                |

## Mapa Interativo

| **ID** | **Requisito**                                                                                   |
| ------ | ----------------------------------------------------------------------------------------------- |
| RF08   | O sistema deve exibir todas as instituições verificadas como marcadores em um mapa.             |
| RF09   | Ao clicar em um marcador, deve abrir um painel lateral ou modal com os detalhes da instituição. |
| RF10   | O sistema deve permitir redimensionamento e navegação pelo mapa.                                |

## Perfil da Instituição

| **ID** | **Requisito**                                                                              |
| ------ | ------------------------------------------------------------------------------------------ |
| RF11   | Cada instituição deve poder cadastrar: nome, descrição, categoria/tipo, endereço completo. |
| RF12   | O sistema deve permitir cadastro de múltiplos projetos por instituição.                    |
| RF13   | O sistema deve permitir links para redes sociais (Instagram, Facebook, WhatsApp, etc.).    |
| RF14   | O sistema deve permitir listar necessidades específicas (itens, serviços, habilidades).    |
| RF15   | O sistema deve permitir cadastro de links de doação externa (PIX, banco, crowdfunding).    |
| RF16   | O sistema deve permitir upload de fotos da instituição e projetos.                         |
| RF17   | O sistema deve mostrar contato oficial da instituição (telefone, e-mail).                  |

## Sistema de Eventos/Calendário

| **ID** | **Requisito**                                                                                             |
| ------ | --------------------------------------------------------------------------------------------------------- |
| RF18   | O sistema deve permitir cadastrar eventos com data, hora, local e descrição.                              |
| RF19   | O calendário deve ser visível no perfil da instituição.                                                   |
| RF20   | O sistema deve permitir filtração de eventos por tipo (voluntariado, arrecadação, campanhas, outro, etc). |

## Busca e Filtros

| **ID** | **Requisito**                                                                        |
| ------ | ------------------------------------------------------------------------------------ |
| RF21   | Barra de pesquisa na parte superior para buscar por nome da instituição.             |
| RF22   | Sistema de filtros por categoria (doação de alimentos, ensino, saúde, abrigo, etc.). |
| RF23   | Sistema de filtro por localização/região.                                            |
| RF24   | Resultados de busca devem atualizar o mapa dinamicamente.                            |

## Interação com Voluntários

| **ID** | **Requisito**                                                                   |
| ------ | ------------------------------------------------------------------------------- |
| RF25   | O sistema deve exibir um botão "Quero me voluntariar" no perfil da instituição. |
| RF26   | O sistema deve permitir ao voluntário enviar mensagem direta à instituição.     |
| RF27   | O sistema deve permitir inscrição em eventos específicos.                       |

# 3\. Requisitos Não Funcionais

## Desempenho

| **ID** | **Requisito**                                                                   |
| ------ | ------------------------------------------------------------------------------- |
| RNF01  | Tempo de carregamento inicial da página ≤ 3 segundos.                           |
| RNF02  | O mapa deve carregar marcadores em até 2 segundos após a página inicializar-se. |
| RNF03  | Suportar mínimo de 1.000 usuários simultâneos sem degradação significativa.     |

## Segurança

| **ID** | **Requisito**                                              |
| ------ | ---------------------------------------------------------- |
| RNF04  | Todos os dados transmitidos via HTTPS com TLS 1.3.         |
| RNF05  | Senhas armazenadas com hash forte (bcrypt/Argon2).         |
| RNF06  | Proteção contra SQL injection, XSS e CSRF.                 |
| RNF07  | Validação e sanitização de todos os inputs do usuário.     |
| RNF08  | Limitação de taxa (rate limiting) para prevenção de abuse. |

## Usabilidade e Acessibilidade

| **ID** | **Requisito**                                                                    |
| ------ | -------------------------------------------------------------------------------- |
| RNF09  | Interface responsiva (funcionar bem em desktop, tablet e mobile).                |
| RNF10  | Cumprir padrões WCAG 2.1 nível AA para acessibilidade.                           |
| RNF11  | Contraste adequado entre texto e fundo (especialmente azul escuro sobre branco). |
| RNF12  | Navegação por teclado totalmente funcional.                                      |

## Design e Estética

| **ID** | **Requisito**                                                         |
| ------ | --------------------------------------------------------------------- |
| RNF13  | Paleta principal: fundo branco (#FFFFFF) com detalhes em azul escuro. |
| RNF14  | Tipografia legível, tamanho mínimo 16px para corpo de texto.          |
| RNF15  | Ícones consistentes para categorias de instituições.                  |

## Confiabilidade

| **ID** | **Requisito**                                     |
| ------ | ------------------------------------------------- |
| RNF16  | Disponibilidade do sistema ≥ 99% (uptime mensal). |
| RNF17  | Backup automático dos dados.                      |
| RNF18  | Recuperação de desastre com RTO ≤ 4 horas.        |

## Escalabilidade

| **ID** | **Requisito**                                                                       |
| ------ | ----------------------------------------------------------------------------------- |
| RNF19  | Arquitetura preparada para crescimento (adicionar novas instituições e usuários).   |
| RNF20  | Banco de dados capaz de suportar crescimento de 10x sem reestruturação majoritária. |

## Legal e Compliance

| **ID** | **Requisito**                                           |
| ------ | ------------------------------------------------------- |
| RNF21  | Conformidade com LGPD (Lei Geral de Proteção de Dados). |
| RNF22  | Política de privacidade clara e termos de uso visíveis. |
| RNF23  | Opção de exclusão de conta e dados sob solicitação.     |

## Manutenibilidade

| **ID** | **Requisito**                                                  |
| ------ | -------------------------------------------------------------- |
| RNF24  | Código documentado e versionado em Git.                        |
| RNF25  | Logs detalhados para troubleshooting.                          |
| RNF26  | Painel administrativo para gestão de denúncias e verificações. |