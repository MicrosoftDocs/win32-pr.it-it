---
title: Canale (servizi Web Windows)
description: I canali incapsulano un contesto di comunicazione tra due o più entità e vengono utilizzati per inviare e ricevere messaggi.
ms.assetid: 5a04580d-c89f-4505-a4b7-0724ffb788fd
keywords:
- Servizi Web del canale per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93819057f2de4ecf82b2def9cdc4fe14dd1b0ee
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103963688"
---
# <a name="channel-windows-web-services"></a>Canale (servizi Web Windows)

I canali incapsulano un contesto di comunicazione tra due o più entità e vengono utilizzati per inviare e ricevere messaggi.


Nel client usare [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) per creare un canale. Sul server usare [**WsCreateChannelForListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) per creare un canale che può essere accettato dal client usando un [listener](listener.md).

Quando si crea un canale, si specificano le informazioni seguenti, che determinano sia il comportamento locale del canale che il protocollo wire da usare.

-   [**Tipo di \_ canale \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type), che identifica il modello di scambio dei messaggi del canale.
-   [**Binding di \_ canale \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)che identifica il protocollo di trasferimento da utilizzare.
-   [**Descrizione della \_ sicurezza \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), che specifica la sicurezza utilizzata per il canale. Quando si creano canali da utilizzare in un server, questa viene specificata una volta per tutti i canali che verranno accettati per un determinato listener.
-   Set [**WS \_ Channel \_ Property**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, che specifica altre impostazioni facoltative (per un elenco di queste impostazioni, vedere le enumerazioni [**\_ \_ \_ ID della proprietà del canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) ).

Prima di usare il canale, è necessario aprirlo chiamando la funzione [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) e specificando l'indirizzo del canale e dell' [endpoint](endpoint-address.md), insieme ad altre informazioni facoltative.

Per informazioni sulle transizioni di stato per un canale, vedere l'argomento [**Stati del canale**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) .

Per ulteriori informazioni sui canali, vedere l'argomento [Panoramica del livello del canale](channel-layer-overview.md) .

I seguenti elementi API vengono usati con i canali.

| Callback                                                                                  | Descrizione                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_callback del \_ messaggio WS Abandon \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)                     | Gestisce la chiamata [**WsAbandonMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage) per un canale con associazione di canale personalizzata.                                              |
| [**\_callback del \_ canale WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)                         | Gestisce la chiamata [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) per un canale con associazione di canale personalizzata.                                                  |
| [**\_callback del \_ canale WS Close \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)                         | Gestisce la chiamata [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) per un canale con associazione di canale personalizzata.                                                  |
| [**\_callback del \_ canale WS create \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)                       | Gestisce la chiamata [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) per un canale con associazione di canale personalizzata.                                                  |
| [**CALLBACK di WS \_ Create \_ decoder \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)                       | Gestisce la creazione di un'istanza del decodificatore.                                                                                                                  |
| [**\_callback WS crea \_ codificatore \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)                       | Gestisce la creazione di un'istanza del codificatore.                                                                                                                 |
| [**\_callback decodifica \_ decodificatore WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)                       | Decodifica un messaggio.                                                                                                                                    |
| [**\_callback finale del decodificatore WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)                             | Decodifica la fine di un messaggio.                                                                                                                         |
| [**\_callback del \_ \_ tipo di contenuto Get del \_ decodificatore WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback) | Ottiene il tipo di contenuto del messaggio.                                                                                                                 |
| [**\_callback di avvio del decodificatore WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)                         | Avvia la decodifica di un messaggio.                                                                                                                            |
| [**\_ \_ callback codifica WS codificatore \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)                       | Codifica un messaggio.                                                                                                                                    |
| [**\_ \_ callback finale WS \_ Encoder**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)                             | Codifica la fine di un messaggio.                                                                                                                         |
| [**\_callback del \_ \_ tipo di contenuto Get \_ \_ di WS Encoder**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback) | Ottiene il tipo di contenuto del messaggio.                                                                                                                 |
| [**\_ \_ callback iniziale WS \_ Encoder**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)                         | Avvia la codifica di un messaggio.                                                                                                                            |
| [**\_ \_ callback canale libero \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)                           | Gestisce la chiamata [**WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel) per un canale con associazione di canale personalizzata.                                                    |
| [**\_callback del \_ decodificatore WS Free \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)                           | Gestisce la liberazione di un'istanza del decodificatore.                                                                                                                   |
| [**\_callback del \_ codificatore WS Free \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)                           | Gestisce la liberazione di un'istanza del codificatore.                                                                                                                  |
| [**\_callback della \_ proprietà del canale WS Get \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)          | Gestisce la chiamata [**WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty) per un canale con associazione di canale personalizzata.                                      |
| [**\_callback di \_ Reindirizzamento \_ http ws**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)                         | Richiamato quando un messaggio sta per essere reindirizzato automaticamente a un altro servizio che utilizza la funzionalità di reindirizzamento automatico HTTP come descritto in sul rfc2616. |
| [**CALLBACK di WS \_ Open \_ Channel \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)                           | Gestisce la chiamata [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) per un canale con associazione di canale personalizzata.                                                    |
| [**\_ \_ callback finale del messaggio WS Read \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)                  | Gestisce la chiamata [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) per un canale con associazione di canale personalizzata.                                              |
| [**\_callback di \_ avvio del messaggio WS Read \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)              | Gestisce la chiamata [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) per un canale con associazione di canale personalizzata.                                              |
| [**\_callback del \_ canale WS Reset \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)                         | Gestisce la chiamata [**WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel) per un canale con associazione di canale personalizzata.                                                  |
| [**\_callback della \_ proprietà del canale WS set \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)          | Gestisce la chiamata [**WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty) per un canale con associazione di canale personalizzata.                                      |
| [**\_ \_ \_ callback canale sessione WS \_ Shutdown**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)  | Gestisce la chiamata [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel) per un canale con associazione di canale personalizzata.                              |
| [**\_ \_ callback finale del messaggio WS Write \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)                | Gestisce la chiamata [**WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend) per un canale con associazione di canale personalizzata.                                            |
| [**\_callback di \_ avvio del messaggio WS Write \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)            | Gestisce la chiamata [**WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart) per un canale con associazione di canale personalizzata.                                        |



 



| Enumerazione                                                 | Descrizione                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_binding di canale WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)          | Indica lo stack di protocolli da utilizzare per il canale.                                                                                      |
| [**\_ID della \_ proprietà del canale WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) | Identifica ogni proprietà del canale in base a un ID.                                                                                                |
| [**\_stato del canale WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state)              | Stato del canale.                                                                                                                 |
| [**\_tipo di canale WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)                | Indica le caratteristiche di base del canale, ad esempio se è con sessione e quali direzioni di comunicazione sono supportate. |
| [**\_codifica WS**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding)                         | Codifiche diverse (formati dei messaggi).                                                                                                |
| [**\_opzione di ricezione WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_receive_option)            | Specifica se un messaggio è obbligatorio per la ricezione da un canale.                                                                    |
| [**\_modalità di trasferimento WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_transfer_mode)              | Specifica se i messaggi inviati o ricevuti vengono trasmessi o memorizzati nel buffer.                                                            |



 



| Funzione                                                         | Descrizione                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**WsAbandonMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage)                     | Ignora il resto di un messaggio per un canale.                                                              |
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)                         | Interrompe tutte le I/O in sospeso su un canale specificato e imposta lo stato del canale su **WS \_ canale stato non \_ \_ riuscito**. |
| [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel)                         | Chiude un canale quando non è più necessario.                                                                |
| [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel)                       | Crea un canale.                                                                                           |
| [**WsCreateChannelForListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) | Crea un canale per un listener.                                                                            |
| [**WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel)                           | Rilascia le risorse di memoria associate a un canale.                                                     |
| [**WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty)             | Recupera una proprietà del canale a cui fa riferimento il parametro del canale.                                     |
| [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel)                           | Apre un canale a un endpoint.                                                                              |
| [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend)                     | Legge gli elementi di chiusura di un messaggio da un canale.                                                      |
| [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart)                 | Legge le intestazioni del messaggio successivo dal canale e prepara la lettura degli elementi del corpo.               |
| [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)                     | Riceve un messaggio e deserializza il corpo del messaggio come valore.                                      |
| [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)                         | Invia un messaggio di richiesta e riceve un messaggio di risposta correlato.                                             |
| [**WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel)                         | Reimpostare un canale per poterlo riutilizzare.                                                                         |
| [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage)                           | Invia un messaggio su un canale utilizzando la serializzazione per scrivere l'elemento Body.                                  |
| [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)                 | Invia un messaggio che rappresenta una risposta a un messaggio ricevuto.                                                       |
| [**WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty)             | Imposta una proprietà di un canale.                                                                                |
| [**WsSetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetmessageproperty)             | Imposta una proprietà di un messaggio.                                                                                |
| [**WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend)                   | Scrive gli elementi di chiusura di un messaggio nel canale.                                                     |
| [**WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart)               | Scrivere le intestazioni di un messaggio nel canale e prepararsi a scrivere gli elementi del corpo.                   |



 



| Handle                        | Descrizione                                 |
|-------------------------------|---------------------------------------------|
| [\_canale WS](ws-channel.md) | Tipo opaco utilizzato per fare riferimento a un canale. |



 



| Struttura                                                                          | Descrizione                                                                                                                                                                                      |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_decoder del canale WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_decoder)                                 | Set di callback che trasformano il tipo di contenuto e i byte codificati di un messaggio ricevuto.                                                                                                      |
| [**\_ \_ codificatore WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_encoder)                                 | Set di callback che possono trasformare il tipo di contenuto e i byte codificati di un messaggio inviato.                                                                                                      |
| [**\_proprietà del canale WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_properties)                           | Set di strutture [**di \_ \_ proprietà del canale WS**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) .                                                                                                                        |
| [**\_proprietà del canale WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)                               | Impostazione specifica del canale.                                                                                                                                                                      |
| [**\_callback del \_ canale \_ personalizzato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_channel_callbacks)              | Set di callback che formano l'implementazione di un canale personalizzato.                                                                                                                             |
| [**\_ \_ proxy HTTP personalizzato \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_http_proxy)                            | usato per specificare il proxy personalizzato per il canale, usando il valore proxy **\_ \_ \_ \_ http personalizzato della proprietà del canale WS** \_ dell'enumerazione dell'ID della [**\_ \_ proprietà \_ del canale WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) . |
| [**\_mapping delle \_ intestazioni WS http \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_mapping)                        | Rappresenta una singola intestazione di cui è stato eseguito il mapping come parte del [**mapping di WS \_ http \_ message \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).                                                                         |
| [**\_mapping dei \_ messaggi \_ http ws**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)                      | Informazioni sulla modalità di rappresentazione di una richiesta o di una risposta HTTP in un oggetto Message.                                                                                                     |
| [**\_contesto di \_ callback del reindirizzamento HTTP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_redirect_callback_context) | Specifica la funzione di callback e lo stato per il controllo del comportamento di reindirizzamento automatico HTTP.                                                                                               |
| [**\_Descrizione del messaggio WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)                         | Schema per il [ \_ messaggio WS](ws-message.md) di input e di output per una descrizione dell'operazione specificata.                                                                                             |



 

 

 




