---
description: Il messaggio della linea TAPI \_ GATHERDIGITS viene inviato quando la richiesta corrente di raccolta di cifre memorizzata nel buffer viene terminata o annullata. Il buffer delle cifre può essere esaminato dopo che il messaggio è stato ricevuto dall'applicazione.
ms.assetid: 0d27904d-9743-44bf-a7bc-132459351e01
title: Messaggio di LINE_GATHERDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0c67c5a9bbd3f798a8f4343b36c311309633ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327408"
---
# <a name="line_gatherdigits-message"></a><span data-ttu-id="29b65-104">\_Messaggio linea GATHERDIGITS</span><span class="sxs-lookup"><span data-stu-id="29b65-104">LINE\_GATHERDIGITS message</span></span>

<span data-ttu-id="29b65-105">Il messaggio della **linea TAPI \_ GATHERDIGITS** viene inviato quando la richiesta corrente di raccolta di cifre memorizzata nel buffer viene terminata o annullata.</span><span class="sxs-lookup"><span data-stu-id="29b65-105">The TAPI **LINE\_GATHERDIGITS** message is sent when the current buffered digit-gathering request has terminated or is canceled.</span></span> <span data-ttu-id="29b65-106">Il buffer delle cifre può essere esaminato dopo che il messaggio è stato ricevuto dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="29b65-106">The digit buffer can be examined after this message has been received by the application.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="29b65-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="29b65-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29b65-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="29b65-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="29b65-109">Handle della chiamata.</span><span class="sxs-lookup"><span data-stu-id="29b65-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="29b65-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="29b65-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="29b65-111">Istanza di callback fornita all'apertura della riga.</span><span class="sxs-lookup"><span data-stu-id="29b65-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="29b65-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="29b65-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="29b65-113">Motivo per cui la raccolta di cifre è stata terminata.</span><span class="sxs-lookup"><span data-stu-id="29b65-113">The reason why digit gathering was terminated.</span></span> <span data-ttu-id="29b65-114">Questo parametro deve essere costituito solo da una delle [**\_ costanti LINEGATHERTERM**](linegatherterm--constants.md).</span><span class="sxs-lookup"><span data-stu-id="29b65-114">This parameter must be one and only one of the [**LINEGATHERTERM\_ constants**](linegatherterm--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="29b65-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="29b65-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="29b65-116">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="29b65-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="29b65-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="29b65-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="29b65-118">"Conteggio dei cicli" (numero di millisecondi dall'avvio di Windows) in corrispondenza del quale è stata completata la raccolta delle cifre.</span><span class="sxs-lookup"><span data-stu-id="29b65-118">The "tick count" (number of milliseconds since Windows started) at which the digit gathering completed.</span></span> <span data-ttu-id="29b65-119">Per le versioni TAPI precedenti alla 2,0, questo parametro è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="29b65-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29b65-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29b65-120">Return value</span></span>

<span data-ttu-id="29b65-121">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="29b65-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29b65-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="29b65-122">Remarks</span></span>

<span data-ttu-id="29b65-123">Il messaggio di **riga \_ GATHERDIGITS** viene inviato all'applicazione che ha avviato la raccolta di cifre sulla chiamata usando [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).</span><span class="sxs-lookup"><span data-stu-id="29b65-123">The **LINE\_GATHERDIGITS** message is only sent to the application that initiated the digit gathering on the call using [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits).</span></span>

<span data-ttu-id="29b65-124">Se la funzione [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) viene usata per annullare una richiesta precedente per la raccolta di cifre, TAPI invia un messaggio di **\_ GATHERDIGITS di riga** con *dwParam1* impostato su LINEGATHERTERM \_ Annulla per l'applicazione che indica che il buffer specificato in origine contiene le cifre raccolte fino all'annullamento.</span><span class="sxs-lookup"><span data-stu-id="29b65-124">If the [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) function is used to cancel a previous request to gather digits, TAPI sends a **LINE\_GATHERDIGITS** message with *dwParam1* set to LINEGATHERTERM\_CANCEL to the application indicating that the originally specified buffer contains the digits gathered up to the cancellation.</span></span>

<span data-ttu-id="29b65-125">Poiché è possibile che il timestamp specificato da *dwParam3* sia stato generato in un computer diverso da quello in cui è in esecuzione l'applicazione, è utile solo per il confronto con altri messaggi con timestamp analoghi generati sullo stesso dispositivo a linee ( [**riga \_ generazione**](line-generate.md), [**riga \_ MONITORDIGITS**](line-monitordigits.md), [**riga \_ MONITORMEDIA**](line-monitormedia.md), [**riga \_ MONITORTONE**](line-monitortone.md)), per determinare la tempistica relativa (separazione tra gli eventi).</span><span class="sxs-lookup"><span data-stu-id="29b65-125">Because the timestamp specified by *dwParam3* may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="29b65-126">Il numero di cicli può essere "avvolto" dopo circa 49,7 giorni. Quando si eseguono calcoli, le applicazioni devono tenere conto di questo.</span><span class="sxs-lookup"><span data-stu-id="29b65-126">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="29b65-127">Se il provider di servizi non genera il timestamp (ad esempio, se è stato creato con una versione precedente di TAPI), TAPI fornisce un timestamp nel punto più vicino al provider di servizi che genera l'evento in modo che il timestamp sintetizzato sia il più accurato possibile.</span><span class="sxs-lookup"><span data-stu-id="29b65-127">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

> [!Note]  
> <span data-ttu-id="29b65-128">Quando un'applicazione richiama qualsiasi operazione asincrona che scrive i dati nella memoria dell'applicazione, l'applicazione deve mantenuta la memoria disponibile per la scrittura fino a quando non viene ricevuta una [**\_ risposta di riga**](line-reply.md) o un messaggio **\_ GATHERDIGITS** .</span><span class="sxs-lookup"><span data-stu-id="29b65-128">When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a [**LINE\_REPLY**](line-reply.md) or **LINE\_GATHERDIGITS** message is received.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="29b65-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29b65-129">Requirements</span></span>



| <span data-ttu-id="29b65-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="29b65-130">Requirement</span></span> | <span data-ttu-id="29b65-131">Valore</span><span class="sxs-lookup"><span data-stu-id="29b65-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="29b65-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="29b65-132">TAPI version</span></span><br/> | <span data-ttu-id="29b65-133">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="29b65-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="29b65-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29b65-134">Header</span></span><br/>       | <dl> <span data-ttu-id="29b65-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="29b65-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29b65-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29b65-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29b65-137">**\_generazione riga**</span><span class="sxs-lookup"><span data-stu-id="29b65-137">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="29b65-138">**LINEA \_ MONITORDIGITS**</span><span class="sxs-lookup"><span data-stu-id="29b65-138">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="29b65-139">**LINEA \_ MONITORMEDIA**</span><span class="sxs-lookup"><span data-stu-id="29b65-139">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="29b65-140">**LINEA \_ MONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="29b65-140">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> <dt>

[<span data-ttu-id="29b65-141">**\_risposta riga**</span><span class="sxs-lookup"><span data-stu-id="29b65-141">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="29b65-142">**lineGatherDigits**</span><span class="sxs-lookup"><span data-stu-id="29b65-142">**lineGatherDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)
</dt> </dl>

 

 




