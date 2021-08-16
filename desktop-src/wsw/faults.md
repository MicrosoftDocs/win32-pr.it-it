---
title: Errori
description: Un messaggio di errore viene usato per comunicare informazioni sull'errore in un endpoint remoto.
ms.assetid: d2bada50-2ddd-4f7f-9b25-7bbec77b431b
keywords:
- Errori dei servizi Web per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cd9e28e9ec9ce2f3068643d44306f542eebabb9b0b0c8860b15e9e986b49b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841771"
---
# <a name="faults"></a>Errori

Un messaggio di errore viene usato per comunicare informazioni sull'errore in un endpoint remoto. Un messaggio di errore è simile a qualsiasi altro messaggio, ad eccezione del formato del corpo del messaggio con un formato standard. Gli errori possono essere utilizzati sia dai protocolli dell'infrastruttura, ad esempio WS-Addressing, sia dai protocolli di applicazione di livello superiore.

-   [Overview](#overview)
-   [Generazione di errori in un servizio](#generating-faults-in-a-service)
-   [Gestione degli errori in un client](#handling-faults-on-a-client)
-   [Uso degli errori con i messaggi](#using-faults-with-messages)

## <a name="overview"></a>Panoramica

Il contenuto del corpo di un messaggio di errore viene rappresentato in questa API usando la [**struttura WS \_ FAULT.**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) Sebbene un errore abbia un set fisso di campi utilizzati per fornire informazioni sull'errore,ad esempio [**WS \_ FAULT \_ CODE**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code) che identifica il tipo di errore e [**WS \_ FAULT \_ REASON**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason) che contiene il testo che descrive l'errore, contiene anche un campo di dettaglio che può essere utilizzato per specificare contenuto XML arbitrario relativo all'errore.

## <a name="generating-faults-in-a-service"></a>Generazione di errori in un servizio

Un servizio in genere invia un errore a causa di un errore rilevato durante l'elaborazione della richiesta. Il modello usato da questa API è che il codice nel servizio che rileva l'errore di elaborazione acquisisce le informazioni di errore necessarie nell'oggetto [WS \_ ERROR](ws-error.md) e quindi il codice a un livello superiore nella catena di chiamate invierà effettivamente l'errore usando le informazioni acquisite al livello inferiore. Questo schema consente al codice che invia l'errore di essere isolato dal modo in cui viene eseguito il mapping delle situazioni di errore agli errori, pur consentendo l'invio di informazioni dettagliate sugli errori.

Le proprietà seguenti possono essere usate con [**WsSetFaultErrorProperty per**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) acquisire informazioni sull'errore per un [oggetto WS \_ ERROR:](ws-error.md)

-   [**WS \_ AZIONE \_ DELLA PROPRIETÀ FAULT \_ ERROR \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Specifica l'azione da utilizzare per il messaggio di errore. Se non viene specificato, viene fornita un'azione predefinita.
-   [**WS \_ ERRORE \_ PROPRIETÀ \_ ERRORE \_ ERRORE**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Contiene la [**struttura WS \_ FAULT**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) inviata nel corpo del messaggio di errore.
-   [**WS \_ INTESTAZIONE \_ DELLA PROPRIETÀ FAULT \_ ERROR \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Alcuni errori includono intestazioni di messaggio che vengono aggiunte al messaggio di errore per comunicare gli errori di elaborazione relativi alle intestazioni del messaggio di richiesta. Questa proprietà può essere utilizzata per specificare un [ \_ \_ buffer XML WS](ws-xml-buffer.md) contenente un'intestazione da aggiungere al messaggio di errore.

Tutte le stringhe di errore aggiunte [all'oggetto WS \_ ERROR](ws-error.md) vengono utilizzate come testo dell'errore inviato. È possibile aggiungere stringhe di errore all'oggetto errore [**usando WsAddErrorString.**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)

La [**funzione WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) può essere usata per impostare queste proprietà dell'oggetto [WS \_ ERROR.](ws-error.md)

Per impostare i dettagli dell'errore archiviato [nell'oggetto WS \_ ERROR,](ws-error.md) usare la [**funzione WsSetFaultErrorDetail.**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail) Questa funzione può essere utilizzata per associare contenuto XML arbitrario all'errore.

[L'host del](service-host.md) servizio invierà automaticamente gli errori utilizzando le informazioni precedenti nell'oggetto [ \_ WS ERROR.](ws-error.md) La [**proprietà FAULT \_ \_ \_ \_ DISCLOSURE di WS SERVICE PUÒ**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) essere utilizzata per controllare la modalità di invio dei dettagli di un errore.

Se si lavora a livello di canale, è possibile inviare errori per un oggetto [WS \_ ERROR](ws-error.md) usando [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror).

## <a name="handling-faults-on-a-client"></a>Gestione degli errori in un client

Se un client riceve un errore quando si usa un [proxy](service-proxy.md) del servizio o [**tramite WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) o [**WsReceiveMessage,**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)verrà restituito l'errore **WS E ENDPOINT FAULT \_ \_ \_ \_ RECEIVED.** Per altre informazioni, vedere l'Windows [valori restituiti dei servizi Web.](windows-web-services-return-values.md) Queste funzioni popolano anche [l'oggetto WS \_ ERROR](ws-error.md) fornito alla chiamata con informazioni sull'errore ricevuto.

È possibile eseguire query sulle proprietà seguenti di un oggetto [WS \_ ERROR](ws-error.md) usando [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty) per ottenere informazioni su un errore ricevuto:

-   [**WS \_ AZIONE \_ DELLA PROPRIETÀ FAULT \_ ERROR \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Specifica il valore dell'azione del messaggio di errore.
-   [**WS \_ ERRORE \_ PROPRIETÀ \_ ERRORE \_ ERRORE**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Contiene la [**struttura WS \_ FAULT**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) deserializzata dal corpo del messaggio di errore.

Un errore può contenere contenuto XML aggiuntivo arbitrario nel dettaglio dell'errore. È possibile accedervi usando la [**funzione WsGetFaultErrorDetail.**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail)

## <a name="using-faults-with-messages"></a>Uso degli errori con i messaggi

La sezione seguente si applica quando si lavora direttamente con il contenuto del corpo di un messaggio di errore.

Il contenuto del corpo di un messaggio di errore è rappresentato dalla struttura [**WS \_ FAULT**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) standard, che dispone del supporto incorporato per la serializzazione.

Ad esempio, il codice seguente può essere usato per scrivere un errore in un corpo del messaggio:

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault = { ... };
hr = WsWriteBody(message, &faultDescription, WS_WRITE_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

Il codice seguente può essere usato per leggere un errore dal corpo di un messaggio:

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault;
hr = WsReadBody(message, &faultDescription, WS_READ_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

Per sapere se un messaggio ricevuto è un errore, è possibile consultare [**WS \_ MESSAGE PROPERTY \_ IS \_ \_ FAULT.**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) Questa proprietà viene impostata in base al fatto che il primo elemento del corpo sia un elemento fault durante [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) o [**WsReadEnvelopeStart.**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)

Per creare un [**errore WS \_ FAULT**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) in base a [un errore \_ WS,](ws-error.md)usare la [**funzione WsCreateFaultFromError.**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)

Le enumerazioni seguenti fanno parte degli errori:

-   [**DIFFUSIONE \_ DI ERRORI WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure)
-   [**ID PROPRIETÀ ERRORE WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)

Le funzioni seguenti fanno parte degli errori:

-   [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)
-   [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail)
-   [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty)
-   [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail)
-   [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty)

Le strutture seguenti fanno parte degli errori:

-   [**WS \_ FAULT**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)
-   [**CODICE DI \_ ERRORE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)
-   [**DESCRIZIONE DEI \_ DETTAGLI \_ \_ DELL'ERRORE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_detail_description)
-   [**WS \_ FAULT \_ REASON**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)

 

 




