---
description: Imposta la frequenza massima di input in tempo reale dei fotogrammi video che vengono inseriti nel codificatore.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: Proprietà CODECAPI_AVEncMaxFrameRate (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c04d1fd1297f299db133cd98bd493c968fcc29c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305497"
---
# <a name="codecapi_avencmaxframerate-property"></a><span data-ttu-id="03ba1-103">Proprietà AVEncMaxFrameRate di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="03ba1-103">CODECAPI\_AVEncMaxFrameRate property</span></span>

<span data-ttu-id="03ba1-104">Imposta la frequenza massima di input in tempo reale dei fotogrammi video che vengono inseriti nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="03ba1-104">Sets the maximum real-time input rate of video frames being fed to the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="03ba1-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="03ba1-105">Data type</span></span>

<span data-ttu-id="03ba1-106">**ULONGULONG** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="03ba1-106">**ULONGULONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="03ba1-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="03ba1-107">Property GUID</span></span>

<span data-ttu-id="03ba1-108">**Codecapis \_ AVEncMaxFrameRate**</span><span class="sxs-lookup"><span data-stu-id="03ba1-108">**CODECAPI\_AVEncMaxFrameRate**</span></span>

## <a name="remarks"></a><span data-ttu-id="03ba1-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="03ba1-109">Remarks</span></span>

<span data-ttu-id="03ba1-110">Questa proprietà consente al chiamante di specificare la frequenza massima di input in tempo reale dei fotogrammi video inviati al codificatore.</span><span class="sxs-lookup"><span data-stu-id="03ba1-110">This property allows the caller to specify the maximum real-time input rate of video frames being fed to the encoder.</span></span> <span data-ttu-id="03ba1-111">In questo modo, il codificatore indica la velocità di elaborazione dei frame in arrivo.</span><span class="sxs-lookup"><span data-stu-id="03ba1-111">This gives the encoder an indication of the rate that it will need to process the incoming frames.</span></span> <span data-ttu-id="03ba1-112">Questa operazione è utile per i codificatori che si configurano in una particolare configurazione dello stato di alimentazione in base alla risoluzione e alla frequenza dei fotogrammi del video di origine.</span><span class="sxs-lookup"><span data-stu-id="03ba1-112">This is useful for encoders that set themselves into a particular power state configuration based on the resolution and frame-rate of the source video.</span></span>

<span data-ttu-id="03ba1-113">La frequenza dei fotogrammi è espressa come rapporto.</span><span class="sxs-lookup"><span data-stu-id="03ba1-113">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="03ba1-114">I 32 bit superiori del valore dell'attributo contengono il numeratore e i 32 bit inferiori contengono il denominatore.</span><span class="sxs-lookup"><span data-stu-id="03ba1-114">The upper 32 bits of the attribute value contain the numerator and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="03ba1-115">Se, ad esempio, la frequenza dei fotogrammi è di 30 fotogrammi al secondo (fps), il rapporto è 30/1.</span><span class="sxs-lookup"><span data-stu-id="03ba1-115">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span> <span data-ttu-id="03ba1-116">Se la frequenza dei fotogrammi è 29,97 fps, il rapporto è 30000/1001.</span><span class="sxs-lookup"><span data-stu-id="03ba1-116">If the frame rate is 29.97 fps, the ratio is 30,000/1001.</span></span>

## <a name="requirements"></a><span data-ttu-id="03ba1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03ba1-117">Requirements</span></span>



| <span data-ttu-id="03ba1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="03ba1-118">Requirement</span></span> | <span data-ttu-id="03ba1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="03ba1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03ba1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03ba1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="03ba1-121">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="03ba1-121">Windows 10 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="03ba1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03ba1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="03ba1-123">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="03ba1-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03ba1-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03ba1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="03ba1-125"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="03ba1-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03ba1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03ba1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ba1-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03ba1-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="03ba1-128">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="03ba1-128">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

