---
title: Effetto compensazione DPI
description: Usare l'effetto di compensazione DPI per modificare automaticamente una bitmap di input in modo che corrisponda al valore DPI del contesto. Questa operazione è utile per le situazioni in cui viene creata o caricata una bitmap con un valore DPI diverso da quello dello schermo.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a0477d2a57f39738fa9b1ce16c97995c60cf96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874650"
---
# <a name="dpi-compensation-effect"></a><span data-ttu-id="10b25-104">Effetto compensazione DPI</span><span class="sxs-lookup"><span data-stu-id="10b25-104">DPI compensation effect</span></span>

<span data-ttu-id="10b25-105">Usare l'effetto di compensazione DPI per modificare automaticamente una bitmap di input in modo che corrisponda al valore DPI del contesto.</span><span class="sxs-lookup"><span data-stu-id="10b25-105">Use the DPI compensation effect to automatically adjust an input bitmap to match the DPI of the context.</span></span> <span data-ttu-id="10b25-106">Questa operazione è utile per le situazioni in cui viene creata o caricata una bitmap con un valore DPI diverso da quello dello schermo.</span><span class="sxs-lookup"><span data-stu-id="10b25-106">This is useful for situations where a bitmap is created or loaded at a different DPI than the screen.</span></span>

<span data-ttu-id="10b25-107">Il CLSID per questo effetto è CLSID \_ D2D1DpiCompensation.</span><span class="sxs-lookup"><span data-stu-id="10b25-107">The CLSID for this effect is CLSID\_D2D1DpiCompensation.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="10b25-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="10b25-108">Effect properties</span></span>



| <span data-ttu-id="10b25-109">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="10b25-109">Display name and index enumeration</span></span>                                                       | <span data-ttu-id="10b25-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10b25-110">Description</span></span>                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10b25-111">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="10b25-111">InterpolationMode</span></span><br/> <span data-ttu-id="10b25-112">\_Modalità di \_ \_ interpolazione della prop DPICOMPENSATION d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="10b25-112">D2D1\_DPICOMPENSATION\_PROP\_INTERPOLATION\_MODE</span></span><br/> | <span data-ttu-id="10b25-113">Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="10b25-113">The interpolation mode the effect uses to scale the image.</span></span><br/> <span data-ttu-id="10b25-114">Il tipo è D2D1 \_ DPICOMPENSATION \_ Interpolation \_ mode.</span><span class="sxs-lookup"><span data-stu-id="10b25-114">The type is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="10b25-115">Il valore predefinito è D2D1 \_ DPICOMPENSATION \_ modalità di interpolazione \_ \_ lineare.</span><span class="sxs-lookup"><span data-stu-id="10b25-115">The default value is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR .</span></span><br/>                  |
| <span data-ttu-id="10b25-116">BorderMode</span><span class="sxs-lookup"><span data-stu-id="10b25-116">BorderMode</span></span><br/> <span data-ttu-id="10b25-117">\_ \_ \_ Modalità bordo prop DPICOMPENSATION \_ d2d1</span><span class="sxs-lookup"><span data-stu-id="10b25-117">D2D1\_DPICOMPENSATION\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="10b25-118">Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard.</span><span class="sxs-lookup"><span data-stu-id="10b25-118">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="10b25-119">Per altre informazioni, vedere [Border modes](https://www.bing.com/search?q=Border+modes) .</span><span class="sxs-lookup"><span data-stu-id="10b25-119">See [Border modes](https://www.bing.com/search?q=Border+modes) for more info.</span></span> <br/> <span data-ttu-id="10b25-120">Il tipo è D2D1 \_ Border \_ mode.</span><span class="sxs-lookup"><span data-stu-id="10b25-120">The type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="10b25-121">Il valore predefinito è D2D1 \_ Border \_ mode \_ .</span><span class="sxs-lookup"><span data-stu-id="10b25-121">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/> |
| <span data-ttu-id="10b25-122">InputDpi</span><span class="sxs-lookup"><span data-stu-id="10b25-122">InputDpi</span></span><br/> <span data-ttu-id="10b25-123">\_Dpi di \_ input della prop DPICOMPENSATION \_ d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="10b25-123">D2D1\_DPICOMPENSATION\_PROP\_INPUT\_DPI</span></span><br/>                   | <span data-ttu-id="10b25-124">Valore DPI dell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="10b25-124">The DPI of the input image.</span></span><br/> <span data-ttu-id="10b25-125">Il tipo è FLOAT.</span><span class="sxs-lookup"><span data-stu-id="10b25-125">The type is FLOAT.</span></span><br/> <span data-ttu-id="10b25-126">Il valore predefinito è 96.0 f.</span><span class="sxs-lookup"><span data-stu-id="10b25-126">The default value is 96.0f.</span></span><br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a><span data-ttu-id="10b25-127">Modalità di interpolazione</span><span class="sxs-lookup"><span data-stu-id="10b25-127">Interpolation modes</span></span>



| <span data-ttu-id="10b25-128">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="10b25-128">Enumeration</span></span>                                                       | <span data-ttu-id="10b25-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10b25-129">Description</span></span>                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10b25-130">D2D1 \_ DPICOMPENSATION- \_ modalità di interpolazione \_ \_ più vicina \_</span><span class="sxs-lookup"><span data-stu-id="10b25-130">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="10b25-131">Campiona il punto singolo più vicino e lo utilizza.</span><span class="sxs-lookup"><span data-stu-id="10b25-131">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="10b25-132">In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.</span><span class="sxs-lookup"><span data-stu-id="10b25-132">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="10b25-133">D2D1 \_ DPICOMPENSATION- \_ modalità di interpolazione \_ \_ lineare</span><span class="sxs-lookup"><span data-stu-id="10b25-133">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="10b25-134">Usa un esempio a quattro punti e un'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="10b25-134">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="10b25-135">Questa modalità utilizza un tempo di elaborazione maggiore rispetto alla modalità adiacente più vicina, ma restituisce un'immagine di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="10b25-135">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="10b25-136">D2D1 \_ DPICOMPENSATION- \_ modalità di interpolazione \_ \_ cubica</span><span class="sxs-lookup"><span data-stu-id="10b25-136">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="10b25-137">Usa un kernel cubico di esempio 16 per l'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="10b25-137">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="10b25-138">Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="10b25-138">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="10b25-139">D2D1 \_ DPICOMPENSATION- \_ modalità di interpolazione più \_ \_ \_ lineare di esempio \_</span><span class="sxs-lookup"><span data-stu-id="10b25-139">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="10b25-140">USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi.</span><span class="sxs-lookup"><span data-stu-id="10b25-140">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="10b25-141">Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.</span><span class="sxs-lookup"><span data-stu-id="10b25-141">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="10b25-142">D2D1 \_ DPICOMPENSATION \_ modalità di interpolazione \_ \_ anisotropico</span><span class="sxs-lookup"><span data-stu-id="10b25-142">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="10b25-143">Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.</span><span class="sxs-lookup"><span data-stu-id="10b25-143">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="10b25-144">D2D1 \_ DPICOMPENSATION- \_ modalità di interpolazione \_ \_ alta \_ qualità \_ cubica</span><span class="sxs-lookup"><span data-stu-id="10b25-144">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="10b25-145">Usa un kernel cubico a dimensione variabile di alta qualità per eseguire un'downscaling dell'immagine se downscaling è associato alla matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="10b25-145">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="10b25-146">USA quindi la modalità di interpolazione cubica per l'output finale.</span><span class="sxs-lookup"><span data-stu-id="10b25-146">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="10b25-147">Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ DPICOMPENSTION \_ modalità di interpolazione \_ \_ lineare.</span><span class="sxs-lookup"><span data-stu-id="10b25-147">If you don't select a mode, the effect defaults to D2D1\_DPICOMPENSTION\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

## <a name="border-modes"></a><span data-ttu-id="10b25-148">Modalità bordo</span><span class="sxs-lookup"><span data-stu-id="10b25-148">Border modes</span></span>



| <span data-ttu-id="10b25-149">Nome</span><span class="sxs-lookup"><span data-stu-id="10b25-149">Name</span></span>                     | <span data-ttu-id="10b25-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10b25-150">Description</span></span>                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10b25-151">\_Modalità bordo \_ d2d1 \_ Soft</span><span class="sxs-lookup"><span data-stu-id="10b25-151">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="10b25-152">I pixel all'esterno dei limiti di input vengono generati dall' [effetto del bordo mirror](border.md).</span><span class="sxs-lookup"><span data-stu-id="10b25-152">Pixels outside of the input boundaries are generated by the [mirror border effect](border.md).</span></span> <br/> |
| <span data-ttu-id="10b25-153">\_Modalità bordo \_ d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="10b25-153">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="10b25-154">I pixel all'esterno dei limiti di input sono neri trasparenti.</span><span class="sxs-lookup"><span data-stu-id="10b25-154">Pixels outside of the input boundaries are transparent black.</span></span><br/>                                    |



 

## <a name="requirements"></a><span data-ttu-id="10b25-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10b25-155">Requirements</span></span>



| <span data-ttu-id="10b25-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="10b25-156">Requirement</span></span> | <span data-ttu-id="10b25-157">Valore</span><span class="sxs-lookup"><span data-stu-id="10b25-157">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="10b25-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10b25-158">Minimum supported client</span></span> | <span data-ttu-id="10b25-159">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="10b25-159">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="10b25-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10b25-160">Minimum supported server</span></span> | <span data-ttu-id="10b25-161">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="10b25-161">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="10b25-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10b25-162">Header</span></span>                   | <span data-ttu-id="10b25-163">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="10b25-163">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="10b25-164">Libreria</span><span class="sxs-lookup"><span data-stu-id="10b25-164">Library</span></span>                  | <span data-ttu-id="10b25-165">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="10b25-165">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="10b25-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="10b25-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10b25-167">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="10b25-167">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

