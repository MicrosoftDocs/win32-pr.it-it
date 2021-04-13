---
description: Specifica il rettangolo utilizzato per racchiudere i glifi in una superficie monocromatica.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: Struttura D3DCOMPOSERECTDESC (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cf9ad5f1c075f4dc52d68b894b37c7d0f0a7b310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401938"
---
# <a name="d3dcomposerectdesc-structure"></a><span data-ttu-id="b9998-103">Struttura D3DCOMPOSERECTDESC</span><span class="sxs-lookup"><span data-stu-id="b9998-103">D3DCOMPOSERECTDESC structure</span></span>

<span data-ttu-id="b9998-104">Specifica il rettangolo utilizzato per racchiudere i glifi in una superficie monocromatica.</span><span class="sxs-lookup"><span data-stu-id="b9998-104">Specifies the rectangle used to enclose glyphs on a monochrome surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9998-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9998-105">Syntax</span></span>


```C++
typedef struct _D3DCOMPOSERECTDESC {
  USHORT X;
  USHORT Y;
  USHORT Width;
  USHORT Height;
} D3DCOMPOSERECTDESC;
```



## <a name="members"></a><span data-ttu-id="b9998-106">Members</span><span class="sxs-lookup"><span data-stu-id="b9998-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b9998-107">**X**</span><span class="sxs-lookup"><span data-stu-id="b9998-107">**X**</span></span>
</dt> <dd>

<span data-ttu-id="b9998-108">Tipo: **[ **ushort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9998-108">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b9998-109">Coordinata sinistra in cui iniziare la copia.</span><span class="sxs-lookup"><span data-stu-id="b9998-109">Left coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="b9998-110">**S**</span><span class="sxs-lookup"><span data-stu-id="b9998-110">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="b9998-111">Tipo: **[ **ushort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9998-111">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b9998-112">Coordinata superiore per iniziare la copia in.</span><span class="sxs-lookup"><span data-stu-id="b9998-112">Top coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="b9998-113">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="b9998-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="b9998-114">Tipo: **[ **ushort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9998-114">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b9998-115">Numero di Texel dalla coordinata sinistra.</span><span class="sxs-lookup"><span data-stu-id="b9998-115">Number of texels from left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="b9998-116">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="b9998-116">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="b9998-117">Tipo: **[ **ushort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9998-117">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b9998-118">Numero di Texel dalla coordinata superiore.</span><span class="sxs-lookup"><span data-stu-id="b9998-118">Number of texels from the top coordinate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9998-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9998-119">Remarks</span></span>

<span data-ttu-id="b9998-120">Questa struttura viene utilizzata nelle chiamate a [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) per racchiudere i glifi nell'area di origine.</span><span class="sxs-lookup"><span data-stu-id="b9998-120">This structure is used in calls to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) to enclose glyphs on the source surface.</span></span> <span data-ttu-id="b9998-121">Un buffer dei vertici (vedere [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) riempito con queste strutture viene creato per contenere le posizioni dei glifi.</span><span class="sxs-lookup"><span data-stu-id="b9998-121">A vertex buffer (see [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) filled with these structures are created to contain the glyph locations.</span></span> <span data-ttu-id="b9998-122">I membri USHORT vengono usati per ridurre il più possibile il footprint di memoria.</span><span class="sxs-lookup"><span data-stu-id="b9998-122">USHORT members are used to reduce the memory footprint as much as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9998-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9998-123">Requirements</span></span>



| <span data-ttu-id="b9998-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9998-124">Requirement</span></span> | <span data-ttu-id="b9998-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b9998-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9998-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9998-126">Header</span></span><br/> | <dl> <span data-ttu-id="b9998-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9998-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9998-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9998-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9998-129">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="b9998-129">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
