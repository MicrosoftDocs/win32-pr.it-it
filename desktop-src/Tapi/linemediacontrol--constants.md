---
description: Le \_ costanti del flag di bit LINEMEDIACONTROL descrivono un set di operazioni generiche sui flussi multimediali.
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: Costanti LINEMEDIACONTROL_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3241a3b5f4f8a0363f30ce7aefaded0c63fc4189
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330742"
---
# <a name="linemediacontrol_-constants"></a><span data-ttu-id="8b89a-103">\_Costanti LINEMEDIACONTROL</span><span class="sxs-lookup"><span data-stu-id="8b89a-103">LINEMEDIACONTROL\_ Constants</span></span>

<span data-ttu-id="8b89a-104">Le costanti del flag di bit **LINEMEDIACONTROL \_** descrivono un set di operazioni generiche sui flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="8b89a-104">The **LINEMEDIACONTROL\_** bit-flag constants describe a set of generic operations on media streams.</span></span> <span data-ttu-id="8b89a-105">Le interpretazioni sono determinate dal flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="8b89a-105">The interpretations are determined by the media stream.</span></span> <span data-ttu-id="8b89a-106">Il dispositivo a linee deve avere la funzionalità di controllo del supporto per l'efficacia di qualsiasi operazione di controllo del supporto.</span><span class="sxs-lookup"><span data-stu-id="8b89a-106">The line device must have the media-control capability for any media-control operation to be effective.</span></span>

<dl> <dt>

<span data-ttu-id="8b89a-107"><span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL \_ None**</span><span class="sxs-lookup"><span data-stu-id="8b89a-107"><span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b89a-108">Non è necessario apportare alcuna modifica al flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="8b89a-108">No change is to be made to the media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b89a-109"><span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**LINEMEDIACONTROL \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="8b89a-109"><span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**LINEMEDIACONTROL\_PAUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b89a-110">Sospende temporaneamente il flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="8b89a-110">Temporarily pause the media stream.</span></span>

<span data-ttu-id="8b89a-111">La velocità del flusso multimediale viene restituita al normale.</span><span class="sxs-lookup"><span data-stu-id="8b89a-111">The speed of the media stream is returned to normal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b89a-112"><span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**\_RATEDOWN LINEMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="8b89a-112"><span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL\_RATEDOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b89a-113">La velocità del flusso multimediale è diminuita in base a una quantità definita dal flusso.</span><span class="sxs-lookup"><span data-stu-id="8b89a-113">The speed of the media stream is decreased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b89a-114"><span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**\_RATENORMAL LINEMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="8b89a-114"><span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL\_RATENORMAL**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b89a-115"><span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**\_Rateup LINEMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="8b89a-115"><span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL\_RATEUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b89a-116">La velocità del flusso multimediale viene aumentata in base a una quantità definita dal flusso.</span><span class="sxs-lookup"><span data-stu-id="8b89a-116">The speed of the media stream is increased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b89a-117"><span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**reimpostazione LINEMEDIACONTROL \_**</span><span class="sxs-lookup"><span data-stu-id="8b89a-117"><span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**LINEMEDIACONTROL\_RESET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b89a-118">Reimpostare il flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="8b89a-118">Reset the media stream.</span></span> <span data-ttu-id="8b89a-119">Equivalente a una fine dell'input.</span><span class="sxs-lookup"><span data-stu-id="8b89a-119">Equivalent to an end-of-input.</span></span> <span data-ttu-id="8b89a-120">Vengono rilasciati tutti i buffer.</span><span class="sxs-lookup"><span data-stu-id="8b89a-120">All buffers are released.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b89a-121"><span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**Riprendi LINEMEDIACONTROL \_**</span><span class="sxs-lookup"><span data-stu-id="8b89a-121"><span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**LINEMEDIACONTROL\_RESUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b89a-122">Riprendere un flusso multimediale sospeso.</span><span class="sxs-lookup"><span data-stu-id="8b89a-122">Resume a paused media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b89a-123"><span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**\_inizio LINEMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="8b89a-123"><span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b89a-124">Avviare il flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="8b89a-124">Start the media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b89a-125"><span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**\_volumedown LINEMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="8b89a-125"><span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL\_VOLUMEDOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b89a-126">L'ampiezza del flusso multimediale è diminuita in base a una quantità definita dal flusso.</span><span class="sxs-lookup"><span data-stu-id="8b89a-126">The amplitude of the media stream is decreased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b89a-127"><span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**\_VOLUMENORMAL LINEMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="8b89a-127"><span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL\_VOLUMENORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b89a-128">L'ampiezza del flusso multimediale viene restituita al normale.</span><span class="sxs-lookup"><span data-stu-id="8b89a-128">The amplitude of the media stream is returned to normal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b89a-129"><span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**\_VOLUMEUP LINEMEDIACONTROL**</span><span class="sxs-lookup"><span data-stu-id="8b89a-129"><span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL\_VOLUMEUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b89a-130">L'ampiezza del flusso multimediale viene aumentata in base a una quantità definita dal flusso.</span><span class="sxs-lookup"><span data-stu-id="8b89a-130">The amplitude of the media stream is increased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b89a-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b89a-131">Remarks</span></span>

<span data-ttu-id="8b89a-132">È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b89a-132">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="8b89a-133">I 16 bit di ordine inferiore sono riservati.</span><span class="sxs-lookup"><span data-stu-id="8b89a-133">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="8b89a-134">Il controllo multimediale viene fornito per migliorare le prestazioni delle azioni sui flussi multimediali in risposta ad eventi correlati alla telefonia.</span><span class="sxs-lookup"><span data-stu-id="8b89a-134">Media control is provided to improve performance of actions on media streams in response to telephony-related events.</span></span> <span data-ttu-id="8b89a-135">L'applicazione deve normalmente gestire un flusso multimediale tramite l'API specifica del supporto.</span><span class="sxs-lookup"><span data-stu-id="8b89a-135">The application should normally manage a media stream through the media-specific API.</span></span> <span data-ttu-id="8b89a-136">La funzionalità di controllo dei supporti disponibile qui non è destinata a sostituire le API multimediali native.</span><span class="sxs-lookup"><span data-stu-id="8b89a-136">The media-control functionality provided here is not intended to replace the native media APIs.</span></span>

<span data-ttu-id="8b89a-137">Le azioni di controllo del supporto possono essere associate al rilevamento di cifre, al rilevamento di toni, alla transizione in uno stato di chiamata e al rilevamento di un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="8b89a-137">Media-control actions can be associated with the detection of digits, the detection of tones, the transition into a call state, and the detection of a media type.</span></span> <span data-ttu-id="8b89a-138">Per determinare se il controllo multimediale è disponibile sulla linea, consultare le funzionalità del dispositivo di una linea.</span><span class="sxs-lookup"><span data-stu-id="8b89a-138">Consult a line's device capabilities to determine whether media control is available on the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b89a-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b89a-139">Requirements</span></span>



| <span data-ttu-id="8b89a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b89a-140">Requirement</span></span> | <span data-ttu-id="8b89a-141">Valore</span><span class="sxs-lookup"><span data-stu-id="8b89a-141">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8b89a-142">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="8b89a-142">TAPI version</span></span><br/> | <span data-ttu-id="8b89a-143">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8b89a-143">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8b89a-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b89a-144">Header</span></span><br/>       | <dl> <span data-ttu-id="8b89a-145"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b89a-145"><dt>Tapi.h</dt></span></span> </dl> |



 

 




