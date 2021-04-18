---
description: Il messaggio MONITORDIGITS della linea TAPI \_ viene inviato quando viene rilevata una cifra. L'invio di questo messaggio viene controllato con la funzione lineMonitorDigits.
ms.assetid: 1c1a729c-a6bb-4432-9617-4a892c76cb8d
title: Messaggio di LINE_MONITORDIGITS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6e85ed515d20c18c6e41cdb185b036312c54ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328426"
---
# <a name="line_monitordigits-message"></a><span data-ttu-id="09bcf-104">\_Messaggio linea MONITORDIGITS</span><span class="sxs-lookup"><span data-stu-id="09bcf-104">LINE\_MONITORDIGITS message</span></span>

<span data-ttu-id="09bcf-105">Il messaggio **\_ MONITORDIGITS della linea** TAPI viene inviato quando viene rilevata una cifra.</span><span class="sxs-lookup"><span data-stu-id="09bcf-105">The TAPI **LINE\_MONITORDIGITS** message is sent when a digit is detected.</span></span> <span data-ttu-id="09bcf-106">L'invio di questo messaggio viene controllato con la funzione [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) .</span><span class="sxs-lookup"><span data-stu-id="09bcf-106">The sending of this message is controlled with the [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="09bcf-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="09bcf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09bcf-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="09bcf-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="09bcf-109">Handle della chiamata.</span><span class="sxs-lookup"><span data-stu-id="09bcf-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="09bcf-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="09bcf-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="09bcf-111">Istanza di callback fornita all'apertura della riga della chiamata.</span><span class="sxs-lookup"><span data-stu-id="09bcf-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="09bcf-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="09bcf-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="09bcf-113">Il byte di ordine inferiore contiene l'ultima cifra ricevuta in una rappresentazione di testo.</span><span class="sxs-lookup"><span data-stu-id="09bcf-113">The low-order byte contains the last digit received in a text representation.</span></span>

</dd> <dt>

<span data-ttu-id="09bcf-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="09bcf-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="09bcf-115">Modalità di cifra rilevata.</span><span class="sxs-lookup"><span data-stu-id="09bcf-115">The digit mode that was detected.</span></span> <span data-ttu-id="09bcf-116">Questo parametro deve essere costituito solo da una delle [**\_ costanti LINEDIGITMODE**](linedigitmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="09bcf-116">This parameter must be one and only one of the [**LINEDIGITMODE\_ constants**](linedigitmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="09bcf-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="09bcf-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="09bcf-118">Il "conteggio dei segni" (numero di millisecondi dall'avvio di Windows) in corrispondenza del quale è stata rilevata la cifra specificata.</span><span class="sxs-lookup"><span data-stu-id="09bcf-118">The "tick count" (number of milliseconds since Windows started) at which the specified digit was detected.</span></span> <span data-ttu-id="09bcf-119">Per le versioni TAPI precedenti alla 2,0, questo parametro è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="09bcf-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09bcf-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09bcf-120">Return value</span></span>

<span data-ttu-id="09bcf-121">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="09bcf-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="09bcf-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="09bcf-122">Remarks</span></span>

<span data-ttu-id="09bcf-123">Il messaggio di **riga \_ MONITORDIGITS** viene inviato all'applicazione che ha abilitato il monitoraggio delle cifre.</span><span class="sxs-lookup"><span data-stu-id="09bcf-123">The **LINE\_MONITORDIGITS** message is sent to the application that has enabled digit monitoring.</span></span>

<span data-ttu-id="09bcf-124">Poiché questo timestamp potrebbe essere stato generato in un computer diverso da quello in cui l'applicazione è in esecuzione, è utile solo per il confronto con altri messaggi con timestamp analoghi generati sullo stesso dispositivo a linee ( [**linea \_ GATHERDIGITS**](line-gatherdigits.md), [**riga \_ generazione**](line-generate.md), [**riga \_ MONITORMEDIA**](line-monitormedia.md), [**riga \_ MONITORTONE**](line-monitortone.md)), per determinare la tempistica relativa (separazione tra gli eventi).</span><span class="sxs-lookup"><span data-stu-id="09bcf-124">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORMEDIA**](line-monitormedia.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="09bcf-125">Il numero di cicli può essere "avvolto" dopo circa 49,7 giorni. Quando si eseguono calcoli, le applicazioni devono tenere conto di questo.</span><span class="sxs-lookup"><span data-stu-id="09bcf-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="09bcf-126">Se il provider di servizi non genera il timestamp (ad esempio, se è stato creato con una versione precedente di TAPI), TAPI fornisce un timestamp nel punto più vicino al provider di servizi che genera l'evento in modo che il timestamp sintetizzato sia il più accurato possibile.</span><span class="sxs-lookup"><span data-stu-id="09bcf-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="09bcf-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09bcf-127">Requirements</span></span>



| <span data-ttu-id="09bcf-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="09bcf-128">Requirement</span></span> | <span data-ttu-id="09bcf-129">Valore</span><span class="sxs-lookup"><span data-stu-id="09bcf-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="09bcf-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="09bcf-130">TAPI version</span></span><br/> | <span data-ttu-id="09bcf-131">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="09bcf-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="09bcf-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09bcf-132">Header</span></span><br/>       | <dl> <span data-ttu-id="09bcf-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="09bcf-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09bcf-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09bcf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09bcf-135">**LINEA \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="09bcf-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="09bcf-136">**\_generazione riga**</span><span class="sxs-lookup"><span data-stu-id="09bcf-136">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="09bcf-137">**LINEA \_ MONITORMEDIA**</span><span class="sxs-lookup"><span data-stu-id="09bcf-137">**LINE\_MONITORMEDIA**</span></span>](line-monitormedia.md)
</dt> <dt>

[<span data-ttu-id="09bcf-138">**LINEA \_ MONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="09bcf-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> <dt>

[<span data-ttu-id="09bcf-139">**lineMonitorDigits**</span><span class="sxs-lookup"><span data-stu-id="09bcf-139">**lineMonitorDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits)
</dt> </dl>

 

 




