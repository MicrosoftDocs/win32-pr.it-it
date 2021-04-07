---
title: Effetto tessera
description: Usare l'effetto icona per ripetere l'area specificata dell'immagine.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- effetto tessera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5def48ab30cadb28673179f6eec5d7ffa7e19e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048444"
---
# <a name="tile-effect"></a><span data-ttu-id="b089d-104">Effetto tessera</span><span class="sxs-lookup"><span data-stu-id="b089d-104">Tile effect</span></span>

<span data-ttu-id="b089d-105">Usare l'effetto icona per ripetere l'area specificata dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b089d-105">Use the tile effect to repeat the specified region of the image.</span></span>

<span data-ttu-id="b089d-106">Il CLSID per questo effetto è CLSID \_ D2D1Tile.</span><span class="sxs-lookup"><span data-stu-id="b089d-106">The CLSID for this effect is CLSID\_D2D1Tile.</span></span>

## <a name="example-image"></a><span data-ttu-id="b089d-107">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="b089d-107">Example image</span></span>



| <span data-ttu-id="b089d-108">Prima</span><span class="sxs-lookup"><span data-stu-id="b089d-108">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg) |
| <span data-ttu-id="b089d-110">After</span><span class="sxs-lookup"><span data-stu-id="b089d-110">After</span></span>                                                      |
| ![immagine dopo la trasformazione.](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="b089d-112">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="b089d-112">Effect properties</span></span>



| <span data-ttu-id="b089d-113">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="b089d-113">Display name and index enumeration</span></span>                | <span data-ttu-id="b089d-114">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="b089d-114">Type and default value</span></span>                                              | <span data-ttu-id="b089d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b089d-115">Description</span></span>                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b089d-116">Rect</span><span class="sxs-lookup"><span data-stu-id="b089d-116">Rect</span></span><br/> <span data-ttu-id="b089d-117">D2D1 \_ riquadro \_ prop \_ Rect</span><span class="sxs-lookup"><span data-stu-id="b089d-117">D2D1\_TILE\_PROP\_RECT</span></span><br/> | <span data-ttu-id="b089d-118">D2D1 \_ vector \_ 4F</span><span class="sxs-lookup"><span data-stu-id="b089d-118">D2D1\_VECTOR\_4F</span></span><br/> <span data-ttu-id="b089d-119">{0,0 f, 0,0 f, 100.0 f, 100.0 f}</span><span class="sxs-lookup"><span data-stu-id="b089d-119">{0.0f, 0.0f, 100.0f, 100.0f}</span></span><br/> | <span data-ttu-id="b089d-120">Area dell'immagine da affiancare.</span><span class="sxs-lookup"><span data-stu-id="b089d-120">The region of the image to be tiled.</span></span> <span data-ttu-id="b089d-121">Questa proprietà è un \_ vettore d2d1 \_ 4F definito come: (Left, top, right, Bottom).</span><span class="sxs-lookup"><span data-stu-id="b089d-121">This property is a D2D1\_VECTOR\_4F defined as: (left, top, right, bottom).</span></span> <span data-ttu-id="b089d-122">Le unità sono in tuffi.</span><span class="sxs-lookup"><span data-stu-id="b089d-122">The units are in DIPs.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="b089d-123">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="b089d-123">Output bitmap</span></span>

<span data-ttu-id="b089d-124">Questo effetto genera una bitmap di dimensioni infinite logicamente.</span><span class="sxs-lookup"><span data-stu-id="b089d-124">This effect generates a logically infinite sized bitmap.</span></span>

<span data-ttu-id="b089d-125">È possibile affiancare un'immagine e restituire una certa dimensione senza effetti aggiuntivi impostando le dimensioni quando si chiama [**ID2D1DeviceContext::D rawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).</span><span class="sxs-lookup"><span data-stu-id="b089d-125">You can tile an image and output a certain size without any additional effects by setting the size when you call [**ID2D1DeviceContext::DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b089d-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b089d-126">Requirements</span></span>



| <span data-ttu-id="b089d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b089d-127">Requirement</span></span> | <span data-ttu-id="b089d-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b089d-128">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b089d-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b089d-129">Minimum supported client</span></span> | <span data-ttu-id="b089d-130">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b089d-130">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b089d-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b089d-131">Minimum supported server</span></span> | <span data-ttu-id="b089d-132">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b089d-132">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b089d-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b089d-133">Header</span></span>                   | <span data-ttu-id="b089d-134">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="b089d-134">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="b089d-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="b089d-135">Library</span></span>                  | <span data-ttu-id="b089d-136">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="b089d-136">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="b089d-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b089d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b089d-138">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="b089d-138">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

