---
description: Definisce un volume.
ms.assetid: 415a96bc-1621-4691-b87a-98ca22f0bf07
title: Struttura D3DBOX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 882f6aadf0d49284b30132d4f08a9c583e5c9d73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234967"
---
# <a name="d3dbox-structure"></a><span data-ttu-id="9bcb5-103">Struttura D3DBOX</span><span class="sxs-lookup"><span data-stu-id="9bcb5-103">D3DBOX structure</span></span>

<span data-ttu-id="9bcb5-104">Definisce un volume.</span><span class="sxs-lookup"><span data-stu-id="9bcb5-104">Defines a volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bcb5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9bcb5-105">Syntax</span></span>


```C++
typedef struct D3DBOX {
  UINT Left;
  UINT Top;
  UINT Right;
  UINT Bottom;
  UINT Front;
  UINT Back;
} D3DBOX, *LPD3DBOX;
```



## <a name="members"></a><span data-ttu-id="9bcb5-106">Members</span><span class="sxs-lookup"><span data-stu-id="9bcb5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9bcb5-107">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="9bcb5-107">**Left**</span></span>
</dt> <dd>

<span data-ttu-id="9bcb5-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bcb5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9bcb5-109">Posizione del lato sinistro della casella sull'asse x.</span><span class="sxs-lookup"><span data-stu-id="9bcb5-109">Position of the left side of the box on the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9bcb5-110">**Top**</span><span class="sxs-lookup"><span data-stu-id="9bcb5-110">**Top**</span></span>
</dt> <dd>

<span data-ttu-id="9bcb5-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bcb5-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9bcb5-112">Posizione della parte superiore della casella sull'asse y.</span><span class="sxs-lookup"><span data-stu-id="9bcb5-112">Position of the top of the box on the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9bcb5-113">**Ok**</span><span class="sxs-lookup"><span data-stu-id="9bcb5-113">**Right**</span></span>
</dt> <dd>

<span data-ttu-id="9bcb5-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bcb5-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9bcb5-115">Posizione del lato destro della casella sull'asse x.</span><span class="sxs-lookup"><span data-stu-id="9bcb5-115">Position of the right side of the box on the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9bcb5-116">**Ultimo**</span><span class="sxs-lookup"><span data-stu-id="9bcb5-116">**Bottom**</span></span>
</dt> <dd>

<span data-ttu-id="9bcb5-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bcb5-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9bcb5-118">Posizione della parte inferiore della casella sull'asse y.</span><span class="sxs-lookup"><span data-stu-id="9bcb5-118">Position of the bottom of the box on the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9bcb5-119">**Front**</span><span class="sxs-lookup"><span data-stu-id="9bcb5-119">**Front**</span></span>
</dt> <dd>

<span data-ttu-id="9bcb5-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bcb5-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9bcb5-121">Posizione della parte anteriore della casella sull'asse z.</span><span class="sxs-lookup"><span data-stu-id="9bcb5-121">Position of the front of the box on the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9bcb5-122">**Back**</span><span class="sxs-lookup"><span data-stu-id="9bcb5-122">**Back**</span></span>
</dt> <dd>

<span data-ttu-id="9bcb5-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bcb5-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9bcb5-124">Posizione della parte posteriore della casella sull'asse z.</span><span class="sxs-lookup"><span data-stu-id="9bcb5-124">Position of the back of the box on the z-axis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bcb5-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bcb5-125">Remarks</span></span>

<span data-ttu-id="9bcb5-126">**D3DBOX** include i bordi sinistro, superiore e anteriore; Tuttavia, i bordi destro, inferiore e indietro non sono inclusi.</span><span class="sxs-lookup"><span data-stu-id="9bcb5-126">**D3DBOX** includes the left, top, and front edges; however, the right, bottom, and back edges are not included.</span></span> <span data-ttu-id="9bcb5-127">Ad esempio, una casella di 100 unità di misura e inizia da 0 (quindi, inclusi i punti fino a 99) viene espressa con un valore pari a 0 per il membro sinistro e il valore 100 per il membro destro.</span><span class="sxs-lookup"><span data-stu-id="9bcb5-127">For example, a box that is 100 units wide and begins at 0 (thus, including the points up to and including 99) would be expressed with a value of 0 for the Left member and a value of 100 for the Right member.</span></span> <span data-ttu-id="9bcb5-128">Si noti che il valore 99 non viene utilizzato per il membro destro.</span><span class="sxs-lookup"><span data-stu-id="9bcb5-128">Note that a value of 99 is not used for the Right member.</span></span>

<span data-ttu-id="9bcb5-129">Le restrizioni sull'ordinamento laterale osservato per **D3DBOX** sono da sinistra a destra, dall'alto verso il basso e viceversa.</span><span class="sxs-lookup"><span data-stu-id="9bcb5-129">The restrictions on side ordering observed for **D3DBOX** are left to right, top to bottom, and front to back.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bcb5-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bcb5-130">Requirements</span></span>



| <span data-ttu-id="9bcb5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bcb5-131">Requirement</span></span> | <span data-ttu-id="9bcb5-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9bcb5-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcb5-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bcb5-133">Header</span></span><br/> | <dl> <span data-ttu-id="9bcb5-134"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bcb5-134"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bcb5-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bcb5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bcb5-136">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="9bcb5-136">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
