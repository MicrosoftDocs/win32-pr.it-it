---
description: Definisce un intervallo.
ms.assetid: 28e8c478-f6ce-4f75-95c6-ea2d08424238
title: Struttura D3DRANGE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRANGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 15ff267528ddfd12f8da77921e2edc2d836e1a39
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322917"
---
# <a name="d3drange-structure"></a><span data-ttu-id="6094c-103">Struttura D3DRANGE</span><span class="sxs-lookup"><span data-stu-id="6094c-103">D3DRANGE structure</span></span>

<span data-ttu-id="6094c-104">Definisce un intervallo.</span><span class="sxs-lookup"><span data-stu-id="6094c-104">Defines a range.</span></span>

## <a name="syntax"></a><span data-ttu-id="6094c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6094c-105">Syntax</span></span>


```C++
typedef struct D3DRANGE {
  UINT Offset;
  UINT Size;
} D3DRANGE, *LPD3DRANGE;
```



## <a name="members"></a><span data-ttu-id="6094c-106">Members</span><span class="sxs-lookup"><span data-stu-id="6094c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6094c-107">**Offset**</span><span class="sxs-lookup"><span data-stu-id="6094c-107">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="6094c-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6094c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6094c-109">Offset, in byte.</span><span class="sxs-lookup"><span data-stu-id="6094c-109">Offset, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6094c-110">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="6094c-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="6094c-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6094c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6094c-112">Dimensioni in byte.</span><span class="sxs-lookup"><span data-stu-id="6094c-112">Size, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6094c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6094c-113">Requirements</span></span>



| <span data-ttu-id="6094c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6094c-114">Requirement</span></span> | <span data-ttu-id="6094c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6094c-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6094c-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6094c-116">Header</span></span><br/> | <dl> <span data-ttu-id="6094c-117"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6094c-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6094c-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6094c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6094c-119">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="6094c-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
