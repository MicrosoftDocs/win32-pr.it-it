---
description: Specifica i tipi di modalità di visualizzazione da filtrare.
ms.assetid: 4a03d0f0-dec5-4209-8c99-b58cc13064f5
title: Struttura D3DDISPLAYMODEFILTER (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEFILTER
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b60c283405bead7b2618b91d6de76158841ff27f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354464"
---
# <a name="d3ddisplaymodefilter-structure"></a><span data-ttu-id="411c8-103">Struttura D3DDISPLAYMODEFILTER</span><span class="sxs-lookup"><span data-stu-id="411c8-103">D3DDISPLAYMODEFILTER structure</span></span>

<span data-ttu-id="411c8-104">Specifica i tipi di modalità di visualizzazione da filtrare.</span><span class="sxs-lookup"><span data-stu-id="411c8-104">Specifies types of display modes to filter out.</span></span>

## <a name="syntax"></a><span data-ttu-id="411c8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="411c8-105">Syntax</span></span>


```C++
typedef struct {
  UINT                Size;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEFILTER;
```



## <a name="members"></a><span data-ttu-id="411c8-106">Members</span><span class="sxs-lookup"><span data-stu-id="411c8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="411c8-107">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="411c8-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="411c8-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="411c8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="411c8-109">Dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="411c8-109">The size of this structure.</span></span> <span data-ttu-id="411c8-110">Questo deve essere sempre impostato su sizeof (D3DDISPLAYMODEFILTER).</span><span class="sxs-lookup"><span data-stu-id="411c8-110">This should always be set to sizeof(D3DDISPLAYMODEFILTER).</span></span>

</dd> <dt>

<span data-ttu-id="411c8-111">**Formato**</span><span class="sxs-lookup"><span data-stu-id="411c8-111">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="411c8-112">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="411c8-112">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="411c8-113">Formato della modalità di visualizzazione da filtrare. Vedere [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="411c8-113">The display mode format to filter out. See [D3DFORMAT](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="411c8-114">**ScanLineOrdering**</span><span class="sxs-lookup"><span data-stu-id="411c8-114">**ScanLineOrdering**</span></span>
</dt> <dd>

<span data-ttu-id="411c8-115">Tipo: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span><span class="sxs-lookup"><span data-stu-id="411c8-115">Type: **[**D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span></span>

</dd> <dd>

<span data-ttu-id="411c8-116">Indica se l'ordinamento scanline è interlacciato o progressivo.</span><span class="sxs-lookup"><span data-stu-id="411c8-116">Whether the scanline ordering is interlaced or progressive.</span></span> <span data-ttu-id="411c8-117">Vedere [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span><span class="sxs-lookup"><span data-stu-id="411c8-117">See [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="411c8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="411c8-118">Requirements</span></span>



| <span data-ttu-id="411c8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="411c8-119">Requirement</span></span> | <span data-ttu-id="411c8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="411c8-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="411c8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="411c8-121">Header</span></span><br/> | <dl> <span data-ttu-id="411c8-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="411c8-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="411c8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="411c8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="411c8-124">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="411c8-124">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
