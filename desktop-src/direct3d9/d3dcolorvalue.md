---
description: 'Struttura D3DCOLORVALUE (D3D9Types.h): descrive i valori dei colori.'
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: Struttura D3DCOLORVALUE (D3D9Types.h)
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
ms.openlocfilehash: c9b55fbf718382e9dca7e3999cce0cabe895a261
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116059"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a><span data-ttu-id="d07c4-103">Struttura D3DCOLORVALUE (D3D9Types.h)</span><span class="sxs-lookup"><span data-stu-id="d07c4-103">D3DCOLORVALUE structure (D3D9Types.h)</span></span>

<span data-ttu-id="d07c4-104">Descrive i valori dei colori.</span><span class="sxs-lookup"><span data-stu-id="d07c4-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d07c4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d07c4-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="d07c4-106">Members</span><span class="sxs-lookup"><span data-stu-id="d07c4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d07c4-107">**r**</span><span class="sxs-lookup"><span data-stu-id="d07c4-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="d07c4-108">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="d07c4-108">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="d07c4-109">Valore a virgola mobile che specifica il componente rosso di un colore.</span><span class="sxs-lookup"><span data-stu-id="d07c4-109">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="d07c4-110">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="d07c4-110">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="d07c4-111">Il valore 0,0 indica l'assenza completa del componente rosso, mentre il valore 1,0 indica che il rosso è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="d07c4-111">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="d07c4-112">**G**</span><span class="sxs-lookup"><span data-stu-id="d07c4-112">**g**</span></span>
</dt> <dd>

<span data-ttu-id="d07c4-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="d07c4-113">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="d07c4-114">Valore a virgola mobile che specifica il componente verde di un colore.</span><span class="sxs-lookup"><span data-stu-id="d07c4-114">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="d07c4-115">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="d07c4-115">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="d07c4-116">Il valore 0,0 indica l'assenza completa del componente verde, mentre il valore 1,0 indica che il verde è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="d07c4-116">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="d07c4-117">**b**</span><span class="sxs-lookup"><span data-stu-id="d07c4-117">**b**</span></span>
</dt> <dd>

<span data-ttu-id="d07c4-118">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="d07c4-118">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="d07c4-119">Valore a virgola mobile che specifica il componente blu di un colore.</span><span class="sxs-lookup"><span data-stu-id="d07c4-119">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="d07c4-120">Questo valore è in genere compreso nell'intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="d07c4-120">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="d07c4-121">Il valore 0,0 indica l'assenza completa del componente blu, mentre il valore 1,0 indica che il blu è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="d07c4-121">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="d07c4-122">**Un**</span><span class="sxs-lookup"><span data-stu-id="d07c4-122">**a**</span></span>
</dt> <dd>

<span data-ttu-id="d07c4-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="d07c4-123">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="d07c4-124">Valore a virgola mobile che specifica il componente alfa di un colore.</span><span class="sxs-lookup"><span data-stu-id="d07c4-124">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="d07c4-125">Questo valore è in genere compreso nell'intervallo da 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="d07c4-125">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="d07c4-126">Un valore pari a 0,0 indica completamente trasparente, mentre un valore pari a 1,0 indica che è completamente opaco.</span><span class="sxs-lookup"><span data-stu-id="d07c4-126">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d07c4-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="d07c4-127">Remarks</span></span>

<span data-ttu-id="d07c4-128">È possibile impostare i membri di questa struttura su valori esterni all'intervallo compreso tra 0 e 1 per implementare alcuni effetti insoliti.</span><span class="sxs-lookup"><span data-stu-id="d07c4-128">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="d07c4-129">I valori maggiori di 1 producono luci forti che tendono a evase una scena.</span><span class="sxs-lookup"><span data-stu-id="d07c4-129">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="d07c4-130">I valori negativi producono luci scuri che rimuovono effettivamente la luce da una scena.</span><span class="sxs-lookup"><span data-stu-id="d07c4-130">Negative values produce dark lights that actually remove light from a scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="d07c4-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d07c4-131">Requirements</span></span>



| <span data-ttu-id="d07c4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d07c4-132">Requirement</span></span> | <span data-ttu-id="d07c4-133">Valore</span><span class="sxs-lookup"><span data-stu-id="d07c4-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d07c4-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d07c4-134">Header</span></span><br/> | <dl> <span data-ttu-id="d07c4-135"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="d07c4-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d07c4-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d07c4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d07c4-137">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="d07c4-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




