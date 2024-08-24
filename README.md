# player-api


# Entities

1. User
id: Identificador único do usuário.
name: Nome do usuário.
email: Endereço de email do usuário.
password: Senha criptografada do usuário.
created_at: Data de criação do usuário.
updated_at: Data da última atualização do usuário.
2. File
id: Identificador único do arquivo.
user_id: Referência ao usuário que fez o upload.
file_name: Nome do arquivo.
file_type: Tipo do arquivo (vídeo, música).
file_size: Tamanho do arquivo.
file_url: URL de onde o arquivo pode ser acessado.
created_at: Data de upload do arquivo.
3. Link
id: Identificador único do link.
file_id: Referência ao arquivo associado ao link.
shared_by: Referência ao usuário que compartilhou o link.
link_url: URL única gerada para compartilhar o arquivo.
expiration_date: Data de expiração do link (se aplicável).
created_at: Data de criação do link.
4. PlaybackSession
id: Identificador único da sessão de reprodução.
file_id: Referência ao arquivo que está sendo reproduzido.
host_user_id: Referência ao usuário que iniciou a sessão.
current_timestamp: Ponto atual de reprodução no arquivo.
is_active: Indica se a sessão está ativa ou não.
created_at: Data de início da sessão.
5. ChatMessage
id: Identificador único da mensagem.
session_id: Referência à sessão de reprodução associada.
user_id: Referência ao usuário que enviou a mensagem.
message_content: Conteúdo da mensagem.
sent_at: Data e hora em que a mensagem foi enviada.
6. AuthToken
id: Identificador único do token.
user_id: Referência ao usuário associado ao token.
token: O token de autenticação em si.
expires_at: Data de expiração do token.
created_at: Data de criação do token.
7. Log
id: Identificador único do log.
user_id: Referência ao usuário associado ao evento (se aplicável).
action: Descrição da ação realizada (e.g., login, upload).
timestamp: Data e hora do evento.
details: Detalhes adicionais sobre o evento.
