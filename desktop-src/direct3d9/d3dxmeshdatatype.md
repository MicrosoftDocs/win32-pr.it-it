---
description: Definisce il tipo di dati mesh presenti in D3DXMESHDATA.
ms.assetid: e5324f85-17cc-46a7-886a-c8f3464baade
title: Enumerazione D3DXMESHDATATYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATATYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 9dea67984992e4bb26cd9e2613013169b1ff097d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322632"
---
# <a name="d3dxmeshdatatype-enumeration"></a><span data-ttu-id="a37dc-103">Enumerazione D3DXMESHDATATYPE</span><span class="sxs-lookup"><span data-stu-id="a37dc-103">D3DXMESHDATATYPE enumeration</span></span>

<span data-ttu-id="a37dc-104">Definisce il tipo di dati mesh presenti in [**D3DXMESHDATA**](d3dxmeshdata.md).</span><span class="sxs-lookup"><span data-stu-id="a37dc-104">Defines the type of mesh data present in [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a37dc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a37dc-105">Syntax</span></span>


```C++
typedef enum D3DXMESHDATATYPE { 
  D3DXMESHTYPE_MESH         = 0x001,
  D3DXMESHTYPE_PATCHMESH    = 0x003,
  D3DXMESHTYPE_FORCE_DWORD  = 0x7fffffff
} D3DXMESHDATATYPE, *LPD3DXMESHDATATYPE;
```



## <a name="constants"></a><span data-ttu-id="a37dc-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="a37dc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a37dc-107"><span id="D3DXMESHTYPE_MESH"></span><span id="d3dxmeshtype_mesh"></span>**\_Mesh D3DXMESHTYPE**</span><span class="sxs-lookup"><span data-stu-id="a37dc-107"><span id="D3DXMESHTYPE_MESH"></span><span id="d3dxmeshtype_mesh"></span>**D3DXMESHTYPE\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="a37dc-108">Il tipo di dati è una mesh.</span><span class="sxs-lookup"><span data-stu-id="a37dc-108">The data type is a mesh.</span></span> <span data-ttu-id="a37dc-109">Vedere [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="a37dc-109">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="a37dc-110"><span id="D3DXMESHTYPE_PATCHMESH"></span><span id="d3dxmeshtype_patchmesh"></span>**\_PATCHMESH D3DXMESHTYPE**</span><span class="sxs-lookup"><span data-stu-id="a37dc-110"><span id="D3DXMESHTYPE_PATCHMESH"></span><span id="d3dxmeshtype_patchmesh"></span>**D3DXMESHTYPE\_PATCHMESH**</span></span>
</dt> <dd>

<span data-ttu-id="a37dc-111">Il tipo di dati è una mesh patch.</span><span class="sxs-lookup"><span data-stu-id="a37dc-111">The data type is a patch mesh.</span></span> <span data-ttu-id="a37dc-112">Vedere [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span><span class="sxs-lookup"><span data-stu-id="a37dc-112">See [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="a37dc-113"><span id="D3DXMESHTYPE_FORCE_DWORD"></span><span id="d3dxmeshtype_force_dword"></span>**D3DXMESHTYPE \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a37dc-113"><span id="D3DXMESHTYPE_FORCE_DWORD"></span><span id="d3dxmeshtype_force_dword"></span>**D3DXMESHTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="a37dc-114">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a37dc-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="a37dc-115">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="a37dc-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="a37dc-116">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="a37dc-116">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a37dc-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a37dc-117">Requirements</span></span>



| <span data-ttu-id="a37dc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a37dc-118">Requirement</span></span> | <span data-ttu-id="a37dc-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a37dc-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a37dc-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a37dc-120">Header</span></span><br/> | <dl> <span data-ttu-id="a37dc-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a37dc-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a37dc-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a37dc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a37dc-123">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="a37dc-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="a37dc-124">**D3DXMESHDATA**</span><span class="sxs-lookup"><span data-stu-id="a37dc-124">**D3DXMESHDATA**</span></span>](d3dxmeshdata.md)
</dt> </dl>

 

 




