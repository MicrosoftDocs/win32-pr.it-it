---
description: Specifica che il frame corrente è codificato utilizzando uno o più frame LTR.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: Proprietà CODECAPI_AVEncVideoUseLTRFrame (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252933180e8212c94c3c2b2442397c53d0f9c559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749354"
---
# <a name="codecapi_avencvideouseltrframe-property"></a><span data-ttu-id="d6027-103">Proprietà AVEncVideoUseLTRFrame di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="d6027-103">CODECAPI\_AVEncVideoUseLTRFrame property</span></span>

<span data-ttu-id="d6027-104">Specifica che il frame corrente è codificato utilizzando uno o più frame LTR.</span><span class="sxs-lookup"><span data-stu-id="d6027-104">Specifies that the current frame is encoded using one or multiple LTR frames.</span></span>

## <a name="data-type"></a><span data-ttu-id="d6027-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d6027-105">Data type</span></span>

<span data-ttu-id="d6027-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="d6027-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d6027-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="d6027-107">Property GUID</span></span>

<span data-ttu-id="d6027-108">**Codecapis \_ AVEncVideoUseLTRFrame**</span><span class="sxs-lookup"><span data-stu-id="d6027-108">**CODECAPI\_AVEncVideoUseLTRFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="d6027-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d6027-109">Property value</span></span>

<span data-ttu-id="d6027-110">Il valore di questo controllo include due campi, in cui ogni campo dispone di 16 bit.</span><span class="sxs-lookup"><span data-stu-id="d6027-110">The value of this control includes two fields, where each field has 16 bits.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6027-111">Valore</span><span class="sxs-lookup"><span data-stu-id="d6027-111">Value</span></span></th>
<th><span data-ttu-id="d6027-112">Significato</span><span class="sxs-lookup"><span data-stu-id="d6027-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <span data-ttu-id="d6027-113"><dt><strong>Il primo campo</strong></dt> <dt>bits [0.. 15]</dt> </span><span class="sxs-lookup"><span data-stu-id="d6027-113"><dt><strong>The first field</strong></dt> <dt>Bits[0..15]</dt> </span></span></dl></td>
<td><span data-ttu-id="d6027-114">Indica i frame LTR consentiti per la codifica del frame corrente.</span><span class="sxs-lookup"><span data-stu-id="d6027-114">Indicates which LTR frame(s) are allowed for encoding the current frame.</span></span> <br/> <span data-ttu-id="d6027-115"><strong>Codificatori H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="d6027-115"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="d6027-116">Si tratta di una bitmap che indica i frame LTR che possono essere usati come riferimento per il frame.</span><span class="sxs-lookup"><span data-stu-id="d6027-116">This is a bitmap that indicates which LTR frames can be used as a reference for this frame.</span></span> <span data-ttu-id="d6027-117">Il bit meno significativo corrisponde a LTR index 0, il secondo bit meno significativo corrisponde a LTR index 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="d6027-117">The least significant bit corresponds to LTR index 0, the second least significant bit corresponds to LTR index 1, etc.</span></span><br/> <span data-ttu-id="d6027-118">Il valore non deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="d6027-118">This value shall not be 0.</span></span><br/> <span data-ttu-id="d6027-119">L'indice più alto specificato da questo valore non deve essere maggiore del numero massimo di frame LTR specificati nella proprietà <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> meno uno.</span><span class="sxs-lookup"><span data-stu-id="d6027-119">The highest index specified by this value shall not be greater than the maximum number of LTR frames specified in the <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> property less one.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <span data-ttu-id="d6027-120"><dt><strong>Il secondo bit di campo</strong></dt> <dt>[16.. 31]</dt> </span><span class="sxs-lookup"><span data-stu-id="d6027-120"><dt><strong>The second field</strong></dt> <dt>Bits[16..31]</dt> </span></span></dl></td>
<td><span data-ttu-id="d6027-121">Flag che indica se sono necessarie limitazioni aggiuntive per la codifica dei frame successivi.</span><span class="sxs-lookup"><span data-stu-id="d6027-121">Flag that indicates whether additional limitations are required for encoding subsequent frames.</span></span> <br/> <span data-ttu-id="d6027-122"><strong>Codificatori H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="d6027-122"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="d6027-123">1 è l'unico valore valido per questo campo.</span><span class="sxs-lookup"><span data-stu-id="d6027-123">1 is on the only valid value for this field.</span></span> <span data-ttu-id="d6027-124">Tutti gli altri valori non sono validi e sono riservati per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d6027-124">All other values are invalid and reserved for future use.</span></span><br/> <span data-ttu-id="d6027-125">Quando il flag è 1, il codificatore deve codificare i frame successivi nell'ordine di codifica in base ai vincoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="d6027-125">When the flag is 1, the encoder shall encode subsequent frames in encoding order subject to the following constraints:</span></span><br/>
<ul>
<li><span data-ttu-id="d6027-126">Non utilizzerà frame di riferimento a breve termine nell'ordine di codifica anteriore al frame corrente o alla codifica futura nell'ordine di codifica.</span><span class="sxs-lookup"><span data-stu-id="d6027-126">It shall not use short term reference frames in encoding order older than the current frame or future encoding in encoding order.</span></span></li>
<li><span data-ttu-id="d6027-127">Non deve usare i frame LTR non descritti dal controllo CODECAPI_AVEncVideoUseLTRFrame più recente.</span><span class="sxs-lookup"><span data-stu-id="d6027-127">It shall not use LTR frames not described by the most recent CODECAPI_AVEncVideoUseLTRFrame control.</span></span></li>
<li><span data-ttu-id="d6027-128">Può usare i frame LTR aggiornati dopo il frame corrente.</span><span class="sxs-lookup"><span data-stu-id="d6027-128">It may use LTR frames updated after the current frame.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="d6027-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6027-129">Remarks</span></span>

<span data-ttu-id="d6027-130">**Codificatori H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="d6027-130">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="d6027-131">Questa proprietà non deve essere chiamata se una chiamata in sospeso per l'utilizzo di un frame LTR è stata eseguita utilizzando la \_ Proprietà codecapi AVEncVideoUseLTRFrame e il codificatore non ha ancora generato un frame in cui è stato utilizzato il valore ltr.</span><span class="sxs-lookup"><span data-stu-id="d6027-131">This property should not be called if a pending call to use an LTR frame has been issued using the CODECAPI\_AVEncVideoUseLTRFrame property and the encoder has not yet generated a frame that has used the LTR.</span></span> <span data-ttu-id="d6027-132">In altre parole, il codificatore non deve accodare le richieste AVEncVideoUseLTRFrame di codecapis \_ .</span><span class="sxs-lookup"><span data-stu-id="d6027-132">In other words, the encoder should not queue up CODECAPI\_AVEncVideoUseLTRFrame requests.</span></span>

<span data-ttu-id="d6027-133">Se viene inviata una richiesta AVEncVideoUseLTRFrame di codecapite \_ mentre un'altra \_ richiesta AVEncVideoUseLTRFrame di codecapites è ancora in sospeso, la richiesta precedente deve essere eliminata.</span><span class="sxs-lookup"><span data-stu-id="d6027-133">If a CODECAPI\_AVEncVideoUseLTRFrame request is submitted while another CODECAPI\_AVEncVideoUseLTRFrame request is still pending, then the older request should be dropped.</span></span>

<span data-ttu-id="d6027-134">La chiamata a codecapit \_ AVEncVideoUseLTRFrame su un frame del livello non di base è valida e deve essere applicata al frame del livello non di base, senza ritardo in un frame del livello di base.</span><span class="sxs-lookup"><span data-stu-id="d6027-134">Calling CODECAPI\_AVEncVideoUseLTRFrame on a non-base layer frame is valid and shall apply to the non-base layer frame, without delay to a base layer frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6027-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6027-135">Requirements</span></span>



| <span data-ttu-id="d6027-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6027-136">Requirement</span></span> | <span data-ttu-id="d6027-137">Valore</span><span class="sxs-lookup"><span data-stu-id="d6027-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6027-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6027-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d6027-139">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d6027-139">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="d6027-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6027-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d6027-141">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d6027-141">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d6027-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6027-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6027-143"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6027-143"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6027-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6027-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6027-145">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6027-145">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




