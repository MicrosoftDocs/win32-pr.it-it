---
title: Annullamento delle chiamate
description: La notifica di annullamento delle chiamate annulla il funzionamento delle operazioni del servizio lato server e dei callback del modello di servizio.
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- Chiamare i servizi Web di annullamento per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda4ec4227403bed5239b68cfa05d2064976517a7473fa7926c8de5f56227645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026699"
---
# <a name="call-cancellation"></a>Annullamento delle chiamate

La notifica di annullamento delle chiamate annulla il funzionamento delle [operazioni del servizio lato server](server-side-service-operations.md) e dei callback del modello di servizio. L'annullamento può essere per uno dei due motivi seguenti:

-   L'host del servizio ha arrestato le operazioni a causa di una chiamata alla [**funzione WsAbortServiceHost.**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)
-   Il canale sottostante ha generato un errore.


Per ricevere una notifica di annullamento, l'operazione del servizio o il callback del modello di servizio deve registrare un callback [**WS \_ OPERATION CANCEL \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) chiamando la [**funzione WsRegisterOperationForCancel.**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel)

Facoltativamente, come parte della registrazione per la notifica di annullamento, l'operazione del servizio o il callback del modello di servizio può anche registrare dati di stato specifici dell'applicazione e il callback [**WS \_ OPERATION FREE \_ STATE \_ \_ CALLBACK.**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)

I dati sullo stato vengono resi disponibili per il callback [**WS \_ OPERATION CANCEL \_ \_ CALLBACK.**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) Al completamento della chiamata, viene chiamato il callback [**WS \_ OPERATION FREE STATE \_ \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) per offrire all'applicazione la possibilità di liberare i dati sullo stato.

Per un esempio di codice, vedere [BlockingServiceExample.](blockingserviceexample.md)

Il callback di annullamento viene chiamato una sola volta per la durata delle operazioni del servizio [lato server](server-side-service-operations.md) o della funzione di callback.

L'annullamento delle chiamate è disponibile in per tutti i callback dell'host del servizio che [accettano WS \_ OPERATION \_ CONTEXT](ws-operation-context.md) come parametro.

Gli elementi API seguenti sono correlati all'annullamento delle chiamate.

| Callback                                                                         | Descrizione                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**CALLBACK DI \_ ANNULLAMENTO \_ DELL'OPERAZIONE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | Richiamato dal modello di servizio per notificare l'annullamento di un'operazione asincrona del servizio in seguito a un arresto interrotto dell'host del servizio. |
| [**CALLBACK DELLO \_ STATO \_ LIBERO \_ DELL'OPERAZIONE \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | Richiamato dal modello di servizio per consentire a un'applicazione di pulire i dati sullo stato registrati con il callback di annullamento.                |



 



| Funzione                                                             | Descrizione                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | Consente a un'operazione del servizio o a un callback del modello di servizio di registrarsi per una notifica di annullamento. |



 

 

 




