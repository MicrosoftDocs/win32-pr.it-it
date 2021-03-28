---
title: Enumerazione D3DX11_FILTER_FLAG (D3DX11tex. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Flag di filtro della trama.
ms.assetid: 083a6a19-1933-4831-9501-36d4867f3dce
keywords:
- Enumerazione D3DX11_FILTER_FLAG Direct3D 11
- Puntatore di enumerazione LPD3DX11_FILTER_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_FILTER_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2105970efb7f2ec07464d8a902df49d8f75bc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982574"
---
# <a name="d3dx11_filter_flag-enumeration"></a><span data-ttu-id="aa9ec-106">\_Enumerazione flag di filtro D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="aa9ec-106">D3DX11\_FILTER\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="aa9ec-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="aa9ec-108">Flag di filtro della trama.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-108">Texture filtering flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9ec-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa9ec-109">Syntax</span></span>


```C++
typedef enum D3DX11_FILTER_FLAG { 
  D3DX11_FILTER_NONE              = (1 << 0),
  D3DX11_FILTER_POINT             = (2 << 0),
  D3DX11_FILTER_LINEAR            = (3 << 0),
  D3DX11_FILTER_TRIANGLE          = (4 << 0),
  D3DX11_FILTER_BOX               = (5 << 0),
  D3DX11_FILTER_MIRROR_U          = (1 << 16),
  D3DX11_FILTER_MIRROR_V          = (2 << 16),
  D3DX11_FILTER_MIRROR_W          = (4 << 16),
  D3DX11_FILTER_MIRROR            = (7 << 16),
  D3DX11_FILTER_DITHER            = (1 << 19),
  D3DX11_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX11_FILTER_SRGB_IN           = (1 << 21),
  D3DX11_FILTER_SRGB_OUT          = (2 << 21),
  D3DX11_FILTER_SRGB              = (3 << 21)
} D3DX11_FILTER_FLAG, *LPD3DX11_FILTER_FLAG;
```



## <a name="constants"></a><span data-ttu-id="aa9ec-110">Costanti</span><span class="sxs-lookup"><span data-stu-id="aa9ec-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="aa9ec-111"><span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**\_Filtro D3DX11 \_ None**</span><span class="sxs-lookup"><span data-stu-id="aa9ec-111"><span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**D3DX11\_FILTER\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="aa9ec-112">Non verrà eseguita alcuna operazione di ridimensionamento o filtro.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-112">No scaling or filtering will take place.</span></span> <span data-ttu-id="aa9ec-113">Si presuppone che i pixel all'esterno dei limiti dell'immagine di origine siano neri trasparenti.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-113">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>

</dd> <dt>

<span data-ttu-id="aa9ec-114"><span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**\_Punto di filtro D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="aa9ec-114"><span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**D3DX11\_FILTER\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="aa9ec-115">Ogni pixel di destinazione viene calcolato eseguendo il campionamento del pixel più vicino dall'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-115">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>

</dd> <dt>

<span data-ttu-id="aa9ec-116"><span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**\_Filtro D3DX11 \_ lineare**</span><span class="sxs-lookup"><span data-stu-id="aa9ec-116"><span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**D3DX11\_FILTER\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="aa9ec-117">Ogni pixel di destinazione viene calcolato eseguendo il campionamento dei quattro pixel più vicini dall'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-117">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="aa9ec-118">Questo filtro funziona meglio quando la scala su entrambi gli assi è minore di due.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-118">This filter works best when the scale on both axes is less than two.</span></span>

</dd> <dt>

<span data-ttu-id="aa9ec-119"><span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**\_Triangolo filtro \_ D3DX11**</span><span class="sxs-lookup"><span data-stu-id="aa9ec-119"><span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**D3DX11\_FILTER\_TRIANGLE**</span></span>
</dt> <dd>

<span data-ttu-id="aa9ec-120">Ogni pixel nell'immagine di origine contribuisce ugualmente all'immagine di destinazione.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-120">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="aa9ec-121">Questo è il più lento dei filtri.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-121">This is the slowest of the filters.</span></span>

</dd> <dt>

<span data-ttu-id="aa9ec-122"><span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**\_Casella filtro \_ D3DX11**</span><span class="sxs-lookup"><span data-stu-id="aa9ec-122"><span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**D3DX11\_FILTER\_BOX**</span></span>
</dt> <dd>

<span data-ttu-id="aa9ec-123">Ogni pixel viene calcolato calcolando la media di una casella 2x2 (X2) di pixel dall'immagine di origine.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-123">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="aa9ec-124">Questo filtro funziona solo quando le dimensioni della destinazione sono la metà di quelle dell'origine, come nel caso di mipmap.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-124">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span>

</dd> <dt>

<span data-ttu-id="aa9ec-125"><span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**D3DX11 \_ filtro \_ mirror \_ U**</span><span class="sxs-lookup"><span data-stu-id="aa9ec-125"><span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**D3DX11\_FILTER\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="aa9ec-126">I pixel al di fuori del bordo della trama sull'asse u devono essere speculari, non incapsulati.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-126">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="aa9ec-127"><span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**\_Mirror del filtro D3DX11 \_ \_ V**</span><span class="sxs-lookup"><span data-stu-id="aa9ec-127"><span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**D3DX11\_FILTER\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="aa9ec-128">I pixel al di fuori del bordo della trama sull'asse v devono essere rispecchiati, non incapsulati.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-128">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="aa9ec-129"><span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**\_Mirror filtro \_ D3DX11 \_ W**</span><span class="sxs-lookup"><span data-stu-id="aa9ec-129"><span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**D3DX11\_FILTER\_MIRROR\_W**</span></span>
</dt> <dd>

<span data-ttu-id="aa9ec-130">I pixel al di fuori del bordo della trama sull'asse w devono essere speculari, non incapsulati.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-130">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="aa9ec-131"><span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**\_Mirror del filtro D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="aa9ec-131"><span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**D3DX11\_FILTER\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="aa9ec-132">Specificare questo flag equivale a specificare i flag D3DX Filter \_ mirror \_ \_ U, D3DX \_ Filter \_ mirror \_ V e D3DX \_ Filter \_ mirror \_ W.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-132">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>

</dd> <dt>

<span data-ttu-id="aa9ec-133"><span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**\_Dithering filtro D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="aa9ec-133"><span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**D3DX11\_FILTER\_DITHER**</span></span>
</dt> <dd>

<span data-ttu-id="aa9ec-134">L'immagine risultante deve essere retinata usando un algoritmo di dithering ordinato 4x4.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-134">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span> <span data-ttu-id="aa9ec-135">Questo errore si verifica quando si esegue la conversione da un formato a un altro.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-135">This happens when converting from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="aa9ec-136"><span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**\_Diffusione del \_ dithering del filtro D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="aa9ec-136"><span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**D3DX11\_FILTER\_DITHER\_DIFFUSION**</span></span>
</dt> <dd>

<span data-ttu-id="aa9ec-137">Quando si passa da un formato a un altro, è necessario diffonderne l'immagine.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-137">Do diffuse dithering on the image when changing from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="aa9ec-138"><span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**\_Filtro D3DX11 \_ sRGB \_ in**</span><span class="sxs-lookup"><span data-stu-id="aa9ec-138"><span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11\_FILTER\_SRGB\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="aa9ec-139">I dati di input sono nello spazio colore RGB (sRGB) standard.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-139">Input data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="aa9ec-140">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-140">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="aa9ec-141"><span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11 \_ filtro \_ sRGB in \_ uscita**</span><span class="sxs-lookup"><span data-stu-id="aa9ec-141"><span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11\_FILTER\_SRGB\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="aa9ec-142">I dati di output sono nello spazio colore RGB (sRGB) standard.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-142">Output data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="aa9ec-143">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-143">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="aa9ec-144"><span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11 \_ Filter \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="aa9ec-144"><span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11\_FILTER\_SRGB**</span></span>
</dt> <dd>

<span data-ttu-id="aa9ec-145">Equivale a specificare il \_ filtro \_ D3DX \_ sRGB \| nel \_ filtro \_ D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="aa9ec-145">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span> <span data-ttu-id="aa9ec-146">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-146">See remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa9ec-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa9ec-147">Remarks</span></span>

<span data-ttu-id="aa9ec-148">D3DX11 esegue automaticamente la correzione gamma (per convertire i dati di colore dallo spazio RGB allo spazio RGB standard) quando si caricano i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-148">D3DX11 automatically performs gamma correction (to convert color data from RGB space to standard RGB space) when loading texture data.</span></span> <span data-ttu-id="aa9ec-149">Questa operazione viene eseguita automaticamente ad esempio quando i dati RGB vengono caricati da un file con estensione png in una trama sRGB.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-149">This is automatically done for instance when RGB data is loaded from a .png file into an sRGB texture.</span></span> <span data-ttu-id="aa9ec-150">Usare i flag di filtro SRGB per indicare se non è necessario convertire i dati nello spazio sRGB.</span><span class="sxs-lookup"><span data-stu-id="aa9ec-150">Use the SRGB filter flags to indicate if the data does not need to be converted into sRGB space.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa9ec-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa9ec-151">Requirements</span></span>



| <span data-ttu-id="aa9ec-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa9ec-152">Requirement</span></span> | <span data-ttu-id="aa9ec-153">Valore</span><span class="sxs-lookup"><span data-stu-id="aa9ec-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9ec-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa9ec-154">Header</span></span><br/> | <dl> <span data-ttu-id="aa9ec-155"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa9ec-155"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa9ec-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa9ec-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9ec-157">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="aa9ec-157">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





