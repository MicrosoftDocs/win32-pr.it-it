---
description: Descrive una casella bloccata (volume).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: Struttura D3DLOCKED_BOX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_BOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 41fc5b0fd81405f9f12f65fca4fae53239110bfa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235072"
---
# <a name="d3dlocked_box-structure"></a><span data-ttu-id="152e1-103">\_Struttura D3DLOCKED box</span><span class="sxs-lookup"><span data-stu-id="152e1-103">D3DLOCKED\_BOX structure</span></span>

<span data-ttu-id="152e1-104">Descrive una casella bloccata (volume).</span><span class="sxs-lookup"><span data-stu-id="152e1-104">Describes a locked box (volume).</span></span>

## <a name="syntax"></a><span data-ttu-id="152e1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="152e1-105">Syntax</span></span>


```C++
typedef struct D3DLOCKED_BOX {
  int  RowPitch;
  int  SlicePitch;
  void *pBits;
} D3DLOCKED_BOX, *LPD3DLOCKED_BOX;
```



## <a name="members"></a><span data-ttu-id="152e1-106">Members</span><span class="sxs-lookup"><span data-stu-id="152e1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="152e1-107">**RowPitch**</span><span class="sxs-lookup"><span data-stu-id="152e1-107">**RowPitch**</span></span>
</dt> <dd>

<span data-ttu-id="152e1-108">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="152e1-108">Type: **[**int**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="152e1-109">Offset dei byte dal bordo sinistro di una riga al bordo sinistro della riga successiva.</span><span class="sxs-lookup"><span data-stu-id="152e1-109">Byte offset from the left edge of one row to the left edge of the next row.</span></span>

</dd> <dt>

<span data-ttu-id="152e1-110">**SlicePitch**</span><span class="sxs-lookup"><span data-stu-id="152e1-110">**SlicePitch**</span></span>
</dt> <dd>

<span data-ttu-id="152e1-111">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="152e1-111">Type: **[**int**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="152e1-112">Offset di byte dalla parte superiore sinistra di una sezione alla parte superiore sinistra della sezione più profonda successiva.</span><span class="sxs-lookup"><span data-stu-id="152e1-112">Byte offset from the top-left of one slice to the top-left of the next deepest slice.</span></span>

</dd> <dt>

<span data-ttu-id="152e1-113">**pBits**</span><span class="sxs-lookup"><span data-stu-id="152e1-113">**pBits**</span></span>
</dt> <dd>

<span data-ttu-id="152e1-114">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="152e1-114">Type: **void\***</span></span>

</dd> <dd>

<span data-ttu-id="152e1-115">Puntatore all'inizio della casella del volume.</span><span class="sxs-lookup"><span data-stu-id="152e1-115">Pointer to the beginning of the volume box.</span></span> <span data-ttu-id="152e1-116">Se è stato specificato un [**D3DBOX**](d3dbox.md) per la chiamata all'archivio protetto, pBits verrà spostato in modo appropriato dall'inizio del volume.</span><span class="sxs-lookup"><span data-stu-id="152e1-116">If a [**D3DBOX**](d3dbox.md) was provided to the LockBox call, pBits will be appropriately offset from the start of the volume.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="152e1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="152e1-117">Remarks</span></span>

<span data-ttu-id="152e1-118">I volumi possono essere visualizzati come organizzati in sezioni di larghezza x superfici 2D di altezza in pila per ottenere una larghezza x altezza x volume profondità.</span><span class="sxs-lookup"><span data-stu-id="152e1-118">Volumes can be visualized as being organized into slices of width x height 2D surfaces stacked up to make a width x height x depth volume.</span></span> <span data-ttu-id="152e1-119">Per altre informazioni, vedere [risorse di trama del volume (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="152e1-119">For more information, see [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="152e1-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="152e1-120">Requirements</span></span>



| <span data-ttu-id="152e1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="152e1-121">Requirement</span></span> | <span data-ttu-id="152e1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="152e1-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="152e1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="152e1-123">Header</span></span><br/> | <dl> <span data-ttu-id="152e1-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="152e1-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="152e1-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="152e1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152e1-126">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="152e1-126">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="152e1-127">**IDirect3DVolume9:: archivio protetto**</span><span class="sxs-lookup"><span data-stu-id="152e1-127">**IDirect3DVolume9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="152e1-128">**IDirect3DVolumeTexture9:: archivio protetto**</span><span class="sxs-lookup"><span data-stu-id="152e1-128">**IDirect3DVolumeTexture9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
