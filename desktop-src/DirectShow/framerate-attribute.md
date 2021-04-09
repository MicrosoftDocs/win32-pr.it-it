---
description: L'attributo framerate specifica un framerate, in frame al secondo.
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: Attributo framerate (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1af5deb8ae2a851b328fcd6d9ffa3923328708
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965656"
---
# <a name="framerate-attribute-directshow"></a><span data-ttu-id="0c675-103">Attributo framerate (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="0c675-103">framerate Attribute (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="0c675-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="0c675-104">\[Deprecated.</span></span> <span data-ttu-id="0c675-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0c675-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0c675-106">L' `framerate` attributo specifica un framerate, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="0c675-106">The `framerate` attribute specifies a framerate, in frames per second.</span></span>

## <a name="possible-values"></a><span data-ttu-id="0c675-107">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="0c675-107">Possible Values</span></span>

<span data-ttu-id="0c675-108">Valore a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="0c675-108">Floating-point value.</span></span> <span data-ttu-id="0c675-109">Il valore deve includere lo zero iniziali prima della posizione decimale.</span><span class="sxs-lookup"><span data-stu-id="0c675-109">The value must include the leading zero before the decimal place.</span></span> <span data-ttu-id="0c675-110">Ad esempio, 0,3, not. 3.</span><span class="sxs-lookup"><span data-stu-id="0c675-110">For example, 0.3, not .3.</span></span> <span data-ttu-id="0c675-111">Non usare più di sette cifre decimali.</span><span class="sxs-lookup"><span data-stu-id="0c675-111">Do not use more than seven decimal digits.</span></span>

## <a name="applies-to"></a><span data-ttu-id="0c675-112">Si applica a</span><span class="sxs-lookup"><span data-stu-id="0c675-112">Applies To</span></span>

<span data-ttu-id="0c675-113">[**clip**](clip-element.md), [**gruppo**](group-element.md), [**sequenza temporale**](timeline-element.md)</span><span class="sxs-lookup"><span data-stu-id="0c675-113">[**clip**](clip-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md)</span></span>

## <a name="remarks"></a><span data-ttu-id="0c675-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c675-114">Remarks</span></span>

<span data-ttu-id="0c675-115">Per l'elemento **clip** , questo attributo specifica la frequenza dei fotogrammi predefinita dell'origine.</span><span class="sxs-lookup"><span data-stu-id="0c675-115">For the **clip** element, this attribute specifies the default frame rate of the source.</span></span> <span data-ttu-id="0c675-116">Specificare l'attributo per le sequenze andDIB di immagini ancora.</span><span class="sxs-lookup"><span data-stu-id="0c675-116">Specify the attribute for still images andDIB sequences.</span></span> <span data-ttu-id="0c675-117">Per un'immagine ancora, impostare il valore su zero.</span><span class="sxs-lookup"><span data-stu-id="0c675-117">For a still image, set the value to zero.</span></span> <span data-ttu-id="0c675-118">Per una sequenza DIB, usare un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="0c675-118">For a DIB sequence, use a nonzero value.</span></span> <span data-ttu-id="0c675-119">Il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="0c675-119">The default value is zero.</span></span>

<span data-ttu-id="0c675-120">Per l'elemento **Group** , questo attributo specifica la frequenza dei fotogrammi di output per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="0c675-120">For the **group** element, this attribute specifies the output frame rate for the group.</span></span>

<span data-ttu-id="0c675-121">Per l'elemento **Timeline** , questo attributo specifica la frequenza dei fotogrammi predefinita per tutti i gruppi.</span><span class="sxs-lookup"><span data-stu-id="0c675-121">For the **timeline** element, this attribute specifies the default frame rate for all groups.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c675-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c675-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c675-123">Attributi XTL</span><span class="sxs-lookup"><span data-stu-id="0c675-123">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="0c675-124">**IAMTimelineSrc::SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="0c675-124">**IAMTimelineSrc::SetDefaultFPS**</span></span>](iamtimelinesrc-setdefaultfps.md)
</dt> <dt>

[<span data-ttu-id="0c675-125">**IAMTimelineGroup::SetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="0c675-125">**IAMTimelineGroup::SetOutputFPS**</span></span>](iamtimelinegroup-setoutputfps.md)
</dt> <dt>

[<span data-ttu-id="0c675-126">**IAMTimeline::SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="0c675-126">**IAMTimeline::SetDefaultFPS**</span></span>](iamtimeline-setdefaultfps.md)
</dt> </dl>

 

 



