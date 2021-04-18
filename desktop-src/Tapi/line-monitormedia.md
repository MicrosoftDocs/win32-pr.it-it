---
description: Il messaggio LINE_MONITORMEDIA TAPI viene inviato quando viene rilevata una modifica nel tipo di supporto calls. L'invio di questo messaggio viene controllato con la funzione lineMonitorMedia
ms.assetid: 1cfba455-9a15-45f3-8d56-74b8348e080e
title: Messaggio di LINE_MONITORMEDIA (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b6e3d0d2928ab3256b844a27727657978dbe0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327785"
---
# <a name="line_monitormedia-message"></a><span data-ttu-id="f7b2f-104">\_Messaggio linea MONITORMEDIA</span><span class="sxs-lookup"><span data-stu-id="f7b2f-104">LINE\_MONITORMEDIA message</span></span>

<span data-ttu-id="f7b2f-105">Il messaggio **\_ MONITORMEDIA della linea** TAPI viene inviato quando viene rilevata una modifica nel tipo di supporto della chiamata.</span><span class="sxs-lookup"><span data-stu-id="f7b2f-105">The TAPI **LINE\_MONITORMEDIA** message is sent when a change in the call's media type is detected.</span></span> <span data-ttu-id="f7b2f-106">L'invio di questo messaggio viene controllato con la funzione [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) .</span><span class="sxs-lookup"><span data-stu-id="f7b2f-106">The sending of this message is controlled with the [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) function.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="f7b2f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7b2f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b2f-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="f7b2f-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b2f-109">Handle della chiamata.</span><span class="sxs-lookup"><span data-stu-id="f7b2f-109">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="f7b2f-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="f7b2f-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b2f-111">Istanza di callback fornita all'apertura della riga.</span><span class="sxs-lookup"><span data-stu-id="f7b2f-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="f7b2f-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f7b2f-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b2f-113">Nuovo tipo di supporto (o modalità).</span><span class="sxs-lookup"><span data-stu-id="f7b2f-113">The new media type (or mode).</span></span> <span data-ttu-id="f7b2f-114">Questo parametro deve essere costituito solo da una delle [**\_ costanti LINEMEDIAMODE**](linemediamode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="f7b2f-114">This parameter must be one and only one of the [**LINEMEDIAMODE\_ constants**](linemediamode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7b2f-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f7b2f-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b2f-116">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="f7b2f-116">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="f7b2f-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="f7b2f-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b2f-118">Il "conteggio dei segni" (numero di millisecondi dall'avvio di Windows) in corrispondenza del quale è stato rilevato il supporto specificato.</span><span class="sxs-lookup"><span data-stu-id="f7b2f-118">The "tick count" (number of milliseconds since Windows started) at which the specified media was detected.</span></span> <span data-ttu-id="f7b2f-119">Per le versioni TAPI precedenti alla 2,0, questo parametro è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="f7b2f-119">For TAPI versions earlier than 2.0, this parameter is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b2f-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7b2f-120">Return value</span></span>

<span data-ttu-id="f7b2f-121">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f7b2f-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b2f-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7b2f-122">Remarks</span></span>

<span data-ttu-id="f7b2f-123">Il messaggio di **riga \_ MONITORMEDIA** viene inviato all'applicazione che ha abilitato il monitoraggio del supporto per il tipo di supporto rilevato.</span><span class="sxs-lookup"><span data-stu-id="f7b2f-123">The **LINE\_MONITORMEDIA** message is sent to the application that has enabled media monitoring for the media type detected.</span></span>

<span data-ttu-id="f7b2f-124">Poiché questo timestamp potrebbe essere stato generato in un computer diverso da quello in cui l'applicazione è in esecuzione, è utile solo per il confronto con altri messaggi con timestamp analoghi generati sullo stesso dispositivo a linee ( [**linea \_ GATHERDIGITS**](line-gatherdigits.md), [**riga \_ generazione**](line-generate.md), [**riga \_ MONITORDIGITS**](line-monitordigits.md), [**riga \_ MONITORTONE**](line-monitortone.md)), per determinare la tempistica relativa (separazione tra gli eventi).</span><span class="sxs-lookup"><span data-stu-id="f7b2f-124">Because this timestamp may have been generated on a computer other than the one on which the application is executing, it is useful only for comparison to other similarly timestamped messages generated on the same line device ( [**LINE\_GATHERDIGITS**](line-gatherdigits.md), [**LINE\_GENERATE**](line-generate.md), [**LINE\_MONITORDIGITS**](line-monitordigits.md), [**LINE\_MONITORTONE**](line-monitortone.md)), in order to determine their relative timing (separation between events).</span></span> <span data-ttu-id="f7b2f-125">Il numero di cicli può essere "avvolto" dopo circa 49,7 giorni. Quando si eseguono calcoli, le applicazioni devono tenere conto di questo.</span><span class="sxs-lookup"><span data-stu-id="f7b2f-125">The tick count can "wrap around" after approximately 49.7 days; applications must take this into account when performing calculations.</span></span>

<span data-ttu-id="f7b2f-126">Se il provider di servizi non genera il timestamp (ad esempio, se è stato creato con una versione precedente di TAPI), TAPI fornisce un timestamp nel punto più vicino al provider di servizi che genera l'evento in modo che il timestamp sintetizzato sia il più accurato possibile.</span><span class="sxs-lookup"><span data-stu-id="f7b2f-126">If the service provider does not generate the timestamp (for example, if it was created using an earlier version of TAPI), then TAPI provides a timestamp at the point closest to the service provider generating the event so that the synthesized timestamp is as accurate as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b2f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7b2f-127">Requirements</span></span>



| <span data-ttu-id="f7b2f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7b2f-128">Requirement</span></span> | <span data-ttu-id="f7b2f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f7b2f-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f7b2f-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f7b2f-130">TAPI version</span></span><br/> | <span data-ttu-id="f7b2f-131">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f7b2f-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f7b2f-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7b2f-132">Header</span></span><br/>       | <dl> <span data-ttu-id="f7b2f-133"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7b2f-133"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7b2f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7b2f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b2f-135">**LINEA \_ GATHERDIGITS**</span><span class="sxs-lookup"><span data-stu-id="f7b2f-135">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> <dt>

[<span data-ttu-id="f7b2f-136">**\_generazione riga**</span><span class="sxs-lookup"><span data-stu-id="f7b2f-136">**LINE\_GENERATE**</span></span>](line-generate.md)
</dt> <dt>

[<span data-ttu-id="f7b2f-137">**LINEA \_ MONITORDIGITS**</span><span class="sxs-lookup"><span data-stu-id="f7b2f-137">**LINE\_MONITORDIGITS**</span></span>](line-monitordigits.md)
</dt> <dt>

[<span data-ttu-id="f7b2f-138">**LINEA \_ MONITORTONE**</span><span class="sxs-lookup"><span data-stu-id="f7b2f-138">**LINE\_MONITORTONE**</span></span>](line-monitortone.md)
</dt> </dl>

 

 




