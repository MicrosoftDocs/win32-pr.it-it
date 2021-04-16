---
description: Specifica il numero massimo di frame di riferimento a lungo termine (LTR) controllati dall'applicazione.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: Proprietà CODECAPI_AVEncVideoLTRBufferControl (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33adfc7d0ba2db87c2127489d9496dc5e0bb4158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524633"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a><span data-ttu-id="66e54-103">Proprietà AVEncVideoLTRBufferControl di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="66e54-103">CODECAPI\_AVEncVideoLTRBufferControl property</span></span>

<span data-ttu-id="66e54-104">Specifica il numero massimo di frame di riferimento a lungo termine (LTR) controllati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="66e54-104">Specifies the maximum number of Long Term Reference (LTR) frames controlled by application.</span></span>

## <a name="data-type"></a><span data-ttu-id="66e54-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="66e54-105">Data type</span></span>

<span data-ttu-id="66e54-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="66e54-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="66e54-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="66e54-107">Property GUID</span></span>

<span data-ttu-id="66e54-108">**Codecapis \_ AVEncVideoLTRBufferControl**</span><span class="sxs-lookup"><span data-stu-id="66e54-108">**CODECAPI\_AVEncVideoLTRBufferControl**</span></span>

## <a name="property-value"></a><span data-ttu-id="66e54-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="66e54-109">Property value</span></span>

<span data-ttu-id="66e54-110">Il valore di questo controllo include due campi, in cui ogni campo dispone di 16 bit.</span><span class="sxs-lookup"><span data-stu-id="66e54-110">The value of this control includes two fields, where each field has 16 bits.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66e54-111">Valore</span><span class="sxs-lookup"><span data-stu-id="66e54-111">Value</span></span></th>
<th><span data-ttu-id="66e54-112">Significato</span><span class="sxs-lookup"><span data-stu-id="66e54-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <span data-ttu-id="66e54-113"><dt><strong>Il primo campo</strong></dt> <dt>bits [0.. 15]</dt> </span><span class="sxs-lookup"><span data-stu-id="66e54-113"><dt><strong>The first field</strong></dt> <dt>Bits[0..15]</dt> </span></span></dl></td>
<td><span data-ttu-id="66e54-114">Numero di fotogrammi LTR controllati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="66e54-114">The number of LTR frames controlled by the application.</span></span><br/> <span data-ttu-id="66e54-115"><strong>Codificatori H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="66e54-115"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="66e54-116">Supponendo che il valore sia N e N sia un valore diverso da zero, in ogni frame IDR il codificatore deve contrassegnare automaticamente i frame che seguono il frame IDR (e includere il frame IDR) come frame LTR purché siano applicabili tutti i 3 degli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="66e54-116">Assuming the value is N and N is non-zero value, at each IDR frame the encoder must automatically mark the frames following the IDR frame (and including the IDR frame) as LTR frames as long as all 3 of the following apply:</span></span>
<ul>
<li><span data-ttu-id="66e54-117">Il frame non è già impostato per essere contrassegnato come frame di riferimento a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="66e54-117">The frame is not already set to be marked as a long term reference frame.</span></span></li>
<li><span data-ttu-id="66e54-118">Il frame è un frame del livello di base.</span><span class="sxs-lookup"><span data-stu-id="66e54-118">The frame is a base layer frame.</span></span> <span data-ttu-id="66e54-119">Ad esempio, l'elemento Syntax <strong>temporal_id</strong> uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="66e54-119">For example, syntax element <strong>temporal_id</strong> equal to 0.</span></span></li>
<li><span data-ttu-id="66e54-120">Il numero di frame attualmente contrassegnati come LTR è inferiore a N.</span><span class="sxs-lookup"><span data-stu-id="66e54-120">The number of frames currently marked as LTR is less than N.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <span data-ttu-id="66e54-121"><dt><strong>Il secondo bit di campo</strong></dt> <dt>[16.. 31]</dt> </span><span class="sxs-lookup"><span data-stu-id="66e54-121"><dt><strong>The second field</strong></dt> <dt>Bits[16..31]</dt> </span></span></dl></td>
<td><span data-ttu-id="66e54-122">Modalità di attendibilità del controllo LTR.</span><span class="sxs-lookup"><span data-stu-id="66e54-122">The trust mode of LTR control.</span></span><br/> <span data-ttu-id="66e54-123"><strong>Codificatori H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="66e54-123"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="66e54-124">1 (trust fino a) significa che il codificatore può usare un frame LTR, a meno che l'app non lo invalidi in modo esplicito tramite il controllo <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> .</span><span class="sxs-lookup"><span data-stu-id="66e54-124">1 (Trust Until) means the encoder may use an LTR frame unless the app explicitly invalidates it through the <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> control.</span></span> <br/> <span data-ttu-id="66e54-125">Altri valori non sono validi e sono riservati per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="66e54-125">Other values are invalid and reserved for future use.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="66e54-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="66e54-126">Remarks</span></span>

<span data-ttu-id="66e54-127">Si tratta di un'API statica.</span><span class="sxs-lookup"><span data-stu-id="66e54-127">This is a static API.</span></span>

<span data-ttu-id="66e54-128">Il valore predefinito deve essere 0</span><span class="sxs-lookup"><span data-stu-id="66e54-128">Default value shall be 0</span></span>

## <a name="requirements"></a><span data-ttu-id="66e54-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66e54-129">Requirements</span></span>



| <span data-ttu-id="66e54-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="66e54-130">Requirement</span></span> | <span data-ttu-id="66e54-131">Valore</span><span class="sxs-lookup"><span data-stu-id="66e54-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66e54-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66e54-132">Minimum supported client</span></span><br/> | <span data-ttu-id="66e54-133">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="66e54-133">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="66e54-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66e54-134">Minimum supported server</span></span><br/> | <span data-ttu-id="66e54-135">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="66e54-135">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="66e54-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66e54-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="66e54-137"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="66e54-137"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66e54-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66e54-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66e54-139">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66e54-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




