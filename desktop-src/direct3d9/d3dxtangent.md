---
description: Definisce le impostazioni utilizzate per i calcoli del frame tangente della mesh.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: Enumerazione D3DXTANGENT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTANGENT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 43e3c5ced0eee3366b85070ce89d19154d048ab4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322580"
---
# <a name="d3dxtangent-enumeration"></a><span data-ttu-id="b66ff-103">Enumerazione D3DXTANGENT</span><span class="sxs-lookup"><span data-stu-id="b66ff-103">D3DXTANGENT enumeration</span></span>

<span data-ttu-id="b66ff-104">Definisce le impostazioni utilizzate per i calcoli del frame tangente della mesh.</span><span class="sxs-lookup"><span data-stu-id="b66ff-104">Defines settings used for mesh tangent frame computations.</span></span>

## <a name="syntax"></a><span data-ttu-id="b66ff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b66ff-105">Syntax</span></span>


```C++
typedef enum D3DXTANGENT { 
  D3DXTANGENT_WRAP_U                   = 0x01,
  D3DXTANGENT_WRAP_V                   = 0x02,
  D3DXTANGENT_WRAP_UV                  = 0x03,
  D3DXTANGENT_DONT_NORMALIZE_PARTIALS  = 0x04,
  D3DXTANGENT_DONT_ORTHOGONALIZE       = 0x08,
  D3DXTANGENT_ORTHOGONALIZE_FROM_V     = 0x010,
  D3DXTANGENT_ORTHOGONALIZE_FROM_U     = 0x020,
  D3DXTANGENT_WEIGHT_BY_AREA           = 0x040,
  D3DXTANGENT_WEIGHT_EQUAL             = 0x080,
  D3DXTANGENT_WIND_CW                  = 0x0100,
  D3DXTANGENT_CALCULATE_NORMALS        = 0x0200,
  D3DXTANGENT_GENERATE_IN_PLACE        = 0x0400
} D3DXTANGENT, *LPD3DXTANGENT;
```



## <a name="constants"></a><span data-ttu-id="b66ff-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="b66ff-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b66ff-107"><span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT a \_ capo automatico \_ U**</span><span class="sxs-lookup"><span data-stu-id="b66ff-107"><span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT\_WRAP\_U**</span></span>
</dt> <dd>

<span data-ttu-id="b66ff-108">I valori delle coordinate di trama nella direzione u sono compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="b66ff-108">Texture coordinate values in the u direction are between 0 and 1.</span></span> <span data-ttu-id="b66ff-109">In questo caso verrà scelto un set di coordinate di trama che riduce al minimo il perimetro del triangolo.</span><span class="sxs-lookup"><span data-stu-id="b66ff-109">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="b66ff-110">Vedere [wrapping della trama (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="b66ff-110">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="b66ff-111"><span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ Wrap \_ V**</span><span class="sxs-lookup"><span data-stu-id="b66ff-111"><span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT\_WRAP\_V**</span></span>
</dt> <dd>

<span data-ttu-id="b66ff-112">I valori delle coordinate di trama nella direzione v sono compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="b66ff-112">Texture coordinate values in the v direction are between 0 and 1.</span></span> <span data-ttu-id="b66ff-113">In questo caso verrà scelto un set di coordinate di trama che riduce al minimo il perimetro del triangolo.</span><span class="sxs-lookup"><span data-stu-id="b66ff-113">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="b66ff-114">Vedere [wrapping della trama (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="b66ff-114">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="b66ff-115"><span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT a \_ capo \_ UV**</span><span class="sxs-lookup"><span data-stu-id="b66ff-115"><span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT\_WRAP\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="b66ff-116">I valori delle coordinate di trama nelle direzioni u e v sono compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="b66ff-116">Texture coordinate values in both u and v directions are between 0 and 1.</span></span> <span data-ttu-id="b66ff-117">In questo caso verrà scelto un set di coordinate di trama che riduce al minimo il perimetro del triangolo.</span><span class="sxs-lookup"><span data-stu-id="b66ff-117">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="b66ff-118">Vedere [wrapping della trama (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="b66ff-118">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="b66ff-119"><span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ dont \_ normalizzare i \_ parziali**</span><span class="sxs-lookup"><span data-stu-id="b66ff-119"><span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT\_DONT\_NORMALIZE\_PARTIALS**</span></span>
</dt> <dd>

<span data-ttu-id="b66ff-120">Non normalizzare le derivazioni parziali rispetto alle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="b66ff-120">Do not normalize partial derivatives with respect to texture coordinates.</span></span> <span data-ttu-id="b66ff-121">Se non normalizzato, la scala dei derivati parziali è proporzionale alla scala del modello 3D divisa per la scala del triangolo nello spazio (u, v).</span><span class="sxs-lookup"><span data-stu-id="b66ff-121">If not normalized, the scale of the partial derivatives is proportional to the scale of the 3D model divided by the scale of the triangle in (u, v) space.</span></span> <span data-ttu-id="b66ff-122">Questo valore di scala fornisce una misura del grado di estensione della trama in una determinata direzione.</span><span class="sxs-lookup"><span data-stu-id="b66ff-122">This scale value provides a measure of how much the texture is stretched in a given direction.</span></span> <span data-ttu-id="b66ff-123">La lunghezza del vettore risultante è una somma ponderata delle lunghezze dei derivati parziali.</span><span class="sxs-lookup"><span data-stu-id="b66ff-123">The resulting vector length is a weighted sum of the lengths of the partial derivatives.</span></span>

</dd> <dt>

<span data-ttu-id="b66ff-124"><span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT \_ dont \_ ORTHOGONALIZE**</span><span class="sxs-lookup"><span data-stu-id="b66ff-124"><span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT\_DONT\_ORTHOGONALIZE**</span></span>
</dt> <dd>

<span data-ttu-id="b66ff-125">Non trasformare le coordinate di trama in coordinate cartesiane ortogonali.</span><span class="sxs-lookup"><span data-stu-id="b66ff-125">Do not transform texture coordinates to orthogonal Cartesian coordinates.</span></span> <span data-ttu-id="b66ff-126">Si escludono a vicenda con D3DXTANGENT \_ ORTHOGONALIZE \_ \_ e D3DXTANGENT \_ ORTHOGONALIZE \_ da \_ V.</span><span class="sxs-lookup"><span data-stu-id="b66ff-126">Mutually exclusive with D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V.</span></span>

</dd> <dt>

<span data-ttu-id="b66ff-127"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**\_ORTHOGONALIZE D3DXTANGENT \_ da \_ V**</span><span class="sxs-lookup"><span data-stu-id="b66ff-127"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V**</span></span>
</dt> <dd>

<span data-ttu-id="b66ff-128">Calcolare la derivata parziale per quanto concerne la coordinata di trama v in modo indipendente per ogni vertice, quindi calcolare la derivata parziale per quanto riguarda il prodotto incrociato del derivato parziale rispetto a v e il vettore normale.</span><span class="sxs-lookup"><span data-stu-id="b66ff-128">Compute the partial derivative with respect to texture coordinate v independently for each vertex, and then compute the partial derivative with respect to u as the cross product of the partial derivative with respect to v and the normal vector.</span></span> <span data-ttu-id="b66ff-129">Si escludono a vicenda con D3DXTANGENT \_ dont \_ ORTHOGONALIZE e D3DXTANGENT \_ ORTHOGONALIZE \_ da \_ U.</span><span class="sxs-lookup"><span data-stu-id="b66ff-129">Mutually exclusive with D3DXTANGENT\_DONT\_ORTHOGONALIZE and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U.</span></span>

</dd> <dt>

<span data-ttu-id="b66ff-130"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**\_ORTHOGONALIZE D3DXTANGENT \_ da \_ U**</span><span class="sxs-lookup"><span data-stu-id="b66ff-130"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U**</span></span>
</dt> <dd>

<span data-ttu-id="b66ff-131">Calcolare la derivata parziale per quanto concerne la coordinata di trama u in modo indipendente per ogni vertice, quindi calcolare la derivata parziale rispetto a v come prodotto incrociato del vettore normale e la derivata parziale rispetto all'utente.</span><span class="sxs-lookup"><span data-stu-id="b66ff-131">Compute the partial derivative with respect to texture coordinate u independently for each vertex, and then compute the partial derivative with respect to v as the cross product of the normal vector and the partial derivative with respect to u.</span></span> <span data-ttu-id="b66ff-132">Si escludono a vicenda con D3DXTANGENT \_ dont \_ ORTHOGONALIZE e D3DXTANGENT \_ ORTHOGONALIZE \_ da \_ V.</span><span class="sxs-lookup"><span data-stu-id="b66ff-132">Mutually exclusive with D3DXTANGENT\_DONT\_ORTHOGONALIZE and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V.</span></span>

</dd> <dt>

<span data-ttu-id="b66ff-133"><span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT \_ ponderato \_ per \_ area**</span><span class="sxs-lookup"><span data-stu-id="b66ff-133"><span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT\_WEIGHT\_BY\_AREA**</span></span>
</dt> <dd>

<span data-ttu-id="b66ff-134">Ponderare la direzione del vettore calcolato per vertice normale o parziale derivato in base alle aree dei triangoli collegati al vertice.</span><span class="sxs-lookup"><span data-stu-id="b66ff-134">Weight the direction of the computed per-vertex normal or partial derivative vector according to the areas of triangles attached to that vertex.</span></span> <span data-ttu-id="b66ff-135">Si escludono a vicenda con D3DXTANGENT \_ Weight \_ uguale a.</span><span class="sxs-lookup"><span data-stu-id="b66ff-135">Mutually exclusive with D3DXTANGENT\_WEIGHT\_EQUAL.</span></span>

</dd> <dt>

<span data-ttu-id="b66ff-136"><span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT \_ peso \_ uguale**</span><span class="sxs-lookup"><span data-stu-id="b66ff-136"><span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT\_WEIGHT\_EQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="b66ff-137">Calcola un vettore normale a lunghezza di unità per ogni triangolo della mesh di input.</span><span class="sxs-lookup"><span data-stu-id="b66ff-137">Compute a unit-length normal vector for each triangle of the input mesh.</span></span> <span data-ttu-id="b66ff-138">Si escludono a vicenda con D3DXTANGENT \_ Weight \_ by \_ area.</span><span class="sxs-lookup"><span data-stu-id="b66ff-138">Mutually exclusive with D3DXTANGENT\_WEIGHT\_BY\_AREA.</span></span>

</dd> <dt>

<span data-ttu-id="b66ff-139"><span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT \_ vento \_ CW**</span><span class="sxs-lookup"><span data-stu-id="b66ff-139"><span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT\_WIND\_CW**</span></span>
</dt> <dd>

<span data-ttu-id="b66ff-140">I vertici vengono ordinati in senso orario intorno a ogni triangolo.</span><span class="sxs-lookup"><span data-stu-id="b66ff-140">Vertices are ordered in a clockwise direction around each triangle.</span></span> <span data-ttu-id="b66ff-141">La direzione del vettore normale calcolata è quindi invertita di 180 gradi dalla direzione calcolata utilizzando l'ordine dei vertici in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="b66ff-141">The computed normal vector direction is therefore inverted 180 degrees from the direction computed using counterclockwise vertex ordering.</span></span>

</dd> <dt>

<span data-ttu-id="b66ff-142"><span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ Calcola \_ normali**</span><span class="sxs-lookup"><span data-stu-id="b66ff-142"><span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT\_CALCULATE\_NORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="b66ff-143">Calcolare il vettore normale per vertice per ogni triangolo della mesh di input e ignorare i vettori normali già presenti nella mesh di input.</span><span class="sxs-lookup"><span data-stu-id="b66ff-143">Compute the per-vertex normal vector for each triangle of the input mesh, and ignore any normal vectors already in the input mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b66ff-144"><span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ genera \_ sul \_ posto**</span><span class="sxs-lookup"><span data-stu-id="b66ff-144"><span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT\_GENERATE\_IN\_PLACE**</span></span>
</dt> <dd>

<span data-ttu-id="b66ff-145">I risultati vengono archiviati nella mesh di input originale e la mesh di output non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="b66ff-145">The results are stored in the original input mesh, and the output mesh is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b66ff-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b66ff-146">Requirements</span></span>



| <span data-ttu-id="b66ff-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="b66ff-147">Requirement</span></span> | <span data-ttu-id="b66ff-148">Valore</span><span class="sxs-lookup"><span data-stu-id="b66ff-148">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b66ff-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b66ff-149">Header</span></span><br/> | <dl> <span data-ttu-id="b66ff-150"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b66ff-150"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b66ff-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b66ff-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b66ff-152">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="b66ff-152">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="b66ff-153">**D3DXComputeTangentFrameEx**</span><span class="sxs-lookup"><span data-stu-id="b66ff-153">**D3DXComputeTangentFrameEx**</span></span>](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




