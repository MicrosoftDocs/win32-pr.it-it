---
description: I dispositivi portatili Windows supportano le proprietà immagine seguenti.
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: Proprietà immagine (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 959a008d9c30991058226e52db6e45ed417ee6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333523"
---
# <a name="image-properties"></a><span data-ttu-id="74455-103">Proprietà immagine</span><span class="sxs-lookup"><span data-stu-id="74455-103">Image Properties</span></span>

<span data-ttu-id="74455-104">I dispositivi portatili Windows supportano le proprietà immagine seguenti.</span><span class="sxs-lookup"><span data-stu-id="74455-104">Windows Portable Devices supports the following image properties.</span></span>



| <span data-ttu-id="74455-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="74455-105">Property</span></span>                                                                                                                                       | <span data-ttu-id="74455-106">VarType</span><span class="sxs-lookup"><span data-stu-id="74455-106">VarType</span></span>     | <span data-ttu-id="74455-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74455-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74455-108">**immagine di WPD \_ \_ BITDEPTH**</span><span class="sxs-lookup"><span data-stu-id="74455-108">**WPD\_IMAGE\_BITDEPTH**</span></span>                                                                                                                       | <span data-ttu-id="74455-109">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="74455-109">**VT\_UI4**</span></span> | <span data-ttu-id="74455-110">Profondità di bit dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="74455-110">The bit depth of the image.</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="74455-111"><span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**\_ \_ \_ stato correzione colore immagine \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="74455-111"><span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**WPD\_IMAGE\_COLOR\_CORRECTED\_STATUS**</span></span> | <span data-ttu-id="74455-112">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="74455-112">**VT\_UI4**</span></span> | <span data-ttu-id="74455-113">Enumerazione [**\_ \_ \_ \_ dei valori di stato con correzione del colore WPD**](wpd-color-corrected-status-values.md) che specifica se il file è stato con correzione del colore. In questo modo si impedisce a più dispositivi di correggere automaticamente il colore dell'immagine durante la post-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="74455-113">A [**WPD\_COLOR\_CORRECTED\_STATUS\_VALUES**](wpd-color-corrected-status-values.md) enumeration that specifies whether the file has been color-corrected.This prevents multiple devices from automatically color-correcting the image during post-processing.</span></span><br/>                                                                       |
| <span data-ttu-id="74455-114">**\_ \_ stato ritagliato immagine WPD \_**</span><span class="sxs-lookup"><span data-stu-id="74455-114">**WPD\_IMAGE\_CROPPED\_STATUS**</span></span>                                                                                                                | <span data-ttu-id="74455-115">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="74455-115">**VT\_UI4**</span></span> | <span data-ttu-id="74455-116">Enumerazione [**\_ \_ \_ dei valori di stato ritagliata WPD**](wpd-cropped-status-values.md) che specifica se il file è stato ritagliato. In questo modo si impedisce a più dispositivi di ritagliare automaticamente l'immagine durante la post-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="74455-116">A [**WPD\_CROPPED\_STATUS\_VALUES**](wpd-cropped-status-values.md) enumeration that specifies whether the file has been cropped.This prevents multiple devices from automatically cropping the image during post-processing.</span></span><br/>                                                                                                        |
| <span data-ttu-id="74455-117">**\_indice di \_ esposizione \_ Immagini WPD**</span><span class="sxs-lookup"><span data-stu-id="74455-117">**WPD\_IMAGE\_EXPOSURE\_INDEX**</span></span>                                                                                                                | <span data-ttu-id="74455-118">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="74455-118">**VT\_UI4**</span></span> | <span data-ttu-id="74455-119">Valore che identifica le impostazioni della velocità della pellicola quando l'immagine è stata acquisita. Le impostazioni corrispondono alle designazioni ISO di ASA/DIN.</span><span class="sxs-lookup"><span data-stu-id="74455-119">A value that identifies the film speed settings when this image was captured.The settings correspond to the ISO designations of ASA/DIN.</span></span><br/> <span data-ttu-id="74455-120">In genere, un dispositivo supporta valori enumerati discreti, ma è possibile il controllo continuo su un intervallo.</span><span class="sxs-lookup"><span data-stu-id="74455-120">Typically, a device supports discrete enumerated values, but continuous control over a range is possible.</span></span><br/> <span data-ttu-id="74455-121">Il valore 0xFFFFFFFF corrisponde all'impostazione ISO automatica.</span><span class="sxs-lookup"><span data-stu-id="74455-121">A value of 0xFFFFFFFF corresponds to automatic ISO setting.</span></span><br/> |
| <span data-ttu-id="74455-122">**WPD \_ \_ tempo di esposizione immagine \_**</span><span class="sxs-lookup"><span data-stu-id="74455-122">**WPD\_IMAGE\_EXPOSURE\_TIME**</span></span>                                                                                                                 | <span data-ttu-id="74455-123">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="74455-123">**VT\_UI4**</span></span> | <span data-ttu-id="74455-124">Identifica la velocità dell'otturatore del dispositivo quando l'immagine è stata acquisita. Le unità sono in secondi ridimensionate di 10000.</span><span class="sxs-lookup"><span data-stu-id="74455-124">Identifies the shutter speed of the device when this image was captured.Units are in seconds scaled by 10000.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="74455-125">**immagine di WPD \_ \_ FNUMBER**</span><span class="sxs-lookup"><span data-stu-id="74455-125">**WPD\_IMAGE\_FNUMBER**</span></span>                                                                                                                        | <span data-ttu-id="74455-126">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="74455-126">**VT\_UI4**</span></span> | <span data-ttu-id="74455-127">Identifica l'impostazione di apertura della lente quando l'immagine è stata acquisita. Le unità sono uguali al numero f ridimensionato di 100.</span><span class="sxs-lookup"><span data-stu-id="74455-127">Identifies the aperture setting of the lens when this image was captured.Units are equal to the f-number scaled by 100.</span></span><br/>                                                                                                                                                                                                              |
| <span data-ttu-id="74455-128">**\_ \_ risoluzione orizzontale immagine \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="74455-128">**WPD\_IMAGE\_HORIZONTAL\_RESOLUTION**</span></span>                                                                                                         | <span data-ttu-id="74455-129">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="74455-129">**VT\_R8**</span></span>  | <span data-ttu-id="74455-130">Indica la risoluzione orizzontale di un'immagine, espressa in punti per pollice (DPI).</span><span class="sxs-lookup"><span data-stu-id="74455-130">Indicates the horizontal resolution of an image, in dots per inch (DPI) .</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="74455-131">**\_ \_ risoluzione verticale dell'immagine WPD \_**</span><span class="sxs-lookup"><span data-stu-id="74455-131">**WPD\_IMAGE\_VERTICAL\_RESOLUTION**</span></span>                                                                                                           | <span data-ttu-id="74455-132">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="74455-132">**VT\_R8**</span></span>  | <span data-ttu-id="74455-133">Indica la risoluzione verticale di un'immagine, espressa in punti per pollice (DPI).</span><span class="sxs-lookup"><span data-stu-id="74455-133">Indicates the vertical resolution of an image, in dots per inch (DPI) .</span></span>                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="74455-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74455-134">Requirements</span></span>



| <span data-ttu-id="74455-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="74455-135">Requirement</span></span> | <span data-ttu-id="74455-136">Valore</span><span class="sxs-lookup"><span data-stu-id="74455-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="74455-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74455-137">Header</span></span><br/> | <dl> <span data-ttu-id="74455-138"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="74455-138"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74455-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74455-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74455-140">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="74455-140">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




