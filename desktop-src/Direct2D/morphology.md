---
title: Effetto morfologia
description: Usare l'effetto morfologia per assottigliare o ispessire i limiti del bordo in un'immagine.
ms.assetid: 4B3CFC51-D556-4729-B433-7307C80291F4
keywords:
- effetti morfologici
- effetto dilate
- erosione effetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43cf41810ae0b16c9bc96dd37473a0231fc132c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120470"
---
# <a name="morphology-effect"></a><span data-ttu-id="d5d25-106">Effetto morfologia</span><span class="sxs-lookup"><span data-stu-id="d5d25-106">Morphology effect</span></span>

<span data-ttu-id="d5d25-107">Usare l'effetto morfologia per assottigliare o ispessire i limiti del bordo in un'immagine.</span><span class="sxs-lookup"><span data-stu-id="d5d25-107">Use the morphology effect to thin or thicken edge boundaries in an image.</span></span> <span data-ttu-id="d5d25-108">Questo effetto crea un kernel che è 2 volte i valori di larghezza e altezza specificati.</span><span class="sxs-lookup"><span data-stu-id="d5d25-108">This effect creates a kernel that is 2 times the Width and Height values you specify.</span></span> <span data-ttu-id="d5d25-109">Questo effetto centra il kernel sul pixel che sta calcolando e restituisce il valore massimo nel kernel (se si dilata) o il valore minimo nel kernel (in caso di erosione).</span><span class="sxs-lookup"><span data-stu-id="d5d25-109">This effect centers the kernel on the pixel it is calculating and returns the maximum value in the kernel (if dilating) or minimum value in the kernel (if eroding).</span></span>

<span data-ttu-id="d5d25-110">Il CLSID per questo effetto è CLSID \_ D2D1Morphology.</span><span class="sxs-lookup"><span data-stu-id="d5d25-110">The CLSID for this effect is CLSID\_D2D1Morphology.</span></span>

## <a name="example-images"></a><span data-ttu-id="d5d25-111">Immagini di esempio</span><span class="sxs-lookup"><span data-stu-id="d5d25-111">Example images</span></span>

<span data-ttu-id="d5d25-112">Questo esempio mostra l'output dell'effetto quando si usa la modalità di erosione.</span><span class="sxs-lookup"><span data-stu-id="d5d25-112">This example shows the output of the effect when using the erode mode.</span></span>



| <span data-ttu-id="d5d25-113">Prima</span><span class="sxs-lookup"><span data-stu-id="d5d25-113">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg) |
| <span data-ttu-id="d5d25-115">After</span><span class="sxs-lookup"><span data-stu-id="d5d25-115">After</span></span>                                                      |
| ![immagine dopo la trasformazione.](images/7-morphology.png) |



 


```C++
ComPtr<ID2D1Effect> morphologyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Morphology, &morphologyEffect);

morphologyEffect->SetInput(0, bitmap);

morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_MODE, D2D1_MORPHOLOGY_MODE_ERODE);
morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_WIDTH, 14);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(morphologyEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a><span data-ttu-id="d5d25-117">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="d5d25-117">Effect properties</span></span>



| <span data-ttu-id="d5d25-118">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="d5d25-118">Display name and index enumeration</span></span>                          | <span data-ttu-id="d5d25-119">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="d5d25-119">Type and default value</span></span>                                                     | <span data-ttu-id="d5d25-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5d25-120">Description</span></span>                                                                                                                                                       |
|-------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d25-121">Mode</span><span class="sxs-lookup"><span data-stu-id="d5d25-121">Mode</span></span><br/> <span data-ttu-id="d5d25-122">\_Modalità prop della morfologia d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="d5d25-122">D2D1\_MORPHOLOGY\_PROP\_MODE</span></span><br/>     | <span data-ttu-id="d5d25-123">\_Modalità morfologia d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="d5d25-123">D2D1\_MORPHOLOGY\_MODE</span></span><br/> <span data-ttu-id="d5d25-124">\_ \_ Erosione della modalità MORFOLOGIa d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="d5d25-124">D2D1\_MORPHOLOGY\_MODE\_ERODE</span></span><br/> | <span data-ttu-id="d5d25-125">Modalità morfologia.</span><span class="sxs-lookup"><span data-stu-id="d5d25-125">The morphology mode.</span></span> <span data-ttu-id="d5d25-126">Le modalità disponibili sono Erode (Flat) e dilate (ispessimento).</span><span class="sxs-lookup"><span data-stu-id="d5d25-126">The available modes are erode (flatten) and dilate (thicken).</span></span><br/> <span data-ttu-id="d5d25-127">Per altre informazioni, vedere [modalità di morfologia](#morphology-modes) .</span><span class="sxs-lookup"><span data-stu-id="d5d25-127">See [Morphology modes](#morphology-modes) for more info.</span></span><br/> |
| <span data-ttu-id="d5d25-128">Larghezza</span><span class="sxs-lookup"><span data-stu-id="d5d25-128">Width</span></span><br/> <span data-ttu-id="d5d25-129">\_Larghezza prop della morfologia d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="d5d25-129">D2D1\_MORPHOLOGY\_PROP\_WIDTH</span></span><br/>   | <span data-ttu-id="d5d25-130">UINT</span><span class="sxs-lookup"><span data-stu-id="d5d25-130">UINT</span></span><br/> <span data-ttu-id="d5d25-131">1</span><span class="sxs-lookup"><span data-stu-id="d5d25-131">1</span></span><br/>                                               | <span data-ttu-id="d5d25-132">Dimensione del kernel nella direzione X.</span><span class="sxs-lookup"><span data-stu-id="d5d25-132">Size of the kernel in the X direction.</span></span> <span data-ttu-id="d5d25-133">Le unità sono in tuffi.</span><span class="sxs-lookup"><span data-stu-id="d5d25-133">The units are in DIPs.</span></span> <span data-ttu-id="d5d25-134">I valori devono essere compresi tra 1 e 100 inclusi.</span><span class="sxs-lookup"><span data-stu-id="d5d25-134">Values must be between 1 and 100 inclusive.</span></span>                                                         |
| <span data-ttu-id="d5d25-135">Altezza</span><span class="sxs-lookup"><span data-stu-id="d5d25-135">Height</span></span><br/> <span data-ttu-id="d5d25-136">\_Altezza della \_ prop MORFOLOGIa d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="d5d25-136">D2D1\_MORPHOLOGY\_PROP\_HEIGHT</span></span><br/> | <span data-ttu-id="d5d25-137">UINT</span><span class="sxs-lookup"><span data-stu-id="d5d25-137">UINT</span></span><br/> <span data-ttu-id="d5d25-138">1</span><span class="sxs-lookup"><span data-stu-id="d5d25-138">1</span></span><br/>                                               | <span data-ttu-id="d5d25-139">Dimensione del kernel nella direzione Y.</span><span class="sxs-lookup"><span data-stu-id="d5d25-139">Size of the kernel in the Y direction.</span></span> <span data-ttu-id="d5d25-140">Le unità sono in tuffi.</span><span class="sxs-lookup"><span data-stu-id="d5d25-140">The units are in DIPs.</span></span> <span data-ttu-id="d5d25-141">I valori devono essere compresi tra 1 e 100 inclusi.</span><span class="sxs-lookup"><span data-stu-id="d5d25-141">Values must be between 1 and 100 inclusive.</span></span>                                                         |



 

## <a name="morphology-modes"></a><span data-ttu-id="d5d25-142">Modalità morfologia</span><span class="sxs-lookup"><span data-stu-id="d5d25-142">Morphology modes</span></span>



| <span data-ttu-id="d5d25-143">Nome</span><span class="sxs-lookup"><span data-stu-id="d5d25-143">Name</span></span>                           | <span data-ttu-id="d5d25-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5d25-144">Description</span></span>                                                    |
|--------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d5d25-145">\_ \_ Erosione della modalità MORFOLOGIa d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="d5d25-145">D2D1\_MORPHOLOGY\_MODE\_ERODE</span></span>  | <span data-ttu-id="d5d25-146">Viene usato il valore massimo di ogni canale RGB nel kernel.</span><span class="sxs-lookup"><span data-stu-id="d5d25-146">The maximum value from each RGB channel in the kernel is used.</span></span> |
| <span data-ttu-id="d5d25-147">\_Modalità morfologia d2d1 \_ \_ dilate</span><span class="sxs-lookup"><span data-stu-id="d5d25-147">D2D1\_MORPHOLOGY\_MODE\_DILATE</span></span> | <span data-ttu-id="d5d25-148">Viene usato il valore minimo di ogni canale RGB nel kernel.</span><span class="sxs-lookup"><span data-stu-id="d5d25-148">The minimum value from each RGB channel in the kernel is used.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="d5d25-149">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="d5d25-149">Output bitmap</span></span>

<span data-ttu-id="d5d25-150">Per la modalità dilate, le dimensioni della bitmap di output aumentano:</span><span class="sxs-lookup"><span data-stu-id="d5d25-150">For DILATE mode, the Output Bitmap size grows:</span></span> 

| <span data-ttu-id="d5d25-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5d25-151">Requirement</span></span> | <span data-ttu-id="d5d25-152">Valore</span><span class="sxs-lookup"><span data-stu-id="d5d25-152">Value</span></span> |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="d5d25-153">Aumento dimensioni bitmap di output X =</span><span class="sxs-lookup"><span data-stu-id="d5d25-153">Output Bitmap Growth X =</span></span> | <span data-ttu-id="d5d25-154">INT (FLOAT (width) \* ((dpi utente)/96)</span><span class="sxs-lookup"><span data-stu-id="d5d25-154">INT(FLOAT(Width) \* ((User DPI) / 96))</span></span>  |
| <span data-ttu-id="d5d25-155">Crescita bitmap di output Y =</span><span class="sxs-lookup"><span data-stu-id="d5d25-155">Output Bitmap Growth Y =</span></span> | <span data-ttu-id="d5d25-156">INT (FLOAT (Height) \* ((dpi utente)/96)</span><span class="sxs-lookup"><span data-stu-id="d5d25-156">INT(FLOAT(Height) \* ((User DPI) / 96))</span></span> |



 

<span data-ttu-id="d5d25-157">Per la modalità di Erode, le dimensioni della bitmap di output vengono compattate:</span><span class="sxs-lookup"><span data-stu-id="d5d25-157">For ERODE mode, the Output Bitmap size shrinks:</span></span>

| <span data-ttu-id="d5d25-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5d25-158">Requirement</span></span> | <span data-ttu-id="d5d25-159">Valore</span><span class="sxs-lookup"><span data-stu-id="d5d25-159">Value</span></span> |
|--------------------------|------------------------------------------|
| <span data-ttu-id="d5d25-160">Aumento dimensioni bitmap di output X =</span><span class="sxs-lookup"><span data-stu-id="d5d25-160">Output Bitmap Growth X =</span></span> | <span data-ttu-id="d5d25-161">INT (FLOAT (-width) \* ((dpi utente)/96)</span><span class="sxs-lookup"><span data-stu-id="d5d25-161">INT(FLOAT(-Width) \* ((User DPI) / 96))</span></span>  |
| <span data-ttu-id="d5d25-162">Crescita bitmap di output Y =</span><span class="sxs-lookup"><span data-stu-id="d5d25-162">Output Bitmap Growth Y =</span></span> | <span data-ttu-id="d5d25-163">INT (FLOAT (-Height) \* ((dpi utente)/96))</span><span class="sxs-lookup"><span data-stu-id="d5d25-163">INT(FLOAT(-Height) \* ((User DPI) / 96))</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d5d25-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5d25-164">Requirements</span></span>



| <span data-ttu-id="d5d25-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5d25-165">Requirement</span></span> | <span data-ttu-id="d5d25-166">Valore</span><span class="sxs-lookup"><span data-stu-id="d5d25-166">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d25-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5d25-167">Minimum supported client</span></span> | <span data-ttu-id="d5d25-168">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d5d25-168">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d5d25-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5d25-169">Minimum supported server</span></span> | <span data-ttu-id="d5d25-170">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="d5d25-170">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="d5d25-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5d25-171">Header</span></span>                   | <span data-ttu-id="d5d25-172">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="d5d25-172">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="d5d25-173">Libreria</span><span class="sxs-lookup"><span data-stu-id="d5d25-173">Library</span></span>                  | <span data-ttu-id="d5d25-174">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="d5d25-174">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="d5d25-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5d25-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5d25-176">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="d5d25-176">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

