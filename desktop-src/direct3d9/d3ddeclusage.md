---
description: Identifica l'uso previsto dei dati dei vertici.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: Enumerazione D3DDECLUSAGE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLUSAGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f3997aa38a7a97455b9f36d8afbee896ca9ae937
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322410"
---
# <a name="d3ddeclusage-enumeration"></a><span data-ttu-id="30f32-103">Enumerazione D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="30f32-103">D3DDECLUSAGE enumeration</span></span>

<span data-ttu-id="30f32-104">Identifica l'uso previsto dei dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="30f32-104">Identifies the intended use of vertex data.</span></span>

## <a name="syntax"></a><span data-ttu-id="30f32-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30f32-105">Syntax</span></span>


```C++
typedef enum D3DDECLUSAGE { 
  D3DDECLUSAGE_POSITION      = 0,
  D3DDECLUSAGE_BLENDWEIGHT   = 1,
  D3DDECLUSAGE_BLENDINDICES  = 2,
  D3DDECLUSAGE_NORMAL        = 3,
  D3DDECLUSAGE_PSIZE         = 4,
  D3DDECLUSAGE_TEXCOORD      = 5,
  D3DDECLUSAGE_TANGENT       = 6,
  D3DDECLUSAGE_BINORMAL      = 7,
  D3DDECLUSAGE_TESSFACTOR    = 8,
  D3DDECLUSAGE_POSITIONT     = 9,
  D3DDECLUSAGE_COLOR         = 10,
  D3DDECLUSAGE_FOG           = 11,
  D3DDECLUSAGE_DEPTH         = 12,
  D3DDECLUSAGE_SAMPLE        = 13
} D3DDECLUSAGE, *LPD3DDECLUSAGE;
```



## <a name="constants"></a><span data-ttu-id="30f32-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="30f32-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="30f32-107"><span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**\_Posizione D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="30f32-107"><span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGE\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="30f32-108">Posizionare i dati compresi tra (-1,-1) e (1, 1).</span><span class="sxs-lookup"><span data-stu-id="30f32-108">Position data ranging from (-1,-1) to (1,1).</span></span> <span data-ttu-id="30f32-109">Usare \_ la posizione D3DDECLUSAGE con un indice di utilizzo 0 per specificare la posizione non trasformata per l'elaborazione del vertice della funzione fissa e l'mosaico n-patch.</span><span class="sxs-lookup"><span data-stu-id="30f32-109">Use D3DDECLUSAGE\_POSITION with a usage index of 0 to specify untransformed position for fixed function vertex processing and the n-patch tessellator.</span></span> <span data-ttu-id="30f32-110">Usare la \_ posizione D3DDECLUSAGE con un indice di utilizzo 1 per specificare una posizione non trasformata nel vertex shader della funzione fissa per l'interpolazione dei vertici.</span><span class="sxs-lookup"><span data-stu-id="30f32-110">Use D3DDECLUSAGE\_POSITION with a usage index of 1 to specify untransformed position in the fixed function vertex shader for vertex tweening.</span></span>

</dd> <dt>

<span data-ttu-id="30f32-111"><span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**\_BLENDWEIGHT D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="30f32-111"><span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE\_BLENDWEIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="30f32-112">Fusione dei dati del peso.</span><span class="sxs-lookup"><span data-stu-id="30f32-112">Blending weight data.</span></span> <span data-ttu-id="30f32-113">Usare D3DDECLUSAGE \_ BLENDWEIGHT con un indice di utilizzo 0 per specificare i pesi di Blend usati nella combinazione di vertici indicizzati e non indicizzati.</span><span class="sxs-lookup"><span data-stu-id="30f32-113">Use D3DDECLUSAGE\_BLENDWEIGHT with a usage index of 0 to specify the blend weights used in indexed and nonindexed vertex blending.</span></span>

</dd> <dt>

<span data-ttu-id="30f32-114"><span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**\_BLENDINDICES D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="30f32-114"><span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE\_BLENDINDICES**</span></span>
</dt> <dd>

<span data-ttu-id="30f32-115">Fusione dei dati degli indici.</span><span class="sxs-lookup"><span data-stu-id="30f32-115">Blending indices data.</span></span> <span data-ttu-id="30f32-116">Usare D3DDECLUSAGE \_ BLENDINDICES con un indice di utilizzo 0 per specificare gli indici di matrice per la funzionalità di skinning con tavolozza indicizzata.</span><span class="sxs-lookup"><span data-stu-id="30f32-116">Use D3DDECLUSAGE\_BLENDINDICES with a usage index of 0 to specify matrix indices for indexed paletted skinning.</span></span>

</dd> <dt>

<span data-ttu-id="30f32-117"><span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE \_ normale**</span><span class="sxs-lookup"><span data-stu-id="30f32-117"><span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE\_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="30f32-118">Dati normali dei vertici.</span><span class="sxs-lookup"><span data-stu-id="30f32-118">Vertex normal data.</span></span> <span data-ttu-id="30f32-119">Usare D3DDECLUSAGE \_ Normal con un indice di utilizzo 0 per specificare le normali dei vertici per l'elaborazione del vertice della funzione fissa e l'mosaico n-patch.</span><span class="sxs-lookup"><span data-stu-id="30f32-119">Use D3DDECLUSAGE\_NORMAL with a usage index of 0 to specify vertex normals for fixed function vertex processing and the n-patch tessellator.</span></span> <span data-ttu-id="30f32-120">Usare D3DDECLUSAGE \_ Normal con un indice di utilizzo 1 per specificare le normali dei vertici per l'elaborazione del vertice della funzione fissa per l'interpolazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="30f32-120">Use D3DDECLUSAGE\_NORMAL with a usage index of 1 to specify vertex normals for fixed function vertex processing for vertex tweening.</span></span>

</dd> <dt>

<span data-ttu-id="30f32-121"><span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**\_PSIZE D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="30f32-121"><span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE\_PSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="30f32-122">Dati delle dimensioni del punto.</span><span class="sxs-lookup"><span data-stu-id="30f32-122">Point size data.</span></span> <span data-ttu-id="30f32-123">Usare D3DDECLUSAGE \_ PSIZE con un indice di utilizzo 0 per specificare l'attributo di dimensione punto usato dal motore di installazione del rasterizzatore per espandere un punto in un quad per la funzionalità Point-sprite.</span><span class="sxs-lookup"><span data-stu-id="30f32-123">Use D3DDECLUSAGE\_PSIZE with a usage index of 0 to specify the point-size attribute used by the setup engine of the rasterizer to expand a point into a quad for the point-sprite functionality.</span></span>

</dd> <dt>

<span data-ttu-id="30f32-124"><span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**\_TEXCOORD D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="30f32-124"><span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE\_TEXCOORD**</span></span>
</dt> <dd>

<span data-ttu-id="30f32-125">Dati delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="30f32-125">Texture coordinate data.</span></span> <span data-ttu-id="30f32-126">Usare D3DDECLUSAGE \_ TEXCOORD, n per specificare le coordinate di trama nell'elaborazione dei vertici delle funzioni fisse e nei pixel shader precedenti a PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="30f32-126">Use D3DDECLUSAGE\_TEXCOORD, n to specify texture coordinates in fixed function vertex processing and in pixel shaders prior to ps\_3\_0.</span></span> <span data-ttu-id="30f32-127">Questi possono essere usati per passare dati definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="30f32-127">These can be used to pass user defined data.</span></span>

</dd> <dt>

<span data-ttu-id="30f32-128"><span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**\_Tangente D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="30f32-128"><span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE\_TANGENT**</span></span>
</dt> <dd>

<span data-ttu-id="30f32-129">Dati della tangente del vertice.</span><span class="sxs-lookup"><span data-stu-id="30f32-129">Vertex tangent data.</span></span>

</dd> <dt>

<span data-ttu-id="30f32-130"><span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE- \_ normale**</span><span class="sxs-lookup"><span data-stu-id="30f32-130"><span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE\_BINORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="30f32-131">Dati binormali vertice.</span><span class="sxs-lookup"><span data-stu-id="30f32-131">Vertex binormal data.</span></span>

</dd> <dt>

<span data-ttu-id="30f32-132"><span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**\_TESSFACTOR D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="30f32-132"><span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE\_TESSFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="30f32-133">Singolo valore a virgola mobile positivo.</span><span class="sxs-lookup"><span data-stu-id="30f32-133">Single positive floating point value.</span></span> <span data-ttu-id="30f32-134">Usare D3DDECLUSAGE \_ TESSFACTOR con un indice di utilizzo 0 per specificare un fattore a mosaico usato nell'unità a mosaico per controllare la frequenza dello schema a mosaico.</span><span class="sxs-lookup"><span data-stu-id="30f32-134">Use D3DDECLUSAGE\_TESSFACTOR with a usage index of 0 to specify a tessellation factor used in the tessellation unit to control the rate of tessellation.</span></span> <span data-ttu-id="30f32-135">Per ulteriori informazioni sul tipo di dati, vedere D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="30f32-135">For more information about the data type, see D3DDECLTYPE\_FLOAT1.</span></span>

</dd> <dt>

<span data-ttu-id="30f32-136"><span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**\_Posizione D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="30f32-136"><span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE\_POSITIONT**</span></span>
</dt> <dd>

<span data-ttu-id="30f32-137">I dati dei vertici contengono dati di posizione trasformati compresi tra (0, 0) e (larghezza del viewport, altezza del viewport).</span><span class="sxs-lookup"><span data-stu-id="30f32-137">Vertex data contains transformed position data ranging from (0,0) to (viewport width, viewport height).</span></span> <span data-ttu-id="30f32-138">Usare D3DDECLUSAGE \_ positiont con un indice di utilizzo 0 per specificare la posizione trasformata.</span><span class="sxs-lookup"><span data-stu-id="30f32-138">Use D3DDECLUSAGE\_POSITIONT with a usage index of 0 to specify transformed position.</span></span> <span data-ttu-id="30f32-139">Quando viene impostata una dichiarazione contenente questo oggetto, la pipeline non esegue l'elaborazione dei vertici.</span><span class="sxs-lookup"><span data-stu-id="30f32-139">When a declaration containing this is set, the pipeline does not perform vertex processing.</span></span>

</dd> <dt>

<span data-ttu-id="30f32-140"><span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**\_Colore D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="30f32-140"><span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**D3DDECLUSAGE\_COLOR**</span></span>
</dt> <dd>

<span data-ttu-id="30f32-141">I dati dei vertici contengono il colore speculare o diffuso.</span><span class="sxs-lookup"><span data-stu-id="30f32-141">Vertex data contains diffuse or specular color.</span></span> <span data-ttu-id="30f32-142">Usare il \_ colore D3DDECLUSAGE con un indice di utilizzo 0 per specificare il colore diffuso nel vertex shader della funzione fissa e nei pixel shader precedenti a PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="30f32-142">Use D3DDECLUSAGE\_COLOR with a usage index of 0 to specify the diffuse color in the fixed function vertex shader and pixel shaders prior to ps\_3\_0.</span></span> <span data-ttu-id="30f32-143">Usare il \_ colore D3DDECLUSAGE con un indice di utilizzo 1 per specificare il colore speculare nel vertex shader della funzione fissa e nei pixel shader precedenti a PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="30f32-143">Use D3DDECLUSAGE\_COLOR with a usage index of 1 to specify the specular color in the fixed function vertex shader and pixel shaders prior to ps\_3\_0.</span></span>

</dd> <dt>

<span data-ttu-id="30f32-144"><span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE \_ nebbia**</span><span class="sxs-lookup"><span data-stu-id="30f32-144"><span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE\_FOG**</span></span>
</dt> <dd>

<span data-ttu-id="30f32-145">I dati dei vertici contengono dati di nebbia.</span><span class="sxs-lookup"><span data-stu-id="30f32-145">Vertex data contains fog data.</span></span> <span data-ttu-id="30f32-146">Usare D3DDECLUSAGE \_ Fog con un indice di utilizzo 0 per specificare un valore di Blend di nebbia usato dopo il completamento dell'ombreggiatura dei pixel.</span><span class="sxs-lookup"><span data-stu-id="30f32-146">Use D3DDECLUSAGE\_FOG with a usage index of 0 to specify a fog blend value used after pixel shading finishes.</span></span> <span data-ttu-id="30f32-147">Si applica ai pixel shader prima della versione PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="30f32-147">This applies to pixel shaders prior to version ps\_3\_0.</span></span>

</dd> <dt>

<span data-ttu-id="30f32-148"><span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**\_Profondità D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="30f32-148"><span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**D3DDECLUSAGE\_DEPTH**</span></span>
</dt> <dd>

<span data-ttu-id="30f32-149">I dati dei vertici contengono dati di profondità.</span><span class="sxs-lookup"><span data-stu-id="30f32-149">Vertex data contains depth data.</span></span>

</dd> <dt>

<span data-ttu-id="30f32-150"><span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**\_Esempio D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="30f32-150"><span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**D3DDECLUSAGE\_SAMPLE**</span></span>
</dt> <dd>

<span data-ttu-id="30f32-151">I dati dei vertici contengono dati del campionatore.</span><span class="sxs-lookup"><span data-stu-id="30f32-151">Vertex data contains sampler data.</span></span> <span data-ttu-id="30f32-152">Usare \_ l'esempio D3DDECLUSAGE con un indice di utilizzo 0 per specificare il valore di spostamento da ricercare.</span><span class="sxs-lookup"><span data-stu-id="30f32-152">Use D3DDECLUSAGE\_SAMPLE with a usage index of 0 to specify the displacement value to look up.</span></span> <span data-ttu-id="30f32-153">Può essere usato solo con la \_ ricerca D3DDECLUSAGE LOOKUPPRESAMPLED o D3DDECLUSAGE \_ .</span><span class="sxs-lookup"><span data-stu-id="30f32-153">It can be used only with D3DDECLUSAGE\_LOOKUPPRESAMPLED or D3DDECLUSAGE\_LOOKUP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30f32-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="30f32-154">Remarks</span></span>

<span data-ttu-id="30f32-155">I dati dei vertici vengono dichiarati con una matrice di strutture [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="30f32-155">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="30f32-156">Ogni elemento nella matrice contiene un tipo di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="30f32-156">Each element in the array contains a usage type.</span></span>

<span data-ttu-id="30f32-157">Per altre informazioni sulle dichiarazioni dei vertici, vedere [dichiarazione vertici (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="30f32-157">For more information about vertex declarations, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30f32-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30f32-158">Requirements</span></span>



| <span data-ttu-id="30f32-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="30f32-159">Requirement</span></span> | <span data-ttu-id="30f32-160">Valore</span><span class="sxs-lookup"><span data-stu-id="30f32-160">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30f32-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30f32-161">Header</span></span><br/> | <dl> <span data-ttu-id="30f32-162"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="30f32-162"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30f32-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30f32-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f32-164">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="30f32-164">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="30f32-165">Dichiarazione vertici (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="30f32-165">Vertex Declaration (Direct3D 9)</span></span>](vertex-declaration.md)
</dt> </dl>

 

 




