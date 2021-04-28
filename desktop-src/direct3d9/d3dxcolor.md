---
description: 'Struttura D3DXCOLOR (D3dx9math.h): descrive i valori dei colori.'
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: Struttura D3DXCOLOR (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 58b02abc49b695169674a2579b73dc2359801a73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115929"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a><span data-ttu-id="80a84-103">Struttura D3DXCOLOR (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="80a84-103">D3DXCOLOR structure (D3dx9math.h)</span></span>

<span data-ttu-id="80a84-104">Descrive i valori dei colori.</span><span class="sxs-lookup"><span data-stu-id="80a84-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="80a84-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80a84-105">Syntax</span></span>


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a><span data-ttu-id="80a84-106">Members</span><span class="sxs-lookup"><span data-stu-id="80a84-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="80a84-107">**r**</span><span class="sxs-lookup"><span data-stu-id="80a84-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="80a84-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80a84-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="80a84-109">Componente rosso del colore.</span><span class="sxs-lookup"><span data-stu-id="80a84-109">Red component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="80a84-110">**G**</span><span class="sxs-lookup"><span data-stu-id="80a84-110">**g**</span></span>
</dt> <dd>

<span data-ttu-id="80a84-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80a84-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="80a84-112">Componente verde del colore.</span><span class="sxs-lookup"><span data-stu-id="80a84-112">Green component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="80a84-113">**b**</span><span class="sxs-lookup"><span data-stu-id="80a84-113">**b**</span></span>
</dt> <dd>

<span data-ttu-id="80a84-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80a84-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="80a84-115">Componente blu del colore.</span><span class="sxs-lookup"><span data-stu-id="80a84-115">Blue component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="80a84-116">**Un**</span><span class="sxs-lookup"><span data-stu-id="80a84-116">**a**</span></span>
</dt> <dd>

<span data-ttu-id="80a84-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80a84-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="80a84-118">Componente alfa del colore.</span><span class="sxs-lookup"><span data-stu-id="80a84-118">Alpha component of the color.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80a84-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="80a84-119">Remarks</span></span>

<span data-ttu-id="80a84-120">I programmatori C++ possono sfruttare l'overload degli operatori e il cast dei tipi con le estensioni [**D3DXCOLOR**](d3dxcolor-extensions.md), che implementano costruttori di overload, nonché operatori di assegnazione, unario e binario (inclusa l'uguaglianza).</span><span class="sxs-lookup"><span data-stu-id="80a84-120">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXCOLOR Extensions**](d3dxcolor-extensions.md), which implement overloaded constructors, as well as assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="80a84-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80a84-121">Requirements</span></span>



| <span data-ttu-id="80a84-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="80a84-122">Requirement</span></span> | <span data-ttu-id="80a84-123">Valore</span><span class="sxs-lookup"><span data-stu-id="80a84-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80a84-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80a84-124">Header</span></span><br/> | <dl> <span data-ttu-id="80a84-125"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="80a84-125"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80a84-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80a84-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a84-127">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="80a84-127">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
