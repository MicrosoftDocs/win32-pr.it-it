---
description: Definisce un tipo di dati di dichiarazione vertici.
ms.assetid: 993fc7e4-4752-4bce-82d0-0a034fdc69c0
title: Enumerazione D3DDECLTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3edb3f936772a7265c627f10eeb7aeb4f461701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354379"
---
# <a name="d3ddecltype-enumeration"></a><span data-ttu-id="0cae1-103">Enumerazione D3DDECLTYPE</span><span class="sxs-lookup"><span data-stu-id="0cae1-103">D3DDECLTYPE enumeration</span></span>

<span data-ttu-id="0cae1-104">Definisce un tipo di dati di dichiarazione vertici.</span><span class="sxs-lookup"><span data-stu-id="0cae1-104">Defines a vertex declaration data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cae1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0cae1-105">Syntax</span></span>


```C++
typedef enum D3DDECLTYPE { 
  D3DDECLTYPE_FLOAT1     = 0,
  D3DDECLTYPE_FLOAT2     = 1,
  D3DDECLTYPE_FLOAT3     = 2,
  D3DDECLTYPE_FLOAT4     = 3,
  D3DDECLTYPE_D3DCOLOR   = 4,
  D3DDECLTYPE_UBYTE4     = 5,
  D3DDECLTYPE_SHORT2     = 6,
  D3DDECLTYPE_SHORT4     = 7,
  D3DDECLTYPE_UBYTE4N    = 8,
  D3DDECLTYPE_SHORT2N    = 9,
  D3DDECLTYPE_SHORT4N    = 10,
  D3DDECLTYPE_USHORT2N   = 11,
  D3DDECLTYPE_USHORT4N   = 12,
  D3DDECLTYPE_UDEC3      = 13,
  D3DDECLTYPE_DEC3N      = 14,
  D3DDECLTYPE_FLOAT16_2  = 15,
  D3DDECLTYPE_FLOAT16_4  = 16,
  D3DDECLTYPE_UNUSED     = 17
} D3DDECLTYPE, *LPD3DDECLTYPE;
```



## <a name="constants"></a><span data-ttu-id="0cae1-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="0cae1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0cae1-107"><span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**\_FLOAT1 D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-107"><span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE\_FLOAT1**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-108">Float a un componente espanso fino a (float, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="0cae1-108">One-component float expanded to (float, 0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-109"><span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**\_FLOAT2 D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-109"><span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE\_FLOAT2**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-110">Float a due componenti espanso a (float, float, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="0cae1-110">Two-component float expanded to (float, float, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-111"><span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**\_FLOAT3 D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-111"><span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE\_FLOAT3**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-112">Float a tre componenti espanso a (float, float, float, 1).</span><span class="sxs-lookup"><span data-stu-id="0cae1-112">Three-component float expanded to (float, float, float, 1).</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-113"><span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**\_Float4 D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-113"><span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE\_FLOAT4**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-114">Float a quattro componenti espanso a (float, float, float, float).</span><span class="sxs-lookup"><span data-stu-id="0cae1-114">Four-component float expanded to (float, float, float, float).</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-115"><span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**\_D3DCOLOR D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-115"><span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE\_D3DCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-116">Byte con quattro componenti, compressi e senza segno mappati a un intervallo compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="0cae1-116">Four-component, packed, unsigned bytes mapped to 0 to 1 range.</span></span> <span data-ttu-id="0cae1-117">Input è un [**D3DCOLOR**](d3dcolor.md) ed è espanso nell'ordine RGBA.</span><span class="sxs-lookup"><span data-stu-id="0cae1-117">Input is a [**D3DCOLOR**](d3dcolor.md) and is expanded to RGBA order.</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-118"><span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**\_UBYTE4 D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-118"><span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE\_UBYTE4**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-119">Byte senza segno a quattro componenti.</span><span class="sxs-lookup"><span data-stu-id="0cae1-119">Four-component, unsigned byte.</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-120"><span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**\_SHORT2 D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-120"><span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE\_SHORT2**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-121">A due componenti, con segno Short espanso a (valore, valore, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="0cae1-121">Two-component, signed short expanded to (value, value, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-122"><span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**\_SHORT4 D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-122"><span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE\_SHORT4**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-123">A quattro componenti, con segno Short espanso a (valore, valore, valore, valore).</span><span class="sxs-lookup"><span data-stu-id="0cae1-123">Four-component, signed short expanded to (value, value, value, value).</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-124"><span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**\_Dati UBYTE4N D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-124"><span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE\_UBYTE4N**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-125">Byte a quattro componenti con ogni byte normalizzato dividendo con 255.0 f.</span><span class="sxs-lookup"><span data-stu-id="0cae1-125">Four-component byte with each byte normalized by dividing with 255.0f.</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-126"><span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**\_SHORT2N D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-126"><span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE\_SHORT2N**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-127">Normalizzato, a due componenti, con segno Short, espanso in (First short/32767.0, Second short/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="0cae1-127">Normalized, two-component, signed short, expanded to (first short/32767.0, second short/32767.0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-128"><span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**\_SHORT4N D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-128"><span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE\_SHORT4N**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-129">Normalizzato, a quattro componenti, con segno Short, espanso a (First short/32767.0, Second short/32767.0, terzo short/32767.0, Fourth short/32767.0).</span><span class="sxs-lookup"><span data-stu-id="0cae1-129">Normalized, four-component, signed short, expanded to (first short/32767.0, second short/32767.0, third short/32767.0, fourth short/32767.0).</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-130"><span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**\_USHORT2N D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-130"><span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE\_USHORT2N**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-131">Normalizzato, a due componenti, a breve senza segno, espanso a (First Short/65535.0, Short Short/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="0cae1-131">Normalized, two-component, unsigned short, expanded to (first short/65535.0, short short/65535.0, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-132"><span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**\_USHORT4N D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-132"><span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE\_USHORT4N**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-133">Normalizzato, a quattro componenti, senza segno breve, espanso in (First Short/65535.0, Second Short/65535.0, terzo Short/65535.0, Fourth Short/65535.0).</span><span class="sxs-lookup"><span data-stu-id="0cae1-133">Normalized, four-component, unsigned short, expanded to (first short/65535.0, second short/65535.0, third short/65535.0, fourth short/65535.0).</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-134"><span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**\_UDEC3 D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-134"><span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE\_UDEC3**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-135">Formato a tre componenti, senza segno, 10 10 10 espanso a (valore, valore, valore, 1).</span><span class="sxs-lookup"><span data-stu-id="0cae1-135">Three-component, unsigned, 10 10 10 format expanded to (value, value, value, 1).</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-136"><span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**\_DEC3N D3DDECLTYPE**</span><span class="sxs-lookup"><span data-stu-id="0cae1-136"><span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE\_DEC3N**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-137">Formato a tre componenti, firmato, 10 10 10 normalizzato ed espanso a (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).</span><span class="sxs-lookup"><span data-stu-id="0cae1-137">Three-component, signed, 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-138"><span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE \_ FLOAT16 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="0cae1-138"><span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE\_FLOAT16\_2**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-139">A due componenti, a 16 bit, a virgola mobile espansa (valore, valore, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="0cae1-139">Two-component, 16-bit, floating point expanded to (value, value, 0, 1).</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-140"><span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE \_ FLOAT16 \_ 4**</span><span class="sxs-lookup"><span data-stu-id="0cae1-140"><span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE\_FLOAT16\_4**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-141">A quattro componenti, a 16 bit, a virgola mobile espansa (valore, valore, valore, valore).</span><span class="sxs-lookup"><span data-stu-id="0cae1-141">Four-component, 16-bit, floating point expanded to (value, value, value, value).</span></span>

</dd> <dt>

<span data-ttu-id="0cae1-142"><span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE non \_ usato**</span><span class="sxs-lookup"><span data-stu-id="0cae1-142"><span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="0cae1-143">Il campo tipo nella dichiarazione non è usato.</span><span class="sxs-lookup"><span data-stu-id="0cae1-143">Type field in the declaration is unused.</span></span> <span data-ttu-id="0cae1-144">Questa soluzione è progettata per l'uso con D3DDECLMETHOD \_ UV e D3DDECLMETHOD \_ LOOKUPPRESAMPLED.</span><span class="sxs-lookup"><span data-stu-id="0cae1-144">This is designed for use with D3DDECLMETHOD\_UV and D3DDECLMETHOD\_LOOKUPPRESAMPLED.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0cae1-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="0cae1-145">Remarks</span></span>

<span data-ttu-id="0cae1-146">I dati dei vertici vengono dichiarati con una matrice di strutture [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="0cae1-146">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="0cae1-147">Ogni elemento nella matrice contiene un tipo di dati di dichiarazione vertici.</span><span class="sxs-lookup"><span data-stu-id="0cae1-147">Each element in the array contains a vertex declaration data type.</span></span>

<span data-ttu-id="0cae1-148">Usare lo strumento DirectX Caps Viewer (DXCapsViewer.exe) per vedere quali tipi sono supportati nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0cae1-148">Use the DirectX Caps Viewer Tool (DXCapsViewer.exe) to see which types are supported on your device.</span></span> <span data-ttu-id="0cae1-149">È possibile ottenere questo strumento e ottenere informazioni su di esso da DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="0cae1-149">You can get this tool and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="0cae1-150">Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="0cae1-150">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cae1-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cae1-151">Requirements</span></span>



| <span data-ttu-id="0cae1-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cae1-152">Requirement</span></span> | <span data-ttu-id="0cae1-153">Valore</span><span class="sxs-lookup"><span data-stu-id="0cae1-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cae1-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0cae1-154">Header</span></span><br/> | <dl> <span data-ttu-id="0cae1-155"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cae1-155"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cae1-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cae1-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cae1-157">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="0cae1-157">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="0cae1-158">**D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="0cae1-158">**D3DDECLMETHOD**</span></span>](./d3ddeclmethod.md)
</dt> </dl>

 

 
