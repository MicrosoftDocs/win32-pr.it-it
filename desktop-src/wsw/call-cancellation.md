---
title: Annullamento della chiamata
description: La notifica di annullamento della chiamata Annulla il funzionamento delle operazioni del servizio sul lato server e dei callback del modello di servizio.
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- Chiamare i servizi Web di annullamento per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5107f9ece421a3130f99c78b3b33788ee6c7e9f0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300708"
---
# <a name="call-cancellation"></a>Annullamento della chiamata

La notifica di annullamento della chiamata Annulla il funzionamento delle [operazioni del servizio sul lato server](server-side-service-operations.md) e dei callback del modello di servizio. Questo annullamento può essere dovuto a uno dei due motivi seguenti:

-   L'host del servizio ha interrotto le operazioni a causa di una chiamata alla funzione [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) .
-   Il canale sottostante ha generato un errore.


Per ricevere una notifica di annullamento, l'operazione del servizio o il callback del modello di servizio deve registrare una richiamata del [**callback di \_ annullamento dell'operazione \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) chiamando la funzione [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) .

Facoltativamente, durante la registrazione per la notifica di annullamento, l'operazione del servizio o il callback del modello di servizio può registrare anche i dati dello stato specifici dell'applicazione e il callback di [**\_ \_ \_ \_ callback dello stato libero dell'operazione WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) .

I dati relativi allo stato vengono resi disponibili per l' [**\_ operazione WS \_ Annulla \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback callback. Al completamento della chiamata, viene chiamato il callback di [**\_ \_ \_ \_ callback dello stato libero dell'operazione WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) per dare all'applicazione la possibilità di liberare i dati di stato.

Per un esempio di codice, vedere [BlockingServiceExample](blockingserviceexample.md).

Il callback di annullamento viene chiamato una sola volta per la durata delle [operazioni del servizio sul lato server](server-side-service-operations.md) o della funzione di callback.

L'annullamento della chiamata è disponibile in per tutti i callback dell'host del servizio che accettano il [ \_ \_ contesto dell'operazione WS](ws-operation-context.md) come parametro.

Gli elementi API seguenti sono correlati all'annullamento della chiamata.

| Callback                                                                         | Descrizione                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ annullamento callback operazione \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | Richiamato dal modello di servizio per notificare l'annullamento di un'operazione asincrona del servizio in seguito a un arresto interrotto dell'host del servizio. |
| [**\_ \_ \_ callback dello stato libero dell'operazione WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | Richiamato dal modello di servizio per consentire a un'applicazione di pulire i dati di stato registrati con il callback di annullamento.                |



 



| Funzione                                                             | Descrizione                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | Consente a un'operazione del servizio o a un callback del modello di servizio di registrarsi per una notifica di annullamento. |



 

 

 




