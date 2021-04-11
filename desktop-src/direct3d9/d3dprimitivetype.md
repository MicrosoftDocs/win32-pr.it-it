---
description: Definisce le primitive supportate da Direct3D.
ms.assetid: 89e697f9-02b9-4ae1-9e86-6178da0cb008
title: Enumerazione D3DPRIMITIVETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRIMITIVETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 933bbec72950bd2c73fda8b3781dd46393ca4c96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132358"
---
# <a name="d3dprimitivetype-enumeration"></a><span data-ttu-id="9b8bd-103">Enumerazione D3DPRIMITIVETYPE</span><span class="sxs-lookup"><span data-stu-id="9b8bd-103">D3DPRIMITIVETYPE enumeration</span></span>

<span data-ttu-id="9b8bd-104">Definisce le primitive supportate da Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-104">Defines the primitives supported by Direct3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b8bd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b8bd-105">Syntax</span></span>


```C++
typedef enum D3DPRIMITIVETYPE { 
  D3DPT_POINTLIST      = 1,
  D3DPT_LINELIST       = 2,
  D3DPT_LINESTRIP      = 3,
  D3DPT_TRIANGLELIST   = 4,
  D3DPT_TRIANGLESTRIP  = 5,
  D3DPT_TRIANGLEFAN    = 6,
  D3DPT_FORCE_DWORD    = 0x7fffffff
} D3DPRIMITIVETYPE, *LPD3DPRIMITIVETYPE;
```



## <a name="constants"></a><span data-ttu-id="9b8bd-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="9b8bd-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9b8bd-107"><span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT \_**</span><span class="sxs-lookup"><span data-stu-id="9b8bd-107"><span id="D3DPT_POINTLIST"></span><span id="d3dpt_pointlist"></span>**D3DPT\_POINTLIST**</span></span>
</dt> <dd>

<span data-ttu-id="9b8bd-108">Esegue il rendering dei vertici come una raccolta di punti isolati.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-108">Renders the vertices as a collection of isolated points.</span></span> <span data-ttu-id="9b8bd-109">Questo valore non è supportato per le primitive indicizzate.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-109">This value is unsupported for indexed primitives.</span></span>

</dd> <dt>

<span data-ttu-id="9b8bd-110"><span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**\_Linea D3DPT**</span><span class="sxs-lookup"><span data-stu-id="9b8bd-110"><span id="D3DPT_LINELIST"></span><span id="d3dpt_linelist"></span>**D3DPT\_LINELIST**</span></span>
</dt> <dd>

<span data-ttu-id="9b8bd-111">Esegue il rendering dei vertici come un elenco di segmenti di linea rettilinei isolati.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-111">Renders the vertices as a list of isolated straight line segments.</span></span>

</dd> <dt>

<span data-ttu-id="9b8bd-112"><span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**\_LINESTRIP D3DPT**</span><span class="sxs-lookup"><span data-stu-id="9b8bd-112"><span id="D3DPT_LINESTRIP"></span><span id="d3dpt_linestrip"></span>**D3DPT\_LINESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="9b8bd-113">Esegue il rendering dei vertici come una singola polilinea.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-113">Renders the vertices as a single polyline.</span></span>

</dd> <dt>

<span data-ttu-id="9b8bd-114"><span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**Triangolo D3DPT \_**</span><span class="sxs-lookup"><span data-stu-id="9b8bd-114"><span id="D3DPT_TRIANGLELIST"></span><span id="d3dpt_trianglelist"></span>**D3DPT\_TRIANGLELIST**</span></span>
</dt> <dd>

<span data-ttu-id="9b8bd-115">Esegue il rendering dei vertici specificati come una sequenza di triangoli isolati.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-115">Renders the specified vertices as a sequence of isolated triangles.</span></span> <span data-ttu-id="9b8bd-116">Ogni gruppo di tre vertici definisce un triangolo separato.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-116">Each group of three vertices defines a separate triangle.</span></span>

<span data-ttu-id="9b8bd-117">L'abbattimento di back-face è influenzato dallo stato di rendering dell'ordine di esecuzione corrente.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-117">Back-face culling is affected by the current winding-order render state.</span></span>

</dd> <dt>

<span data-ttu-id="9b8bd-118"><span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**\_TRIANGLESTRIP D3DPT**</span><span class="sxs-lookup"><span data-stu-id="9b8bd-118"><span id="D3DPT_TRIANGLESTRIP"></span><span id="d3dpt_trianglestrip"></span>**D3DPT\_TRIANGLESTRIP**</span></span>
</dt> <dd>

<span data-ttu-id="9b8bd-119">Esegue il rendering dei vertici come una striscia di triangolo.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-119">Renders the vertices as a triangle strip.</span></span> <span data-ttu-id="9b8bd-120">Il flag per l'abbattimento delle backvisore viene automaticamente capovolto in triangoli uniformi.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-120">The backface-culling flag is automatically flipped on even-numbered triangles.</span></span>

</dd> <dt>

<span data-ttu-id="9b8bd-121"><span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**\_TRIANGLEFAN D3DPT**</span><span class="sxs-lookup"><span data-stu-id="9b8bd-121"><span id="D3DPT_TRIANGLEFAN"></span><span id="d3dpt_trianglefan"></span>**D3DPT\_TRIANGLEFAN**</span></span>
</dt> <dd>

<span data-ttu-id="9b8bd-122">Esegue il rendering dei vertici come ventola del triangolo.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-122">Renders the vertices as a triangle fan.</span></span>

</dd> <dt>

<span data-ttu-id="9b8bd-123"><span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9b8bd-123"><span id="D3DPT_FORCE_DWORD"></span><span id="d3dpt_force_dword"></span>**D3DPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="9b8bd-124">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-124">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="9b8bd-125">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-125">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="9b8bd-126">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-126">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b8bd-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b8bd-127">Remarks</span></span>

<span data-ttu-id="9b8bd-128">L'uso di [strisce triangolari](triangle-strips.md) o [ventilatori triangolari (Direct3D 9)](triangle-fans.md) è spesso più efficiente rispetto all'uso di elenchi di triangolo, perché i vertici sono duplicati.</span><span class="sxs-lookup"><span data-stu-id="9b8bd-128">Using [Triangle Strips](triangle-strips.md) or [Triangle Fans (Direct3D 9)](triangle-fans.md) is often more efficient than using triangle lists because fewer vertices are duplicated.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b8bd-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b8bd-129">Requirements</span></span>



| <span data-ttu-id="9b8bd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b8bd-130">Requirement</span></span> | <span data-ttu-id="9b8bd-131">Valore</span><span class="sxs-lookup"><span data-stu-id="9b8bd-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8bd-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b8bd-132">Header</span></span><br/> | <dl> <span data-ttu-id="9b8bd-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b8bd-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b8bd-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b8bd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b8bd-135">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="9b8bd-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="9b8bd-136">**IDirect3DDevice9::D rawIndexedPrimitive**</span><span class="sxs-lookup"><span data-stu-id="9b8bd-136">**IDirect3DDevice9::DrawIndexedPrimitive**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)
</dt> <dt>

[<span data-ttu-id="9b8bd-137">**IDirect3DDevice9::D rawIndexedPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="9b8bd-137">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)
</dt> <dt>

[<span data-ttu-id="9b8bd-138">**IDirect3DDevice9::D rawPrimitive**</span><span class="sxs-lookup"><span data-stu-id="9b8bd-138">**IDirect3DDevice9::DrawPrimitive**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)
</dt> <dt>

[<span data-ttu-id="9b8bd-139">**IDirect3DDevice9::D rawPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="9b8bd-139">**IDirect3DDevice9::DrawPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
</dt> </dl>

 

 
