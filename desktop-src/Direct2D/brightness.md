---
title: Effetto luminosità
description: Usare l'effetto di luminosità per controllare la luminosità dell'immagine.
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- effetto luminosità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dd9797aa125e7099ba4a706bac730a30715f6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104552095"
---
# <a name="brightness-effect"></a><span data-ttu-id="0454a-104">Effetto luminosità</span><span class="sxs-lookup"><span data-stu-id="0454a-104">Brightness effect</span></span>

<span data-ttu-id="0454a-105">Usare l'effetto di luminosità per controllare la luminosità dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0454a-105">Use the brightness effect to control the brightness of the image.</span></span>

<span data-ttu-id="0454a-106">Il CLSID per questo effetto è CLSID \_ D2D1Brightness.</span><span class="sxs-lookup"><span data-stu-id="0454a-106">The CLSID for this effect is CLSID\_D2D1Brightness.</span></span>

-   [<span data-ttu-id="0454a-107">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="0454a-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="0454a-108">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="0454a-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="0454a-109">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="0454a-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="0454a-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0454a-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="0454a-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0454a-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="0454a-112">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="0454a-112">Example image</span></span>



| <span data-ttu-id="0454a-113">Prima</span><span class="sxs-lookup"><span data-stu-id="0454a-113">Before</span></span>                                                      |
|-------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)  |
| <span data-ttu-id="0454a-115">After</span><span class="sxs-lookup"><span data-stu-id="0454a-115">After</span></span>                                                       |
| ![immagine dopo la trasformazione.](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="0454a-117">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="0454a-117">Effect properties</span></span>



| <span data-ttu-id="0454a-118">Nome visualizzato proprietà</span><span class="sxs-lookup"><span data-stu-id="0454a-118">Property Display Name</span></span>                                                 | <span data-ttu-id="0454a-119">Tipo e valore predefinito</span><span class="sxs-lookup"><span data-stu-id="0454a-119">Type and default value</span></span>                              | <span data-ttu-id="0454a-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0454a-120">Description</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0454a-121">WhitePoint</span><span class="sxs-lookup"><span data-stu-id="0454a-121">WhitePoint</span></span><br/> <span data-ttu-id="0454a-122">\_ \_ \_ Punto bianco prop luminosità \_ d2d1</span><span class="sxs-lookup"><span data-stu-id="0454a-122">D2D1\_BRIGHTNESS\_PROP\_WHITE\_POINT</span></span><br/> | <span data-ttu-id="0454a-123">D2D1 \_ vector \_ 2F</span><span class="sxs-lookup"><span data-stu-id="0454a-123">D2D1\_VECTOR\_2F</span></span><br/> <span data-ttu-id="0454a-124">{1.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="0454a-124">{1.0f, 1.0f}</span></span><br/> | <span data-ttu-id="0454a-125">Parte superiore della curva di trasferimento della luminosità.</span><span class="sxs-lookup"><span data-stu-id="0454a-125">The upper portion of the brightness transfer curve.</span></span> <span data-ttu-id="0454a-126">Il punto bianco regola l'aspetto delle parti più luminose dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0454a-126">The white point adjusts the appearance of the brighter portions of the image.</span></span> <span data-ttu-id="0454a-127">Questa proprietà è per il valore x e il valore y, in questo ordine.</span><span class="sxs-lookup"><span data-stu-id="0454a-127">This property is for both the x value and the y value, in that order.</span></span> <span data-ttu-id="0454a-128">Ognuno dei valori di questa proprietà è compreso tra 0 e 1 inclusi.</span><span class="sxs-lookup"><span data-stu-id="0454a-128">Each of the values of this property are between 0 and 1, inclusive.</span></span> |
| <span data-ttu-id="0454a-129">BlackPoint</span><span class="sxs-lookup"><span data-stu-id="0454a-129">BlackPoint</span></span><br/> <span data-ttu-id="0454a-130">\_ \_ Punto nero della prop d2d1 brightness \_ \_</span><span class="sxs-lookup"><span data-stu-id="0454a-130">D2D1\_BRIGHTNESS\_PROP\_BLACK\_POINT</span></span><br/> | <span data-ttu-id="0454a-131">D2D1 \_ vector \_ 2F</span><span class="sxs-lookup"><span data-stu-id="0454a-131">D2D1\_VECTOR\_2F</span></span><br/> <span data-ttu-id="0454a-132">{0,0 f, 0,0 f}</span><span class="sxs-lookup"><span data-stu-id="0454a-132">{0.0f, 0.0f}</span></span><br/> | <span data-ttu-id="0454a-133">Parte inferiore della curva di trasferimento della luminosità.</span><span class="sxs-lookup"><span data-stu-id="0454a-133">The lower portion of the brightness transfer curve.</span></span> <span data-ttu-id="0454a-134">Il punto nero regola l'aspetto delle parti più scure dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0454a-134">The black point adjusts the appearance of the darker portions of the image.</span></span> <span data-ttu-id="0454a-135">Questa proprietà è per il valore x e il valore y, in questo ordine.</span><span class="sxs-lookup"><span data-stu-id="0454a-135">This property is for both the x value and the y value, in that order.</span></span> <span data-ttu-id="0454a-136">Ognuno dei valori di questa proprietà è compreso tra 0 e 1 inclusi.</span><span class="sxs-lookup"><span data-stu-id="0454a-136">Each of the values of this property are between 0 and 1, inclusive.</span></span>   |



 

<span data-ttu-id="0454a-137">Questo effetto utilizza i punti bianco e nero specificati per generare una funzione di trasferimento utilizzata per modificare la bitmap.</span><span class="sxs-lookup"><span data-stu-id="0454a-137">This effect uses the specified white and black points to generate a transfer function used to adjust the bitmap.</span></span> <span data-ttu-id="0454a-138">L'equazione successiva descrive la funzione di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="0454a-138">The next equation describes the transfer function.</span></span> <span data-ttu-id="0454a-139">Le intensità di input sono definite tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="0454a-139">The input intensities are defined between 0 and 1.</span></span>

![algoritmo di luminosità](images/brightness-formula1.png)

<span data-ttu-id="0454a-141">L'algoritmo Effect implementa un'equazione che crea la funzione di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="0454a-141">The effect algorithm implements an equation that creates the transfer function.</span></span> <span data-ttu-id="0454a-142">Questa funzione viene usata per modificare i pixel dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0454a-142">We use this function to adjust the image pixels.</span></span> <span data-ttu-id="0454a-143">I valori x e y del punto nero e del punto bianco sono le coordinate in due dimensioni connesse alla trasformazione.</span><span class="sxs-lookup"><span data-stu-id="0454a-143">The x and y values of the black point and the white point are the coordinates in two dimensions that are connected to form the transform.</span></span> <span data-ttu-id="0454a-144">Ogni parte dell'equazione di output finale:</span><span class="sxs-lookup"><span data-stu-id="0454a-144">Each part of the final output equation:</span></span>

1.  <span data-ttu-id="0454a-145">Converte i dati dell'immagine dallo spazio lineare allo spazio non lineare utilizzando questa equazione:</span><span class="sxs-lookup"><span data-stu-id="0454a-145">Converts the image data from linear space to non-linear space using this equation:</span></span>![funzione helper 1](images/brightness-formula2.png)

2.  <span data-ttu-id="0454a-147">Regola l'immagine in base a questi valori:</span><span class="sxs-lookup"><span data-stu-id="0454a-147">Adjusts the image according to these values:</span></span>
    -   <span data-ttu-id="0454a-148">*input* è il valore di intensità pixel dell'immagine di input compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="0454a-148">*input* is the input image pixel intensity values from 0 to 1.</span></span>

    -   <span data-ttu-id="0454a-149">*PT bianco. (x, y)* posizione della curva di trasformazione per le intensità dei pixel più brillanti.</span><span class="sxs-lookup"><span data-stu-id="0454a-149">*White Pt. (x, y)* the location of the transform curve for brighter pixel intensities.</span></span>

    -   <span data-ttu-id="0454a-150">*Black pt. (x, y)* è la posizione della curva di trasformazione per le intensità dei pixel dimmer.</span><span class="sxs-lookup"><span data-stu-id="0454a-150">*Black Pt. (x, y)* is the location of the transform curve for dimmer pixel intensities.</span></span>

3.  <span data-ttu-id="0454a-151">Converte nuovamente i dati dell'immagine nello spazio lineare usando questa equazione:</span><span class="sxs-lookup"><span data-stu-id="0454a-151">Converts the image data back to linear space using this equation:</span></span> ![funzione helper 2](images/brightness-formula3.png)

<span data-ttu-id="0454a-153">L'equazione di output finale e le parti del componente sono illustrate di seguito.</span><span class="sxs-lookup"><span data-stu-id="0454a-153">The final output equation and the component parts are shown here.</span></span>

![calcoli completi per la regolazione della luminosità](images/brightness-formula4.png)

## <a name="output-bitmap"></a><span data-ttu-id="0454a-155">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="0454a-155">Output bitmap</span></span>

<span data-ttu-id="0454a-156">La dimensione bitmap di output corrisponde alla dimensione bitmap di input.</span><span class="sxs-lookup"><span data-stu-id="0454a-156">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="0454a-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0454a-157">Requirements</span></span>



| <span data-ttu-id="0454a-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="0454a-158">Requirement</span></span> | <span data-ttu-id="0454a-159">Valore</span><span class="sxs-lookup"><span data-stu-id="0454a-159">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0454a-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0454a-160">Minimum supported client</span></span> | <span data-ttu-id="0454a-161">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="0454a-161">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0454a-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0454a-162">Minimum supported server</span></span> | <span data-ttu-id="0454a-163">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="0454a-163">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="0454a-164">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0454a-164">Header</span></span>                   | <span data-ttu-id="0454a-165">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="0454a-165">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="0454a-166">Libreria</span><span class="sxs-lookup"><span data-stu-id="0454a-166">Library</span></span>                  | <span data-ttu-id="0454a-167">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="0454a-167">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="0454a-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0454a-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0454a-169">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="0454a-169">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

