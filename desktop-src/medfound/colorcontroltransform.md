---
description: Regola le caratteristiche dei colori di un flusso video.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: Trasformazione controllo colori DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b94c8314bfd2be85a3bbc392bfa0e83767ff0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749346"
---
# <a name="color-control-transform-dsp"></a><span data-ttu-id="5f5d0-103">Trasformazione controllo colori DSP</span><span class="sxs-lookup"><span data-stu-id="5f5d0-103">Color Control Transform DSP</span></span>

<span data-ttu-id="5f5d0-104">Regola le caratteristiche dei colori di un flusso video.</span><span class="sxs-lookup"><span data-stu-id="5f5d0-104">Adjusts the color characteristics of a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="5f5d0-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="5f5d0-105">CLSID</span></span>

<span data-ttu-id="5f5d0-106">\_CCOLORCONTROLDMO CLSID</span><span class="sxs-lookup"><span data-stu-id="5f5d0-106">CLSID\_CColorControlDmo</span></span>

## <a name="interfaces"></a><span data-ttu-id="5f5d0-107">Interfacce</span><span class="sxs-lookup"><span data-stu-id="5f5d0-107">Interfaces</span></span>

-   <span data-ttu-id="5f5d0-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="5f5d0-108">**IMediaObject**</span></span>
-   <span data-ttu-id="5f5d0-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="5f5d0-109">**IMFTransform**</span></span>
-   <span data-ttu-id="5f5d0-110">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="5f5d0-110">**IPropertyStore**</span></span>

## <a name="formats"></a><span data-ttu-id="5f5d0-111">Formati</span><span class="sxs-lookup"><span data-stu-id="5f5d0-111">Formats</span></span>

-   <span data-ttu-id="5f5d0-112">RGB 24</span><span class="sxs-lookup"><span data-stu-id="5f5d0-112">RGB 24</span></span>
-   <span data-ttu-id="5f5d0-113">RGB 32</span><span class="sxs-lookup"><span data-stu-id="5f5d0-113">RGB 32</span></span>
-   <span data-ttu-id="5f5d0-114">RGB 555</span><span class="sxs-lookup"><span data-stu-id="5f5d0-114">RGB 555</span></span>
-   <span data-ttu-id="5f5d0-115">RGB 565</span><span class="sxs-lookup"><span data-stu-id="5f5d0-115">RGB 565</span></span>
-   <span data-ttu-id="5f5d0-116">AYUV</span><span class="sxs-lookup"><span data-stu-id="5f5d0-116">AYUV</span></span>
-   <span data-ttu-id="5f5d0-117">UYVY</span><span class="sxs-lookup"><span data-stu-id="5f5d0-117">UYVY</span></span>
-   <span data-ttu-id="5f5d0-118">YUY2</span><span class="sxs-lookup"><span data-stu-id="5f5d0-118">YUY2</span></span>
-   <span data-ttu-id="5f5d0-119">YV12</span><span class="sxs-lookup"><span data-stu-id="5f5d0-119">YV12</span></span>

## <a name="properties"></a><span data-ttu-id="5f5d0-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5f5d0-120">Properties</span></span>

-   [<span data-ttu-id="5f5d0-121">\_luminosità colore \_ MFPKEY</span><span class="sxs-lookup"><span data-stu-id="5f5d0-121">MFPKEY\_COLOR\_BRIGHTNESS</span></span>](mfpkey-color-brightness.md)
-   [<span data-ttu-id="5f5d0-122">\_contrasto colori \_ MFPKEY</span><span class="sxs-lookup"><span data-stu-id="5f5d0-122">MFPKEY\_COLOR\_CONTRAST</span></span>](mfpkey-color-contrast.md)
-   [<span data-ttu-id="5f5d0-123">\_tonalità colore \_ MFPKEY</span><span class="sxs-lookup"><span data-stu-id="5f5d0-123">MFPKEY\_COLOR\_HUE</span></span>](mfpkey-color-hue.md)
-   [<span data-ttu-id="5f5d0-124">\_ \_ saturazione colore MFPKEY</span><span class="sxs-lookup"><span data-stu-id="5f5d0-124">MFPKEY\_COLOR\_SATURATION</span></span>](mfpkey-color-saturation.md)

## <a name="remarks"></a><span data-ttu-id="5f5d0-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f5d0-125">Remarks</span></span>

<span data-ttu-id="5f5d0-126">Questo DSP modifica il contenuto del flusso video.</span><span class="sxs-lookup"><span data-stu-id="5f5d0-126">This DSP modifies the contents of the video stream.</span></span> <span data-ttu-id="5f5d0-127">Per la riproduzione, è possibile ottenere effetti simili in modo più efficiente usando l'interfaccia **IMFVideoProcessor** , che controlla l'elaborazione video nella scheda grafica.</span><span class="sxs-lookup"><span data-stu-id="5f5d0-127">For playback, you might be able to achieve similar effects more efficiently by using the **IMFVideoProcessor** interface, which controls video processing in the graphics card.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f5d0-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f5d0-128">Requirements</span></span>



| <span data-ttu-id="5f5d0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f5d0-129">Requirement</span></span> | <span data-ttu-id="5f5d0-130">Valore</span><span class="sxs-lookup"><span data-stu-id="5f5d0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f5d0-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f5d0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5f5d0-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f5d0-132">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5f5d0-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f5d0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5f5d0-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5f5d0-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f5d0-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f5d0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f5d0-136"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f5d0-136"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="5f5d0-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5f5d0-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f5d0-138"><dt>Mfvdsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f5d0-138"><dt>Mfvdsp.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5f5d0-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f5d0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f5d0-140">Processori di segnale digitale</span><span class="sxs-lookup"><span data-stu-id="5f5d0-140">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




