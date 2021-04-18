---
description: Il messaggio della linea \_ PROXYREQUEST di TAPI invia una richiesta a un gestore della funzione proxy registrato.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: Messaggio di LINE_PROXYREQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d536e85a9c773626bb5aacc4745d9d82817fe3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327983"
---
# <a name="line_proxyrequest-message"></a><span data-ttu-id="cd7da-103">\_Messaggio linea PROXYREQUEST</span><span class="sxs-lookup"><span data-stu-id="cd7da-103">LINE\_PROXYREQUEST message</span></span>

<span data-ttu-id="cd7da-104">Il messaggio della **linea \_ PROXYREQUEST** di TAPI invia una richiesta a un gestore della funzione proxy registrato.</span><span class="sxs-lookup"><span data-stu-id="cd7da-104">The TAPI **LINE\_PROXYREQUEST** message delivers a request to a registered proxy function handler.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="cd7da-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd7da-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd7da-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="cd7da-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="cd7da-107">Handle dell'applicazione per il dispositivo della linea in cui è stato modificato lo stato dell'agente.</span><span class="sxs-lookup"><span data-stu-id="cd7da-107">The application's handle to the line device on which the agent status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="cd7da-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="cd7da-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="cd7da-109">Istanza di callback fornita all'apertura della riga della chiamata.</span><span class="sxs-lookup"><span data-stu-id="cd7da-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="cd7da-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="cd7da-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="cd7da-111">Puntatore a una struttura [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) contenente la richiesta che deve essere elaborata dall'applicazione del gestore proxy.</span><span class="sxs-lookup"><span data-stu-id="cd7da-111">Pointer to a [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) structure containing the request to be processed by the proxy handler application.</span></span>

</dd> <dt>

<span data-ttu-id="cd7da-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="cd7da-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="cd7da-113">Riservato.</span><span class="sxs-lookup"><span data-stu-id="cd7da-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="cd7da-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="cd7da-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="cd7da-115">Riservato.</span><span class="sxs-lookup"><span data-stu-id="cd7da-115">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd7da-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd7da-116">Return value</span></span>

<span data-ttu-id="cd7da-117">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="cd7da-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd7da-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd7da-118">Remarks</span></span>

<span data-ttu-id="cd7da-119">Il messaggio di **riga \_ PROXYREQUEST** viene inviato solo alla prima applicazione registrata per gestire le richieste proxy del tipo recapitato.</span><span class="sxs-lookup"><span data-stu-id="cd7da-119">The **LINE\_PROXYREQUEST** message is sent only to the first application that registered to handle proxy requests of the type being delivered.</span></span>

<span data-ttu-id="cd7da-120">L'applicazione deve elaborare la richiesta contenuta nel buffer del proxy e chiamare [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) per restituire i dati o recapitare i risultati.</span><span class="sxs-lookup"><span data-stu-id="cd7da-120">The application should process the request contained in the proxy buffer and call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) to return data or deliver results.</span></span> <span data-ttu-id="cd7da-121">L'elaborazione della richiesta deve essere eseguita nel contesto della funzione di callback TAPI dell'applicazione solo se può essere eseguita immediatamente, senza attendere la risposta da nessun'altra entità.</span><span class="sxs-lookup"><span data-stu-id="cd7da-121">Processing of the request should be done within the context of the application's TAPI callback function only if it can be performed immediately, without waiting for response from any other entity.</span></span> <span data-ttu-id="cd7da-122">Se l'applicazione deve comunicare con altre entità, ad esempio un provider di servizi per gestire ACD basato su PBX o qualsiasi altro servizio di sistema che potrebbe causare il blocco, la richiesta deve essere accodata all'interno dell'applicazione e la funzione di callback è stata chiusa per evitare di ritardare la ricezione di altri messaggi TAPI dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cd7da-122">If the application needs to communicate with other entities (for example, a service provider to handle PBX-based ACD, or any other system service which might result in blocking), then the request should be queued within the application and the callback function exited to avoid delaying the receipt of further TAPI messages by the application.</span></span>

<span data-ttu-id="cd7da-123">Nel momento in cui la **riga \_ PROXYREQUEST** viene recapitata al gestore del proxy, TAPI ha già restituito un risultato positivo della funzione *dwRequestID* nell'applicazione originale e ha sbloccato il thread chiamante per continuare l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="cd7da-123">At the time the **LINE\_PROXYREQUEST** is delivered to the proxy handler, TAPI has already returned a positive *dwRequestID* function result to the original application and unblocked the calling thread to continue execution.</span></span> <span data-ttu-id="cd7da-124">L'applicazione è in attesa di un messaggio di [**\_ risposta di riga**](line-reply.md) , che viene generato automaticamente quando l'applicazione del gestore del proxy chiama [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span><span class="sxs-lookup"><span data-stu-id="cd7da-124">The application is awaiting a [**LINE\_REPLY**](line-reply.md) message, which is automatically generated when the proxy handler application calls [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span></span>

<span data-ttu-id="cd7da-125">L'applicazione non deve liberare la memoria a cui punta *lpProxyRequest*.</span><span class="sxs-lookup"><span data-stu-id="cd7da-125">The application shall not free the memory pointed to by *lpProxyRequest*.</span></span> <span data-ttu-id="cd7da-126">TAPI libera la memoria durante l'esecuzione di [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span><span class="sxs-lookup"><span data-stu-id="cd7da-126">TAPI frees the memory during the execution of [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span></span> <span data-ttu-id="cd7da-127">L'applicazione può chiamare [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) esattamente una volta per ogni messaggio di **riga \_ PROXYREQUEST** .</span><span class="sxs-lookup"><span data-stu-id="cd7da-127">The application can call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) exactly once for each **LINE\_PROXYREQUEST** message.</span></span>

<span data-ttu-id="cd7da-128">Se l'applicazione riceve un messaggio di [**\_ chiusura riga**](line-close.md) mentre contiene richieste proxy in sospeso, deve chiamare [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) per ogni richiesta in sospeso, passando un valore *dwResult* appropriato, ad esempio LINEERR \_ OPERATIONFAILED.</span><span class="sxs-lookup"><span data-stu-id="cd7da-128">If the application receives a [**LINE\_CLOSE**](line-close.md) message while it has pending proxy requests, it should call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) for each pending request, passing in an appropriate *dwResult* value (such as LINEERR\_OPERATIONFAILED).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd7da-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd7da-129">Requirements</span></span>



| <span data-ttu-id="cd7da-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd7da-130">Requirement</span></span> | <span data-ttu-id="cd7da-131">Valore</span><span class="sxs-lookup"><span data-stu-id="cd7da-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cd7da-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="cd7da-132">TAPI version</span></span><br/> | <span data-ttu-id="cd7da-133">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="cd7da-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="cd7da-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd7da-134">Header</span></span><br/>       | <dl> <span data-ttu-id="cd7da-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd7da-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd7da-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd7da-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd7da-137">**\_chiusura riga**</span><span class="sxs-lookup"><span data-stu-id="cd7da-137">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="cd7da-138">**\_risposta riga**</span><span class="sxs-lookup"><span data-stu-id="cd7da-138">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="cd7da-139">**LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="cd7da-139">**LINEPROXYREQUEST**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[<span data-ttu-id="cd7da-140">**lineProxyResponse**</span><span class="sxs-lookup"><span data-stu-id="cd7da-140">**lineProxyResponse**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




