---
title: Elaborazione delle richieste
description: Le richieste di elaborazione includono quattro passaggi.
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e820d425e44daab9d687d1d43b756b833582a092
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "103885901"
---
# <a name="processing-requests"></a><span data-ttu-id="5ae7d-103">Elaborazione delle richieste</span><span class="sxs-lookup"><span data-stu-id="5ae7d-103">Processing Requests</span></span>

<span data-ttu-id="5ae7d-104">Le richieste di elaborazione includono quattro passaggi:</span><span class="sxs-lookup"><span data-stu-id="5ae7d-104">Processing requests includes four steps:</span></span>

-   <span data-ttu-id="5ae7d-105">Ricezione di una richiesta</span><span class="sxs-lookup"><span data-stu-id="5ae7d-105">Receiving a request</span></span>
-   <span data-ttu-id="5ae7d-106">Gestione della richiesta</span><span class="sxs-lookup"><span data-stu-id="5ae7d-106">Handling the request</span></span>
-   <span data-ttu-id="5ae7d-107">Invio della risposta</span><span class="sxs-lookup"><span data-stu-id="5ae7d-107">Sending the response</span></span>
-   <span data-ttu-id="5ae7d-108">Annullamento di richieste che non possono essere elaborate</span><span class="sxs-lookup"><span data-stu-id="5ae7d-108">Canceling requests that cannot be processed</span></span>

![Diagramma che mostra il ciclo di richiesta di elaborazione.](images/processloop.png)

## <a name="receiving-a-request"></a><span data-ttu-id="5ae7d-110">Ricezione di una richiesta</span><span class="sxs-lookup"><span data-stu-id="5ae7d-110">Receiving a Request</span></span>

<span data-ttu-id="5ae7d-111">L'API server HTTP fornisce una struttura di richiesta per archiviare la richiesta in ingresso analizzata.</span><span class="sxs-lookup"><span data-stu-id="5ae7d-111">The HTTP Server API supplies a request structure to store the parsed incoming request.</span></span> <span data-ttu-id="5ae7d-112">Questa struttura viene allocata dall'applicazione e inizializzata quando viene ricevuta una richiesta in ingresso.</span><span class="sxs-lookup"><span data-stu-id="5ae7d-112">This structure is allocated by the application, and initialized when an incoming request is received.</span></span> <span data-ttu-id="5ae7d-113">L'applicazione chiama la funzione [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) per ricevere la richiesta.</span><span class="sxs-lookup"><span data-stu-id="5ae7d-113">The application calls the [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) function to receive the request.</span></span> <span data-ttu-id="5ae7d-114">Se il buffer di richiesta è troppo piccolo per ricevere la richiesta, l'applicazione può aumentare le dimensioni del buffer e chiamare di nuovo **HttpReceiveHttpRequest** per ricevere l'intera richiesta.</span><span class="sxs-lookup"><span data-stu-id="5ae7d-114">If the request buffer is too small to receive the request, the application can increase the buffer size and call **HttpReceiveHttpRequest** again to receive the entire request.</span></span>

<span data-ttu-id="5ae7d-115">Se la richiesta include dati del corpo dell'entità da ricevere, le applicazioni chiamano [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) con l'ID richiesta restituito nel parametro *pRequestBuffer* durante la chiamata a [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).</span><span class="sxs-lookup"><span data-stu-id="5ae7d-115">If the request includes entity body data to be received, the applications calls [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) with the request ID returned in the *pRequestBuffer* parameter during the call to [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).</span></span>

## <a name="handling-the-request"></a><span data-ttu-id="5ae7d-116">Gestione della richiesta</span><span class="sxs-lookup"><span data-stu-id="5ae7d-116">Handling the Request</span></span>

<span data-ttu-id="5ae7d-117">L'applicazione esegue l'elaborazione della richiesta specifica dell'applicazione e formula una risposta.</span><span class="sxs-lookup"><span data-stu-id="5ae7d-117">The application performs application-specific processing of the request and formulates a response.</span></span> <span data-ttu-id="5ae7d-118">L'API server HTTP non impone alcun timeout per questo processo.</span><span class="sxs-lookup"><span data-stu-id="5ae7d-118">The HTTP Server API imposes no timeout on this process.</span></span>

## <a name="sending-the-response"></a><span data-ttu-id="5ae7d-119">Invio della risposta</span><span class="sxs-lookup"><span data-stu-id="5ae7d-119">Sending the Response</span></span>

<span data-ttu-id="5ae7d-120">Al termine della gestione della richiesta e della formulazione della risposta, l'applicazione chiama la funzione [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) per inviare la risposta.</span><span class="sxs-lookup"><span data-stu-id="5ae7d-120">When the application is finished handling the request and formulating the response, it calls the [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) function to send the response.</span></span> <span data-ttu-id="5ae7d-121">Se la risposta include i dati del corpo dell'entità da inviare, l'applicazione chiama anche [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).</span><span class="sxs-lookup"><span data-stu-id="5ae7d-121">If the response includes entity body data to send, the application also calls [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).</span></span>

## <a name="canceling-requests"></a><span data-ttu-id="5ae7d-122">Annullamento di richieste</span><span class="sxs-lookup"><span data-stu-id="5ae7d-122">Canceling Requests</span></span>

<span data-ttu-id="5ae7d-123">Dopo che l'applicazione ha ricevuto un ID richiesta dalla relativa chiamata a [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), può in qualsiasi momento annullare la richiesta chiamando [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).</span><span class="sxs-lookup"><span data-stu-id="5ae7d-123">After the application has received a request ID from its call to [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), it can at any time cancel the request by calling [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).</span></span>

 

 




