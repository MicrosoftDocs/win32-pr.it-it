---
description: Questa costante è il numero massimo di dichiaratori di vertici per una mesh.
ms.assetid: 234e99a2-1907-4065-b03b-fb9e8d6812ab
title: Enumerazione MAX_FVF_DECL_SIZE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MAX_FVF_DECL_SIZE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7204308e6b9355b416218f31af301b5ea6d8fff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322526"
---
# <a name="max_fvf_decl_size-enumeration"></a><span data-ttu-id="d5221-103">\_Enumerazione max FVF \_ decl \_ size</span><span class="sxs-lookup"><span data-stu-id="d5221-103">MAX\_FVF\_DECL\_SIZE enumeration</span></span>

<span data-ttu-id="d5221-104">Questa costante è il numero massimo di dichiaratori di vertici per una mesh.</span><span class="sxs-lookup"><span data-stu-id="d5221-104">This constant is the maximum number of vertex declarators for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5221-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5221-105">Syntax</span></span>


```C++
typedef enum  { 
  MAX_FVF_DECL_SIZE  = MAXD3DDECLLENGTH + 1
} MAX_FVF_DECL_SIZE;
```



## <a name="constants"></a><span data-ttu-id="d5221-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="d5221-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d5221-107"><span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**dimensioni MASSIMe \_ \_ decl FVF \_**</span><span class="sxs-lookup"><span data-stu-id="d5221-107"><span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**MAX\_FVF\_DECL\_SIZE**</span></span>
</dt> <dd>

<span data-ttu-id="d5221-108">Numero massimo di elementi nella dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="d5221-108">The maximum number of elements in the vertex declaration.</span></span> <span data-ttu-id="d5221-109">Il (+ 1) aggiuntivo è per [**D3DDECL \_ end**](d3ddecl-end.md).</span><span class="sxs-lookup"><span data-stu-id="d5221-109">The additional (+1) is for [**D3DDECL\_END**](d3ddecl-end.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5221-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5221-110">Remarks</span></span>

<span data-ttu-id="d5221-111">MAXD3DDECLLENGTH è definito come massimo 64 (vedere d3d9types. h).</span><span class="sxs-lookup"><span data-stu-id="d5221-111">MAXD3DDECLLENGTH is defined as a maximum of 64 (see d3d9types.h).</span></span> <span data-ttu-id="d5221-112">Non include l'elemento del vertice del marcatore "end".</span><span class="sxs-lookup"><span data-stu-id="d5221-112">This does not include the "end" marker vertex element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5221-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5221-113">Requirements</span></span>



| <span data-ttu-id="d5221-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5221-114">Requirement</span></span> | <span data-ttu-id="d5221-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d5221-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5221-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5221-116">Header</span></span><br/> | <dl> <span data-ttu-id="d5221-117"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5221-117"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5221-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5221-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5221-119">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="d5221-119">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="d5221-120">**ID3DXBaseMesh**</span><span class="sxs-lookup"><span data-stu-id="d5221-120">**ID3DXBaseMesh**</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="d5221-121">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="d5221-121">**GetDeclaration**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexdeclaration9-getdeclaration)
</dt> <dt>

[<span data-ttu-id="d5221-122">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="d5221-122">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> <dt>

[<span data-ttu-id="d5221-123">**ID3DXSkinInfo**</span><span class="sxs-lookup"><span data-stu-id="d5221-123">**ID3DXSkinInfo**</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
