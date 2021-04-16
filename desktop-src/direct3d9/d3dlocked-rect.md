---
description: Descrive un'area rettangolare bloccata.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: Struttura D3DLOCKED_RECT (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_RECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9242a267085579cce52e66f2b9326a8e6298c87c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530955"
---
# <a name="d3dlocked_rect-structure"></a><span data-ttu-id="a470d-103">\_Struttura Rect D3DLOCKED</span><span class="sxs-lookup"><span data-stu-id="a470d-103">D3DLOCKED\_RECT structure</span></span>

<span data-ttu-id="a470d-104">Descrive un'area rettangolare bloccata.</span><span class="sxs-lookup"><span data-stu-id="a470d-104">Describes a locked rectangular region.</span></span>

## <a name="syntax"></a><span data-ttu-id="a470d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a470d-105">Syntax</span></span>


```C++
typedef struct D3DLOCKED_RECT {
  INT  Pitch;
  void *pBits;
} D3DLOCKED_RECT, *LPD3DLOCKED_RECT;
```



## <a name="members"></a><span data-ttu-id="a470d-106">Members</span><span class="sxs-lookup"><span data-stu-id="a470d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a470d-107">**Passo**</span><span class="sxs-lookup"><span data-stu-id="a470d-107">**Pitch**</span></span>
</dt> <dd>

<span data-ttu-id="a470d-108">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a470d-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a470d-109">Numero di byte in una riga della superficie.</span><span class="sxs-lookup"><span data-stu-id="a470d-109">Number of bytes in one row of the surface.</span></span>

</dd> <dt>

<span data-ttu-id="a470d-110">**pBits**</span><span class="sxs-lookup"><span data-stu-id="a470d-110">**pBits**</span></span>
</dt> <dd>

<span data-ttu-id="a470d-111">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="a470d-111">Type: **void\***</span></span>

</dd> <dd>

<span data-ttu-id="a470d-112">Puntatore ai bit bloccati.</span><span class="sxs-lookup"><span data-stu-id="a470d-112">Pointer to the locked bits.</span></span> <span data-ttu-id="a470d-113">Se è stato fornito un oggetto [**Rect**](/previous-versions//dd162897(v=vs.85)) alla chiamata [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) , pBits verrà spostato in modo appropriato dall'inizio della superficie.</span><span class="sxs-lookup"><span data-stu-id="a470d-113">If a [**RECT**](/previous-versions//dd162897(v=vs.85)) was provided to the [**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) call, pBits will be appropriately offset from the start of the surface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a470d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a470d-114">Remarks</span></span>

<span data-ttu-id="a470d-115">Il pitch per i formati DXTn è diverso da quello restituito in DirectX 7.</span><span class="sxs-lookup"><span data-stu-id="a470d-115">The pitch for DXTn formats is different from what was returned in DirectX 7.</span></span> <span data-ttu-id="a470d-116">Fa ora riferimento al numero di byte in una riga di blocchi.</span><span class="sxs-lookup"><span data-stu-id="a470d-116">It now refers to the number of bytes in a row of blocks.</span></span> <span data-ttu-id="a470d-117">Se, ad esempio, si dispone di una larghezza di 16, sarà presente un pitch di 4 blocchi (4 \* 8 per DXT1, 4 \* 16 per DXT2-5).</span><span class="sxs-lookup"><span data-stu-id="a470d-117">For example, if you have a width of 16, then you will have a pitch of 4 blocks (4\*8 for DXT1, 4\*16 for DXT2-5.)</span></span>

## <a name="requirements"></a><span data-ttu-id="a470d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a470d-118">Requirements</span></span>



| <span data-ttu-id="a470d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a470d-119">Requirement</span></span> | <span data-ttu-id="a470d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a470d-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a470d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a470d-121">Header</span></span><br/> | <dl> <span data-ttu-id="a470d-122"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a470d-122"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a470d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a470d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a470d-124">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="a470d-124">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="a470d-125">**IDirect3DCubeTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="a470d-125">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="a470d-126">**IDirect3DSurface9:: LockRect**</span><span class="sxs-lookup"><span data-stu-id="a470d-126">**IDirect3DSurface9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[<span data-ttu-id="a470d-127">**IDirect3DTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="a470d-127">**IDirect3DTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
