---
title: Effetto Mappa di spostamento
description: Utilizzare l'effetto Mappa di spostamento per posizionare i pixel dell'immagine di input in base ai valori di intensità di una seconda immagine di input.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- effetto Mappa di spostamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ad2deb0c584ccc9c55faebd60f803d66efa42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119058"
---
# <a name="displacement-map-effect"></a><span data-ttu-id="1d8dc-104">Effetto Mappa di spostamento</span><span class="sxs-lookup"><span data-stu-id="1d8dc-104">Displacement map effect</span></span>

<span data-ttu-id="1d8dc-105">Utilizzare l'effetto Mappa di spostamento per posizionare i pixel dell'immagine di input in base ai valori di intensità di una seconda immagine di input.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-105">Use the displacement map effect to displace the pixels of the input image by the intensity values of a second input image.</span></span>

<span data-ttu-id="1d8dc-106">Il CLSID per questo effetto è CLSID \_ D2D1DisplacementMap.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-106">The CLSID for this effect is CLSID\_D2D1DisplacementMap.</span></span>

-   [<span data-ttu-id="1d8dc-107">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="1d8dc-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="1d8dc-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="1d8dc-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="1d8dc-109">Canali colori</span><span class="sxs-lookup"><span data-stu-id="1d8dc-109">Color channels</span></span>](#color-channels)
-   [<span data-ttu-id="1d8dc-110">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="1d8dc-110">Output Bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="1d8dc-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d8dc-111">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="1d8dc-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d8dc-112">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="1d8dc-113">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="1d8dc-113">Example image</span></span>



| <span data-ttu-id="1d8dc-114">Prima</span><span class="sxs-lookup"><span data-stu-id="1d8dc-114">Before</span></span>                                                           |
|------------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)       |
| <span data-ttu-id="1d8dc-116">After</span><span class="sxs-lookup"><span data-stu-id="1d8dc-116">After</span></span>                                                            |
| ![immagine dopo la trasformazione.](images/19-displacementmap.png) |



 


```C++
ComPtr<ID2D1Effect> displacementMapEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DisplacementMap, &displacementMapEffect);

displacementMapEffect->SetInput(0, bitmap);
displacementMapEffect->SetValue(D2D1_DISPLACEMENTMAP_PROP_SCALE, 100.0f);

// The second input of the displacement effect determines how the input image is transformed.
// For this example, we will use a turbulence effect as the second input to randomly distort the image.
ComPtr<ID2D1Effect> turbulenceEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Turbulence, &turbulenceEffect);
displacementMapEffect->SetInputEffect(1, turbulenceEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(displacementMapEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="1d8dc-118">I percorsi dei pixel nell'output vengono determinati utilizzando la formula seguente:</span><span class="sxs-lookup"><span data-stu-id="1d8dc-118">The locations of the pixels in the output are determined using this formula:</span></span>

<span data-ttu-id="1d8dc-119">C'(x, y) = C (x + scale \* (XChannelSelector (bitmap di spostamento (x, y))-0,5), y + scale \* (YChannelSelector (bitmap di spostamento (x, y))-0,5))</span><span class="sxs-lookup"><span data-stu-id="1d8dc-119">C' (x,y)=C(x+ scale\*(XChannelSelector(Displacement Bitmap (x,y))-0.5),y+ scale\*(YChannelSelector(Displacement Bitmap (x,y))-0.5))</span></span>

<span data-ttu-id="1d8dc-120">Dove:</span><span class="sxs-lookup"><span data-stu-id="1d8dc-120">Where:</span></span><dl> <span data-ttu-id="1d8dc-121">*C (x, y)* è il pixel di output in corrispondenza di (x, y).</span><span class="sxs-lookup"><span data-stu-id="1d8dc-121">*C  (x, y)* is the output pixel at (x, y).</span></span>  
<span data-ttu-id="1d8dc-122">*C (x, y)* è il pixel di input in corrispondenza di (x, y).</span><span class="sxs-lookup"><span data-stu-id="1d8dc-122">*C (x, y)* is the input pixel at (x, y).</span></span>  
<span data-ttu-id="1d8dc-123">La *bitmap di spostamento (x, y)* è l'intensità del pixel di spostamento in corrispondenza delle coordinate specificate.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-123">*Displacement Bitmap (x, y)* is the displacement pixel intensity at the specified coordinates</span></span>  
<span data-ttu-id="1d8dc-124">*XChannelSelector* l'intensità del canale RGBA selezionato dalla bitmap di spostamento che sposta l'immagine di input nella direzione X.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-124">*XChannelSelector* the intensity of the selected RGBA channel from the displacement bitmap that displaces the input image in the X direction.</span></span>  
<span data-ttu-id="1d8dc-125">*YChannelSelector* l'intensità del canale RGBA selezionato dalla bitmap di spostamento che sposta l'immagine di input nella direzione Y.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-125">*YChannelSelector* the intensity of the selected RGBA channel from the displacement bitmap that displaces the input image in the Y direction.</span></span>  
</dl>

<span data-ttu-id="1d8dc-126">L'effetto Ricampiona l'immagine di input in base alla proprietà scale e all'intensità dell'immagine di spostamento.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-126">The effect resamples the input image according to the scale property and the intensity of the displacement image.</span></span> <span data-ttu-id="1d8dc-127">Usa l'interpolazione bilineare se il campionamento è compreso tra i pixel nell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-127">It uses bilinear interpolation if sampling from between pixels in the input image.</span></span>

<span data-ttu-id="1d8dc-128">Questo effetto funziona su immagini alfa diritte e premoltiplicate.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-128">This effect works on straight and premultiplied alpha images.</span></span> <span data-ttu-id="1d8dc-129">Il formato alfa di output corrisponde al formato di input.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-129">The output alpha format is the same as the input format.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="1d8dc-130">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="1d8dc-130">Effect properties</span></span>



| <span data-ttu-id="1d8dc-131">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="1d8dc-131">Display name and index enumeration</span></span>                                                   | <span data-ttu-id="1d8dc-132">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="1d8dc-132">Type and default value</span></span>                                                   | <span data-ttu-id="1d8dc-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d8dc-133">Description</span></span>                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d8dc-134">Scalabilità</span><span class="sxs-lookup"><span data-stu-id="1d8dc-134">Scale</span></span><br/> <span data-ttu-id="1d8dc-135">D2D1 \_ DISPLACEMENTMAP \_ prop \_ scale</span><span class="sxs-lookup"><span data-stu-id="1d8dc-135">D2D1\_DISPLACEMENTMAP\_PROP\_SCALE</span></span><br/>                       | <span data-ttu-id="1d8dc-136">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1d8dc-136">FLOAT</span></span><br/> <span data-ttu-id="1d8dc-137">0,0 f</span><span class="sxs-lookup"><span data-stu-id="1d8dc-137">0.0f</span></span><br/>                                         | <span data-ttu-id="1d8dc-138">Moltiplica l'intensità del canale selezionato dall'immagine di spostamento.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-138">Multiplies the intensity of the selected channel from the displacement image.</span></span> <span data-ttu-id="1d8dc-139">Maggiore è l'impostazione di questa proprietà, maggiore sarà l'effetto di spostamento dei pixel</span><span class="sxs-lookup"><span data-stu-id="1d8dc-139">The higher you set this property, the more the effect displaces the pixels</span></span><br/>                       |
| <span data-ttu-id="1d8dc-140">XChannelSelect</span><span class="sxs-lookup"><span data-stu-id="1d8dc-140">XChannelSelect</span></span><br/> <span data-ttu-id="1d8dc-141">\_Selezione del canale d2d1 DISPLACEMENTMAP \_ prop \_ X \_ \_</span><span class="sxs-lookup"><span data-stu-id="1d8dc-141">D2D1\_DISPLACEMENTMAP\_PROP\_X\_CHANNEL\_SELECT</span></span><br/> | <span data-ttu-id="1d8dc-142">\_Selettore di canale d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="1d8dc-142">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="1d8dc-143">\_ \_ Selettore \_ di canale A d2d1</span><span class="sxs-lookup"><span data-stu-id="1d8dc-143">D2D1\_CHANNEL\_SELECTOR\_A</span></span><br/> | <span data-ttu-id="1d8dc-144">L'effetto estrae l'intensità da questo canale di colore e la usa per posizionare l'immagine nella direzione X.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-144">The effect extracts the intensity from this color channel and uses it to spatially displace the image in the X direction.</span></span> <span data-ttu-id="1d8dc-145">Per altre informazioni, vedere [canali dei colori](#color-channels) .</span><span class="sxs-lookup"><span data-stu-id="1d8dc-145">See [Color channels](#color-channels) for more info.</span></span><br/> |
| <span data-ttu-id="1d8dc-146">YChannelSelect</span><span class="sxs-lookup"><span data-stu-id="1d8dc-146">YChannelSelect</span></span><br/> <span data-ttu-id="1d8dc-147">\_Select d2d1 DISPLACEMENTMAP \_ prop \_ Y \_ Channel \_</span><span class="sxs-lookup"><span data-stu-id="1d8dc-147">D2D1\_DISPLACEMENTMAP\_PROP\_Y\_CHANNEL\_SELECT</span></span><br/> | <span data-ttu-id="1d8dc-148">\_Selettore di canale d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="1d8dc-148">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="1d8dc-149">\_ \_ Selettore \_ di canale A d2d1</span><span class="sxs-lookup"><span data-stu-id="1d8dc-149">D2D1\_CHANNEL\_SELECTOR\_A</span></span><br/> | <span data-ttu-id="1d8dc-150">L'effetto estrae l'intensità da questo canale di colore e la usa per posizionare l'immagine nella direzione Y.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-150">The effect extracts the intensity from this color channel and uses it to spatially displace the image in the Y direction.</span></span> <span data-ttu-id="1d8dc-151">Per altre informazioni, vedere [canali dei colori](#color-channels) .</span><span class="sxs-lookup"><span data-stu-id="1d8dc-151">See [Color channels](#color-channels) for more info.</span></span><br/> |



 

## <a name="color-channels"></a><span data-ttu-id="1d8dc-152">Canali colori</span><span class="sxs-lookup"><span data-stu-id="1d8dc-152">Color channels</span></span>



| <span data-ttu-id="1d8dc-153">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="1d8dc-153">Enumeration</span></span>                | <span data-ttu-id="1d8dc-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d8dc-154">Description</span></span>                                                      |
|----------------------------|------------------------------------------------------------------|
| <span data-ttu-id="1d8dc-155">\_ \_ R selettore canale d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="1d8dc-155">D2D1\_CHANNEL\_SELECTOR\_R</span></span> | <span data-ttu-id="1d8dc-156">L'effetto estrae l'output dell'intensità dal canale rosso.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-156">The effect extracts the intensity output from the red channel.</span></span>   |
| <span data-ttu-id="1d8dc-157">\_Selettore di canale d2d1 \_ \_ G</span><span class="sxs-lookup"><span data-stu-id="1d8dc-157">D2D1\_CHANNEL\_SELECTOR\_G</span></span> | <span data-ttu-id="1d8dc-158">L'effetto estrae l'output dell'intensità dal canale verde.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-158">The effect extracts the intensity output from the green channel.</span></span> |
| <span data-ttu-id="1d8dc-159">\_Selettore di canale d2d1 \_ \_ B</span><span class="sxs-lookup"><span data-stu-id="1d8dc-159">D2D1\_CHANNEL\_SELECTOR\_B</span></span> | <span data-ttu-id="1d8dc-160">L'effetto estrae l'output dell'intensità dal canale blu.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-160">The effect extracts the intensity output from the blue channel.</span></span>  |
| <span data-ttu-id="1d8dc-161">\_ \_ Selettore \_ di canale A d2d1</span><span class="sxs-lookup"><span data-stu-id="1d8dc-161">D2D1\_CHANNEL\_SELECTOR\_A</span></span> | <span data-ttu-id="1d8dc-162">L'effetto estrae l'output dell'intensità dal canale alfa.</span><span class="sxs-lookup"><span data-stu-id="1d8dc-162">The effect extracts the intensity output from the alpha channel.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="1d8dc-163">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="1d8dc-163">Output Bitmap</span></span>

<span data-ttu-id="1d8dc-164">È possibile determinare le dimensioni massime della bitmap di output con le equazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d8dc-164">You can determine the maximum size of the output bitmap with these equations:</span></span>

<span data-ttu-id="1d8dc-165">Bitmap di output?</span><span class="sxs-lookup"><span data-stu-id="1d8dc-165">Output Bitmap?</span></span> <span data-ttu-id="1d8dc-166">Pixel = (dimensioni bitmap di input? ( DIP) + scala) \* (dpi utente/96)</span><span class="sxs-lookup"><span data-stu-id="1d8dc-166">Pixels=(Input Bitmap Size?(DIPs)+Scale)\*(User DPI/96)</span></span>

<span data-ttu-id="1d8dc-167">Bitmap di output<sub>y</sub> pixel = (input bitmap size<sub>y</sub>(DIP) + scale) \* (dpi utente/96)</span><span class="sxs-lookup"><span data-stu-id="1d8dc-167">Output Bitmap<sub>y</sub> Pixels=(Input Bitmap Size<sub>y</sub>(DIPs) + Scale)\*(User DPI/96)</span></span>

## <a name="requirements"></a><span data-ttu-id="1d8dc-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d8dc-168">Requirements</span></span>



| <span data-ttu-id="1d8dc-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d8dc-169">Requirement</span></span> | <span data-ttu-id="1d8dc-170">Valore</span><span class="sxs-lookup"><span data-stu-id="1d8dc-170">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1d8dc-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d8dc-171">Minimum supported client</span></span> | <span data-ttu-id="1d8dc-172">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="1d8dc-172">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="1d8dc-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d8dc-173">Minimum supported server</span></span> | <span data-ttu-id="1d8dc-174">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="1d8dc-174">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="1d8dc-175">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d8dc-175">Header</span></span>                   | <span data-ttu-id="1d8dc-176">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="1d8dc-176">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="1d8dc-177">Libreria</span><span class="sxs-lookup"><span data-stu-id="1d8dc-177">Library</span></span>                  | <span data-ttu-id="1d8dc-178">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="1d8dc-178">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="1d8dc-179">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d8dc-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d8dc-180">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="1d8dc-180">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

