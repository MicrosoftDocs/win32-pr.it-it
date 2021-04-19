---
description: Tipi di patch mesh.
ms.assetid: 229d01b2-781c-48a8-93f2-9dd9dbd67f3e
title: Enumerazione D3DXPATCHMESHTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHMESHTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: d6a663e983b339d79ec89bf1b4ddfe7b4eaa9f1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322112"
---
# <a name="d3dxpatchmeshtype-enumeration"></a><span data-ttu-id="deb99-103">Enumerazione D3DXPATCHMESHTYPE</span><span class="sxs-lookup"><span data-stu-id="deb99-103">D3DXPATCHMESHTYPE enumeration</span></span>

<span data-ttu-id="deb99-104">Tipi di patch mesh.</span><span class="sxs-lookup"><span data-stu-id="deb99-104">Mesh patch types.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb99-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="deb99-105">Syntax</span></span>


```C++
typedef enum D3DXPATCHMESHTYPE { 
  D3DXPATCHMESH_RECT         = 0x001,
  D3DXPATCHMESH_TRI          = 0x002,
  D3DXPATCHMESH_NPATCH       = 0x003,
  D3DXPATCHMESH_FORCE_DWORD  = 0x7fffffff
} D3DXPATCHMESHTYPE, *LPD3DXPATCHMESHTYPE;
```



## <a name="constants"></a><span data-ttu-id="deb99-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="deb99-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="deb99-107"><span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="deb99-107"><span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH\_RECT**</span></span>
</dt> <dd>

<span data-ttu-id="deb99-108">Tipo di mesh patch rettangolo.</span><span class="sxs-lookup"><span data-stu-id="deb99-108">Rectangle patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="deb99-109"><span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH \_ Tri**</span><span class="sxs-lookup"><span data-stu-id="deb99-109"><span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH\_TRI**</span></span>
</dt> <dd>

<span data-ttu-id="deb99-110">Tipo mesh patch del triangolo.</span><span class="sxs-lookup"><span data-stu-id="deb99-110">Triangle patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="deb99-111"><span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**\_NPATCH D3DXPATCHMESH**</span><span class="sxs-lookup"><span data-stu-id="deb99-111"><span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH\_NPATCH**</span></span>
</dt> <dd>

<span data-ttu-id="deb99-112">N: tipo di mesh della patch.</span><span class="sxs-lookup"><span data-stu-id="deb99-112">N-patch mesh type.</span></span>

</dd> <dt>

<span data-ttu-id="deb99-113"><span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="deb99-113"><span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="deb99-114">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="deb99-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="deb99-115">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="deb99-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="deb99-116">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="deb99-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="deb99-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="deb99-117">Remarks</span></span>

<span data-ttu-id="deb99-118">Le patch del triangolo hanno tre lati e sono descritte in [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="deb99-118">Triangle patches have three sides and are described in [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span> <span data-ttu-id="deb99-119">Le patch rettangolari sono a quattro lati e sono descritte in [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="deb99-119">Rectangle patches are four-sided and are described in [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="deb99-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="deb99-120">Requirements</span></span>



| <span data-ttu-id="deb99-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="deb99-121">Requirement</span></span> | <span data-ttu-id="deb99-122">Valore</span><span class="sxs-lookup"><span data-stu-id="deb99-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="deb99-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="deb99-123">Header</span></span><br/> | <dl> <span data-ttu-id="deb99-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="deb99-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deb99-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="deb99-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deb99-126">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="deb99-126">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="deb99-127">Uso di Higher-Order primitive (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="deb99-127">Using Higher-Order Primitives (Direct3D 9)</span></span>](using-higher-order-primitives.md)
</dt> </dl>

 

 




