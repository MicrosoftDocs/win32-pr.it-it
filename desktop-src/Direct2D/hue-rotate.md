---
title: Effetto Rotazione tonalità
description: Usare l'effetto di rotazione tonalità per modificare la tonalità di un'immagine applicando una matrice di colori basata sull'angolo di rotazione.
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- effetto Rotazione tonalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525dbe8fc94377080fbae34b80252c84c05073ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104562147"
---
# <a name="hue-rotatation-effect"></a><span data-ttu-id="22e42-104">Effetto Rotazione tonalità</span><span class="sxs-lookup"><span data-stu-id="22e42-104">Hue rotatation effect</span></span>

<span data-ttu-id="22e42-105">Usare l'effetto di rotazione tonalità per modificare la tonalità di un'immagine applicando una matrice di colori basata sull'angolo di rotazione.</span><span class="sxs-lookup"><span data-stu-id="22e42-105">Use the hue rotate effect to alter the hue of an image by applying a color matrix based on the rotation angle.</span></span>

<span data-ttu-id="22e42-106">Il CLSID per questo effetto è CLSID \_ D2D1HueRotation.</span><span class="sxs-lookup"><span data-stu-id="22e42-106">The CLSID for this effect is CLSID\_D2D1HueRotation.</span></span>

-   [<span data-ttu-id="22e42-107">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="22e42-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="22e42-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="22e42-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="22e42-109">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="22e42-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="22e42-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22e42-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="22e42-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22e42-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="22e42-112">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="22e42-112">Example image</span></span>

<span data-ttu-id="22e42-113">Nell'esempio riportato di seguito vengono illustrate le immagini di input e di output dell'effetto Rotazione tonalità con un angolo di rotazione di 270 gradi.</span><span class="sxs-lookup"><span data-stu-id="22e42-113">The example here shows the input and output images of the hue rotate effect with a rotation angle of 270 degrees.</span></span>



| <span data-ttu-id="22e42-114">Prima</span><span class="sxs-lookup"><span data-stu-id="22e42-114">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)   |
| <span data-ttu-id="22e42-116">After</span><span class="sxs-lookup"><span data-stu-id="22e42-116">After</span></span>                                                        |
| ![immagine dopo la trasformazione.](images/17-huerotation.png) |



 


```C++
ComPtr<ID2D1Effect> hueRotationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueRotation, &hueRotationEffect);

hueRotationEffect->SetInput(0, bitmap);
hueRotationEffect->SetValue(D2D1_HUEROTATION_PROP_ANGLE, 270.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueRotationEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="22e42-118">L'effetto calcola una matrice di colori basata sull'angolo di rotazione (*?*) specificato con la proprietà d2d1 \_ HUEROTATION \_ prop \_ Angle.</span><span class="sxs-lookup"><span data-stu-id="22e42-118">The effect calculates a color matrix based on the rotation angle (*?*) you specify with the D2D1\_HUEROTATION\_PROP\_ANGLE property.</span></span> <span data-ttu-id="22e42-119">Ecco le equazioni della matrice.</span><span class="sxs-lookup"><span data-stu-id="22e42-119">Here are the matrix equations.</span></span>

![calcoli di rotazione tonalità](images/hue-formula.png)

<span data-ttu-id="22e42-121">La matrice creata dipende solo dall'angolo di rotazione.</span><span class="sxs-lookup"><span data-stu-id="22e42-121">The matrix created depends only on the rotation angle.</span></span> <span data-ttu-id="22e42-122">Se è necessaria una matrice specifica, è possibile usare l'effetto della [matrice di colori](color-matrix.md) .</span><span class="sxs-lookup"><span data-stu-id="22e42-122">You can use the [color matrix](color-matrix.md) effect if you need a specific matrix.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="22e42-123">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="22e42-123">Effect properties</span></span>



| <span data-ttu-id="22e42-124">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="22e42-124">Display name and index enumeration</span></span>                         | <span data-ttu-id="22e42-125">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="22e42-125">Type and default value</span></span>           | <span data-ttu-id="22e42-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22e42-126">Description</span></span>                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| <span data-ttu-id="22e42-127">Angle</span><span class="sxs-lookup"><span data-stu-id="22e42-127">Angle</span></span><br/> <span data-ttu-id="22e42-128">\_Angolo della \_ prop \_ HUEROTATION d2d1</span><span class="sxs-lookup"><span data-stu-id="22e42-128">D2D1\_HUEROTATION\_PROP\_ANGLE</span></span><br/> | <span data-ttu-id="22e42-129">FLOAT</span><span class="sxs-lookup"><span data-stu-id="22e42-129">FLOAT</span></span><br/> <span data-ttu-id="22e42-130">0,0 f</span><span class="sxs-lookup"><span data-stu-id="22e42-130">0.0f</span></span><br/> | <span data-ttu-id="22e42-131">Angolo per ruotare la tonalità, in gradi.</span><span class="sxs-lookup"><span data-stu-id="22e42-131">The angle to rotate the hue, in degrees.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="22e42-132">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="22e42-132">Output bitmap</span></span>

<span data-ttu-id="22e42-133">La dimensione bitmap di output corrisponde alla dimensione bitmap di input.</span><span class="sxs-lookup"><span data-stu-id="22e42-133">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="22e42-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22e42-134">Requirements</span></span>



| <span data-ttu-id="22e42-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="22e42-135">Requirement</span></span> | <span data-ttu-id="22e42-136">Valore</span><span class="sxs-lookup"><span data-stu-id="22e42-136">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="22e42-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22e42-137">Minimum supported client</span></span> | <span data-ttu-id="22e42-138">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="22e42-138">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="22e42-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="22e42-139">Minimum supported server</span></span> | <span data-ttu-id="22e42-140">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="22e42-140">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="22e42-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22e42-141">Header</span></span>                   | <span data-ttu-id="22e42-142">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="22e42-142">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="22e42-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="22e42-143">Library</span></span>                  | <span data-ttu-id="22e42-144">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="22e42-144">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="22e42-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22e42-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22e42-146">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="22e42-146">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

