---
description: Informazioni sui flag D3DX_FILTER usati per specificare i canali di una trama su cui operare, ad esempio D3DX_FILTER_TRIANGLE.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7580749eca2134f899356c4632d8171b147aa7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408224"
---
# <a name="d3dx_filter"></a><span data-ttu-id="c40e0-103">FILTRO D3DX \_</span><span class="sxs-lookup"><span data-stu-id="c40e0-103">D3DX\_FILTER</span></span>

<span data-ttu-id="c40e0-104">I flag seguenti vengono usati per specificare i canali in una trama su cui operare.</span><span class="sxs-lookup"><span data-stu-id="c40e0-104">The following flags are used to specify which channels in a texture to operate on.</span></span>



| <span data-ttu-id="c40e0-105">\#Definire</span><span class="sxs-lookup"><span data-stu-id="c40e0-105">\#define</span></span>                | <span data-ttu-id="c40e0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c40e0-106">Description</span></span>                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c40e0-107">FILTRO D3DX \_ \_ NESSUNO</span><span class="sxs-lookup"><span data-stu-id="c40e0-107">D3DX\_FILTER\_NONE</span></span>      | <span data-ttu-id="c40e0-108">Non verrà fatto alcun ridimensionamento o filtro.</span><span class="sxs-lookup"><span data-stu-id="c40e0-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="c40e0-109">Si presuppone che i pixel all'esterno dei limiti dell'immagine di origine siano di colore nero trasparente.</span><span class="sxs-lookup"><span data-stu-id="c40e0-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>                                                                                 |
| <span data-ttu-id="c40e0-110">PUNTO DI FILTRO D3DX \_ \_</span><span class="sxs-lookup"><span data-stu-id="c40e0-110">D3DX\_FILTER\_POINT</span></span>     | <span data-ttu-id="c40e0-111">Ogni pixel di destinazione viene calcolato tramite il campionamento del pixel più vicino dall'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="c40e0-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>                                                                                                                     |
| <span data-ttu-id="c40e0-112">D3DX \_ FILTER \_ LINEAR</span><span class="sxs-lookup"><span data-stu-id="c40e0-112">D3DX\_FILTER\_LINEAR</span></span>    | <span data-ttu-id="c40e0-113">Ogni pixel di destinazione viene calcolato tramite il campionamento dei quattro pixel più vicini dall'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="c40e0-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="c40e0-114">Questo filtro funziona meglio quando la scala su entrambi gli assi è minore di due.</span><span class="sxs-lookup"><span data-stu-id="c40e0-114">This filter works best when the scale on both axes is less than two.</span></span>                                          |
| <span data-ttu-id="c40e0-115">TRIANGOLO FILTRO D3DX \_ \_</span><span class="sxs-lookup"><span data-stu-id="c40e0-115">D3DX\_FILTER\_TRIANGLE</span></span>  | <span data-ttu-id="c40e0-116">Ogni pixel nell'immagine di origine contribuisce equamente all'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c40e0-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="c40e0-117">Questo è il più lento dei filtri.</span><span class="sxs-lookup"><span data-stu-id="c40e0-117">This is the slowest of the filters.</span></span>                                                                                           |
| <span data-ttu-id="c40e0-118">CASELLA FILTRO \_ \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="c40e0-118">D3DX\_FILTER\_BOX</span></span>       | <span data-ttu-id="c40e0-119">Ogni pixel viene calcolato mediamente da una casella di 2x2(x2) di pixel dall'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="c40e0-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="c40e0-120">Questo filtro funziona solo quando le dimensioni della destinazione sono metà di quelle dell'origine, come nel caso delle mipmap.</span><span class="sxs-lookup"><span data-stu-id="c40e0-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span> |
| <span data-ttu-id="c40e0-121">D3DX \_ FILTER \_ MIRROR \_ U</span><span class="sxs-lookup"><span data-stu-id="c40e0-121">D3DX\_FILTER\_MIRROR\_U</span></span> | <span data-ttu-id="c40e0-122">I pixel al di fuori del bordo della trama sull'asse u devono essere speculari, non di cui è stato eseguito il wrapping.</span><span class="sxs-lookup"><span data-stu-id="c40e0-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="c40e0-123">D3DX \_ FILTER \_ MIRROR \_ V</span><span class="sxs-lookup"><span data-stu-id="c40e0-123">D3DX\_FILTER\_MIRROR\_V</span></span> | <span data-ttu-id="c40e0-124">I pixel al di fuori del bordo della trama sull'asse v devono essere speculari, non di cui è stato eseguito il wrapping.</span><span class="sxs-lookup"><span data-stu-id="c40e0-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="c40e0-125">D3DX \_ FILTER \_ MIRROR \_ W</span><span class="sxs-lookup"><span data-stu-id="c40e0-125">D3DX\_FILTER\_MIRROR\_W</span></span> | <span data-ttu-id="c40e0-126">I pixel al di fuori del bordo della trama sull'asse w devono essere speculari, non di cui è stato eseguito il wrapping.</span><span class="sxs-lookup"><span data-stu-id="c40e0-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="c40e0-127">D3DX \_ FILTER \_ MIRROR</span><span class="sxs-lookup"><span data-stu-id="c40e0-127">D3DX\_FILTER\_MIRROR</span></span>    | <span data-ttu-id="c40e0-128">L'impostazione di questo flag è uguale a quando si specificano i flag D3DX \_ FILTER \_ MIRROR \_ U, D3DX FILTER MIRROR V e \_ \_ \_ D3DX \_ FILTER MIRROR \_ \_ W.</span><span class="sxs-lookup"><span data-stu-id="c40e0-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>                                                                     |
| <span data-ttu-id="c40e0-129">DITHERING \_ FILTRO \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="c40e0-129">D3DX\_FILTER\_DITHER</span></span>    | <span data-ttu-id="c40e0-130">L'immagine risultante deve essere dithering usando un algoritmo dithering ordinato 4x4.</span><span class="sxs-lookup"><span data-stu-id="c40e0-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span>                                                                                                                                  |
| <span data-ttu-id="c40e0-131">D3DX \_ FILTER \_ SRGB \_ IN</span><span class="sxs-lookup"><span data-stu-id="c40e0-131">D3DX\_FILTER\_SRGB\_IN</span></span>  | <span data-ttu-id="c40e0-132">I dati di input si trova nello spazio colore sRGB (gamma 2.2).</span><span class="sxs-lookup"><span data-stu-id="c40e0-132">Input data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                              |
| <span data-ttu-id="c40e0-133">FILTRO D3DX \_ \_ SRGB \_ OUT</span><span class="sxs-lookup"><span data-stu-id="c40e0-133">D3DX\_FILTER\_SRGB\_OUT</span></span> | <span data-ttu-id="c40e0-134">I dati di output sono nello spazio colore sRGB (gamma 2.2).</span><span class="sxs-lookup"><span data-stu-id="c40e0-134">The output data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                         |
| <span data-ttu-id="c40e0-135">D3DX \_ FILTER \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="c40e0-135">D3DX\_FILTER\_SRGB</span></span>      | <span data-ttu-id="c40e0-136">Come specificare D3DX \_ FILTER \_ SRGB \_ IN \| D3DX \_ FILTER \_ SRGB \_ OUT.</span><span class="sxs-lookup"><span data-stu-id="c40e0-136">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span>                                                                                                                                       |



 

<span data-ttu-id="c40e0-137">Ogni filtro valido deve contenere esattamente uno dei flag seguenti: D3DX \_ FILTER \_ NONE, D3DX \_ FILTER \_ POINT, D3DX \_ FILTER \_ LINEAR, D3DX FILTER TRIANGLE o \_ \_ D3DX \_ FILTER \_ BOX.</span><span class="sxs-lookup"><span data-stu-id="c40e0-137">Each valid filter must contain exactly one of the following flags: D3DX\_FILTER\_NONE, D3DX\_FILTER\_POINT, D3DX\_FILTER\_LINEAR, D3DX\_FILTER\_TRIANGLE, or D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="c40e0-138">È anche possibile usare l'operatore OR per specificare zero o più dei flag facoltativi seguenti con un filtro valido: D3DX \_ FILTER \_ MIRROR \_ U, D3DX \_ FILTER MIRROR \_ \_ V, D3DX \_ FILTER MIRROR \_ \_ W, \_ \_ D3DX FILTER MIRROR, D3DX \_ FILTER \_ DITHER, D3DX \_ FILTER \_ SRGB \_ IN, D3DX \_ FILTER SRGB OUT o \_ \_ D3DX \_ FILTER \_ SRGB.</span><span class="sxs-lookup"><span data-stu-id="c40e0-138">In addition, you can use the OR operator to specify zero or more of the following optional flags with a valid filter: D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, D3DX\_FILTER\_MIRROR\_W, D3DX\_FILTER\_MIRROR, D3DX\_FILTER\_DITHER, D3DX\_FILTER\_SRGB\_IN, D3DX\_FILTER\_SRGB\_OUT or D3DX\_FILTER\_SRGB.</span></span>

<span data-ttu-id="c40e0-139">Specificare D3DX DEFAULT per questo parametro equivale in genere a specificare \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.</span><span class="sxs-lookup"><span data-stu-id="c40e0-139">Specifying D3DX\_DEFAULT for this parameter is usually the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="c40e0-140">Tuttavia, D3DX \_ DEFAULT può avere significati diversi, a seconda del metodo che usa il filtro.</span><span class="sxs-lookup"><span data-stu-id="c40e0-140">However, D3DX\_DEFAULT can have different meanings, depending on which method uses the filter.</span></span> <span data-ttu-id="c40e0-141">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="c40e0-141">For example:</span></span>

-   <span data-ttu-id="c40e0-142">Quando si [**usa D3DXCreateTextureFromFileEx,**](d3dxcreatetexturefromfileex.md)D3DX DEFAULT esegue il mapping a \_ D3DX \_ FILTER TRIANGLE \_ \| D3DX \_ FILTER \_ DITHER.</span><span class="sxs-lookup"><span data-stu-id="c40e0-142">When using [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>
-   <span data-ttu-id="c40e0-143">Quando si usa [**D3DXFilterTexture,**](d3dxfiltertexture.md)D3DX DEFAULT esegue il mapping a D3DX FILTER BOX se le dimensioni della trama sono due e \_ \_ \_ D3DX \_ FILTER BOX \_ \| D3DX \_ FILTER DITHER \_ in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c40e0-143">When using [**D3DXFilterTexture**](d3dxfiltertexture.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

<span data-ttu-id="c40e0-144">Fare riferimento a ogni metodo per verificare la modalità di mapping del filtro D3DX \_ DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="c40e0-144">Reference each method to check for information about how D3DX\_DEFAULT filter is mapped.</span></span>

## <a name="constant-information"></a><span data-ttu-id="c40e0-145">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="c40e0-145">Constant Information</span></span>



| <span data-ttu-id="c40e0-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="c40e0-146">Requirement</span></span>                         | <span data-ttu-id="c40e0-147">Valore</span><span class="sxs-lookup"><span data-stu-id="c40e0-147">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="c40e0-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c40e0-148">Header</span></span>                   | <span data-ttu-id="c40e0-149">d3dx9tex.h</span><span class="sxs-lookup"><span data-stu-id="c40e0-149">d3dx9tex.h</span></span> |
| <span data-ttu-id="c40e0-150">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="c40e0-150">Minimum operating system</span></span> | <span data-ttu-id="c40e0-151">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c40e0-151">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c40e0-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c40e0-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c40e0-153">Costanti D3DX</span><span class="sxs-lookup"><span data-stu-id="c40e0-153">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



