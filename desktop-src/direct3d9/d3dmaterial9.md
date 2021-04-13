---
description: Specifica le proprietà del materiale.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: Struttura D3DMATERIAL9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIAL9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b9c3ad93fe2cb80fe758e2e66da37cce9d4267ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401977"
---
# <a name="d3dmaterial9-structure"></a><span data-ttu-id="939ab-103">Struttura D3DMATERIAL9</span><span class="sxs-lookup"><span data-stu-id="939ab-103">D3DMATERIAL9 structure</span></span>

<span data-ttu-id="939ab-104">Specifica le proprietà del materiale.</span><span class="sxs-lookup"><span data-stu-id="939ab-104">Specifies material properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="939ab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="939ab-105">Syntax</span></span>


```C++
typedef struct D3DMATERIAL9 {
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Ambient;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Emissive;
  float         Power;
} D3DMATERIAL9, *LPD3DMATERIAL9;
```



## <a name="members"></a><span data-ttu-id="939ab-106">Members</span><span class="sxs-lookup"><span data-stu-id="939ab-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="939ab-107">**Diffusa**</span><span class="sxs-lookup"><span data-stu-id="939ab-107">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="939ab-108">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="939ab-108">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="939ab-109">Valore che specifica il colore diffuso del materiale.</span><span class="sxs-lookup"><span data-stu-id="939ab-109">Value specifying the diffuse color of the material.</span></span> <span data-ttu-id="939ab-110">Vedere [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="939ab-110">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ab-111">**Di ambiente**</span><span class="sxs-lookup"><span data-stu-id="939ab-111">**Ambient**</span></span>
</dt> <dd>

<span data-ttu-id="939ab-112">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="939ab-112">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="939ab-113">Valore che specifica il colore di ambiente del materiale.</span><span class="sxs-lookup"><span data-stu-id="939ab-113">Value specifying the ambient color of the material.</span></span> <span data-ttu-id="939ab-114">Vedere [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="939ab-114">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ab-115">**Speculare**</span><span class="sxs-lookup"><span data-stu-id="939ab-115">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="939ab-116">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="939ab-116">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="939ab-117">Valore che specifica il colore speculare del materiale.</span><span class="sxs-lookup"><span data-stu-id="939ab-117">Value specifying the specular color of the material.</span></span> <span data-ttu-id="939ab-118">Vedere [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="939ab-118">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ab-119">**Emissiva**</span><span class="sxs-lookup"><span data-stu-id="939ab-119">**Emissive**</span></span>
</dt> <dd>

<span data-ttu-id="939ab-120">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="939ab-120">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="939ab-121">Valore che specifica il colore emissivo del materiale.</span><span class="sxs-lookup"><span data-stu-id="939ab-121">Value specifying the emissive color of the material.</span></span> <span data-ttu-id="939ab-122">Vedere [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="939ab-122">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="939ab-123">**Potere**</span><span class="sxs-lookup"><span data-stu-id="939ab-123">**Power**</span></span>
</dt> <dd>

<span data-ttu-id="939ab-124">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="939ab-124">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="939ab-125">Valore a virgola mobile che specifica l'intensità delle evidenziazioni speculari.</span><span class="sxs-lookup"><span data-stu-id="939ab-125">Floating-point value specifying the sharpness of specular highlights.</span></span> <span data-ttu-id="939ab-126">Maggiore è il valore, più nitida è l'evidenziazione.</span><span class="sxs-lookup"><span data-stu-id="939ab-126">The higher the value, the sharper the highlight.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="939ab-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="939ab-127">Remarks</span></span>

<span data-ttu-id="939ab-128">Per disattivare le evidenziazioni speculari, impostare D3DRS \_ SPECULARENABLE su **false** usando [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="939ab-128">To turn off specular highlights, set D3DRS\_SPECULARENABLE to **FALSE**, using [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span> <span data-ttu-id="939ab-129">Questa è l'opzione più rapida perché non verrà calcolata alcuna evidenziazione speculare.</span><span class="sxs-lookup"><span data-stu-id="939ab-129">This is the fastest option because no specular highlights will be calculated.</span></span>

<span data-ttu-id="939ab-130">Per ulteriori informazioni sull'utilizzo del motore di illuminazione per calcolare l'illuminazione speculare, vedere [illuminazione speculare (Direct3D 9)](specular-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="939ab-130">For more information about using the lighting engine to calculate specular lighting, see [Specular Lighting (Direct3D 9)](specular-lighting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="939ab-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="939ab-131">Requirements</span></span>



| <span data-ttu-id="939ab-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="939ab-132">Requirement</span></span> | <span data-ttu-id="939ab-133">Valore</span><span class="sxs-lookup"><span data-stu-id="939ab-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="939ab-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="939ab-134">Header</span></span><br/> | <dl> <span data-ttu-id="939ab-135"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="939ab-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="939ab-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="939ab-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="939ab-137">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="939ab-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="939ab-138">**IDirect3DDevice9:: getmaterial**</span><span class="sxs-lookup"><span data-stu-id="939ab-138">**IDirect3DDevice9::GetMaterial**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[<span data-ttu-id="939ab-139">**IDirect3DDevice9:: sematerial**</span><span class="sxs-lookup"><span data-stu-id="939ab-139">**IDirect3DDevice9::SetMaterial**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
