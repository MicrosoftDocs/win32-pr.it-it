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
# <a name="call-cancellation"></a><span data-ttu-id="48405-106">Annullamento della chiamata</span><span class="sxs-lookup"><span data-stu-id="48405-106">Call cancellation</span></span>

<span data-ttu-id="48405-107">La notifica di annullamento della chiamata Annulla il funzionamento delle [operazioni del servizio sul lato server](server-side-service-operations.md) e dei callback del modello di servizio.</span><span class="sxs-lookup"><span data-stu-id="48405-107">Call cancellation notification cancels the operation of [server side service operations](server-side-service-operations.md) and service-model callbacks.</span></span> <span data-ttu-id="48405-108">Questo annullamento può essere dovuto a uno dei due motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="48405-108">Such cancellation can be for one of two reasons:</span></span>

-   <span data-ttu-id="48405-109">L'host del servizio ha interrotto le operazioni a causa di una chiamata alla funzione [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) .</span><span class="sxs-lookup"><span data-stu-id="48405-109">The service host has stopped operations because of a call to the [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) function.</span></span>
-   <span data-ttu-id="48405-110">Il canale sottostante ha generato un errore.</span><span class="sxs-lookup"><span data-stu-id="48405-110">The underlying channel has raised a fault.</span></span>


<span data-ttu-id="48405-111">Per ricevere una notifica di annullamento, l'operazione del servizio o il callback del modello di servizio deve registrare una richiamata del [**callback di \_ annullamento dell'operazione \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) chiamando la funzione [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) .</span><span class="sxs-lookup"><span data-stu-id="48405-111">To receive a cancellation notification, the service operation or service-model callback must register a [**WS\_OPERATION\_CANCEL\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback by calling the [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) function.</span></span>

<span data-ttu-id="48405-112">Facoltativamente, durante la registrazione per la notifica di annullamento, l'operazione del servizio o il callback del modello di servizio può registrare anche i dati dello stato specifici dell'applicazione e il callback di [**\_ \_ \_ \_ callback dello stato libero dell'operazione WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) .</span><span class="sxs-lookup"><span data-stu-id="48405-112">Optionally, as part of the registering for cancellation notification, the service operation or service-model callback can also register application-specific state data and the [**WS\_OPERATION\_FREE\_STATE\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) callback.</span></span>

<span data-ttu-id="48405-113">I dati relativi allo stato vengono resi disponibili per l' [**\_ operazione WS \_ Annulla \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback callback.</span><span class="sxs-lookup"><span data-stu-id="48405-113">The state data is made available to the [**WS\_OPERATION\_CANCEL\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback.</span></span> <span data-ttu-id="48405-114">Al completamento della chiamata, viene chiamato il callback di [**\_ \_ \_ \_ callback dello stato libero dell'operazione WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) per dare all'applicazione la possibilità di liberare i dati di stato.</span><span class="sxs-lookup"><span data-stu-id="48405-114">On call completion, the [**WS\_OPERATION\_FREE\_STATE\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) callback is called to give the application an opportunity to free the state data.</span></span>

<span data-ttu-id="48405-115">Per un esempio di codice, vedere [BlockingServiceExample](blockingserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="48405-115">For a code example, see [BlockingServiceExample](blockingserviceexample.md).</span></span>

<span data-ttu-id="48405-116">Il callback di annullamento viene chiamato una sola volta per la durata delle [operazioni del servizio sul lato server](server-side-service-operations.md) o della funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="48405-116">The cancellation callback is called only once for the lifetime of the [server side service operations](server-side-service-operations.md) or callback function.</span></span>

<span data-ttu-id="48405-117">L'annullamento della chiamata è disponibile in per tutti i callback dell'host del servizio che accettano il [ \_ \_ contesto dell'operazione WS](ws-operation-context.md) come parametro.</span><span class="sxs-lookup"><span data-stu-id="48405-117">Call cancellation is available in for all service host callbacks that take [WS\_OPERATION\_CONTEXT](ws-operation-context.md) as a parameter.</span></span>

<span data-ttu-id="48405-118">Gli elementi API seguenti sono correlati all'annullamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="48405-118">The following API elements relate to call cancellation.</span></span>

| <span data-ttu-id="48405-119">Callback</span><span class="sxs-lookup"><span data-stu-id="48405-119">Callback</span></span>                                                                         | <span data-ttu-id="48405-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48405-120">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48405-121">**\_ \_ annullamento callback operazione \_ WS**</span><span class="sxs-lookup"><span data-stu-id="48405-121">**WS\_OPERATION\_CANCEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | <span data-ttu-id="48405-122">Richiamato dal modello di servizio per notificare l'annullamento di un'operazione asincrona del servizio in seguito a un arresto interrotto dell'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="48405-122">Invoked by service model to notify a cancellation of an asynchronous service operation as a result of an aborted shutdown of service host.</span></span> |
| [<span data-ttu-id="48405-123">**\_ \_ \_ callback dello stato libero dell'operazione WS \_**</span><span class="sxs-lookup"><span data-stu-id="48405-123">**WS\_OPERATION\_FREE\_STATE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | <span data-ttu-id="48405-124">Richiamato dal modello di servizio per consentire a un'applicazione di pulire i dati di stato registrati con il callback di annullamento.</span><span class="sxs-lookup"><span data-stu-id="48405-124">Invoked by service model to allow an application to clean up state data that was registered with the cancellation callback.</span></span>                |



 



| <span data-ttu-id="48405-125">Funzione</span><span class="sxs-lookup"><span data-stu-id="48405-125">Function</span></span>                                                             | <span data-ttu-id="48405-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48405-126">Description</span></span>                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48405-127">**WsRegisterOperationForCancel**</span><span class="sxs-lookup"><span data-stu-id="48405-127">**WsRegisterOperationForCancel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | <span data-ttu-id="48405-128">Consente a un'operazione del servizio o a un callback del modello di servizio di registrarsi per una notifica di annullamento.</span><span class="sxs-lookup"><span data-stu-id="48405-128">Allows a service operation or service-model callback to register for a cancellation notification.</span></span> |



 

 

 




