---
description: Specifica il glifo e la posizione di origine in una superficie monocromatica in cui copiare i glifi.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: Struttura D3DCOMPOSERECTDESTINATION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESTINATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 56843bc78943a4c76fe4fe0f5e18242728a979c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322367"
---
# <a name="d3dcomposerectdestination-structure"></a><span data-ttu-id="fc6db-103">Struttura D3DCOMPOSERECTDESTINATION</span><span class="sxs-lookup"><span data-stu-id="fc6db-103">D3DCOMPOSERECTDESTINATION structure</span></span>

<span data-ttu-id="fc6db-104">Specifica il glifo e la posizione di origine in una superficie monocromatica in cui copiare i glifi.</span><span class="sxs-lookup"><span data-stu-id="fc6db-104">Specifies the source glyph and location in a monochrome surface to copy glyphs into.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc6db-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc6db-105">Syntax</span></span>


```C++
typedef struct _D3DCOMPOSERECTDESTINATION {
  USHORT SrcRectIndex;
  USHORT Reserved;
  USHORT X;
  USHORT Y;
} D3DCOMPOSERECTDESTINATION;
```



## <a name="members"></a><span data-ttu-id="fc6db-106">Members</span><span class="sxs-lookup"><span data-stu-id="fc6db-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fc6db-107">**SrcRectIndex**</span><span class="sxs-lookup"><span data-stu-id="fc6db-107">**SrcRectIndex**</span></span>
</dt> <dd>

<span data-ttu-id="fc6db-108">Tipo: **[ **ushort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc6db-108">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc6db-109">Indicizzare un glifo particolare dal buffer vertex contenente le strutture [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) .</span><span class="sxs-lookup"><span data-stu-id="fc6db-109">Index particular glyph from vertex buffer containing [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="fc6db-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="fc6db-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="fc6db-111">Tipo: **[ **ushort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc6db-111">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc6db-112">Riservato a scopo di allineamento.</span><span class="sxs-lookup"><span data-stu-id="fc6db-112">Reserved for alignment purposes.</span></span>

</dd> <dt>

<span data-ttu-id="fc6db-113">**X**</span><span class="sxs-lookup"><span data-stu-id="fc6db-113">**X**</span></span>
</dt> <dd>

<span data-ttu-id="fc6db-114">Tipo: **[ **ushort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc6db-114">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc6db-115">Coordinata sinistra in cui iniziare la copia.</span><span class="sxs-lookup"><span data-stu-id="fc6db-115">Left coordinate to begin copy at.</span></span>

</dd> <dt>

<span data-ttu-id="fc6db-116">**S**</span><span class="sxs-lookup"><span data-stu-id="fc6db-116">**Y**</span></span>
</dt> <dd>

<span data-ttu-id="fc6db-117">Tipo: **[ **ushort**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc6db-117">Type: **[**USHORT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc6db-118">Coordinata superiore per iniziare la copia in.</span><span class="sxs-lookup"><span data-stu-id="fc6db-118">Top coordinate to begin copy at.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc6db-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc6db-119">Remarks</span></span>

<span data-ttu-id="fc6db-120">Questa struttura viene utilizzata nelle chiamate a [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) per indicare che i glifi del percorso devono essere copiati in e quale glifo particolare deve essere copiato.</span><span class="sxs-lookup"><span data-stu-id="fc6db-120">This structure is used in calls to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) to indicate the location glyphs should be copied to and which particular glyph should be copied.</span></span> <span data-ttu-id="fc6db-121">Un buffer dei vertici (vedere [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) riempito con queste strutture viene creato per contenere le posizioni dei glifi.</span><span class="sxs-lookup"><span data-stu-id="fc6db-121">A vertex buffer (see [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)) filled with these structures are created to contain the glyph locations.</span></span> <span data-ttu-id="fc6db-122">I membri USHORT vengono usati per ridurre il più possibile il footprint di memoria.</span><span class="sxs-lookup"><span data-stu-id="fc6db-122">USHORT members are used to reduce the memory footprint as much as possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc6db-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc6db-123">Requirements</span></span>



| <span data-ttu-id="fc6db-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc6db-124">Requirement</span></span> | <span data-ttu-id="fc6db-125">Valore</span><span class="sxs-lookup"><span data-stu-id="fc6db-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc6db-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc6db-126">Header</span></span><br/> | <dl> <span data-ttu-id="fc6db-127"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc6db-127"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc6db-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc6db-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc6db-129">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="fc6db-129">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
