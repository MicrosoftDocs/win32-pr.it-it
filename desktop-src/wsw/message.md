---
title: Messaggio (servizi Web Windows)
description: Un messaggio è un oggetto che incapsula i dati trasmessi o ricevuti.
ms.assetid: edc810d9-7d78-4b79-8cbb-e87401f6ae41
keywords:
- Message Web Services for Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1722cbe4a956ef16a1b7195158b695f551419ad600c64f552e92700d3e4ee57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657097"
---
# <a name="message-windows-web-services"></a>Messaggio (servizi Web Windows)

Un messaggio è un oggetto che incapsula i dati trasmessi o ricevuti. La struttura di un messaggio è definita da SOAP e include un set di intestazioni e un corpo. Le intestazioni vengono sempre memorizzate nel buffer in memoria, ma il corpo viene letto e scritto con un'API di streaming.

![Diagramma che mostra un messaggio con l'intestazione memorizzata nel buffer e il corpo trasmesso.](images/messageenvelope.png)


I messaggi hanno un set di proprietà che possono essere usate per specificare impostazioni facoltative che controllano il comportamento di un messaggio e per fornire un modo per recuperare informazioni aggiuntive sui messaggi ricevuti, ad esempio le informazioni di sicurezza. Per un elenco completo delle proprietà del messaggio, vedere [**WS \_ MESSAGE PROPERTY \_ ID \_ (ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) proprietà messaggio WS).

Un messaggio viene indirizzato a un indirizzo [endpoint specifico.](endpoint-address.md)

[**WS \_ FAULT è**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) un tipo speciale di contenuto del messaggio utilizzato per rappresentare gli errori restituiti da un endpoint remoto.

I messaggi vengono sottoposti a codifica che trasforma il codice XML in un formato di trasmissione lineare prima di essere trasmessi.

Per altre informazioni sui messaggi, vedere [l'argomento Channel Layer Overview.](channel-layer-overview.md)

Gli esempi seguenti illustrano l'uso di messaggi in WWSAPI.

| Esempio                                              | Descrizione                                  |
|------------------------------------------------------|----------------------------------------------|
| [CustomHeaderExample](customheaderexample.md)       | Illustra l'uso di intestazioni di messaggio personalizzate.    |
| [MessageEncodingExample](messageencodingexample.md) | Illustra la codifica e la decodifica di un messaggio. |
| [ForwardMessageExample](forwardmessageexample.md)   | Illustra l'inoltro di un messaggio.            |



 

Con i messaggi vengono usati gli elementi API seguenti.

| Callback                                                        | Descrizione                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CALLBACK DEL \_ MESSAGGIO WS \_ \_ COMPLETATO**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback) | Notifica al chiamante che il messaggio ha completato l'utilizzo della struttura WS XML READER fornita alla funzione WsReadEnvelopeStart o della struttura WS XML WRITER fornita alla funzione \_ \_ \_ \_ WsWriteEnvelopeStart. |



 



| Enumerazione                                                      | Descrizione                                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**VERSIONE \_ DI INDIRIZZAMENTO WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)         | Versione della specifica utilizzata per le intestazioni di indirizzamento.                                        |
| [**VERSIONE \_ BUSTA WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_envelope_version)             | Versione della specifica utilizzata per la struttura della busta.                                        |
| [**ATTRIBUTI \_ DELL'INTESTAZIONE \_ WS**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type)           | Set di flag che rappresenta gli attributi mustUnderstand e relay SOAP di un'intestazione.                    |
| [**TIPO DI \_ INTESTAZIONE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type)                       | Tipo dell'intestazione.                                                                                  |
| [**INIZIALIZZAZIONE DEI \_ MESSAGGI WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) | Specifica le intestazioni che [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage) deve aggiungere al messaggio. |
| [**ID PROPRIETÀ \_ DEL \_ MESSAGGIO WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)      | ID di ogni proprietà del messaggio.                                                                         |
| [**WS \_ MESSAGE \_ STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_message_state)                   | Stato del messaggio.                                                                                |



 



| Funzione                                                             | Descrizione                                                                                                                                            |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage)                         | Assegna un indirizzo di destinazione a un messaggio.                                                                                                            |
| [**WsCheckMustUnderstandHeaders**](/windows/desktop/api/WebServices/nf-webservices-wscheckmustunderstandheaders) | Verifica che le intestazioni specificate sono state comprese in modo appropriato dal ricevitore.                                                                         |
| [**WsCreateMessage**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessage)                           | Crea un'istanza di un [oggetto WS \_ MESSAGE.](ws-message.md)                                                                                         |
| [**WsCreateMessageForChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessageforchannel)       | Crea un messaggio appropriato per l'utilizzo con un canale specifico.                                                                                 |
| [**WsFillBody**](/windows/desktop/api/WebServices/nf-webservices-wsfillbody)                                     | Assicura che in un messaggio sia disponibile un numero sufficiente di byte per la lettura.                                                                |
| [**WsFlushBody**](/windows/desktop/api/WebServices/nf-webservices-wsflushbody)                                   | Scarica tutti i dati del corpo del messaggio accumulati scritti.                                                                                       |
| [**WsFreeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsfreemessage)                               | Rilascia la risorsa di memoria associata a un messaggio.                                                                                                |
| [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader)                       | Trova l'intestazione del messaggio definita dall'applicazione e la deserializza.                                                                               |
| [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)                                   | Trova una particolare intestazione standard nel messaggio e la deserializza.                                                                                 |
| [**WsGetHeaderAttributes**](/windows/desktop/api/WebServices/nf-webservices-wsgetheaderattributes)               | Popola un parametro ULONG con [**WS \_ HEADER \_ ATTRIBUTES**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type) dall'elemento di intestazione in cui è posizionato il lettore. |
| [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty)                 | Recupera una proprietà dell'oggetto Message specificata.                                                                                                         |
| [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage)                   | Inizializza le intestazioni per il messaggio in preparazione per l'elaborazione.                                                                                 |
| [**WsMarkHeaderAsUnderstood**](/windows/desktop/api/WebServices/nf-webservices-wsmarkheaderasunderstood)         | Contrassegna un'intestazione come compresa dall'applicazione.                                                                                                       |
| [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody)                                     | Deserializza un valore dal lettore XML del messaggio.                                                                                               |
| [**WsReadEnvelopeEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopeend)                       | Legge gli elementi di chiusura di un messaggio.                                                                                                               |
| [**WsReadEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)                   | Legge le intestazioni del messaggio e si prepara a leggere gli elementi del corpo.                                                                               |
| [**WsRemoveCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremovecustomheader)                 | Rimuove un'intestazione personalizzata dal messaggio.                                                                                                              |
| [**WsRemoveHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremoveheader)                             | Rimuove [**l'oggetto WS \_ HEADER \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type) standard da un messaggio.                                                                 |
| [**WsResetMessage**](/windows/desktop/api/WebServices/nf-webservices-wsresetmessage)                             | Imposta di nuovo lo stato del messaggio **su WS \_ MESSAGE STATE \_ \_ EMPTY.**                                                                                          |
| [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader)                                   | Aggiunge o sostituisce l'intestazione standard specificata nel messaggio.                                                                                         |
| [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody)                                   | Scrive un valore nel corpo di un messaggio.                                                                                                               |
| [**WsWriteEnvelopeEnd**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopeend)                     | Scrive gli elementi di chiusura di un messaggio.                                                                                                              |
| [**WsWriteEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopestart)                 | Scrive l'inizio del messaggio, incluso il set corrente di intestazioni del messaggio, e si prepara a scrivere gli elementi del corpo.                           |



 



| Handle                        | Descrizione                                         |
|-------------------------------|-----------------------------------------------------|
| [MESSAGGIO \_ WS](ws-message.md) | Tipo opaco utilizzato per fare riferimento a un oggetto messaggio. |



 



| Struttura                                                | Descrizione                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ERRORE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)                            | Valore di errore trasportato nel corpo di un messaggio che indica un errore di elaborazione. |
| [**CODICE DI \_ ERRORE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)                 | Rappresenta un codice di errore.                                                             |
| [**MOTIVO \_ ERRORE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)             | Contiene una spiegazione dell'errore.                                                |
| [**PROPRIETÀ DEI MESSAGGI WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_properties) | Specifica un set di [**strutture WS \_ MESSAGE \_ PROPERTY.**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property)  |
| [**PROPRIETÀ DEL MESSAGGIO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property)     | Specifica un'impostazione specifica del messaggio.                                                |



 

 

 




