---
description: 'Struttura D3DXPLANE (D3dx9math.h): descrive un piano.'
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: Struttura D3DXPLANE (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 3df0c94dbd49cf38d9230a2c5392df8497c64761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115719"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a><span data-ttu-id="d04f0-103">Struttura D3DXPLANE (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="d04f0-103">D3DXPLANE structure (D3dx9math.h)</span></span>

<span data-ttu-id="d04f0-104">Descrive un piano.</span><span class="sxs-lookup"><span data-stu-id="d04f0-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="d04f0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d04f0-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="d04f0-106">Members</span><span class="sxs-lookup"><span data-stu-id="d04f0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d04f0-107">**Un**</span><span class="sxs-lookup"><span data-stu-id="d04f0-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="d04f0-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d04f0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d04f0-109">Coefficiente del piano di ritaglio nell'equazione del piano generale.</span><span class="sxs-lookup"><span data-stu-id="d04f0-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="d04f0-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d04f0-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d04f0-111">**b**</span><span class="sxs-lookup"><span data-stu-id="d04f0-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="d04f0-112">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d04f0-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d04f0-113">Coefficiente b del piano di ritaglio nell'equazione del piano generale.</span><span class="sxs-lookup"><span data-stu-id="d04f0-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="d04f0-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d04f0-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d04f0-115">**c**</span><span class="sxs-lookup"><span data-stu-id="d04f0-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="d04f0-116">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d04f0-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d04f0-117">Coefficiente c del piano di ritaglio nell'equazione del piano generale.</span><span class="sxs-lookup"><span data-stu-id="d04f0-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="d04f0-118">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d04f0-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d04f0-119">**d**</span><span class="sxs-lookup"><span data-stu-id="d04f0-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="d04f0-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d04f0-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d04f0-121">Coefficiente d del piano di ritaglio nell'equazione del piano generale.</span><span class="sxs-lookup"><span data-stu-id="d04f0-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="d04f0-122">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d04f0-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d04f0-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d04f0-123">Remarks</span></span>

<span data-ttu-id="d04f0-124">I membri della struttura **D3DXPLANE** hanno la forma dell'equazione del piano generale.</span><span class="sxs-lookup"><span data-stu-id="d04f0-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="d04f0-125">Rientrano nell'equazione del piano generale in **modo** che x + **b** y + **c** z + **d** w = 0.</span><span class="sxs-lookup"><span data-stu-id="d04f0-125">They fit into the general plane equation so that **a** x + **b** y + **c** z + **d** w = 0.</span></span>

<span data-ttu-id="d04f0-126">I programmatori C++ possono sfruttare l'overload degli operatori e il cast dei tipi con le estensioni [**D3DXPLANE**](d3dxplane-extensions.md) che implementano costruttori di overload e operatori di assegnazione, unario e binario (inclusa l'uguaglianza).</span><span class="sxs-lookup"><span data-stu-id="d04f0-126">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXPLANE Extensions**](d3dxplane-extensions.md) which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="d04f0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d04f0-127">Requirements</span></span>



| <span data-ttu-id="d04f0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d04f0-128">Requirement</span></span> | <span data-ttu-id="d04f0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d04f0-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d04f0-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d04f0-130">Header</span></span><br/> | <dl> <span data-ttu-id="d04f0-131"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="d04f0-131"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d04f0-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d04f0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d04f0-133">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="d04f0-133">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
