---
title: Channel (Windows Web Services)
description: I canali incapsulano un contesto di comunicazione tra due o più parti e vengono usati per inviare e ricevere messaggi.
ms.assetid: 5a04580d-c89f-4505-a4b7-0724ffb788fd
keywords:
- Servizi Web del canale per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff11601f372416527f1d521f8fb9880c98821f9421b633f9eed059cc5b4f672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026649"
---
# <a name="channel-windows-web-services"></a>Channel (Windows Web Services)

I canali incapsulano un contesto di comunicazione tra due o più parti e vengono usati per inviare e ricevere messaggi.


Nel client usare [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) per creare un canale. Nel server usare [**WsCreateChannelForListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) per creare un canale che può essere accettato dal client usando un [listener](listener.md).

Quando si crea un canale, specificare le informazioni seguenti, che determinano sia il comportamento locale del canale che il protocollo di collegamento da utilizzare.

-   Tipo [**di canale WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)che identifica il modello di scambio dei messaggi del canale.
-   [**WS \_ CHANNEL \_ BINDING,**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)che identifica il protocollo di trasferimento da utilizzare.
-   Oggetto [**WS \_ SECURITY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)che specifica la sicurezza utilizzata per il canale. Quando si creano canali da usare in un server, questa opzione viene specificata una sola volta per tutti i canali che verranno accettati per un listener specificato.
-   Oggetto set [**WS \_ CHANNEL \_ PROPERTY,**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)che specifica impostazioni facoltative aggiuntive. Per un elenco di queste impostazioni, vedere enumerazioni [**WS \_ CHANNEL PROPERTY \_ \_ ID.**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)

Prima di usare il canale, è necessario aprirlo chiamando la funzione [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) e specificando l'indirizzo del canale e [dell'endpoint,](endpoint-address.md)insieme ad altre informazioni facoltative.

Per informazioni sulle transizioni di stato per un canale, vedere [**l'argomento Stati del**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) canale.

Per altre informazioni sui canali, vedere [l'argomento Channel Layer Overview](channel-layer-overview.md) .

Gli elementi API seguenti vengono usati con i canali.

| Callback                                                                                  | Descrizione                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CALLBACK DEL \_ MESSAGGIO DI \_ ABBANDONO WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)                     | Gestisce la [**chiamata WsAbandonMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage) per un canale con associazione di canale personalizzata.                                              |
| [**CALLBACK DEL \_ CANALE DI \_ INTERRUZIONE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)                         | Gestisce la [**chiamata WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) per un canale con associazione di canale personalizzata.                                                  |
| [**WS \_ CLOSE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)                         | Gestisce la [**chiamata WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) per un canale con associazione di canale personalizzata.                                                  |
| [**WS \_ CREATE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)                       | Gestisce la [**chiamata WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) per un canale con associazione di canale personalizzata.                                                  |
| [**WS \_ CREATE \_ DECODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)                       | Gestisce la creazione di un'istanza del decodificatore.                                                                                                                  |
| [**WS \_ CREATE \_ ENCODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)                       | Gestisce la creazione di un'istanza del codificatore.                                                                                                                 |
| [**CALLBACK \_ \_ DECODE DEL DECODIFICATORE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)                       | Decodifica un messaggio.                                                                                                                                    |
| [**CALLBACK DI FINE DECODIFICATORE WS \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)                             | Decodifica la fine di un messaggio.                                                                                                                         |
| [**CALLBACK DEL \_ TIPO DI CONTENUTO GET \_ \_ DEL \_ DECODIFICATORE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback) | Ottiene il tipo di contenuto del messaggio.                                                                                                                 |
| [**CALLBACK DI \_ AVVIO DEL \_ DECODIFICATORE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)                         | Avvia la decodifica di un messaggio.                                                                                                                            |
| [**CALLBACK DI CODIFICA \_ \_ DEL CODIFICATORE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)                       | Codifica un messaggio.                                                                                                                                    |
| [**CALLBACK DI FINE \_ \_ CODIFICATORE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)                             | Codifica la fine di un messaggio.                                                                                                                         |
| [**CALLBACK DEL TIPO \_ DI CONTENUTO GET DEL \_ \_ \_ CODIFICATORE \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback) | Ottiene il tipo di contenuto del messaggio.                                                                                                                 |
| [**CALLBACK DI \_ AVVIO DEL \_ CODIFICATORE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)                         | Avvia la codifica di un messaggio.                                                                                                                            |
| [**CALLBACK DEL \_ CANALE \_ GRATUITO DI \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)                           | Gestisce la [**chiamata WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel) per un canale con associazione di canale personalizzata.                                                    |
| [**CALLBACK DEL \_ \_ DECODIFICATORE LIBERO WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)                           | Gestisce la liberazione di un'istanza del decodificatore.                                                                                                                   |
| [**CALLBACK DEL \_ \_ CODIFICATORE GRATUITO WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)                           | Gestisce la liberazione di un'istanza del codificatore.                                                                                                                  |
| [**CALLBACK DELLE \_ PROPRIETÀ DEL CANALE WS \_ GET \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)          | Gestisce la [**chiamata WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty) per un canale con associazione di canale personalizzata.                                      |
| [**CALLBACK DI \_ REINDIRIZZAMENTO HTTP WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)                         | Richiamato quando un messaggio sta per essere reindirizzato automaticamente a un altro servizio che utilizza la funzionalità di reindirizzamento automatico HTTP, come descritto in RFC2616. |
| [**CALLBACK DI WS \_ OPEN \_ CHANNEL \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)                           | Gestisce la [**chiamata WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) per un canale con associazione di canale personalizzata.                                                    |
| [**WS \_ READ \_ MESSAGE \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)                  | Gestisce la [**chiamata WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) per un canale con associazione di canale personalizzata.                                              |
| [**CALLBACK DI \_ AVVIO \_ DEL MESSAGGIO \_ WS READ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)              | Gestisce la [**chiamata WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) per un canale con associazione di canale personalizzata.                                              |
| [**CALLBACK DEL \_ CANALE WS RESET \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)                         | Gestisce la [**chiamata WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel) per un canale con associazione di canale personalizzata.                                                  |
| [**CALLBACK DELLE \_ PROPRIETÀ DEL CANALE WS SET \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)          | Gestisce la [**chiamata WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty) per un canale con associazione di canale personalizzata.                                      |
| [**CALLBACK DEL \_ CANALE DELLA SESSIONE DI ARRESTO \_ \_ WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)  | Gestisce la [**chiamata WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel) per un canale con associazione di canale personalizzata.                              |
| [**WS \_ WRITE \_ MESSAGE \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)                | Gestisce la [**chiamata WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend) per un canale con associazione di canale personalizzata.                                            |
| [**CALLBACK DI \_ AVVIO \_ DEL MESSAGGIO \_ WS WRITE \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)            | Gestisce la [**chiamata WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart) per un canale con associazione di canale personalizzata.                                        |



 



| Enumerazione                                                 | Descrizione                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ CHANNEL \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)          | Indica lo stack di protocolli da utilizzare per il canale.                                                                                      |
| [**ID PROPRIETÀ CANALE WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) | Identifica ogni proprietà del canale in base a un ID.                                                                                                |
| [**STATO DEL CANALE WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state)              | Stato del canale.                                                                                                                 |
| [**TIPO DI \_ CANALE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)                | Indica le caratteristiche di base del canale, ad esempio se è con sessione e quali direzioni di comunicazione sono supportate. |
| [**CODIFICA \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding)                         | Le diverse codifiche (formati di messaggio).                                                                                                |
| [**OPZIONE \_ WS RECEIVE \_**](/windows/desktop/api/WebServices/ne-webservices-ws_receive_option)            | Specifica se è necessario un messaggio quando si riceve da un canale.                                                                    |
| [**MODALITÀ DI \_ TRASFERIMENTO \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_transfer_mode)              | Specifica se i messaggi inviati o ricevuti vengono trasmessi o memorizzati nel buffer.                                                            |



 



| Funzione                                                         | Descrizione                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**WsAbandonMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage)                     | Ignora il resto di un messaggio per un canale.                                                              |
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)                         | Interrompe tutte le operazioni di I/O in sospeso su un canale specificato e imposta lo stato del canale su **WS \_ CHANNEL STATE \_ \_ FAULTED.** |
| [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel)                         | Chiude un canale quando non è più necessario.                                                                |
| [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel)                       | Crea un canale.                                                                                           |
| [**WsCreateChannelForListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) | Crea un canale per un listener.                                                                            |
| [**WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel)                           | Rilascia le risorse di memoria associate a un canale.                                                     |
| [**WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty)             | Recupera una proprietà del canale a cui fa riferimento il parametro channel.                                     |
| [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel)                           | Apre un canale a un endpoint.                                                                              |
| [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend)                     | Legge gli elementi di chiusura di un messaggio da un canale.                                                      |
| [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart)                 | Legge le intestazioni del messaggio successivo dal canale e prepara la lettura degli elementi del corpo.               |
| [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)                     | Riceve un messaggio e deserializza il corpo del messaggio come valore.                                      |
| [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)                         | Invia un messaggio di richiesta e riceve un messaggio di risposta correlato.                                             |
| [**WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel)                         | Reimpostare un canale in modo che possa essere riutilizzato.                                                                         |
| [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage)                           | Invia un messaggio su un canale utilizzando la serializzazione per scrivere l'elemento del corpo.                                  |
| [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)                 | Invia un messaggio che è una risposta a un messaggio ricevuto.                                                       |
| [**WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty)             | Imposta una proprietà di un canale.                                                                                |
| [**WsSetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetmessageproperty)             | Imposta una proprietà di un messaggio.                                                                                |
| [**WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend)                   | Scrive gli elementi di chiusura di un messaggio nel canale.                                                     |
| [**WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart)               | Scrivere le intestazioni di un messaggio nel canale e prepararsi a scrivere gli elementi del corpo.                   |



 



| Handle                        | Descrizione                                 |
|-------------------------------|---------------------------------------------|
| [CANALE \_ WS](ws-channel.md) | Tipo opaco utilizzato per fare riferimento a un canale. |



 



| Struttura                                                                          | Descrizione                                                                                                                                                                                      |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DECODIFICATORE DEL CANALE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_decoder)                                 | Set di callback che trasformano il tipo di contenuto e i byte codificati di un messaggio ricevuto.                                                                                                      |
| [**CODIFICATORE DEL CANALE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_encoder)                                 | Set di callback in grado di trasformare il tipo di contenuto e i byte codificati di un messaggio inviato.                                                                                                      |
| [**PROPRIETÀ DEL CANALE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_properties)                           | Set di [**strutture \_ WS CHANNEL \_ PROPERTY.**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)                                                                                                                        |
| [**PROPRIETÀ DEL CANALE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)                               | Impostazione specifica del canale.                                                                                                                                                                      |
| [**CALLBACK DEL \_ \_ CANALE PERSONALIZZATO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_channel_callbacks)              | Set di callback che formano l'implementazione di un canale personalizzato.                                                                                                                             |
| [**PROXY \_ \_ HTTP PERSONALIZZATO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_http_proxy)                            | utilizzato per specificare il proxy personalizzato per il canale, utilizzando il valore PROXY **\_ HTTP \_ \_ \_ PERSONALIZZATO WS CHANNEL PROPERTY** \_ dell'enumerazione [**WS CHANNEL PROPERTY \_ \_ \_ ID.**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) |
| [**MAPPING \_ DELL'INTESTAZIONE HTTP WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_mapping)                        | Rappresenta una singola intestazione mappata come parte di [**WS \_ HTTP MESSAGE \_ \_ MAPPING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).                                                                         |
| [**MAPPING DEI MESSAGGI HTTP WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)                      | Informazioni su come una richiesta o una risposta HTTP deve essere rappresentata in un oggetto messaggio.                                                                                                     |
| [**CONTESTO DI \_ CALLBACK DI \_ REINDIRIZZAMENTO HTTP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_redirect_callback_context) | Specifica la funzione di callback e lo stato per il controllo del comportamento di reindirizzamento automatico HTTP.                                                                                               |
| [**DESCRIZIONE DEL MESSAGGIO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)                         | Schema per l'input e l'output [WS \_ MESSAGE per](ws-message.md) una determinata descrizione dell'operazione.                                                                                             |



 

 

 




