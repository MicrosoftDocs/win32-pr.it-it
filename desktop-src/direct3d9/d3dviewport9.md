---
description: Definisce le dimensioni della finestra di una superficie di destinazione di rendering su cui si proietta un volume 3D.
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: Struttura D3DVIEWPORT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVIEWPORT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3d96000de50934ebdc893ffc3866dd3252703bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323026"
---
# <a name="d3dviewport9-structure"></a><span data-ttu-id="8c68c-103">Struttura D3DVIEWPORT9</span><span class="sxs-lookup"><span data-stu-id="8c68c-103">D3DVIEWPORT9 structure</span></span>

<span data-ttu-id="8c68c-104">Definisce le dimensioni della finestra di una superficie di destinazione di rendering su cui si proietta un volume 3D.</span><span class="sxs-lookup"><span data-stu-id="8c68c-104">Defines the window dimensions of a render-target surface onto which a 3D volume projects.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c68c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c68c-105">Syntax</span></span>


```C++
typedef struct D3DVIEWPORT9 {
  DWORD X;
  DWORD Y;
  DWORD Width;
  DWORD Height;
  float MinZ;
  float MaxZ;
} D3DVIEWPORT9, *LPD3DVIEWPORT9;
```



## <a name="members"></a><span data-ttu-id="8c68c-106">Members</span><span class="sxs-lookup"><span data-stu-id="8c68c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8c68c-107">**X**</span><span class="sxs-lookup"><span data-stu-id="8c68c-107">**X**</span></span>
</dt> <dd>

<span data-ttu-id="8c68c-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c68c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c68c-109">Coordinata pixel dell'angolo superiore sinistro del viewport sulla superficie di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="8c68c-109">Pixel coordinate of the upper-left corner of the viewport on the render-target surface.</span></span> <span data-ttu-id="8c68c-110">A meno che non si desideri eseguire il rendering in un subset della superficie, questo membro può essere impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="8c68c-110">Unless you want to render to a subset of the surface, this member can be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="8c68c-111">**S**</span><span class="sxs-lookup"><span data-stu-id="8c68c-111">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="8c68c-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c68c-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c68c-113">Coordinata pixel dell'angolo superiore sinistro del viewport sulla superficie di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="8c68c-113">Pixel coordinate of the upper-left corner of the viewport on the render-target surface.</span></span> <span data-ttu-id="8c68c-114">A meno che non si desideri eseguire il rendering in un subset della superficie, questo membro può essere impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="8c68c-114">Unless you want to render to a subset of the surface, this member can be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="8c68c-115">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="8c68c-115">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="8c68c-116">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c68c-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c68c-117">Dimensione della larghezza del volume di ritaglio, in pixel.</span><span class="sxs-lookup"><span data-stu-id="8c68c-117">Width dimension of the clip volume, in pixels.</span></span> <span data-ttu-id="8c68c-118">A meno che non si esegua il rendering solo in un subset della superficie, questo membro deve essere impostato sulla dimensione Width della superficie di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="8c68c-118">Unless you are rendering only to a subset of the surface, this member should be set to the width dimension of the render-target surface.</span></span>

</dd> <dt>

<span data-ttu-id="8c68c-119">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="8c68c-119">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="8c68c-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c68c-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8c68c-121">Dimensione dell'altezza del volume di ritaglio, in pixel.</span><span class="sxs-lookup"><span data-stu-id="8c68c-121">Height dimension of the clip volume, in pixels.</span></span> <span data-ttu-id="8c68c-122">A meno che non si esegua il rendering solo in un subset della superficie, questo membro deve essere impostato sulla dimensione Height della superficie di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="8c68c-122">Unless you are rendering only to a subset of the surface, this member should be set to the height dimension of the render-target surface.</span></span>

</dd> <dt>

<span data-ttu-id="8c68c-123">**MinZ**</span><span class="sxs-lookup"><span data-stu-id="8c68c-123">**MinZ**</span></span>
</dt> <dd>

<span data-ttu-id="8c68c-124">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8c68c-124">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="8c68c-125">Insieme a MaxZ, valore che descrive l'intervallo di valori di profondità in cui deve essere eseguito il rendering di una scena, i valori minimo e massimo del volume di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="8c68c-125">Together with MaxZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume.</span></span> <span data-ttu-id="8c68c-126">La maggior parte delle applicazioni imposta questo valore su 0,0.</span><span class="sxs-lookup"><span data-stu-id="8c68c-126">Most applications set this value to 0.0.</span></span> <span data-ttu-id="8c68c-127">Il ritaglio viene eseguito dopo l'applicazione della matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="8c68c-127">Clipping is performed after applying the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="8c68c-128">**MaxZ**</span><span class="sxs-lookup"><span data-stu-id="8c68c-128">**MaxZ**</span></span>
</dt> <dd>

<span data-ttu-id="8c68c-129">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="8c68c-129">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="8c68c-130">Insieme a MinZ, valore che descrive l'intervallo di valori di profondità in cui deve essere eseguito il rendering di una scena, i valori minimo e massimo del volume di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="8c68c-130">Together with MinZ, value describing the range of depth values into which a scene is to be rendered, the minimum and maximum values of the clip volume.</span></span> <span data-ttu-id="8c68c-131">La maggior parte delle applicazioni imposta questo valore su 1,0.</span><span class="sxs-lookup"><span data-stu-id="8c68c-131">Most applications set this value to 1.0.</span></span> <span data-ttu-id="8c68c-132">Il ritaglio viene eseguito dopo l'applicazione della matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="8c68c-132">Clipping is performed after applying the projection matrix.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c68c-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c68c-133">Remarks</span></span>

<span data-ttu-id="8c68c-134">I membri X, Y, larghezza e altezza descrivono la posizione e le dimensioni del viewport sulla superficie di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="8c68c-134">The X, Y, Width, and Height members describe the position and dimensions of the viewport on the render-target surface.</span></span> <span data-ttu-id="8c68c-135">In genere, le applicazioni eseguono il rendering sull'intera superficie di destinazione; Quando si esegue il rendering in una superficie 640 x 480, i membri devono essere rispettivamente 0, 0, 640 e 480.</span><span class="sxs-lookup"><span data-stu-id="8c68c-135">Usually, applications render to the entire target surface; when rendering on a 640 x 480 surface, these members should be 0, 0, 640, and 480, respectively.</span></span> <span data-ttu-id="8c68c-136">MinZ e MaxZ vengono in genere impostati su 0,0 e 1,0, ma possono essere impostati su altri valori per ottenere effetti specifici.</span><span class="sxs-lookup"><span data-stu-id="8c68c-136">The MinZ and MaxZ are typically set to 0.0 and 1.0 but can be set to other values to achieve specific effects.</span></span> <span data-ttu-id="8c68c-137">Ad esempio, è possibile impostare entrambi su 0,0 per forzare il rendering degli oggetti in primo piano di una scena o entrambi a 1,0 per forzare gli oggetti in background.</span><span class="sxs-lookup"><span data-stu-id="8c68c-137">For example, you might set them both to 0.0 to force the system to render objects to the foreground of a scene, or both to 1.0 to force the objects into the background.</span></span>

<span data-ttu-id="8c68c-138">Quando i parametri del viewport per un dispositivo cambiano (a causa di una chiamata al metodo [**seviewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) ), il driver compila una nuova matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="8c68c-138">When the viewport parameters for a device change (because of a call to the [**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) method), the driver builds a new transformation matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c68c-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c68c-139">Requirements</span></span>



| <span data-ttu-id="8c68c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c68c-140">Requirement</span></span> | <span data-ttu-id="8c68c-141">Valore</span><span class="sxs-lookup"><span data-stu-id="8c68c-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c68c-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c68c-142">Header</span></span><br/> | <dl> <span data-ttu-id="8c68c-143"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c68c-143"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c68c-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c68c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c68c-145">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="8c68c-145">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="8c68c-146">**GetViewport**</span><span class="sxs-lookup"><span data-stu-id="8c68c-146">**GetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[<span data-ttu-id="8c68c-147">**Viewport**</span><span class="sxs-lookup"><span data-stu-id="8c68c-147">**SetViewport**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
