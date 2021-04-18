---
description: Definisce le costanti che descrivono i valori dello stato della trasformazione.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Enumerazione D3DTRANSFORMSTATETYPE (D3D9Types. h)
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
ms.openlocfilehash: c618e0e19bf7dd01dec73d35436f23189f9e78a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322451"
---
# <a name="d3dtransformstatetype-enumeration"></a><span data-ttu-id="8c861-103">Enumerazione D3DTRANSFORMSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="8c861-103">D3DTRANSFORMSTATETYPE enumeration</span></span>

<span data-ttu-id="8c861-104">Definisce le costanti che descrivono i valori dello stato della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="8c861-104">Defines constants that describe transformation state values.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c861-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c861-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="8c861-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="8c861-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8c861-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**\_Visualizzazione D3DTS**</span><span class="sxs-lookup"><span data-stu-id="8c861-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS\_VIEW**</span></span>
</dt> <dd>

<span data-ttu-id="8c861-108">Identifica la matrice di trasformazione da impostare come matrice di trasformazione della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8c861-108">Identifies the transformation matrix being set as the view transformation matrix.</span></span> <span data-ttu-id="8c861-109">Il valore predefinito è **null** (matrice di identità).</span><span class="sxs-lookup"><span data-stu-id="8c861-109">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="8c861-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**\_Proiezione D3DTS**</span><span class="sxs-lookup"><span data-stu-id="8c861-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS\_PROJECTION**</span></span>
</dt> <dd>

<span data-ttu-id="8c861-111">Identifica la matrice di trasformazione da impostare come matrice di trasformazione della proiezione.</span><span class="sxs-lookup"><span data-stu-id="8c861-111">Identifies the transformation matrix being set as the projection transformation matrix.</span></span> <span data-ttu-id="8c861-112">Il valore predefinito è **null** (matrice di identità).</span><span class="sxs-lookup"><span data-stu-id="8c861-112">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="8c861-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**\_TEXTURE0 D3DTS**</span><span class="sxs-lookup"><span data-stu-id="8c861-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS\_TEXTURE0**</span></span>
</dt> <dd>

<span data-ttu-id="8c861-114">Identifica la matrice di trasformazione da impostare per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="8c861-114">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8c861-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**\_TEXTURE1 D3DTS**</span><span class="sxs-lookup"><span data-stu-id="8c861-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS\_TEXTURE1**</span></span>
</dt> <dd>

<span data-ttu-id="8c861-116">Identifica la matrice di trasformazione da impostare per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="8c861-116">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8c861-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**\_TRAMA2 D3DTS**</span><span class="sxs-lookup"><span data-stu-id="8c861-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS\_TEXTURE2**</span></span>
</dt> <dd>

<span data-ttu-id="8c861-118">Identifica la matrice di trasformazione da impostare per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="8c861-118">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8c861-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**\_TEXTURE3 D3DTS**</span><span class="sxs-lookup"><span data-stu-id="8c861-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS\_TEXTURE3**</span></span>
</dt> <dd>

<span data-ttu-id="8c861-120">Identifica la matrice di trasformazione da impostare per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="8c861-120">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8c861-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**\_TEXTURE4 D3DTS**</span><span class="sxs-lookup"><span data-stu-id="8c861-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS\_TEXTURE4**</span></span>
</dt> <dd>

<span data-ttu-id="8c861-122">Identifica la matrice di trasformazione da impostare per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="8c861-122">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8c861-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**\_TEXTURE5 D3DTS**</span><span class="sxs-lookup"><span data-stu-id="8c861-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS\_TEXTURE5**</span></span>
</dt> <dd>

<span data-ttu-id="8c861-124">Identifica la matrice di trasformazione da impostare per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="8c861-124">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8c861-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**\_TEXTURE6 D3DTS**</span><span class="sxs-lookup"><span data-stu-id="8c861-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS\_TEXTURE6**</span></span>
</dt> <dd>

<span data-ttu-id="8c861-126">Identifica la matrice di trasformazione da impostare per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="8c861-126">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8c861-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**\_TEXTURE7 D3DTS**</span><span class="sxs-lookup"><span data-stu-id="8c861-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS\_TEXTURE7**</span></span>
</dt> <dd>

<span data-ttu-id="8c861-128">Identifica la matrice di trasformazione da impostare per la fase di trama specificata.</span><span class="sxs-lookup"><span data-stu-id="8c861-128">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="8c861-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8c861-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8c861-130">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8c861-130">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="8c861-131">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="8c861-131">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="8c861-132">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8c861-132">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c861-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c861-133">Remarks</span></span>

<span data-ttu-id="8c861-134">Gli Stati di trasformazione nell'intervallo compreso tra 256 e 511 sono riservati per archiviare fino a 256 matrici globali che possono essere indicizzate usando le \_ macro D3DTS WORLDMATRIX e D3DTS \_ World.</span><span class="sxs-lookup"><span data-stu-id="8c861-134">The transform states in the range 256 through 511 are reserved to store up to 256 world matrices that can be indexed using the D3DTS\_WORLDMATRIX and D3DTS\_WORLD macros.</span></span>



| <span data-ttu-id="8c861-135">Macro</span><span class="sxs-lookup"><span data-stu-id="8c861-135">Macros</span></span>                                                  |                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c861-136">**\_Mondo D3DTS**</span><span class="sxs-lookup"><span data-stu-id="8c861-136">**D3DTS\_WORLD**</span></span>](d3dts-world.md)                     | <span data-ttu-id="8c861-137">Equivale a D3DTS \_ WORLDMATRIX (0).</span><span class="sxs-lookup"><span data-stu-id="8c861-137">Equivalent to D3DTS\_WORLDMATRIX(0).</span></span>                                                                                                                                  |
| <span data-ttu-id="8c861-138">[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (indice)</span><span class="sxs-lookup"><span data-stu-id="8c861-138">[**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span></span> | <span data-ttu-id="8c861-139">Identifica la matrice di trasformazione da impostare per la matrice globale in corrispondenza dell'indice.</span><span class="sxs-lookup"><span data-stu-id="8c861-139">Identifies the transform matrix to set for the world matrix at index.</span></span> <span data-ttu-id="8c861-140">Più matrici internazionali vengono usate solo per la fusione dei vertici.</span><span class="sxs-lookup"><span data-stu-id="8c861-140">Multiple world matrices are used only for vertex blending.</span></span> <span data-ttu-id="8c861-141">In caso contrario \_ , viene usato solo D3DTS World.</span><span class="sxs-lookup"><span data-stu-id="8c861-141">Otherwise only D3DTS\_WORLD is used.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="8c861-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c861-142">Requirements</span></span>



| <span data-ttu-id="8c861-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c861-143">Requirement</span></span> | <span data-ttu-id="8c861-144">Valore</span><span class="sxs-lookup"><span data-stu-id="8c861-144">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c861-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c861-145">Header</span></span><br/> | <dl> <span data-ttu-id="8c861-146"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c861-146"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c861-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c861-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c861-148">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="8c861-148">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="8c861-149">**IDirect3DDevice9:: GetTransform**</span><span class="sxs-lookup"><span data-stu-id="8c861-149">**IDirect3DDevice9::GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="8c861-150">**IDirect3DDevice9:: MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="8c861-150">**IDirect3DDevice9::MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="8c861-151">**IDirect3DDevice9:: setransform**</span><span class="sxs-lookup"><span data-stu-id="8c861-151">**IDirect3DDevice9::SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="8c861-152">**\_Mondo D3DTS**</span><span class="sxs-lookup"><span data-stu-id="8c861-152">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="8c861-153">**D3DTS \_ mondo**</span><span class="sxs-lookup"><span data-stu-id="8c861-153">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="8c861-154">**\_WORLDMATRIX D3DTS**</span><span class="sxs-lookup"><span data-stu-id="8c861-154">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
