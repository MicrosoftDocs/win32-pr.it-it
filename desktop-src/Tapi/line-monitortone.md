---
description: Il messaggio della linea TAPI \_ MONITORTONE viene inviato quando viene rilevato un tono. L'invio di questo messaggio viene controllato con la funzione lineMonitorTones.
ms.assetid: ffdca615-5341-4f02-bb38-b8133cd9477d
title: Messaggio di LINE_MONITORTONE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de88863111dc0d00ea32953eeac76d4b570b5848
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332690"
---
# <a name="line_monitortone-message"></a><span data-ttu-id="373f3-104">\_Messaggio linea MONITORTONE</span><span class="sxs-lookup"><span data-stu-id="373f3-104">LINE\_MONITORTONE message</span></span>

<span data-ttu-id="373f3-105">Il messaggio della **linea TAPI \_ MONITORTONE** viene inviato quando viene rilevato un tono.</span><span class="sxs-lookup"><span data-stu-id="373f3-105">The TAPI **LINE\_MONITORTONE** message is sent when a tone is detected.</span></span> <span data-ttu-id="373f3-106">L'invio di questo messaggio viene controllato con la funzione [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) .</span><span class="sxs-lookup"><span data-stu-id="373f3-106">The sending of this message is controlled with the [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="373f3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="373f3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="373f3-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="373f3-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="373f3-109">Handle della chiamata.</span><span class="sxs-lookup"><span data-stu-id="373f3-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="373f3-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="373f3-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="373f3-111">Istanza di callback fornita all'apertura della riga della chiamata.</span><span class="sxs-lookup"><span data-stu-id="373f3-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="373f3-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="373f3-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="373f3-113">Membro **dwAppSpecific** specifico dell'applicazione della struttura [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) per il tono rilevato.</span><span class="sxs-lookup"><span data-stu-id="373f3-113">The application-specific **dwAppSpecific** member of the [**LINEMONITORTONE**](/windows/desktop/api/Tapi/ns-tapi-linemonitortone) structure for the tone that was detected.</span></span>

</dd> <dt>

<span data-ttu-id="373f3-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="373f3-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="373f3-115">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="373f3-115">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="373f3-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="373f3-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="373f3-117">Il "conteggio dei segni" (numero di millisecondi dall'avvio di Windows) in corrispondenza del quale è stato rilevato il tono.</span><span class="sxs-lookup"><span data-stu-id="373f3-117">The "tick count" (number of milliseconds since Windows started) at which the tone was detected.</span></span> <span data-ttu-id="373f3-118">Per le versioni API precedenti alla 2,0, questo parametro è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="373f3-118">For API versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="373f3-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="373f3-119">Return value</span></span>

<span data-ttu-id="373f3-120">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="373f3-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="373f3-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="373f3-121">Remarks</span></span>

<span data-ttu-id="373f3-122">Il messaggio di **riga \_ MONITORTONE** viene inviato solo all'applicazione che ha richiesto il monitoraggio del tono.</span><span class="sxs-lookup"><span data-stu-id="373f3-122">The **LINE\_MONITORTONE** message is only sent to the application that has requested the tone be monitored.</span></span>

<span data-ttu-id="373f3-123">Poiché questo timestamp potrebbe essere stato generato in un computer diverso da quello in cui l'applicazione è in esecuzione, è utile solo per il confronto con altri messaggi con timestamp analoghi generati sullo stesso dispositivo a linee ( [**linea \_ GATHERDIGITS**](line-gatherdigits.md), [**riga \_ generazione**](line-generate.md), [**riga \_ MONITORDIGITS**](line-monitordigits.md), **riga \_ MONITORTONE**), per determinare la tempistica relativa (separazione tra gli eventi).</span><span class="sxs-lookup"><span data-stu-id="373f3-123">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), **LINE\_MONITORTONE**), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="373f3-124">Il numero di cicli può essere "avvolto" dopo circa 49,7 giorni. Quando si eseguono calcoli, le applicazioni devono tenere conto di questo.</span><span class="sxs-lookup"><span data-stu-id="373f3-124">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="373f3-125">Se il provider di servizi non genera il timestamp (ad esempio, se è stato creato con una versione precedente di TAPI), TAPI fornisce un timestamp nel punto più vicino al provider di servizi che genera l'evento in modo che il timestamp sintetizzato sia il più accurato possibile.</span><span class="sxs-lookup"><span data-stu-id="373f3-125">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="373f3-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="373f3-126">Requirements</span></span>



| <span data-ttu-id="373f3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="373f3-127">Requirement</span></span> | <span data-ttu-id="373f3-128">Valore</span><span class="sxs-lookup"><span data-stu-id="373f3-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="373f3-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="373f3-129">TAPI version</span></span><br/> | <span data-ttu-id="373f3-130">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="373f3-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="373f3-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="373f3-131">Header</span></span><br/>       | <dl> <span data-ttu-id="373f3-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="373f3-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="373f3-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="373f3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="373f3-134">**LINEA \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="373f3-134">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="373f3-135">**\_generazione riga**</span><span class="sxs-lookup"><span data-stu-id="373f3-135">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="373f3-136">**LINEA \_ MONITORDIGITS**</span><span class="sxs-lookup"><span data-stu-id="373f3-136">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="373f3-137">**LINEMONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="373f3-137">**LINEMONITORTONE**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linemonitortone)
</dt> <dt>

[<span data-ttu-id="373f3-138">**lineMonitorTones**</span><span class="sxs-lookup"><span data-stu-id="373f3-138">**lineMonitorTones**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)
</dt> </dl>

 

 




