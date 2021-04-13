---
description: La semantica esegue il mapping di un parametro ai registri vertici o pixel shader. Possono anche essere stringhe descrittive facoltative associate a parametri non di registro.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: Struttura D3DXSEMANTIC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSEMANTIC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 08a30ac4d669beb5b93f2823219cb167d9e8d67f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401951"
---
# <a name="d3dxsemantic-structure"></a><span data-ttu-id="db4da-104">Struttura D3DXSEMANTIC</span><span class="sxs-lookup"><span data-stu-id="db4da-104">D3DXSEMANTIC structure</span></span>

<span data-ttu-id="db4da-105">La semantica esegue il mapping di un parametro ai registri vertici o pixel shader.</span><span class="sxs-lookup"><span data-stu-id="db4da-105">Semantics map a parameter to vertex or pixel shader registers.</span></span> <span data-ttu-id="db4da-106">Possono anche essere stringhe descrittive facoltative associate a parametri non di registro.</span><span class="sxs-lookup"><span data-stu-id="db4da-106">They can also be optional descriptive strings attached to non-register parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="db4da-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db4da-107">Syntax</span></span>


```C++
typedef struct D3DXSEMANTIC {
  UINT Usage;
  UINT UsageIndex;
} D3DXSEMANTIC, *LPD3DXSEMANTIC;
```



## <a name="members"></a><span data-ttu-id="db4da-108">Members</span><span class="sxs-lookup"><span data-stu-id="db4da-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="db4da-109">**Utilizzo**</span><span class="sxs-lookup"><span data-stu-id="db4da-109">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="db4da-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db4da-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="db4da-111">Opzioni che identificano la modalità di utilizzo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="db4da-111">Options that identify how resources are used.</span></span> <span data-ttu-id="db4da-112">Vedere [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="db4da-112">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="db4da-113">**UsageIndex**</span><span class="sxs-lookup"><span data-stu-id="db4da-113">**UsageIndex**</span></span>
</dt> <dd>

<span data-ttu-id="db4da-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db4da-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="db4da-115">Opzioni che modificano il modo in cui viene interpretato l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="db4da-115">Options that modify how the usage is interpreted.</span></span> <span data-ttu-id="db4da-116">L'utilizzo e l'indice di utilizzo costituiscono una dichiarazione di vertice.</span><span class="sxs-lookup"><span data-stu-id="db4da-116">The usage and usage index make up a vertex declaration.</span></span> <span data-ttu-id="db4da-117">Vedere [dichiarazione vertici (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="db4da-117">See [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db4da-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="db4da-118">Remarks</span></span>

<span data-ttu-id="db4da-119">La semantica è obbligatoria per i registri Vertex e pixel shader, di input e di output.</span><span class="sxs-lookup"><span data-stu-id="db4da-119">Semantics are required for vertex and pixel shader, input and output registers.</span></span>

## <a name="requirements"></a><span data-ttu-id="db4da-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db4da-120">Requirements</span></span>



| <span data-ttu-id="db4da-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="db4da-121">Requirement</span></span> | <span data-ttu-id="db4da-122">Valore</span><span class="sxs-lookup"><span data-stu-id="db4da-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="db4da-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db4da-123">Header</span></span><br/> | <dl> <span data-ttu-id="db4da-124"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="db4da-124"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db4da-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db4da-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db4da-126">Strutture degli effetti</span><span class="sxs-lookup"><span data-stu-id="db4da-126">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
