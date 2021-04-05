---
title: Effetto saturazione
description: Utilizzare questo effetto per modificare la saturazione di un'immagine.
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- effetto saturazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6912e64c9297a3554b4785128e1282a3974d36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048238"
---
# <a name="saturation-effect"></a><span data-ttu-id="bda59-104">Effetto saturazione</span><span class="sxs-lookup"><span data-stu-id="bda59-104">Saturation effect</span></span>

<span data-ttu-id="bda59-105">Utilizzare questo effetto per modificare la saturazione di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="bda59-105">Use this effect to alter the saturation of an image.</span></span> <span data-ttu-id="bda59-106">L'effetto di saturazione è una specializzazione dell'effetto della [matrice di colori](color-matrix.md) .</span><span class="sxs-lookup"><span data-stu-id="bda59-106">The saturation effect is a specialization of the [color matrix](color-matrix.md) effect.</span></span>

<span data-ttu-id="bda59-107">Il CLSID per questo effetto è CLSID \_ D2D1Saturation.</span><span class="sxs-lookup"><span data-stu-id="bda59-107">The CLSID for this effect is CLSID\_D2D1Saturation.</span></span>

-   [<span data-ttu-id="bda59-108">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="bda59-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="bda59-109">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="bda59-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="bda59-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bda59-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="bda59-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bda59-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="bda59-112">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="bda59-112">Example image</span></span>

<span data-ttu-id="bda59-113">Nell'esempio riportato di seguito vengono illustrate le immagini di input e di output dell'effetto di saturazione con una saturazione pari allo 0%.</span><span class="sxs-lookup"><span data-stu-id="bda59-113">The example here shows the input and output images of the saturation effect with a saturation of 0%.</span></span>



| <span data-ttu-id="bda59-114">Prima</span><span class="sxs-lookup"><span data-stu-id="bda59-114">Before</span></span>                                                      |
|-------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)  |
| <span data-ttu-id="bda59-116">After</span><span class="sxs-lookup"><span data-stu-id="bda59-116">After</span></span>                                                       |
| ![immagine dopo la trasformazione.](images/16-saturation.png) |



 


```C++
ComPtr<ID2D1Effect> saturationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Saturation, &saturationEffect);

saturationEffect->SetInput(0, bitmap);

saturationEffect->SetValue(D2D1_SATURATION_PROP_SATURATION, 0.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(saturationEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="bda59-118">L'effetto calcola una matrice di colori in base al valore di saturazione (*s* nell'equazione qui) specificata con la \_ \_ \_ Proprietà saturazione d2d1 saturazione.</span><span class="sxs-lookup"><span data-stu-id="bda59-118">The effect calculates a color matrix based on the saturation value (*s* in the equation here) you specify with the D2D1\_SATURATION\_PROP\_SATURATION property.</span></span> <span data-ttu-id="bda59-119">L'equazione della matrice è illustrata di seguito.</span><span class="sxs-lookup"><span data-stu-id="bda59-119">The matrix equation is shown here.</span></span>

![formula per il calcolo di una matrice di saturazione.](images/saturation-formula.png)

<span data-ttu-id="bda59-121">La matrice creata dipende solo dal valore di saturazione.</span><span class="sxs-lookup"><span data-stu-id="bda59-121">The matrix created depends only on the saturation value.</span></span> <span data-ttu-id="bda59-122">Se è necessaria una matrice specifica, è possibile usare l'effetto della [matrice di colori](color-matrix.md) .</span><span class="sxs-lookup"><span data-stu-id="bda59-122">You can use the [color matrix](color-matrix.md) effect if you need a specific matrix.</span></span>

<span data-ttu-id="bda59-123">Questo effetto utilizza e restituisce immagini alfa premoltiplicate.</span><span class="sxs-lookup"><span data-stu-id="bda59-123">This effect consumes and outputs premultiplied alpha images.</span></span> <span data-ttu-id="bda59-124">L'effetto non funzionerà su immagini Alpha dritte a meno che non siano completamente opache.</span><span class="sxs-lookup"><span data-stu-id="bda59-124">The effect won't work on straight alpha images unless they are fully opaque.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="bda59-125">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="bda59-125">Effect properties</span></span>



| <span data-ttu-id="bda59-126">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="bda59-126">Display name and index enumeration</span></span>                                  | <span data-ttu-id="bda59-127">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="bda59-127">Type and default value</span></span>           | <span data-ttu-id="bda59-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bda59-128">Description</span></span>                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bda59-129">Saturazione</span><span class="sxs-lookup"><span data-stu-id="bda59-129">Saturation</span></span><br/> <span data-ttu-id="bda59-130">\_Saturazione d2d1 saturazione \_ \_</span><span class="sxs-lookup"><span data-stu-id="bda59-130">D2D1\_SATURATION\_PROP\_SATURATION</span></span><br/> | <span data-ttu-id="bda59-131">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bda59-131">FLOAT</span></span><br/> <span data-ttu-id="bda59-132">0,5 f</span><span class="sxs-lookup"><span data-stu-id="bda59-132">0.5f</span></span><br/> | <span data-ttu-id="bda59-133">Saturazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="bda59-133">The saturation of the image.</span></span> <span data-ttu-id="bda59-134">È possibile impostare la saturazione su un valore compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="bda59-134">You can set the saturation to a value between 0 and 1.</span></span> <span data-ttu-id="bda59-135">Se lo si imposta su 1, l'immagine di output è completamente satura.</span><span class="sxs-lookup"><span data-stu-id="bda59-135">If you set it to 1 the output image is fully saturated.</span></span> <span data-ttu-id="bda59-136">Se lo si imposta su 0, l'immagine di output è monocromatica.</span><span class="sxs-lookup"><span data-stu-id="bda59-136">If you set it to 0 the output image is monochrome.</span></span> <span data-ttu-id="bda59-137">Il valore di saturazione è di unità.</span><span class="sxs-lookup"><span data-stu-id="bda59-137">The saturation value is unitless.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="bda59-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bda59-138">Requirements</span></span>



| <span data-ttu-id="bda59-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="bda59-139">Requirement</span></span> | <span data-ttu-id="bda59-140">Valore</span><span class="sxs-lookup"><span data-stu-id="bda59-140">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bda59-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bda59-141">Minimum supported client</span></span> | <span data-ttu-id="bda59-142">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="bda59-142">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="bda59-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bda59-143">Minimum supported server</span></span> | <span data-ttu-id="bda59-144">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="bda59-144">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="bda59-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bda59-145">Header</span></span>                   | <span data-ttu-id="bda59-146">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="bda59-146">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="bda59-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="bda59-147">Library</span></span>                  | <span data-ttu-id="bda59-148">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="bda59-148">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="bda59-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bda59-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bda59-150">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="bda59-150">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

