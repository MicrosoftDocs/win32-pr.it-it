---
description: Il messaggio di generazione della linea TAPI \_ viene inviato per notificare all'applicazione che la cifra corrente o la generazione di un tono è stata interrotta.
ms.assetid: 375823c5-22c2-4010-bfb4-5b8b46141c72
title: Messaggio di LINE_GENERATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916dc95d1a6343b0f8ebc0eef9e589b04aa2112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330743"
---
# <a name="line_generate-message"></a><span data-ttu-id="7d5ca-103">\_Messaggio di generazione riga</span><span class="sxs-lookup"><span data-stu-id="7d5ca-103">LINE\_GENERATE message</span></span>

<span data-ttu-id="7d5ca-104">Il messaggio **di \_ generazione della linea** TAPI viene inviato per notificare all'applicazione che la cifra corrente o la generazione di un tono è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="7d5ca-104">The TAPI **LINE\_GENERATE** message is sent to notify the application that the current digit or tone generation has terminated.</span></span> <span data-ttu-id="7d5ca-105">Solo una di queste richieste di generazione può essere in corso una determinata chiamata in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="7d5ca-105">Only one such generation request can be in progress an a given call at any time.</span></span> <span data-ttu-id="7d5ca-106">Questo messaggio viene inviato anche quando viene annullata la generazione di numeri o toni.</span><span class="sxs-lookup"><span data-stu-id="7d5ca-106">This message is also sent when digit or tone generation is canceled.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="7d5ca-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d5ca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d5ca-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="7d5ca-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="7d5ca-109">Handle della chiamata.</span><span class="sxs-lookup"><span data-stu-id="7d5ca-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="7d5ca-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="7d5ca-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="7d5ca-111">Istanza di callback fornita all'apertura della riga.</span><span class="sxs-lookup"><span data-stu-id="7d5ca-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="7d5ca-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="7d5ca-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="7d5ca-113">Motivo per cui la generazione di numeri o toni è stata terminata.</span><span class="sxs-lookup"><span data-stu-id="7d5ca-113">The reason why digit or tone generation was terminated.</span></span> <span data-ttu-id="7d5ca-114">Questo parametro deve essere costituito solo da una delle [**\_ costanti LINEGENERATETERM**](linegenerateterm--constants.md).</span><span class="sxs-lookup"><span data-stu-id="7d5ca-114">This parameter must be one and only one of the [**LINEGENERATETERM\_ constants**](linegenerateterm--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d5ca-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="7d5ca-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="7d5ca-116">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7d5ca-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="7d5ca-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="7d5ca-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="7d5ca-118">"Conteggio dei cicli" (numero di millisecondi dall'avvio di Windows) in corrispondenza del quale la cifra o la generazione del tono è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7d5ca-118">The "tick count" (number of milliseconds since Windows started) at which the digit or tone generation completed.</span></span> <span data-ttu-id="7d5ca-119">Per le versioni API precedenti alla 2,0, questo parametro è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="7d5ca-119">For API versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d5ca-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d5ca-120">Return value</span></span>

<span data-ttu-id="7d5ca-121">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="7d5ca-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d5ca-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d5ca-122">Remarks</span></span>

<span data-ttu-id="7d5ca-123">Il **messaggio \_ di generazione riga** viene inviato solo all'applicazione che ha richiesto la generazione di numeri o toni.</span><span class="sxs-lookup"><span data-stu-id="7d5ca-123">The **LINE\_GENERATE** message is only sent to the application that requested the digit or tone generation.</span></span>

<span data-ttu-id="7d5ca-124">Poiché è possibile che il timestamp specificato da *dwParam3* sia stato generato in un computer diverso da quello in cui è in esecuzione l'applicazione, è utile solo per il confronto con altri messaggi con timestamp analoghi generati sullo stesso dispositivo a linee ( [**linea \_ GATHERDIGITS**](line-gatherdigits.md), [**linea \_ MONITORDIGITS**](line-monitordigits.md), [**riga \_ MONITORMEDIA**](line-monitormedia.md), [**linea \_ MONITORTONE**](line-monitortone.md)), per determinare la tempistica relativa (separazione tra gli eventi).</span><span class="sxs-lookup"><span data-stu-id="7d5ca-124">Because the timestamp specified by *dwParam3* may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="7d5ca-125">Il numero di cicli può essere "avvolto" dopo circa 49,7 giorni. Quando si eseguono calcoli, le applicazioni devono tenere conto di questo.</span><span class="sxs-lookup"><span data-stu-id="7d5ca-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="7d5ca-126">Se il provider di servizi non genera il timestamp (ad esempio, se è stato creato con una versione precedente di TAPI), TAPI fornisce un timestamp nel punto più vicino al provider di servizi che genera l'evento in modo che il timestamp sintetizzato sia il più accurato possibile.</span><span class="sxs-lookup"><span data-stu-id="7d5ca-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d5ca-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d5ca-127">Requirements</span></span>



| <span data-ttu-id="7d5ca-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d5ca-128">Requirement</span></span> | <span data-ttu-id="7d5ca-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7d5ca-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7d5ca-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7d5ca-130">TAPI version</span></span><br/> | <span data-ttu-id="7d5ca-131">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7d5ca-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7d5ca-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d5ca-132">Header</span></span><br/>       | <dl> <span data-ttu-id="7d5ca-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d5ca-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d5ca-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d5ca-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d5ca-135">**LINEA \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="7d5ca-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="7d5ca-136">**LINEA \_ MONITORDIGITS**</span><span class="sxs-lookup"><span data-stu-id="7d5ca-136">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="7d5ca-137">**LINEA \_ MONITORMEDIA**</span><span class="sxs-lookup"><span data-stu-id="7d5ca-137">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="7d5ca-138">**LINEA \_ MONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="7d5ca-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> </dl>

 

 




