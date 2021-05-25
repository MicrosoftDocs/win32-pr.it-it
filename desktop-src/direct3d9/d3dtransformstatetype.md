---
description: Definisce costanti che descrivono i valori dello stato di trasformazione.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Enumerazione D3DTRANSFORMSTATETYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRANSFORMSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 022aa20fab0739b32aa75eb5f4bc575c0a8ad853
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342996"
---
# <a name="d3dtransformstatetype-enumeration"></a><span data-ttu-id="d2006-103">Enumerazione D3DTRANSFORMSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="d2006-103">D3DTRANSFORMSTATETYPE enumeration</span></span>

<span data-ttu-id="d2006-104">Definisce costanti che descrivono i valori dello stato di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="d2006-104">Defines constants that describe transformation state values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2006-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2006-105">Syntax</span></span>


```C++
typedef enum D3DTRANSFORMSTATETYPE { 
  D3DTS_VIEW         = 2,
  D3DTS_PROJECTION   = 3,
  D3DTS_TEXTURE0     = 16,
  D3DTS_TEXTURE1     = 17,
  D3DTS_TEXTURE2     = 18,
  D3DTS_TEXTURE3     = 19,
  D3DTS_TEXTURE4     = 20,
  D3DTS_TEXTURE5     = 21,
  D3DTS_TEXTURE6     = 22,
  D3DTS_TEXTURE7     = 23,
  D3DTS_FORCE_DWORD  = 0x7fffffff
} D3DTRANSFORMSTATETYPE, *LPD3DTRANSFORMSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="d2006-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="d2006-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d2006-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**VISTA D3DTS \_**</span><span class="sxs-lookup"><span data-stu-id="d2006-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS\_VIEW**</span></span>
</dt> <dd>

<span data-ttu-id="d2006-108">Identifica la matrice di trasformazione impostata come matrice di trasformazione della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d2006-108">Identifies the transformation matrix being set as the view transformation matrix.</span></span> <span data-ttu-id="d2006-109">Il valore predefinito è **NULL** (matrice di identità).</span><span class="sxs-lookup"><span data-stu-id="d2006-109">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="d2006-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**PROIEZIONE D3DTS \_**</span><span class="sxs-lookup"><span data-stu-id="d2006-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS\_PROJECTION**</span></span>
</dt> <dd>

<span data-ttu-id="d2006-111">Identifica la matrice di trasformazione impostata come matrice di trasformazione della proiezione.</span><span class="sxs-lookup"><span data-stu-id="d2006-111">Identifies the transformation matrix being set as the projection transformation matrix.</span></span> <span data-ttu-id="d2006-112">Il valore predefinito è **NULL** (matrice di identità).</span><span class="sxs-lookup"><span data-stu-id="d2006-112">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="d2006-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**TRAMA D3DTS0 \_**</span><span class="sxs-lookup"><span data-stu-id="d2006-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS\_TEXTURE0**</span></span>
</dt> <dd>

<span data-ttu-id="d2006-114">Identifica la matrice di trasformazione impostata per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="d2006-114">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="d2006-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**TRAMA D3DTS1 \_**</span><span class="sxs-lookup"><span data-stu-id="d2006-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS\_TEXTURE1**</span></span>
</dt> <dd>

<span data-ttu-id="d2006-116">Identifica la matrice di trasformazione impostata per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="d2006-116">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="d2006-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**TRAMA D3DTS2 \_**</span><span class="sxs-lookup"><span data-stu-id="d2006-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS\_TEXTURE2**</span></span>
</dt> <dd>

<span data-ttu-id="d2006-118">Identifica la matrice di trasformazione impostata per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="d2006-118">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="d2006-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**TRAMA D3DTS3 \_**</span><span class="sxs-lookup"><span data-stu-id="d2006-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS\_TEXTURE3**</span></span>
</dt> <dd>

<span data-ttu-id="d2006-120">Identifica la matrice di trasformazione impostata per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="d2006-120">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="d2006-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**TRAMA D3DTS4 \_**</span><span class="sxs-lookup"><span data-stu-id="d2006-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS\_TEXTURE4**</span></span>
</dt> <dd>

<span data-ttu-id="d2006-122">Identifica la matrice di trasformazione impostata per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="d2006-122">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="d2006-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**TRAMA D3DTS5 \_**</span><span class="sxs-lookup"><span data-stu-id="d2006-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS\_TEXTURE5**</span></span>
</dt> <dd>

<span data-ttu-id="d2006-124">Identifica la matrice di trasformazione impostata per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="d2006-124">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="d2006-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**TRAMA D3DTS6 \_**</span><span class="sxs-lookup"><span data-stu-id="d2006-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS\_TEXTURE6**</span></span>
</dt> <dd>

<span data-ttu-id="d2006-126">Identifica la matrice di trasformazione impostata per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="d2006-126">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="d2006-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**TRAMA D3DTS7 \_**</span><span class="sxs-lookup"><span data-stu-id="d2006-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS\_TEXTURE7**</span></span>
</dt> <dd>

<span data-ttu-id="d2006-128">Identifica la matrice di trasformazione impostata per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="d2006-128">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="d2006-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d2006-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="d2006-130">Forza la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="d2006-130">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="d2006-131">Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="d2006-131">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="d2006-132">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d2006-132">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2006-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2006-133">Remarks</span></span>

<span data-ttu-id="d2006-134">Gli stati di trasformazione nell'intervallo da 256 a 511 sono riservati per archiviare fino a 256 matrici del mondo che possono essere indicizzate usando le macro D3DTS \_ WORLDMATRIX e D3DTS \_ WORLD.</span><span class="sxs-lookup"><span data-stu-id="d2006-134">The transform states in the range 256 through 511 are reserved to store up to 256 world matrices that can be indexed using the D3DTS\_WORLDMATRIX and D3DTS\_WORLD macros.</span></span>



| <span data-ttu-id="d2006-135">Macro</span><span class="sxs-lookup"><span data-stu-id="d2006-135">Macros</span></span>                                                  | <span data-ttu-id="d2006-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2006-136">Description</span></span>                                                                                                                                                                      |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d2006-137">**MONDO D3DTS \_**</span><span class="sxs-lookup"><span data-stu-id="d2006-137">**D3DTS\_WORLD**</span></span>](d3dts-world.md)                     | <span data-ttu-id="d2006-138">Equivalente a D3DTS \_ WORLDMATRIX(0).</span><span class="sxs-lookup"><span data-stu-id="d2006-138">Equivalent to D3DTS\_WORLDMATRIX(0).</span></span>                                                                                                                                  |
| <span data-ttu-id="d2006-139">[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (indice)</span><span class="sxs-lookup"><span data-stu-id="d2006-139">[**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span></span> | <span data-ttu-id="d2006-140">Identifica la matrice di trasformazione da impostare per la matrice globale in corrispondenza dell'indice.</span><span class="sxs-lookup"><span data-stu-id="d2006-140">Identifies the transform matrix to set for the world matrix at index.</span></span> <span data-ttu-id="d2006-141">Più matrici di mondo vengono usate solo per la fusione dei vertici.</span><span class="sxs-lookup"><span data-stu-id="d2006-141">Multiple world matrices are used only for vertex blending.</span></span> <span data-ttu-id="d2006-142">In caso contrario, viene usato solo D3DTS \_ WORLD.</span><span class="sxs-lookup"><span data-stu-id="d2006-142">Otherwise only D3DTS\_WORLD is used.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d2006-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2006-143">Requirements</span></span>



| <span data-ttu-id="d2006-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2006-144">Requirement</span></span> | <span data-ttu-id="d2006-145">Valore</span><span class="sxs-lookup"><span data-stu-id="d2006-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2006-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2006-146">Header</span></span><br/> | <dl> <span data-ttu-id="d2006-147"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="d2006-147"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2006-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2006-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2006-149">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="d2006-149">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="d2006-150">**IDirect3DDevice9::GetTransform**</span><span class="sxs-lookup"><span data-stu-id="d2006-150">**IDirect3DDevice9::GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="d2006-151">**IDirect3DDevice9::MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="d2006-151">**IDirect3DDevice9::MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="d2006-152">**IDirect3DDevice9::SetTransform**</span><span class="sxs-lookup"><span data-stu-id="d2006-152">**IDirect3DDevice9::SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="d2006-153">**MONDO D3DTS \_**</span><span class="sxs-lookup"><span data-stu-id="d2006-153">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="d2006-154">**D3DTS \_ WORLDn**</span><span class="sxs-lookup"><span data-stu-id="d2006-154">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="d2006-155">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="d2006-155">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
