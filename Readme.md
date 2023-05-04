# PDM - Notificações

Este é um exemplo de uso do sistema de notificações do Expo.

Notificações locais (disparadas pelo próprio aplicativo) são mais simples de implementar, porém para fazer uso de notificações remotas (enviadas pelo servidor do expo) é necessário criar um projeto na plataforma do expo (https://expo.dev/).

Todo o código deste exemplo está contido no arquivo `App.tsx`, que possui comentários explicando todo o processo.

Lembrar dos 3 passos:

1.  Obter o token (função pronta)
2.  Enviar a notificação: pode ser local ou remota
3.  Responder à notificação

A seguir são listados detalhes sobre o uso de notificações locais e remotas.

## Notificações Locais

As notificações locais podem ser enviadas pelo próprio aplicativo ou algum serviço que esteja executando em background. Existe um exemplo no método `schedulePushNotification`, que executa uma chamada ao método `Notifications.scheduleNotificationAsync` para enviar uma notificação local.

## Notificações remotas

Conforme dito anteriormente, notificações remotas precisam ter um projeto vinculado na plataforma do expo. Para isto, crie uma conta em https://expo.dev/, e em seguida crie um novo projeto, ao abrir este projeto você poderá visualizar e copiar o **ID**, ex: f76084b6-e5c2-4f66-bac8-b0cc25c18c42 (este projeto já foi excluído, então esse ID não vai funcionar, crie o seu para testar).

O ID do projeto deve ser utilizado no método `registerForPushNotificationsAsync`.
