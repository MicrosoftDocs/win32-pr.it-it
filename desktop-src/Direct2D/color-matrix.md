---
title: Effetto matrice colori
description: Utilizzare l'effetto matrice colori per modificare i valori RGBA di una bitmap.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- effetto matrice colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1078b1858bc68396546e1036c717e01acb1069c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048240"
---
# <a name="color-matrix-effect"></a><span data-ttu-id="9ea03-104">Effetto matrice colori</span><span class="sxs-lookup"><span data-stu-id="9ea03-104">Color matrix effect</span></span>

<span data-ttu-id="9ea03-105">Utilizzare l'effetto matrice colori per modificare i valori RGBA di una bitmap.</span><span class="sxs-lookup"><span data-stu-id="9ea03-105">Use the color matrix effect to alter the RGBA values of a bitmap.</span></span>

<span data-ttu-id="9ea03-106">È possibile utilizzare questo effetto per:</span><span class="sxs-lookup"><span data-stu-id="9ea03-106">You can use this effect to:</span></span>

-   <span data-ttu-id="9ea03-107">Rimuovere un canale di colore da un'immagine.</span><span class="sxs-lookup"><span data-stu-id="9ea03-107">Remove a color channel from an image.</span></span>
-   <span data-ttu-id="9ea03-108">Ridurre il colore in un'immagine.</span><span class="sxs-lookup"><span data-stu-id="9ea03-108">Reduce the color in an image.</span></span>
-   <span data-ttu-id="9ea03-109">Scambia canali colori.</span><span class="sxs-lookup"><span data-stu-id="9ea03-109">Swap color channels.</span></span>
-   <span data-ttu-id="9ea03-110">Combinare i canali colori.</span><span class="sxs-lookup"><span data-stu-id="9ea03-110">Combine color channels.</span></span>

<span data-ttu-id="9ea03-111">Molti effetti predefiniti sono specializzazioni della matrice di colori ottimizzate per l'uso previsto degli effetti.</span><span class="sxs-lookup"><span data-stu-id="9ea03-111">Many built-in effects are specializations of color matrix that are optimized for the intended use of the effects.</span></span> <span data-ttu-id="9ea03-112">Gli esempi includono [saturazione](saturation.md), [Rotazione tonalità](hue-rotate.md), [seppia](sepia-effect.md), [temperatura e tonalità](temperature-and-tint-effect.md).</span><span class="sxs-lookup"><span data-stu-id="9ea03-112">Examples include [saturation](saturation.md), [hue rotate](hue-rotate.md), [sepia](sepia-effect.md), and [temperature and tint](temperature-and-tint-effect.md).</span></span>

<span data-ttu-id="9ea03-113">Il CLSID per questo effetto è CLSID \_ D2D1ColorMatrix.</span><span class="sxs-lookup"><span data-stu-id="9ea03-113">The CLSID for this effect is CLSID\_D2D1ColorMatrix.</span></span>

-   [<span data-ttu-id="9ea03-114">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="9ea03-114">Example image</span></span>](#example-image)
-   [<span data-ttu-id="9ea03-115">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="9ea03-115">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="9ea03-116">Modalità Alpha</span><span class="sxs-lookup"><span data-stu-id="9ea03-116">Alpha modes</span></span>](#alpha-modes)
-   [<span data-ttu-id="9ea03-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ea03-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="9ea03-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9ea03-118">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="9ea03-119">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="9ea03-119">Example image</span></span>

<span data-ttu-id="9ea03-120">Nell'esempio riportato di seguito vengono illustrate le immagini di input e di output dell'effetto della matrice di colori che scambia i canali rosso e blu.</span><span class="sxs-lookup"><span data-stu-id="9ea03-120">The example here shows the input and output images of the color matrix effect that swaps the red and blue channels.</span></span>



| <span data-ttu-id="9ea03-121">Prima</span><span class="sxs-lookup"><span data-stu-id="9ea03-121">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)   |
| <span data-ttu-id="9ea03-123">After</span><span class="sxs-lookup"><span data-stu-id="9ea03-123">After</span></span>                                                        |
| ![immagine dopo la trasformazione.](images/15-colormatrix.png) |



 


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect);

colorMatrixEffect->SetInput(0, bitmap);
D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="9ea03-125">Questo effetto moltiplica i valori RGBA dell'immagine in base a un 5x4, la matrice principale della colonna, come illustrato in questa equazione.</span><span class="sxs-lookup"><span data-stu-id="9ea03-125">This effect multiplies the RGBA values of the image by a 5x4, column major matrix as shown in this equation.</span></span>

![definizione di matrice di esempio.](images/color-matrix-formula.png)

<span data-ttu-id="9ea03-127">Questo effetto funziona su immagini alfa diritte e premoltiplicate.</span><span class="sxs-lookup"><span data-stu-id="9ea03-127">This effect works on straight and premultiplied alpha images.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="9ea03-128">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="9ea03-128">Effect properties</span></span>



| <span data-ttu-id="9ea03-129">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="9ea03-129">Display name and index enumeration</span></span>                                       | <span data-ttu-id="9ea03-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ea03-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ea03-131">ColorMatrix</span><span class="sxs-lookup"><span data-stu-id="9ea03-131">ColorMatrix</span></span><br/> <span data-ttu-id="9ea03-132">\_Matrice di \_ colori della prop d2d1 COLORMATRIX \_ \_</span><span class="sxs-lookup"><span data-stu-id="9ea03-132">D2D1\_COLORMATRIX\_PROP\_COLOR\_MATRIX</span></span><br/> | <span data-ttu-id="9ea03-133">Matrice 5x4 di valori float.</span><span class="sxs-lookup"><span data-stu-id="9ea03-133">A 5x4 matrix of float values.</span></span> <span data-ttu-id="9ea03-134">Gli elementi nella matrice non sono limitati e sono senza unità.</span><span class="sxs-lookup"><span data-stu-id="9ea03-134">The elements in the matrix are not bounded and are unitless.</span></span><br/> <span data-ttu-id="9ea03-135">Il valore predefinito è la matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="9ea03-135">The default is the identity matrix.</span></span><br/> <span data-ttu-id="9ea03-136">Il tipo è D2D1 \_ Matrix \_ 5x4 \_ F.</span><span class="sxs-lookup"><span data-stu-id="9ea03-136">The type is D2D1\_MATRIX\_5X4\_F.</span></span><br/> <span data-ttu-id="9ea03-137">Il valore predefinito è Matrix5x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="9ea03-137">The default value is Matrix5x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0).</span></span> <br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="9ea03-138">AlphaMode</span><span class="sxs-lookup"><span data-stu-id="9ea03-138">AlphaMode</span></span><br/> <span data-ttu-id="9ea03-139">D2D1 \_ la \_ \_ modalità Alpha della Prop \_</span><span class="sxs-lookup"><span data-stu-id="9ea03-139">D2D1\_COLORMATRIX\_PROP\_ALPHA\_MODE</span></span><br/>     | <span data-ttu-id="9ea03-140">Modalità Alpha dell'output.</span><span class="sxs-lookup"><span data-stu-id="9ea03-140">The alpha mode of the output.</span></span> <span data-ttu-id="9ea03-141">Per altre informazioni, vedere [modalità Alpha](#alpha-modes) .</span><span class="sxs-lookup"><span data-stu-id="9ea03-141">See [Alpha modes](#alpha-modes) for more info.</span></span> <br/> <span data-ttu-id="9ea03-142">Il tipo è D2D1 \_ COLORMATRIX \_ Alpha \_ mode.</span><span class="sxs-lookup"><span data-stu-id="9ea03-142">The type is D2D1\_COLORMATRIX\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="9ea03-143">Il valore predefinito è D2D1 \_ COLORMATRIX \_ Alpha \_ mode \_ premoltiplicato.</span><span class="sxs-lookup"><span data-stu-id="9ea03-143">The default value is D2D1\_COLORMATRIX\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="9ea03-144">ClampOutput</span><span class="sxs-lookup"><span data-stu-id="9ea03-144">ClampOutput</span></span><br/> <span data-ttu-id="9ea03-145">\_Output d2d1 COLORMATRIX \_ prop \_ Clamp \_</span><span class="sxs-lookup"><span data-stu-id="9ea03-145">D2D1\_COLORMATRIX\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="9ea03-146">Indica se l'effetto fissa i valori dei colori a un valore compreso tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico.</span><span class="sxs-lookup"><span data-stu-id="9ea03-146">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="9ea03-147">L'effetto blocca i valori prima di premoltiplicare l'alfa.</span><span class="sxs-lookup"><span data-stu-id="9ea03-147">The effect clamps the values before it premultiplies the alpha .</span></span><br/> <span data-ttu-id="9ea03-148">Se si imposta questa impostazione su TRUE, i valori vengono bloccati dall'effetto.</span><span class="sxs-lookup"><span data-stu-id="9ea03-148">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="9ea03-149">Se si imposta questa proprietà su FALSE, l'effetto non blocca i valori dei colori, mentre altri effetti e la superficie di output possono bloccare i valori se non hanno una precisione sufficientemente elevata.</span><span class="sxs-lookup"><span data-stu-id="9ea03-149">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> <span data-ttu-id="9ea03-150">Il tipo è BOOL.</span><span class="sxs-lookup"><span data-stu-id="9ea03-150">The type is BOOL.</span></span><br/> <span data-ttu-id="9ea03-151">Il valore predefinito è FALSE.</span><span class="sxs-lookup"><span data-stu-id="9ea03-151">The default value is FALSE.</span></span><br/> |



 

## <a name="alpha-modes"></a><span data-ttu-id="9ea03-152">Modalità Alpha</span><span class="sxs-lookup"><span data-stu-id="9ea03-152">Alpha modes</span></span>



| <span data-ttu-id="9ea03-153">Nome</span><span class="sxs-lookup"><span data-stu-id="9ea03-153">Name</span></span>                                          | <span data-ttu-id="9ea03-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ea03-154">Description</span></span>                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ea03-155">D2D1 \_ COLORMATRIX \_ \_ modalità alfa \_ premoltiplicata</span><span class="sxs-lookup"><span data-stu-id="9ea03-155">D2D1\_COLORMATRIX\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="9ea03-156">L'effetto Annulla la premoltiplicazione dell'input, applica la matrice di colori e premoltiplica l'output.</span><span class="sxs-lookup"><span data-stu-id="9ea03-156">The effect un-premultiplies the input, applies the color matrix, and premultiplies the output.</span></span><br/> |
| <span data-ttu-id="9ea03-157">D2D1 \_ \_ modalità Alpha \_ COLORMATRIX \_ lineare</span><span class="sxs-lookup"><span data-stu-id="9ea03-157">D2D1\_COLORMATRIX\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="9ea03-158">L'effetto applica la matrice di colori direttamente all'input e non premoltiplica l'output.</span><span class="sxs-lookup"><span data-stu-id="9ea03-158">The effect applies the color matrix directly to the input, and doesn't premultiply the output.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9ea03-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ea03-159">Requirements</span></span>



| <span data-ttu-id="9ea03-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ea03-160">Requirement</span></span> | <span data-ttu-id="9ea03-161">Valore</span><span class="sxs-lookup"><span data-stu-id="9ea03-161">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9ea03-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ea03-162">Minimum supported client</span></span> | <span data-ttu-id="9ea03-163">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="9ea03-163">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9ea03-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ea03-164">Minimum supported server</span></span> | <span data-ttu-id="9ea03-165">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="9ea03-165">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="9ea03-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ea03-166">Header</span></span>                   | <span data-ttu-id="9ea03-167">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="9ea03-167">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="9ea03-168">Libreria</span><span class="sxs-lookup"><span data-stu-id="9ea03-168">Library</span></span>                  | <span data-ttu-id="9ea03-169">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="9ea03-169">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="9ea03-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9ea03-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ea03-171">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="9ea03-171">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

