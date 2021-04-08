---
description: Statistiche sull'utilizzo delle risorse.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: Struttura D3DDEVINFO_ResourceManager (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_ResourceManager
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bf4e84fa247ca5b2603547efef73ea6b9cbe0aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761968"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a><span data-ttu-id="f235a-103">D3DDEVINFO \_ struttura ResourceManager</span><span class="sxs-lookup"><span data-stu-id="f235a-103">D3DDEVINFO\_ResourceManager structure</span></span>

<span data-ttu-id="f235a-104">Statistiche sull'utilizzo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="f235a-104">Resource usage statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="f235a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f235a-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_ResourceManager {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_ResourceManager, *LPD3DDEVINFO_ResourceManager;
```



## <a name="members"></a><span data-ttu-id="f235a-106">Members</span><span class="sxs-lookup"><span data-stu-id="f235a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f235a-107">**Statistiche**</span><span class="sxs-lookup"><span data-stu-id="f235a-107">**stats**</span></span>
</dt> <dd>

<span data-ttu-id="f235a-108">Tipo: **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**</span><span class="sxs-lookup"><span data-stu-id="f235a-108">Type: **[**D3DRESOURCESTATS**](d3dresourcestats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f235a-109">Matrice di elementi Statistics delle risorse.</span><span class="sxs-lookup"><span data-stu-id="f235a-109">Array of resource statistics elements.</span></span> <span data-ttu-id="f235a-110">Vedere [**D3DRESOURCESTATS**](d3dresourcestats.md).</span><span class="sxs-lookup"><span data-stu-id="f235a-110">See [**D3DRESOURCESTATS**](d3dresourcestats.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f235a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f235a-111">Remarks</span></span>

<span data-ttu-id="f235a-112">D3DRTYPECOUNT fa riferimento al numero di enumerazioni in [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span><span class="sxs-lookup"><span data-stu-id="f235a-112">D3DRTYPECOUNT refers to the number of enumerations in [**D3DRESOURCETYPE**](./d3dresourcetype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f235a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f235a-113">Requirements</span></span>



| <span data-ttu-id="f235a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f235a-114">Requirement</span></span> | <span data-ttu-id="f235a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f235a-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f235a-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f235a-116">Header</span></span><br/> | <dl> <span data-ttu-id="f235a-117"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f235a-117"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f235a-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f235a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f235a-119">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="f235a-119">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
