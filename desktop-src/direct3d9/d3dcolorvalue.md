---
description: Descrive i valori dei colori.
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: Struttura D3DCOLORVALUE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1fe2f187921749207bbbf51d7fcfd75357a70858
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354409"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a><span data-ttu-id="a1647-103">Struttura D3DCOLORVALUE (D3D9Types. h)</span><span class="sxs-lookup"><span data-stu-id="a1647-103">D3DCOLORVALUE structure (D3D9Types.h)</span></span>

<span data-ttu-id="a1647-104">Descrive i valori dei colori.</span><span class="sxs-lookup"><span data-stu-id="a1647-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1647-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1647-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="a1647-106">Members</span><span class="sxs-lookup"><span data-stu-id="a1647-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1647-107">**r**</span><span class="sxs-lookup"><span data-stu-id="a1647-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="a1647-108">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="a1647-108">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="a1647-109">Valore a virgola mobile che specifica il componente rosso di un colore.</span><span class="sxs-lookup"><span data-stu-id="a1647-109">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="a1647-110">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="a1647-110">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="a1647-111">Il valore 0,0 indica l'assenza completa del componente rosso, mentre un valore pari a 1,0 indica che il colore rosso è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="a1647-111">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="a1647-112">**g**</span><span class="sxs-lookup"><span data-stu-id="a1647-112">**g**</span></span>
</dt> <dd>

<span data-ttu-id="a1647-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="a1647-113">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="a1647-114">Valore a virgola mobile che specifica il componente verde di un colore.</span><span class="sxs-lookup"><span data-stu-id="a1647-114">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="a1647-115">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="a1647-115">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="a1647-116">Il valore 0,0 indica l'assenza completa del componente verde, mentre un valore pari a 1,0 indica che il verde è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="a1647-116">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="a1647-117">**b**</span><span class="sxs-lookup"><span data-stu-id="a1647-117">**b**</span></span>
</dt> <dd>

<span data-ttu-id="a1647-118">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="a1647-118">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="a1647-119">Valore a virgola mobile che specifica il componente blu di un colore.</span><span class="sxs-lookup"><span data-stu-id="a1647-119">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="a1647-120">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="a1647-120">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="a1647-121">Il valore 0,0 indica l'assenza completa del componente blu, mentre il valore 1,0 indica che il blu è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="a1647-121">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="a1647-122">**un**</span><span class="sxs-lookup"><span data-stu-id="a1647-122">**a**</span></span>
</dt> <dd>

<span data-ttu-id="a1647-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="a1647-123">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="a1647-124">Valore a virgola mobile che specifica il componente alfa di un colore.</span><span class="sxs-lookup"><span data-stu-id="a1647-124">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="a1647-125">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="a1647-125">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="a1647-126">Il valore 0,0 indica completamente trasparente, mentre un valore pari a 1,0 indica una piena opacità.</span><span class="sxs-lookup"><span data-stu-id="a1647-126">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1647-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1647-127">Remarks</span></span>

<span data-ttu-id="a1647-128">È possibile impostare i membri di questa struttura su valori non compresi nell'intervallo compreso tra 0 e 1 per implementare alcuni effetti insoliti.</span><span class="sxs-lookup"><span data-stu-id="a1647-128">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="a1647-129">I valori maggiori di 1 producono luci forti che tendono a pulire una scena.</span><span class="sxs-lookup"><span data-stu-id="a1647-129">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="a1647-130">I valori negativi producono luci scure che effettivamente rimuovono la luce da una scena.</span><span class="sxs-lookup"><span data-stu-id="a1647-130">Negative values produce dark lights that actually remove light from a scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1647-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1647-131">Requirements</span></span>



| <span data-ttu-id="a1647-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1647-132">Requirement</span></span> | <span data-ttu-id="a1647-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a1647-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1647-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1647-134">Header</span></span><br/> | <dl> <span data-ttu-id="a1647-135"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1647-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1647-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1647-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1647-137">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="a1647-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




