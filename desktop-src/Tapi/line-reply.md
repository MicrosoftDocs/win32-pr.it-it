---
description: Il messaggio di risposta della linea TAPI \_ viene inviato per segnalare i risultati delle chiamate di funzione completate in modo asincrono.
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: Messaggio di LINE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed963a777a5073b0182e809eec83fb7f904768e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332918"
---
# <a name="line_reply-message"></a><span data-ttu-id="15651-103">Messaggio di risposta di riga \_</span><span class="sxs-lookup"><span data-stu-id="15651-103">LINE\_REPLY message</span></span>

<span data-ttu-id="15651-104">Il messaggio **di \_ risposta della linea** TAPI viene inviato per segnalare i risultati delle chiamate di funzione completate in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="15651-104">The TAPI **LINE\_REPLY** message is sent to report the results of function calls that completed asynchronously.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="15651-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="15651-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15651-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="15651-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="15651-107">Non usato.</span><span class="sxs-lookup"><span data-stu-id="15651-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="15651-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="15651-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="15651-109">Restituisce l'istanza di callback dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="15651-109">Returns the application's callback instance.</span></span>

</dd> <dt>

<span data-ttu-id="15651-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="15651-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="15651-111">Identificatore della richiesta per cui si tratta della risposta.</span><span class="sxs-lookup"><span data-stu-id="15651-111">The request identifier for which this is the reply.</span></span>

</dd> <dt>

<span data-ttu-id="15651-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="15651-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="15651-113">Indicazione di esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="15651-113">The success or error indication.</span></span> <span data-ttu-id="15651-114">L'applicazione deve eseguire il cast di questo parametro in un valore LONG.</span><span class="sxs-lookup"><span data-stu-id="15651-114">The application should cast this parameter into a LONG.</span></span> <span data-ttu-id="15651-115">Zero indica esito positivo; un numero negativo indica un errore.</span><span class="sxs-lookup"><span data-stu-id="15651-115">Zero indicates success; a negative number indicates an error.</span></span>

</dd> <dt>

<span data-ttu-id="15651-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="15651-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="15651-117">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="15651-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15651-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15651-118">Return value</span></span>

<span data-ttu-id="15651-119">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="15651-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15651-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="15651-120">Remarks</span></span>

<span data-ttu-id="15651-121">Le funzioni che operano in modo asincrono restituiscono un valore di identificatore di richiesta positivo all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="15651-121">Functions that operate asynchronously return a positive request identifier value to the application.</span></span> <span data-ttu-id="15651-122">Questo identificatore di richiesta viene restituito con il messaggio di risposta per identificare la richiesta completata.</span><span class="sxs-lookup"><span data-stu-id="15651-122">This request identifier is returned with the reply message to identify the request that was completed.</span></span> <span data-ttu-id="15651-123">L'altro parametro per il messaggio di **\_ risposta di riga** contiene l'indicazione di esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="15651-123">The other parameter for the **LINE\_REPLY** message carries the success or failure indication.</span></span> <span data-ttu-id="15651-124">Gli errori possibili sono gli stessi di quelli definiti dalla funzione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="15651-124">Possible errors are the same as those defined by the corresponding function.</span></span> <span data-ttu-id="15651-125">Questo messaggio non può essere disabilitato.</span><span class="sxs-lookup"><span data-stu-id="15651-125">This message cannot be disabled.</span></span>

<span data-ttu-id="15651-126">In alcuni casi, un'applicazione potrebbe non essere in grado di ricevere il messaggio di **\_ risposta di riga** corrispondente a una chiamata a una funzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="15651-126">In some cases, an application may fail to receive the **LINE\_REPLY** message corresponding to a call to an asynchronous function.</span></span> <span data-ttu-id="15651-127">Questo errore si verifica se l'handle di chiamata corrispondente viene deallocato prima che il messaggio sia stato ricevuto.</span><span class="sxs-lookup"><span data-stu-id="15651-127">This occurs if the corresponding call handle is deallocated before the message has been received.</span></span>

> [!Note]  
> <span data-ttu-id="15651-128">Quando un'applicazione richiama qualsiasi operazione asincrona che scrive i dati nella memoria dell'applicazione, l'applicazione deve mantenuta la memoria disponibile per la scrittura fino a quando non viene ricevuta una **\_ risposta di riga** o un messaggio [**\_ GATHERDIGITS**](line-gatherdigits.md) .</span><span class="sxs-lookup"><span data-stu-id="15651-128">When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a **LINE\_REPLY** or [**LINE\_GATHERDIGITS**](line-gatherdigits.md) message is received.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="15651-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15651-129">Requirements</span></span>



| <span data-ttu-id="15651-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="15651-130">Requirement</span></span> | <span data-ttu-id="15651-131">Valore</span><span class="sxs-lookup"><span data-stu-id="15651-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="15651-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="15651-132">TAPI version</span></span><br/> | <span data-ttu-id="15651-133">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="15651-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="15651-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15651-134">Header</span></span><br/>       | <dl> <span data-ttu-id="15651-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="15651-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15651-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15651-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15651-137">**LINEA \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="15651-137">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> </dl>

 

 




