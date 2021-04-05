---
title: Effetto di ritaglio
description: Usare l'effetto di ritaglio per restituire un'area specificata di un'immagine.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- effetto di ritaglio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ceaf4cf8b5922fe05e151c1639269f3169b57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873761"
---
# <a name="crop-effect"></a><span data-ttu-id="606a3-104">Effetto di ritaglio</span><span class="sxs-lookup"><span data-stu-id="606a3-104">Crop effect</span></span>

<span data-ttu-id="606a3-105">Usare l'effetto di ritaglio per restituire un'area specificata di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="606a3-105">Use the crop effect to output a specified region of an image.</span></span>

<span data-ttu-id="606a3-106">Il CLSID per questo effetto è CLSID \_ D2D1Crop.</span><span class="sxs-lookup"><span data-stu-id="606a3-106">The CLSID for this effect is CLSID\_D2D1Crop.</span></span>

-   [<span data-ttu-id="606a3-107">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="606a3-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="606a3-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="606a3-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="606a3-109">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="606a3-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="606a3-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="606a3-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="606a3-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="606a3-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="606a3-112">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="606a3-112">Example image</span></span>



| <span data-ttu-id="606a3-113">Prima</span><span class="sxs-lookup"><span data-stu-id="606a3-113">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg) |
| <span data-ttu-id="606a3-115">After</span><span class="sxs-lookup"><span data-stu-id="606a3-115">After</span></span>                                                      |
| ![immagine dopo la trasformazione.](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="606a3-117">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="606a3-117">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="606a3-118">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="606a3-118">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="606a3-119">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="606a3-119">Type and default value</span></span></th>
<th><span data-ttu-id="606a3-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="606a3-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="606a3-121">Rect</span><span class="sxs-lookup"><span data-stu-id="606a3-121">Rect</span></span><br/></td>
<td><span data-ttu-id="606a3-122">D2D1_VECTOR_4F</span><span class="sxs-lookup"><span data-stu-id="606a3-122">D2D1_VECTOR_4F</span></span><br/></td>
<td><span data-ttu-id="606a3-123">Area da ritagliare specificata come vettore nel form (a sinistra, superiore, larghezza, altezza).</span><span class="sxs-lookup"><span data-stu-id="606a3-123">The region to be cropped specified as a vector in the form (left, top, width, height).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="606a3-124">D2D1_CROP_PROP_RECT</span><span class="sxs-lookup"><span data-stu-id="606a3-124">D2D1_CROP_PROP_RECT</span></span><br/></td>
<td><span data-ttu-id="606a3-125">{-FLT_MAX,-FLT_MAX, FLT_MAX, FLT_MAX}</span><span class="sxs-lookup"><span data-stu-id="606a3-125">{-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}</span></span><br/></td>
<td><span data-ttu-id="606a3-126">Le unità sono in tuffi.</span><span class="sxs-lookup"><span data-stu-id="606a3-126">The units are in DIPs.</span></span> <br/>
<blockquote>
<p>[!Note]</p>
<p><span data-ttu-id="606a3-127">Il rettangolo verrà troncato se si sovrappone ai limiti del bordo dell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="606a3-127">The Rect will be truncated if it overlaps the edge boundaries of the input image.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="606a3-128">D2D1_CROP_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="606a3-128">D2D1_CROP_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="606a3-129">D2D1_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="606a3-129">D2D1_BORDER_MODE</span></span> <br/> <span data-ttu-id="606a3-130">D2D1_BORDER_MODE_SOFT</span><span class="sxs-lookup"><span data-stu-id="606a3-130">D2D1_BORDER_MODE_SOFT</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="606a3-131">D2D1_BORDER_MODE_SOFT: se il rettangolo di ritaglio è costituito da coordinate dei pixel frazionari, l'effetto applica l'anti-aliasing che produce un bordo flessibile.</span><span class="sxs-lookup"><span data-stu-id="606a3-131">D2D1_BORDER_MODE_SOFT : If the crop rectangle falls on fractional pixel coordinates, the effect applies antialiasing which results in a soft edge.</span></span></li>
<li><span data-ttu-id="606a3-132">D2D1_BORDER_MODE_HARD: se il rettangolo di ritaglio è costituito da coordinate dei pixel frazionari, l'effetto si blocca che determina un bordo rigido.</span><span class="sxs-lookup"><span data-stu-id="606a3-132">D2D1_BORDER_MODE_HARD : If the crop rectangle falls on fractional pixel coordinates, the effect clamps which results in a hard edge.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="output-bitmap"></a><span data-ttu-id="606a3-133">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="606a3-133">Output bitmap</span></span>

<span data-ttu-id="606a3-134">L'output di questo effetto corrisponde alla dimensione della proprietà Rect.</span><span class="sxs-lookup"><span data-stu-id="606a3-134">The output of this effect is the size of the Rect property.</span></span> <span data-ttu-id="606a3-135">La lunghezza e la larghezza sono calcoli</span><span class="sxs-lookup"><span data-stu-id="606a3-135">The length and width are calc</span></span>

<span data-ttu-id="606a3-136">ulated usando le equazioni qui:</span><span class="sxs-lookup"><span data-stu-id="606a3-136">ulated using the equations here:</span></span> <dl> <span data-ttu-id="606a3-137">Lunghezza di output in pixel = (Rect. Right-Rect. Left) \* (dpi utente/96)</span><span class="sxs-lookup"><span data-stu-id="606a3-137">Output length in Pixels=(Rect.Right-Rect.Left)\*(User's DPI/96)</span></span>  
<span data-ttu-id="606a3-138">Altezza di output in pixel = (Rect. Bottom-Rect.Top) \* (dpi utente/96)</span><span class="sxs-lookup"><span data-stu-id="606a3-138">Output height in pixels=(Rect.Bottom-Rect.Top)\*(User's DPI/96)</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="606a3-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="606a3-139">Requirements</span></span>



| <span data-ttu-id="606a3-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="606a3-140">Requirement</span></span> | <span data-ttu-id="606a3-141">Valore</span><span class="sxs-lookup"><span data-stu-id="606a3-141">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="606a3-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="606a3-142">Minimum supported client</span></span> | <span data-ttu-id="606a3-143">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="606a3-143">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="606a3-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="606a3-144">Minimum supported server</span></span> | <span data-ttu-id="606a3-145">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="606a3-145">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="606a3-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="606a3-146">Header</span></span>                   | <span data-ttu-id="606a3-147">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="606a3-147">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="606a3-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="606a3-148">Library</span></span>                  | <span data-ttu-id="606a3-149">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="606a3-149">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="606a3-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="606a3-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="606a3-151">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="606a3-151">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

