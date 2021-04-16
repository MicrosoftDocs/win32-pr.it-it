---
title: Messaggio (servizi Web Windows)
description: Un messaggio è un oggetto che incapsula i dati trasmessi o ricevuti.
ms.assetid: edc810d9-7d78-4b79-8cbb-e87401f6ae41
keywords:
- Servizi Web di messaggistica per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704df318e10521bd56e62632af16e683b7baccfc
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104563415"
---
# <a name="message-windows-web-services"></a>Messaggio (servizi Web Windows)

Un messaggio è un oggetto che incapsula i dati trasmessi o ricevuti. La struttura di un messaggio è definita da SOAP e include un set di intestazioni e un corpo. Le intestazioni vengono sempre memorizzate nel buffer in memoria, ma il corpo viene letto e scritto con un'API di streaming.

![Diagramma che mostra un messaggio con l'intestazione memorizzata nel buffer e il corpo trasmesso.](images/messageenvelope.png)


I messaggi includono un set di proprietà che possono essere utilizzate per specificare le impostazioni facoltative che controllano il comportamento di un messaggio e per fornire un modo per recuperare informazioni aggiuntive sui messaggi ricevuti, ad esempio le informazioni sulla sicurezza. Per un elenco completo delle proprietà dei messaggi, vedere [**\_ ID della \_ proprietà \_ del messaggio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) .

Un messaggio viene indirizzato a un [indirizzo endpoint](endpoint-address.md)specifico.

Un [**\_ errore WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) è un tipo speciale di contenuto del messaggio utilizzato per rappresentare gli errori restituiti da da un endpoint remoto.

I messaggi vengono sottoposti a codifica per trasformare il codice XML in un formato wire lineare prima della trasmissione.

Per ulteriori informazioni sui messaggi, vedere l'argomento [Panoramica del livello del canale](channel-layer-overview.md) .

Gli esempi seguenti illustrano l'uso dei messaggi in WWSAPI.

| Esempio                                              | Descrizione                                  |
|------------------------------------------------------|----------------------------------------------|
| [CustomHeaderExample](customheaderexample.md)       | Viene illustrato l'utilizzo di intestazioni di messaggio personalizzate.    |
| [MessageEncodingExample](messageencodingexample.md) | Viene illustrato come codificare e decodificare un messaggio. |
| [ForwardMessageExample](forwardmessageexample.md)   | Viene illustrato l'invio di un messaggio.            |



 

Con i messaggi vengono usati gli elementi API seguenti.

| Callback                                                        | Descrizione                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CALLBACK di WS \_ message \_ Done \_**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback) | Notifica al chiamante che il messaggio ha completato l'utilizzo della \_ struttura del lettore XML WS \_ fornita alla funzione WsReadEnvelopeStart o della \_ struttura WS XML \_ writer fornita alla funzione WsWriteEnvelopeStart. |



 



| Enumerazione                                                      | Descrizione                                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**\_versione WS Addressing \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)         | Versione della specifica utilizzata per le intestazioni di indirizzamento.                                        |
| [**\_versione busta \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_envelope_version)             | Versione della specifica utilizzata per la struttura della busta.                                        |
| [**\_attributi di intestazione WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type)           | Set di flag che rappresentano gli attributi mustUnderstand e di inoltro SOAP di un'intestazione.                    |
| [**\_tipo di intestazione WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type)                       | Tipo dell'intestazione.                                                                                  |
| [**\_inizializzazione del messaggio WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) | Specifica le intestazioni che il [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage) deve aggiungere al messaggio. |
| [**\_ID della \_ proprietà del messaggio WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)      | ID di ogni proprietà del messaggio.                                                                         |
| [**\_stato messaggio \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_state)                   | Stato del messaggio.                                                                                |



 



| Funzione                                                             | Descrizione                                                                                                                                            |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage)                         | Assegna un indirizzo di destinazione a un messaggio.                                                                                                            |
| [**WsCheckMustUnderstandHeaders**](/windows/desktop/api/WebServices/nf-webservices-wscheckmustunderstandheaders) | Verifica che le intestazioni specificate siano state correttamente riconosciute dal ricevitore.                                                                         |
| [**WsCreateMessage**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessage)                           | Crea un'istanza di un oggetto [WS \_ Message](ws-message.md) .                                                                                         |
| [**WsCreateMessageForChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessageforchannel)       | Crea un messaggio appropriato per l'utilizzo con un canale specifico.                                                                                 |
| [**WsFillBody**](/windows/desktop/api/WebServices/nf-webservices-wsfillbody)                                     | Garantisce la disponibilità di un numero sufficiente di byte in un messaggio per la lettura.                                                                |
| [**WsFlushBody**](/windows/desktop/api/WebServices/nf-webservices-wsflushbody)                                   | Scarica tutti i dati del corpo del messaggio accumulati che sono stati scritti.                                                                                       |
| [**WsFreeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsfreemessage)                               | Rilascia la risorsa di memoria associata a un messaggio.                                                                                                |
| [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader)                       | Trova l'intestazione definita dall'applicazione del messaggio e la deserializza.                                                                               |
| [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)                                   | Trova una particolare intestazione standard nel messaggio e la deserializza.                                                                                 |
| [**WsGetHeaderAttributes**](/windows/desktop/api/WebServices/nf-webservices-wsgetheaderattributes)               | Compila un parametro ULONG con gli [**attributi di \_ intestazione \_ WS**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type) dall'elemento Header su cui è posizionato il Reader. |
| [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty)                 | Recupera una proprietà dell'oggetto messaggio specificata.                                                                                                         |
| [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage)                   | Inizializza le intestazioni del messaggio in preparazione per l'elaborazione.                                                                                 |
| [**WsMarkHeaderAsUnderstood**](/windows/desktop/api/WebServices/nf-webservices-wsmarkheaderasunderstood)         | Contrassegna un'intestazione come riconosciuta dall'applicazione.                                                                                                       |
| [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody)                                     | Deserializza un valore dal lettore XML del messaggio.                                                                                               |
| [**WsReadEnvelopeEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopeend)                       | Legge gli elementi di chiusura di un messaggio.                                                                                                               |
| [**WsReadEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)                   | Legge le intestazioni del messaggio e prepara la lettura degli elementi del corpo.                                                                               |
| [**WsRemoveCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremovecustomheader)                 | Rimuove un'intestazione personalizzata dal messaggio.                                                                                                              |
| [**WsRemoveHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremoveheader)                             | Rimuove l'oggetto [**\_ \_ tipo di intestazione WS**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type) standard da un messaggio.                                                                 |
| [**WsResetMessage**](/windows/desktop/api/WebServices/nf-webservices-wsresetmessage)                             | Imposta lo stato del messaggio di nuovo sullo **\_ stato del messaggio WS \_ \_ vuoto**.                                                                                          |
| [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader)                                   | Aggiunge o sostituisce l'intestazione standard specificata nel messaggio.                                                                                         |
| [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody)                                   | Scrive un valore nel corpo di un messaggio.                                                                                                               |
| [**WsWriteEnvelopeEnd**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopeend)                     | Scrive gli elementi di chiusura di un messaggio.                                                                                                              |
| [**WsWriteEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopestart)                 | Scrive l'inizio del messaggio, incluso il set di intestazioni corrente del messaggio e si prepara a scrivere gli elementi del corpo.                           |



 



| Handle                        | Descrizione                                         |
|-------------------------------|-----------------------------------------------------|
| [\_messaggio WS](ws-message.md) | Tipo opaco utilizzato per fare riferimento a un oggetto Message. |



 



| Struttura                                                | Descrizione                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**\_errore WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)                            | Valore di errore trasferito nel corpo di un messaggio che indica un errore di elaborazione. |
| [**\_codice errore \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)                 | Rappresenta un codice di errore.                                                             |
| [**\_motivo dell'errore WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)             | Contiene una spiegazione dell'errore.                                                |
| [**\_proprietà del messaggio WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_properties) | Specifica un set di strutture di [**\_ \_ proprietà del messaggio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property) .  |
| [**WS \_ Message ( \_ proprietà)**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property)     | Specifica un'impostazione specifica del messaggio.                                                |



 

 

 




