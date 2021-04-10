---
title: Effetto Flood
description: Usare l'effetto Flood per generare una bitmap in base al colore e al valore alfa specificati. È possibile utilizzare questo effetto quando si desidera un colore specifico come input per un effetto, ad esempio un colore di sfondo.
ms.assetid: F80A6DC0-E18C-4324-BE4A-FE40C5722988
keywords:
- effetto Flood
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92d34a41c0913a0d250fc24467b37b0d347b4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964603"
---
# <a name="flood-effect"></a><span data-ttu-id="3fb78-105">Effetto Flood</span><span class="sxs-lookup"><span data-stu-id="3fb78-105">Flood effect</span></span>

<span data-ttu-id="3fb78-106">Usare l'effetto Flood per generare una bitmap in base al colore e al valore alfa specificati.</span><span class="sxs-lookup"><span data-stu-id="3fb78-106">Use the flood effect to generate a bitmap based on the specified color and alpha value.</span></span> <span data-ttu-id="3fb78-107">È possibile utilizzare questo effetto quando si desidera un colore specifico come input per un effetto, ad esempio un colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="3fb78-107">You can use this effect when you want a specific color as an input for an effect, like a background color.</span></span>

> [!Note]  
> <span data-ttu-id="3fb78-108">L'effetto passa lungo il valore del colore specificato, come specificato.</span><span class="sxs-lookup"><span data-stu-id="3fb78-108">The effect passes along the specified color value as specified.</span></span> <span data-ttu-id="3fb78-109">È necessario pre-moltiplicare manualmente i valori se si prevede di passare l'output agli effetti che prevedono un input pre-moltiplicato.</span><span class="sxs-lookup"><span data-stu-id="3fb78-109">You must manually pre-multiply the values if you plan to pass the output to effects that expect a pre-multiplied input.</span></span>

 

<span data-ttu-id="3fb78-110">Il CLSID per questo effetto è CLSID \_ D2D1Flood.</span><span class="sxs-lookup"><span data-stu-id="3fb78-110">The CLSID for this effect is CLSID\_D2D1Flood.</span></span>

<span data-ttu-id="3fb78-111">L'effetto Flood non ha un'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="3fb78-111">The flood effect has no input image.</span></span>

-   [<span data-ttu-id="3fb78-112">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="3fb78-112">Example image</span></span>](#example-image)
-   [<span data-ttu-id="3fb78-113">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="3fb78-113">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="3fb78-114">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="3fb78-114">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="3fb78-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fb78-115">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="3fb78-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3fb78-116">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="3fb78-117">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="3fb78-117">Example image</span></span>

![immagine di esempio dell'effetto Flood che produce l'effetto verde.](images/20-flood.png)


```C++
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(0.0f, 1.0f, 0.0f, 1.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(floodEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="3fb78-119">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="3fb78-119">Effect properties</span></span>



| <span data-ttu-id="3fb78-120">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="3fb78-120">Display name and index enumeration</span></span>                   | <span data-ttu-id="3fb78-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fb78-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb78-122">Colore</span><span class="sxs-lookup"><span data-stu-id="3fb78-122">Color</span></span><br/> <span data-ttu-id="3fb78-123">\_Colore della \_ prop d2d1 Flood \_</span><span class="sxs-lookup"><span data-stu-id="3fb78-123">D2D1\_FLOOD\_PROP\_COLOR</span></span><br/> | <span data-ttu-id="3fb78-124">Il colore e l'opacità della bitmap.</span><span class="sxs-lookup"><span data-stu-id="3fb78-124">The color and opacity of the bitmap.</span></span> <span data-ttu-id="3fb78-125">Questa proprietà è un \_ vettore d2d1 \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="3fb78-125">This property is a D2D1\_VECTOR\_4F.</span></span> <span data-ttu-id="3fb78-126">I singoli valori per ogni canale sono di tipo FLOAT, unbounded e senza unità.</span><span class="sxs-lookup"><span data-stu-id="3fb78-126">The individual values for each channel are of type FLOAT, unbounded and unitless.</span></span> <span data-ttu-id="3fb78-127">L'effetto non modifica i valori per i canali.</span><span class="sxs-lookup"><span data-stu-id="3fb78-127">The effect doesn't modify the values for the channels.</span></span><br/> <span data-ttu-id="3fb78-128">I valori di RGBA per ogni canale variano da 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="3fb78-128">The RGBA values for each channel range from 0 to 1.</span></span><br/> <span data-ttu-id="3fb78-129">Il tipo è D2D1 \_ vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="3fb78-129">The type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="3fb78-130">Il valore predefinito è {0,0 f, 0,0 f, 0,0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="3fb78-130">The default value is {0.0f, 0.0f, 0.0f, 1.0f}.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="3fb78-131">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="3fb78-131">Output bitmap</span></span>

<span data-ttu-id="3fb78-132">Questo effetto genera una bitmap di dimensioni infinite logicamente.</span><span class="sxs-lookup"><span data-stu-id="3fb78-132">This effect generates a logically infinite sized bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb78-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fb78-133">Requirements</span></span>



| <span data-ttu-id="3fb78-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fb78-134">Requirement</span></span> | <span data-ttu-id="3fb78-135">Valore</span><span class="sxs-lookup"><span data-stu-id="3fb78-135">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb78-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fb78-136">Minimum supported client</span></span> | <span data-ttu-id="3fb78-137">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="3fb78-137">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="3fb78-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fb78-138">Minimum supported server</span></span> | <span data-ttu-id="3fb78-139">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="3fb78-139">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="3fb78-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fb78-140">Header</span></span>                   | <span data-ttu-id="3fb78-141">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="3fb78-141">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="3fb78-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="3fb78-142">Library</span></span>                  | <span data-ttu-id="3fb78-143">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="3fb78-143">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="3fb78-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3fb78-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fb78-145">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="3fb78-145">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

