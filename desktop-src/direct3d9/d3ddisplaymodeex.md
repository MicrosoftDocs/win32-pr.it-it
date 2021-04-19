---
description: Informazioni sulle proprietà di una modalità di visualizzazione.
ms.assetid: df9d12b9-7acb-435b-9d54-0b095c871f0e
title: Struttura D3DDISPLAYMODEEX (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODEEX
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5906b6b23cc83e6d2379f0c5923b08b220285708
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322394"
---
# <a name="d3ddisplaymodeex-structure"></a><span data-ttu-id="526b9-103">Struttura D3DDISPLAYMODEEX</span><span class="sxs-lookup"><span data-stu-id="526b9-103">D3DDISPLAYMODEEX structure</span></span>

<span data-ttu-id="526b9-104">Informazioni sulle proprietà di una modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="526b9-104">Information about the properties of a display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="526b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="526b9-105">Syntax</span></span>


```C++
typedef struct {
  UINT                Size;
  UINT                Width;
  UINT                Height;
  UINT                RefreshRate;
  D3DFORMAT           Format;
  D3DSCANLINEORDERING ScanLineOrdering;
} D3DDISPLAYMODEEX;
```



## <a name="members"></a><span data-ttu-id="526b9-106">Members</span><span class="sxs-lookup"><span data-stu-id="526b9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="526b9-107">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="526b9-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="526b9-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="526b9-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="526b9-109">Dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="526b9-109">The size of this structure.</span></span> <span data-ttu-id="526b9-110">Questo deve essere sempre impostato su sizeof (D3DDISPLAYMODEEX).</span><span class="sxs-lookup"><span data-stu-id="526b9-110">This should always be set to sizeof(D3DDISPLAYMODEEX).</span></span>

</dd> <dt>

<span data-ttu-id="526b9-111">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="526b9-111">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="526b9-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="526b9-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="526b9-113">Larghezza della modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="526b9-113">Width of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="526b9-114">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="526b9-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="526b9-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="526b9-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="526b9-116">Altezza della modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="526b9-116">Height of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="526b9-117">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="526b9-117">**RefreshRate**</span></span>
</dt> <dd>

<span data-ttu-id="526b9-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="526b9-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="526b9-119">Frequenza di aggiornamento della modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="526b9-119">Refresh rate of the display mode.</span></span>

</dd> <dt>

<span data-ttu-id="526b9-120">**Formato**</span><span class="sxs-lookup"><span data-stu-id="526b9-120">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="526b9-121">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="526b9-121">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="526b9-122">Formato della modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="526b9-122">Format of the display mode.</span></span> <span data-ttu-id="526b9-123">Vedere [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="526b9-123">See [D3DFORMAT](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="526b9-124">**ScanLineOrdering**</span><span class="sxs-lookup"><span data-stu-id="526b9-124">**ScanLineOrdering**</span></span>
</dt> <dd>

<span data-ttu-id="526b9-125">Tipo: **[ **D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span><span class="sxs-lookup"><span data-stu-id="526b9-125">Type: **[**D3DSCANLINEORDERING**](./d3dscanlineordering.md)**</span></span>

</dd> <dd>

<span data-ttu-id="526b9-126">Indica se l'ordine scanline è progressivo o interlacciato.</span><span class="sxs-lookup"><span data-stu-id="526b9-126">Indicates whether the scanline order is progressive or interlaced.</span></span> <span data-ttu-id="526b9-127">Vedere [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span><span class="sxs-lookup"><span data-stu-id="526b9-127">See [**D3DSCANLINEORDERING**](./d3dscanlineordering.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="526b9-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="526b9-128">Remarks</span></span>

<span data-ttu-id="526b9-129">Questa struttura viene utilizzata in vari metodi per creare e gestire i dispositivi Direct3D 9Ex ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) e le catene ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).</span><span class="sxs-lookup"><span data-stu-id="526b9-129">This structure is used in various methods to create and manage Direct3D 9Ex devices ([**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex)) and swapchains ([**IDirect3DSwapChain9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dswapchain9ex)).</span></span>

## <a name="requirements"></a><span data-ttu-id="526b9-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="526b9-130">Requirements</span></span>



| <span data-ttu-id="526b9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="526b9-131">Requirement</span></span> | <span data-ttu-id="526b9-132">Valore</span><span class="sxs-lookup"><span data-stu-id="526b9-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="526b9-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="526b9-133">Header</span></span><br/> | <dl> <span data-ttu-id="526b9-134"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="526b9-134"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="526b9-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="526b9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="526b9-136">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="526b9-136">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
