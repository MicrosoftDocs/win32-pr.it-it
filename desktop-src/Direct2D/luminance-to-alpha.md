---
title: Luminanza all'effetto Alfa
description: Utilizzare la luminanza per l'effetto Alfa per impostare il canale alfa sulla luminanza dell'immagine e impostare i canali dei colori su 0.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- luminanza all'effetto Alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb4c6fb78a1d49498b2adab6716d41e93d30deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104561026"
---
# <a name="luminance-to-alpha-effect"></a><span data-ttu-id="8140b-104">Luminanza all'effetto Alfa</span><span class="sxs-lookup"><span data-stu-id="8140b-104">Luminance to alpha effect</span></span>

<span data-ttu-id="8140b-105">Utilizzare la luminanza per l'effetto Alfa per impostare il canale alfa sulla luminanza dell'immagine e impostare i canali dei colori su 0.</span><span class="sxs-lookup"><span data-stu-id="8140b-105">Use the luminance to alpha effect to set the alpha channel to the luminance of the image and sets the color channels to 0.</span></span> <span data-ttu-id="8140b-106">È possibile usare l'output di questo effetto per creare una sovrapposizione semitrasparente basata sulla luminosità dell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="8140b-106">You can use the output of this effect to make a semitransparent overlay based on the brightness of the input image.</span></span> <span data-ttu-id="8140b-107">In alternativa, è possibile usarlo per creare una maschera immagine.</span><span class="sxs-lookup"><span data-stu-id="8140b-107">Or you can use it to make an image mask.</span></span>

> [!Note]  
> <span data-ttu-id="8140b-108">Questo effetto non ha proprietà.</span><span class="sxs-lookup"><span data-stu-id="8140b-108">This effect has no properties.</span></span>

 

<span data-ttu-id="8140b-109">Il CLSID per questo effetto è CLSID \_ D2D1LuminanceToAlpha.</span><span class="sxs-lookup"><span data-stu-id="8140b-109">The CLSID for this effect is CLSID\_D2D1LuminanceToAlpha.</span></span>

## <a name="example-image"></a><span data-ttu-id="8140b-110">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="8140b-110">Example image</span></span>

<span data-ttu-id="8140b-111">Questo esempio mostra l'output della luminanza all'effetto Alfa composito su una superficie bianca per visualizzare l'opacità.</span><span class="sxs-lookup"><span data-stu-id="8140b-111">This example shows the output of the luminance to alpha effect composited over a white surface to show opacity.</span></span>



| <span data-ttu-id="8140b-112">Prima</span><span class="sxs-lookup"><span data-stu-id="8140b-112">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)        |
| <span data-ttu-id="8140b-114">After</span><span class="sxs-lookup"><span data-stu-id="8140b-114">After</span></span>                                                             |
| ![immagine dopo la trasformazione.](images/18-luminancetoalpha.png) |



 


```C++
ComPtr<ID2D1Effect> luminanceToAlphaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LuminanceToAlpha, &luminanceToAlphaEffect);

luminanceToAlphaEffect->SetInput(0, bitmap);

// LuminanceToAlpha result is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);
floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, luminanceToAlphaEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="8140b-116">Questo effetto imposta il canale alfa dell'output sulla luminanza dell'immagine di input usando questa matrice di colori.</span><span class="sxs-lookup"><span data-stu-id="8140b-116">This effect sets the alpha channel of the output to the luminance of the input image using this color matrix.</span></span>

![matrice di colori utilizzata dall'effetto per impostare il canale alfa.](images/luminance-to-alpha-math1.png)

<span data-ttu-id="8140b-118">Questo effetto utilizza e restituisce immagini alfa premoltiplicate.</span><span class="sxs-lookup"><span data-stu-id="8140b-118">This effect consumes and outputs premultiplied alpha images.</span></span> <span data-ttu-id="8140b-119">L'effetto non funzionerà su immagini Alpha dritte a meno che non siano completamente opache.</span><span class="sxs-lookup"><span data-stu-id="8140b-119">The effect won't work on straight alpha images unless they are fully opaque.</span></span>

> [!Note]
>
> <span data-ttu-id="8140b-120">Poiché le immagini vengono archiviate in un formato con compensazione gamma, prima di calcolare la luminanza per un'immagine, è necessario prima eseguire la correzione gamma inversa per ottenere i valori di colore true per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="8140b-120">Because images are stored in a gamma-compensated format, before you calculate the luminance for an image you should first perform inverse gamma correction to get the true color values for the image.</span></span> <span data-ttu-id="8140b-121">Poiché le immagini vengono in genere archiviate in 2,2 gamma, è possibile usare l'effetto di trasferimento gamma con un esponente di (1/2.2) e quindi usare l'output di tale effetto.</span><span class="sxs-lookup"><span data-stu-id="8140b-121">Since images are normally stored at 2.2 gamma, you can use the Gamma transfer effect with an exponent of (1/2.2) and then use the output of that effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8140b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8140b-122">Requirements</span></span>



| <span data-ttu-id="8140b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8140b-123">Requirement</span></span> | <span data-ttu-id="8140b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8140b-124">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8140b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8140b-125">Minimum supported client</span></span> | <span data-ttu-id="8140b-126">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="8140b-126">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8140b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8140b-127">Minimum supported server</span></span> | <span data-ttu-id="8140b-128">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="8140b-128">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8140b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8140b-129">Header</span></span>                   | <span data-ttu-id="8140b-130">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="8140b-130">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="8140b-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="8140b-131">Library</span></span>                  | <span data-ttu-id="8140b-132">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="8140b-132">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="output-bitmap"></a><span data-ttu-id="8140b-133">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="8140b-133">Output bitmap</span></span>

<span data-ttu-id="8140b-134">L'output ha le stesse dimensioni dell'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="8140b-134">The output is the same size as the input image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8140b-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8140b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8140b-136">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="8140b-136">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
