---
title: Metodo ID2D1CommandSink1 SetPrimitiveBlend1
description: Imposta una nuova modalità di Blend primitiva.
ms.assetid: 3EA9EC07-1B2F-48A2-ABFB-2DA0E2EFFBF4
keywords:
- Direct2D metodo SetPrimitiveBlend1
- Metodo SetPrimitiveBlend1 Direct2D, interfaccia ID2D1CommandSink1
- Interfaccia Direct2D di ID2D1CommandSink1, metodo SetPrimitiveBlend1
topic_type:
- apiref
api_name:
- ID2D1CommandSink1.SetPrimitiveBlend1
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3aa961eec873cc84e5b34ce41279c09f580e63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119651"
---
# <a name="id2d1commandsink1setprimitiveblend1-method"></a><span data-ttu-id="accff-106">Metodo ID2D1CommandSink1:: SetPrimitiveBlend1</span><span class="sxs-lookup"><span data-stu-id="accff-106">ID2D1CommandSink1::SetPrimitiveBlend1 method</span></span>

<span data-ttu-id="accff-107">Imposta una nuova modalità di Blend primitiva.</span><span class="sxs-lookup"><span data-stu-id="accff-107">Sets a new primitive blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="accff-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="accff-108">Syntax</span></span>


```C++
HRESULT SetPrimitiveBlend1(
   D2D1_PRIMITIVE_BLEND primitiveBlend
);
```



## <a name="parameters"></a><span data-ttu-id="accff-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="accff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="accff-110">*primitiveBlend*</span><span class="sxs-lookup"><span data-stu-id="accff-110">*primitiveBlend*</span></span> 
</dt> <dd>

<span data-ttu-id="accff-111">Tipo: **[ **d2d1 \_ primitive \_ Blend**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**</span><span class="sxs-lookup"><span data-stu-id="accff-111">Type: **[**D2D1\_PRIMITIVE\_BLEND**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**</span></span>

<span data-ttu-id="accff-112">Blend primitiva che si applicherà alle primitive successive.</span><span class="sxs-lookup"><span data-stu-id="accff-112">The primitive blend that will apply to subsequent primitives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="accff-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="accff-113">Return value</span></span>

<span data-ttu-id="accff-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="accff-114">Type: **HRESULT**</span></span>

<span data-ttu-id="accff-115">Se il metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="accff-115">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="accff-116">Se ha esito negativo, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="accff-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="accff-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="accff-117">Remarks</span></span>

### <a name="blend-modes"></a><span data-ttu-id="accff-118">Modalità di Blend</span><span class="sxs-lookup"><span data-stu-id="accff-118">Blend modes</span></span>

<span data-ttu-id="accff-119">Per il rendering con alias (ad eccezione della modalità MIN), il valore di output O viene calcolato tramite l'interpolazione lineare del valore *Blend (S, D)* con il valore del pixel di destinazione, in base alla quantità che la primitiva copre il pixel di destinazione.</span><span class="sxs-lookup"><span data-stu-id="accff-119">For aliased rendering (except for MIN mode), the output value O is computed by linearly interpolating the value *blend(S, D)* with the destination pixel value, based on the amount that the primitive covers the destination pixel.</span></span>

<span data-ttu-id="accff-120">La tabella seguente mostra le modalità di Blend primitive per la fusione con alias e con aliasing.</span><span class="sxs-lookup"><span data-stu-id="accff-120">The table here shows the primitive blend modes for both aliased and antialiased blending.</span></span> <span data-ttu-id="accff-121">Le equazioni elencate nella tabella utilizzano questi elementi:</span><span class="sxs-lookup"><span data-stu-id="accff-121">The equations listed in the table use these elements:</span></span>

-   <span data-ttu-id="accff-122">O = output</span><span class="sxs-lookup"><span data-stu-id="accff-122">O = Output</span></span>
-   <span data-ttu-id="accff-123">S = origine</span><span class="sxs-lookup"><span data-stu-id="accff-123">S = Source</span></span>
-   <span data-ttu-id="accff-124">SA = Alpha di origine</span><span class="sxs-lookup"><span data-stu-id="accff-124">SA = Source Alpha</span></span>
-   <span data-ttu-id="accff-125">D = destinazione</span><span class="sxs-lookup"><span data-stu-id="accff-125">D = Destination</span></span>
-   <span data-ttu-id="accff-126">DA = Alpha di destinazione</span><span class="sxs-lookup"><span data-stu-id="accff-126">DA = Destination Alpha</span></span>
-   <span data-ttu-id="accff-127">C = copertura pixel</span><span class="sxs-lookup"><span data-stu-id="accff-127">C = Pixel coverage</span></span>



| <span data-ttu-id="accff-128">Modalità di Blend primitiva</span><span class="sxs-lookup"><span data-stu-id="accff-128">Primitive blend mode</span></span>                 | <span data-ttu-id="accff-129">Fusione con alias</span><span class="sxs-lookup"><span data-stu-id="accff-129">Aliased blending</span></span>                            | <span data-ttu-id="accff-130">Blending con anti-aliasing</span><span class="sxs-lookup"><span data-stu-id="accff-130">Antialiased blending</span></span>            | <span data-ttu-id="accff-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="accff-131">Description</span></span>                                                                                                              |
|--------------------------------------|---------------------------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="accff-132">D2D1 \_ \_ origine Blend primitiva \_ \_</span><span class="sxs-lookup"><span data-stu-id="accff-132">D2D1\_PRIMITIVE\_BLEND\_SOURCE\_OVER</span></span> | <span data-ttu-id="accff-133">O = (S + (1 SA) \* D) \* C + D \* (1 C)</span><span class="sxs-lookup"><span data-stu-id="accff-133">O = (S + (1   SA) \* D) \* C + D \* (1   C)</span></span> | <span data-ttu-id="accff-134">O = S \* C + D \* (1 SA \* c)</span><span class="sxs-lookup"><span data-stu-id="accff-134">O = S \* C + D \*(1   SA \*C)</span></span>   | <span data-ttu-id="accff-135">Modalità di Blend di origine/destinazione standard.</span><span class="sxs-lookup"><span data-stu-id="accff-135">The standard source-over-destination blend mode.</span></span>                                                                         |
| <span data-ttu-id="accff-136">\_Copia di \_ Blend PRIMItiva d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="accff-136">D2D1\_PRIMITIVE\_BLEND\_COPY</span></span>         | <span data-ttu-id="accff-137">O = S \* C + D \* (1 C)</span><span class="sxs-lookup"><span data-stu-id="accff-137">O = S \* C + D \* (1   C)</span></span>                   | <span data-ttu-id="accff-138">O = S \* C + D \* (1 C)</span><span class="sxs-lookup"><span data-stu-id="accff-138">O = S \* C + D \* (1   C)</span></span>       | <span data-ttu-id="accff-139">L'origine viene copiata nella destinazione. i pixel di destinazione vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="accff-139">The source is copied to the destination; the destination pixels are ignored.</span></span>                                             |
| <span data-ttu-id="accff-140">\_Min Blend primitiva d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="accff-140">D2D1\_PRIMITIVE\_BLEND\_MIN</span></span>          | <span data-ttu-id="accff-141">O = min (S + 1-SA, D)</span><span class="sxs-lookup"><span data-stu-id="accff-141">O = Min(S + 1-SA, D)</span></span>                        | <span data-ttu-id="accff-142">O = min (S \* c + 1 SA \* c, D)</span><span class="sxs-lookup"><span data-stu-id="accff-142">O = Min(S \* C + 1   SA \*C, D)</span></span> | <span data-ttu-id="accff-143">I valori pixel risultanti usano il minimo dei valori di pixel di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="accff-143">The resulting pixel values use the minimum of the source and destination pixel values.</span></span> <span data-ttu-id="accff-144">Disponibile in Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="accff-144">Available in Windows 8 and later.</span></span> |
| <span data-ttu-id="accff-145">\_Aggiunta d2d1 primitive \_ Blend \_</span><span class="sxs-lookup"><span data-stu-id="accff-145">D2D1\_PRIMITIVE\_BLEND\_ADD</span></span>          | <span data-ttu-id="accff-146">O = (S + D) \* C + d \* (1 C)</span><span class="sxs-lookup"><span data-stu-id="accff-146">O = (S + D) \* C + D \* (1   C)</span></span>             | <span data-ttu-id="accff-147">O = S \* C + D</span><span class="sxs-lookup"><span data-stu-id="accff-147">O = S \* C + D</span></span>                  | <span data-ttu-id="accff-148">I valori pixel risultanti sono la somma dei valori dei pixel di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="accff-148">The resulting pixel values are the sum of the source and destination pixel values.</span></span> <span data-ttu-id="accff-149">Disponibile in Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="accff-149">Available in Windows 8 and later.</span></span>     |



 

![illustrazione delle modalità di Blend primitive Direct2D con opacità e sfondi diversi.](images/primblenddemo.png)

<span data-ttu-id="accff-151">Illustrazione delle modalità di Blend primitive con opacità e sfondi diversi.</span><span class="sxs-lookup"><span data-stu-id="accff-151">An illustration of the primitive blend modes with varying opacity and backgrounds.</span></span>

<span data-ttu-id="accff-152">La Blend primitiva verrà applicata a tutte le primitive disegnate nel contesto, a meno che non venga sottoposto a override con il parametro *compositeMode* nell'API [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) .</span><span class="sxs-lookup"><span data-stu-id="accff-152">The primitive blend will apply to all of the primitive drawn on the context, unless this is overridden with the *compositeMode* parameter on the [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) API.</span></span>

<span data-ttu-id="accff-153">La Blend primitiva si applica all'interno di qualsiasi primitiva disegnata nel contesto.</span><span class="sxs-lookup"><span data-stu-id="accff-153">The primitive blend applies to the interior of any primitives drawn on the context.</span></span> <span data-ttu-id="accff-154">Nel caso di [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), questo sarà implicito nel rettangolo dell'immagine, nell'offset e nella trasformazione globale.</span><span class="sxs-lookup"><span data-stu-id="accff-154">In the case of [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), this will be implied by the image rectangle, offset and world transform.</span></span>

<span data-ttu-id="accff-155">Se la Blend primitiva è un valore diverso da **d2d1 \_ primitive \_ Blend \_** , il rendering ClearType verrà disattivato.</span><span class="sxs-lookup"><span data-stu-id="accff-155">If the primitive blend is anything other than **D2D1\_PRIMITIVE\_BLEND\_OVER** then ClearType rendering will be turned off.</span></span> <span data-ttu-id="accff-156">Se l'applicazione forza in modo esplicito il rendering ClearType in queste modalità, il contesto di disegno verrà inserito in uno stato di errore.</span><span class="sxs-lookup"><span data-stu-id="accff-156">If the application explicitly forces ClearType rendering in these modes, the drawing context will be placed in an error state.</span></span> <span data-ttu-id="accff-157">\_ \_ Lo stato D2DERR errato verrà restituito da [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span><span class="sxs-lookup"><span data-stu-id="accff-157">D2DERR\_WRONG\_STATE will be returned from either [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span></span>

## <a name="requirements"></a><span data-ttu-id="accff-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="accff-158">Requirements</span></span>



| <span data-ttu-id="accff-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="accff-159">Requirement</span></span> | <span data-ttu-id="accff-160">Valore</span><span class="sxs-lookup"><span data-stu-id="accff-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="accff-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="accff-161">Minimum supported client</span></span><br/> | <span data-ttu-id="accff-162">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="accff-162">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="accff-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="accff-163">Minimum supported server</span></span><br/> | <span data-ttu-id="accff-164">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="accff-164">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="accff-165">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="accff-165">Minimum supported phone</span></span><br/>  | <span data-ttu-id="accff-166">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="accff-166">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="accff-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="accff-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="accff-168">**ID2D1CommandSink1**</span><span class="sxs-lookup"><span data-stu-id="accff-168">**ID2D1CommandSink1**</span></span>](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1commandsink1)
</dt> </dl>

 

