---
description: I flag seguenti vengono utilizzati per specificare i canali in una trama su cui operare.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 128525de2e403c11239c300372b79bd8ee8c1277
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481308"
---
# <a name="d3dx_filter"></a><span data-ttu-id="a9f22-103">\_Filtro D3DX</span><span class="sxs-lookup"><span data-stu-id="a9f22-103">D3DX\_FILTER</span></span>

<span data-ttu-id="a9f22-104">I flag seguenti vengono utilizzati per specificare i canali in una trama su cui operare.</span><span class="sxs-lookup"><span data-stu-id="a9f22-104">The following flags are used to specify which channels in a texture to operate on.</span></span>



|                         |                                                                                                                                                                                                             |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f22-105">\#definire</span><span class="sxs-lookup"><span data-stu-id="a9f22-105">\#define</span></span>                | <span data-ttu-id="a9f22-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9f22-106">Description</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="a9f22-107">\_Filtro D3DX \_ None</span><span class="sxs-lookup"><span data-stu-id="a9f22-107">D3DX\_FILTER\_NONE</span></span>      | <span data-ttu-id="a9f22-108">Non verrà eseguita alcuna operazione di ridimensionamento o filtro.</span><span class="sxs-lookup"><span data-stu-id="a9f22-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="a9f22-109">Si presuppone che i pixel all'esterno dei limiti dell'immagine di origine siano neri trasparenti.</span><span class="sxs-lookup"><span data-stu-id="a9f22-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>                                                                                 |
| <span data-ttu-id="a9f22-110">\_Punto di filtro D3DX \_</span><span class="sxs-lookup"><span data-stu-id="a9f22-110">D3DX\_FILTER\_POINT</span></span>     | <span data-ttu-id="a9f22-111">Ogni pixel di destinazione viene calcolato eseguendo il campionamento del pixel più vicino dall'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="a9f22-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>                                                                                                                     |
| <span data-ttu-id="a9f22-112">\_Filtro D3DX \_ lineare</span><span class="sxs-lookup"><span data-stu-id="a9f22-112">D3DX\_FILTER\_LINEAR</span></span>    | <span data-ttu-id="a9f22-113">Ogni pixel di destinazione viene calcolato eseguendo il campionamento dei quattro pixel più vicini dall'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="a9f22-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="a9f22-114">Questo filtro funziona meglio quando la scala su entrambi gli assi è minore di due.</span><span class="sxs-lookup"><span data-stu-id="a9f22-114">This filter works best when the scale on both axes is less than two.</span></span>                                          |
| <span data-ttu-id="a9f22-115">\_Triangolo filtro \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="a9f22-115">D3DX\_FILTER\_TRIANGLE</span></span>  | <span data-ttu-id="a9f22-116">Ogni pixel nell'immagine di origine contribuisce ugualmente all'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a9f22-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="a9f22-117">Questo è il più lento dei filtri.</span><span class="sxs-lookup"><span data-stu-id="a9f22-117">This is the slowest of the filters.</span></span>                                                                                           |
| <span data-ttu-id="a9f22-118">\_Casella filtro \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="a9f22-118">D3DX\_FILTER\_BOX</span></span>       | <span data-ttu-id="a9f22-119">Ogni pixel viene calcolato calcolando la media di una casella 2x2 (X2) di pixel dall'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="a9f22-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="a9f22-120">Questo filtro funziona solo quando le dimensioni della destinazione sono la metà di quelle dell'origine, come nel caso di mipmap.</span><span class="sxs-lookup"><span data-stu-id="a9f22-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span> |
| <span data-ttu-id="a9f22-121">D3DX \_ filtro \_ mirror \_ U</span><span class="sxs-lookup"><span data-stu-id="a9f22-121">D3DX\_FILTER\_MIRROR\_U</span></span> | <span data-ttu-id="a9f22-122">I pixel al di fuori del bordo della trama sull'asse u devono essere speculari, non incapsulati.</span><span class="sxs-lookup"><span data-stu-id="a9f22-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="a9f22-123">\_Mirror del filtro D3DX \_ \_ V</span><span class="sxs-lookup"><span data-stu-id="a9f22-123">D3DX\_FILTER\_MIRROR\_V</span></span> | <span data-ttu-id="a9f22-124">I pixel al di fuori del bordo della trama sull'asse v devono essere rispecchiati, non incapsulati.</span><span class="sxs-lookup"><span data-stu-id="a9f22-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="a9f22-125">\_Mirror filtro \_ D3DX \_ W</span><span class="sxs-lookup"><span data-stu-id="a9f22-125">D3DX\_FILTER\_MIRROR\_W</span></span> | <span data-ttu-id="a9f22-126">I pixel al di fuori del bordo della trama sull'asse w devono essere speculari, non incapsulati.</span><span class="sxs-lookup"><span data-stu-id="a9f22-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="a9f22-127">\_Mirror del filtro D3DX \_</span><span class="sxs-lookup"><span data-stu-id="a9f22-127">D3DX\_FILTER\_MIRROR</span></span>    | <span data-ttu-id="a9f22-128">Specificare questo flag equivale a specificare i flag D3DX Filter \_ mirror \_ \_ U, D3DX \_ Filter \_ mirror \_ V e D3DX \_ Filter \_ mirror \_ W.</span><span class="sxs-lookup"><span data-stu-id="a9f22-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>                                                                     |
| <span data-ttu-id="a9f22-129">\_Dithering filtro D3DX \_</span><span class="sxs-lookup"><span data-stu-id="a9f22-129">D3DX\_FILTER\_DITHER</span></span>    | <span data-ttu-id="a9f22-130">L'immagine risultante deve essere retinata usando un algoritmo di dithering ordinato 4x4.</span><span class="sxs-lookup"><span data-stu-id="a9f22-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span>                                                                                                                                  |
| <span data-ttu-id="a9f22-131">\_Filtro D3DX \_ sRGB \_ in</span><span class="sxs-lookup"><span data-stu-id="a9f22-131">D3DX\_FILTER\_SRGB\_IN</span></span>  | <span data-ttu-id="a9f22-132">I dati di input sono nello spazio colore sRGB (gamma 2,2).</span><span class="sxs-lookup"><span data-stu-id="a9f22-132">Input data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                              |
| <span data-ttu-id="a9f22-133">D3DX \_ filtro \_ sRGB in \_ uscita</span><span class="sxs-lookup"><span data-stu-id="a9f22-133">D3DX\_FILTER\_SRGB\_OUT</span></span> | <span data-ttu-id="a9f22-134">I dati di output sono nello spazio colore sRGB (gamma 2,2).</span><span class="sxs-lookup"><span data-stu-id="a9f22-134">The output data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                         |
| <span data-ttu-id="a9f22-135">D3DX \_ Filter \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="a9f22-135">D3DX\_FILTER\_SRGB</span></span>      | <span data-ttu-id="a9f22-136">Equivale a specificare il \_ filtro \_ D3DX \_ sRGB \| nel \_ filtro \_ D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="a9f22-136">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span>                                                                                                                                       |



 

<span data-ttu-id="a9f22-137">Ogni filtro valido deve contenere esattamente uno dei flag seguenti: filtro D3DX \_ \_ None, punto di \_ filtro D3DX \_ , D3DX \_ filtro \_ lineare, \_ triangolo di filtro D3DX \_ o \_ casella filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="a9f22-137">Each valid filter must contain exactly one of the following flags: D3DX\_FILTER\_NONE, D3DX\_FILTER\_POINT, D3DX\_FILTER\_LINEAR, D3DX\_FILTER\_TRIANGLE, or D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="a9f22-138">Inoltre, è possibile usare l'operatore OR per specificare zero o più dei flag facoltativi seguenti con un filtro valido: D3DX \_ Filter mirror \_ \_ U, D3DX \_ Filter \_ mirror \_ V, D3DX \_ Filter \_ mirror \_ W, D3DX \_ Filter \_ mirror, D3DX Filter \_ \_ spther, D3DX \_ Filter \_ sRGB \_ in, D3DX \_ Filter \_ sRGB \_ out o D3DX \_ Filter \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="a9f22-138">In addition, you can use the OR operator to specify zero or more of the following optional flags with a valid filter: D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, D3DX\_FILTER\_MIRROR\_W, D3DX\_FILTER\_MIRROR, D3DX\_FILTER\_DITHER, D3DX\_FILTER\_SRGB\_IN, D3DX\_FILTER\_SRGB\_OUT or D3DX\_FILTER\_SRGB.</span></span>

<span data-ttu-id="a9f22-139">Specificare \_ il valore predefinito di D3DX per questo parametro è in genere equivalente alla specifica del \_ \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="a9f22-139">Specifying D3DX\_DEFAULT for this parameter is usually the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="a9f22-140">Tuttavia, \_ il valore predefinito di D3DX può avere significati diversi, a seconda del metodo che usa il filtro.</span><span class="sxs-lookup"><span data-stu-id="a9f22-140">However, D3DX\_DEFAULT can have different meanings, depending on which method uses the filter.</span></span> <span data-ttu-id="a9f22-141">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="a9f22-141">For example:</span></span>

-   <span data-ttu-id="a9f22-142">Quando si usa [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), l' \_ impostazione predefinita di D3DX viene mappata al \_ triangolo di filtro D3DX D3DX del \_ \| \_ filtro \_ .</span><span class="sxs-lookup"><span data-stu-id="a9f22-142">When using [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>
-   <span data-ttu-id="a9f22-143">Quando si usa [**D3DXFilterTexture**](d3dxfiltertexture.md), \_ il valore predefinito di D3DX viene mappato alla \_ casella di filtro D3DX \_ se le dimensioni della trama sono una potenza di due e la \_ casella di filtro D3DX \_ \| D3DX filtro di \_ \_ dithering.</span><span class="sxs-lookup"><span data-stu-id="a9f22-143">When using [**D3DXFilterTexture**](d3dxfiltertexture.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

<span data-ttu-id="a9f22-144">Fare riferimento a ogni metodo per verificare le informazioni sulla modalità di \_ mapping del filtro predefinito di D3DX.</span><span class="sxs-lookup"><span data-stu-id="a9f22-144">Reference each method to check for information about how D3DX\_DEFAULT filter is mapped.</span></span>

## <a name="constant-information"></a><span data-ttu-id="a9f22-145">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="a9f22-145">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="a9f22-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9f22-146">Header</span></span>                   | <span data-ttu-id="a9f22-147">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="a9f22-147">d3dx9tex.h</span></span> |
| <span data-ttu-id="a9f22-148">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="a9f22-148">Minimum operating system</span></span> | <span data-ttu-id="a9f22-149">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a9f22-149">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a9f22-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9f22-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9f22-151">Costanti D3DX</span><span class="sxs-lookup"><span data-stu-id="a9f22-151">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



