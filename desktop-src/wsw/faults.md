---
title: Errori
description: Un messaggio di errore viene utilizzato per comunicare informazioni sugli errori relativi a un errore in un endpoint remoto.
ms.assetid: d2bada50-2ddd-4f7f-9b25-7bbec77b431b
keywords:
- Errori dei servizi Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ecad1b63335b7f2bfc81c099b4f920d9de21c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297919"
---
# <a name="faults"></a>Errori

Un messaggio di errore viene utilizzato per comunicare informazioni sugli errori relativi a un errore in un endpoint remoto. Un messaggio di errore è analogo a qualsiasi altro messaggio, ad eccezione del fatto che il formato del corpo del messaggio è standard. Gli errori possono essere utilizzati sia da protocolli di infrastruttura, ad esempio WS-Addressing, che da protocolli applicativi di livello superiore.

-   [Overview](#overview)
-   [Generazione di errori in un servizio](#generating-faults-in-a-service)
-   [Gestione degli errori in un client](#handling-faults-on-a-client)
-   [Utilizzo di errori con messaggi](#using-faults-with-messages)

## <a name="overview"></a>Panoramica

Il contenuto del corpo di un messaggio di errore viene rappresentato in questa API utilizzando la struttura [**WS \_ fault**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) . Sebbene un errore disponga di un set fisso di campi utilizzati per fornire informazioni sull'errore (ad esempio, il [**\_ \_ codice di errore WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code) che identifica il tipo di errore e il [**\_ \_ motivo dell'errore WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason) che contiene il testo che descrive l'errore), contiene anche un campo dettagli che può essere utilizzato per specificare contenuto XML arbitrario correlato all'errore.

## <a name="generating-faults-in-a-service"></a>Generazione di errori in un servizio

Un servizio in genere invia un errore a causa di un errore che si è verificato durante l'elaborazione della richiesta. Il modello utilizzato da questa API è che il codice del servizio che rileva l'errore di elaborazione acquisirà le informazioni di errore necessarie nell'oggetto [WS \_ Error](ws-error.md) e quindi il codice a un livello superiore nella catena di chiamate invierà effettivamente l'errore usando le informazioni acquisite a livello inferiore. Questo schema consente di isolare il codice che invia l'errore da come viene eseguito il mapping delle situazioni di errore agli errori, consentendo comunque di inviare informazioni dettagliate sugli errori.

Le proprietà seguenti possono essere utilizzate con [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) per acquisire informazioni sugli errori per un oggetto [WS \_ Error](ws-error.md) :

-   [**WS \_ \_azione della \_ proprietà \_ errore errori**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Consente di specificare l'azione da utilizzare per il messaggio di errore. Se non viene specificato, viene fornita un'azione predefinita.
-   [**WS \_ \_errore della \_ proprietà \_ errore**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Contiene la struttura [**di \_ errore WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) inviata nel corpo del messaggio di errore.
-   [**WS \_ \_intestazione della \_ proprietà \_ errore errori**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Alcuni errori includono le intestazioni dei messaggi che vengono aggiunte al messaggio di errore per trasferire errori di elaborazione relativi alle intestazioni del messaggio di richiesta. Questa proprietà può essere utilizzata per specificare un [ \_ \_ buffer WS XML](ws-xml-buffer.md) contenente un'intestazione da aggiungere al messaggio di errore.

Qualsiasi stringa di errore aggiunta all'oggetto [ \_ errore WS](ws-error.md) viene utilizzata come testo nell'errore inviato. Le stringhe di errore possono essere aggiunte all'oggetto Error usando [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring).

La funzione [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) può essere utilizzata per impostare queste proprietà dell'oggetto [ \_ errore WS](ws-error.md) .

Per impostare i dettagli dell'errore archiviato nell'oggetto [WS \_ Error](ws-error.md) , utilizzare la funzione [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail) . Questa funzione può essere utilizzata per associare un contenuto XML arbitrario a un errore.

L' [host del servizio](service-host.md) invierà automaticamente errori usando le informazioni sopra riportate nell'oggetto [WS \_ Error](ws-error.md) . La proprietà di [**\_ \_ \_ \_ divulgazione degli errori della proprietà del servizio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) può essere utilizzata per controllare la modalità di invio di un errore.

Se si utilizza il livello del canale, è possibile inviare errori per un oggetto [WS \_ Error](ws-error.md) utilizzando [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror).

## <a name="handling-faults-on-a-client"></a>Gestione degli errori in un client

Se un client riceve un errore quando si utilizza un [proxy del servizio](service-proxy.md) o tramite [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) o [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage), viene restituito l'errore di **WS \_ E \_ endpoint \_ \_ received** . Per ulteriori informazioni, vedere [valori restituiti dei servizi Web Windows](windows-web-services-return-values.md). Queste funzioni compileranno anche l'oggetto [WS \_ Error](ws-error.md) fornito alla chiamata con le informazioni sull'errore ricevuto.

È possibile eseguire una query sulle proprietà seguenti di un oggetto [WS \_ Error](ws-error.md) utilizzando [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty) per ottenere informazioni su un errore ricevuto:

-   [**WS \_ \_azione della \_ proprietà \_ errore errori**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Specifica il valore dell'azione del messaggio di errore.
-   [**WS \_ \_errore della \_ proprietà \_ errore**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Contiene la struttura [**di \_ errore WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) che è stata deserializzata dal corpo del messaggio di errore.

Un errore può contenere contenuto XML arbitrario aggiuntivo nei dettagli dell'errore. È possibile accedervi usando la funzione [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail) .

## <a name="using-faults-with-messages"></a>Utilizzo di errori con messaggi

La sezione seguente si applica quando si tratta direttamente del contenuto del corpo di un messaggio di errore.

Il contenuto del corpo di un messaggio di errore è rappresentato dalla struttura di [**\_ errore**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) standard di WS, che include il supporto incorporato per la serializzazione.

Il codice seguente, ad esempio, può essere utilizzato per scrivere un errore in un corpo del messaggio:

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault = { ... };
hr = WsWriteBody(message, &faultDescription, WS_WRITE_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

Il codice seguente può essere utilizzato per leggere un errore da un corpo del messaggio:

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault;
hr = WsReadBody(message, &faultDescription, WS_READ_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

Per sapere se un messaggio ricevuto è un errore o meno, è possibile consultare [**la \_ \_ proprietà \_ \_ WS Message**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) . Questa proprietà viene impostata in base al fatto che il primo elemento nel corpo sia un elemento fault durante [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) o [**WsReadEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart).

Per creare un [**errore \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) dato un [ \_ errore WS](ws-error.md), utilizzare la funzione [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror) .

Le enumerazioni seguenti fanno parte di errori:

-   [**\_divulgazione di errori WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure)
-   [**\_ \_ \_ ID proprietà errore WS-fault \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)

Le funzioni seguenti fanno parte degli errori:

-   [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)
-   [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail)
-   [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty)
-   [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail)
-   [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty)

Le strutture seguenti fanno parte di errori:

-   [**\_errore WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)
-   [**\_codice errore \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)
-   [**\_ \_ Descrizione Dettagli errore \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_detail_description)
-   [**\_motivo dell'errore WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)

 

 




