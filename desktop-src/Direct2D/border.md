---
title: Effetto bordo
description: Utilizzare l'effetto bordo per estendere un'immagine dai bordi.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- effetto bordo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fb43ae8b3e9c4eb449a8231f8b4ffcacf7658b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104530414"
---
# <a name="border-effect"></a><span data-ttu-id="f2367-104">Effetto bordo</span><span class="sxs-lookup"><span data-stu-id="f2367-104">Border effect</span></span>

<span data-ttu-id="f2367-105">Utilizzare l'effetto bordo per estendere un'immagine dai bordi.</span><span class="sxs-lookup"><span data-stu-id="f2367-105">Use the border effect to extend an image from the edges.</span></span> <span data-ttu-id="f2367-106">È possibile utilizzare questo effetto per ripetere i pixel dai bordi dell'immagine, eseguire il wrapping dei pixel dall'estremità opposta dell'immagine o eseguire il mirroring dei pixel sul bordo della bitmap per estendere l'area bitmap.</span><span class="sxs-lookup"><span data-stu-id="f2367-106">You can use this effect to repeat the pixels from the edges of the image, wrap the pixels from the opposite end of the image, or mirror the pixels across the bitmap border to extend the bitmap region.</span></span>

<span data-ttu-id="f2367-107">Il CLSID per questo effetto è CLSID \_ D2D1Border.</span><span class="sxs-lookup"><span data-stu-id="f2367-107">The CLSID for this effect is CLSID\_D2D1Border.</span></span>

## <a name="example-images"></a><span data-ttu-id="f2367-108">Immagini di esempio</span><span class="sxs-lookup"><span data-stu-id="f2367-108">Example images</span></span>

<span data-ttu-id="f2367-109">Negli esempi riportati di seguito viene illustrato l'output dell'effetto del bordo utilizzando ogni modalità.</span><span class="sxs-lookup"><span data-stu-id="f2367-109">The examples here show the output of the border effect using each mode.</span></span> <span data-ttu-id="f2367-110">Le dimensioni di output sono infinite, ma queste immagini di esempio vengono ritagliate fino al doppio delle dimensioni.</span><span class="sxs-lookup"><span data-stu-id="f2367-110">The output size is infinite, but these example images are cropped to twice the size.</span></span>

### <a name="mirror"></a><span data-ttu-id="f2367-111">Mirror</span><span class="sxs-lookup"><span data-stu-id="f2367-111">Mirror</span></span>



| <span data-ttu-id="f2367-112">Prima</span><span class="sxs-lookup"><span data-stu-id="f2367-112">Before</span></span>                                                    |
|-----------------------------------------------------------|
| ![Screenshot che mostra l'immagine prima dell'effetto.](images/border-before.jpg) |
| <span data-ttu-id="f2367-114">After</span><span class="sxs-lookup"><span data-stu-id="f2367-114">After</span></span>                                                     |
| ![Screenshot che mostra l'immagine dopo la trasformazione.](images/10-border.png)   |



 

### <a name="clamp"></a><span data-ttu-id="f2367-116">Clamp</span><span class="sxs-lookup"><span data-stu-id="f2367-116">Clamp</span></span>



| <span data-ttu-id="f2367-117">Prima</span><span class="sxs-lookup"><span data-stu-id="f2367-117">Before</span></span>                                                        |
|---------------------------------------------------------------|
| ![Screenshot che mostra l'immagine prima dell'effetto per un morsetto.](images/border-before.jpg)     |
| <span data-ttu-id="f2367-119">After</span><span class="sxs-lookup"><span data-stu-id="f2367-119">After</span></span>                                                         |
| ![Screenshot che mostra l'immagine dopo la trasformazione per un morsetto.](images/10-border-clamp.png) |



 

### <a name="wrap"></a><span data-ttu-id="f2367-121">Wrap</span><span class="sxs-lookup"><span data-stu-id="f2367-121">Wrap</span></span>



| <span data-ttu-id="f2367-122">Prima</span><span class="sxs-lookup"><span data-stu-id="f2367-122">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![Screenshot che mostra l'immagine prima dell'effetto per un ritorno a capo.](images/border-before.jpg)    |
| <span data-ttu-id="f2367-124">After</span><span class="sxs-lookup"><span data-stu-id="f2367-124">After</span></span>                                                        |
| ![Screenshot che mostra l'immagine dopo la trasformazione per un ritorno a capo.](images/10-border-wrap.png) |



 


```C++
ComPtr<ID2D1Effect> borderEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Border, &borderEffect);

borderEffect->SetInput(0, bitmap);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_X, D2D1_BORDER_EDGE_MODE_MIRROR);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_Y, D2D1_BORDER_EDGE_MODE_MIRROR);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(borderEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a><span data-ttu-id="f2367-126">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="f2367-126">Effect properties</span></span>



| <span data-ttu-id="f2367-127">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="f2367-127">Display name and index enumeration</span></span>                                  | <span data-ttu-id="f2367-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2367-128">Description</span></span>                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2367-129">Modalità bordo X</span><span class="sxs-lookup"><span data-stu-id="f2367-129">Edge Mode X</span></span><br/> <span data-ttu-id="f2367-130">\_ \_ \_ Modalità bordo prop bordo \_ d2d1 \_ X</span><span class="sxs-lookup"><span data-stu-id="f2367-130">D2D1\_BORDER\_PROP\_EDGE\_MODE\_X</span></span><br/> | <span data-ttu-id="f2367-131">Modalità bordo nella direzione X dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="f2367-131">The edge mode in the X direction for the effect.</span></span> <span data-ttu-id="f2367-132">È possibile impostare questa impostazione su Clamp, wrap o mirror.</span><span class="sxs-lookup"><span data-stu-id="f2367-132">You can set this to clamp, wrap, or mirror.</span></span> <span data-ttu-id="f2367-133">Per altre informazioni, vedere [modalità Edge](#edge-modes) .</span><span class="sxs-lookup"><span data-stu-id="f2367-133">See [Edge modes](#edge-modes) for more info.</span></span><br/> <span data-ttu-id="f2367-134">Il tipo è D2D1 \_ Border \_ Edge \_ mode.</span><span class="sxs-lookup"><span data-stu-id="f2367-134">The type is D2D1\_BORDER\_EDGE\_MODE.</span></span><br/> <span data-ttu-id="f2367-135">Il valore predefinito è D2D1 \_ Border \_ Edge \_ mode \_ Clamp.</span><span class="sxs-lookup"><span data-stu-id="f2367-135">The default value is D2D1\_BORDER\_EDGE\_MODE\_CLAMP.</span></span><br/> |
| <span data-ttu-id="f2367-136">Modalità bordo Y</span><span class="sxs-lookup"><span data-stu-id="f2367-136">Edge Mode Y</span></span><br/> <span data-ttu-id="f2367-137">D2D1 \_ bordo della \_ prop in \_ \_ modalità bordo \_ Y</span><span class="sxs-lookup"><span data-stu-id="f2367-137">D2D1\_BORDER\_PROP\_EDGE\_MODE\_Y</span></span><br/> | <span data-ttu-id="f2367-138">Modalità bordo nella direzione Y dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="f2367-138">The edge mode in the Y direction for the effect.</span></span> <span data-ttu-id="f2367-139">È possibile impostare questa impostazione su Clamp, wrap o mirror.</span><span class="sxs-lookup"><span data-stu-id="f2367-139">You can set this to clamp, wrap, or mirror.</span></span> <span data-ttu-id="f2367-140">Per altre informazioni, vedere [modalità Edge](#edge-modes) .</span><span class="sxs-lookup"><span data-stu-id="f2367-140">See [Edge modes](#edge-modes) for more info.</span></span><br/> <span data-ttu-id="f2367-141">Il tipo è D2D1 \_ Border \_ Edge \_ mode.</span><span class="sxs-lookup"><span data-stu-id="f2367-141">The type is D2D1\_BORDER\_EDGE\_MODE.</span></span><br/> <span data-ttu-id="f2367-142">Il valore predefinito è D2D1 \_ Border \_ Edge \_ mode \_ Clamp.</span><span class="sxs-lookup"><span data-stu-id="f2367-142">The default value is D2D1\_BORDER\_EDGE\_MODE\_CLAMP.</span></span><br/> |



 

## <a name="edge-modes"></a><span data-ttu-id="f2367-143">Modalità Edge</span><span class="sxs-lookup"><span data-stu-id="f2367-143">Edge modes</span></span>



| <span data-ttu-id="f2367-144">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="f2367-144">Display name and index enumeration</span></span>                            | <span data-ttu-id="f2367-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2367-145">Description</span></span>                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f2367-146">Clamp</span><span class="sxs-lookup"><span data-stu-id="f2367-146">Clamp</span></span><br/> <span data-ttu-id="f2367-147">\_Clamp in \_ \_ modalità bordo d2d1 bordo \_</span><span class="sxs-lookup"><span data-stu-id="f2367-147">D2D1\_BORDER\_EDGE\_MODE\_CLAMP</span></span><br/>   | <span data-ttu-id="f2367-148">Ripete i pixel dai bordi dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="f2367-148">Repeats the pixels from the edges of the image.</span></span>      |
| <span data-ttu-id="f2367-149">Wrap</span><span class="sxs-lookup"><span data-stu-id="f2367-149">Wrap</span></span><br/> <span data-ttu-id="f2367-150">\_Wrapping in \_ \_ modalità bordo \_ bordo d2d1</span><span class="sxs-lookup"><span data-stu-id="f2367-150">D2D1\_BORDER\_EDGE\_MODE\_WRAP</span></span><br/>     | <span data-ttu-id="f2367-151">USA i pixel dall'estremità opposta dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="f2367-151">Uses pixels from the opposite end edge of the image.</span></span> |
| <span data-ttu-id="f2367-152">Mirror</span><span class="sxs-lookup"><span data-stu-id="f2367-152">Mirror</span></span><br/> <span data-ttu-id="f2367-153">\_ \_ \_ Mirroring della modalità \_ bordo bordo d2d1</span><span class="sxs-lookup"><span data-stu-id="f2367-153">D2D1\_BORDER\_EDGE\_MODE\_MIRROR</span></span><br/> | <span data-ttu-id="f2367-154">Riflette i pixel relativi al bordo dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="f2367-154">Reflects pixels about the edge of the image.</span></span>         |



 

## <a name="output-bitmap"></a><span data-ttu-id="f2367-155">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="f2367-155">Output bitmap</span></span>

<span data-ttu-id="f2367-156">Le dimensioni della bitmap di output sono infinite per tutti gli input, ad eccezione di un'immagine di input di dimensioni 0.</span><span class="sxs-lookup"><span data-stu-id="f2367-156">The output bitmap size is infinite for all inputs, except a 0 sized input image.</span></span> <span data-ttu-id="f2367-157">Se l'altezza o la larghezza di un'immagine di input è 0, le dimensioni di output sono pari a 0.</span><span class="sxs-lookup"><span data-stu-id="f2367-157">If the height or the width of an input image is 0, the output size is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2367-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2367-158">Requirements</span></span>



| <span data-ttu-id="f2367-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2367-159">Requirement</span></span> | <span data-ttu-id="f2367-160">Valore</span><span class="sxs-lookup"><span data-stu-id="f2367-160">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f2367-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2367-161">Minimum supported client</span></span> | <span data-ttu-id="f2367-162">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="f2367-162">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f2367-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2367-163">Minimum supported server</span></span> | <span data-ttu-id="f2367-164">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="f2367-164">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="f2367-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2367-165">Header</span></span>                   | <span data-ttu-id="f2367-166">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="f2367-166">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="f2367-167">Libreria</span><span class="sxs-lookup"><span data-stu-id="f2367-167">Library</span></span>                  | <span data-ttu-id="f2367-168">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="f2367-168">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="f2367-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f2367-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2367-170">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="f2367-170">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

