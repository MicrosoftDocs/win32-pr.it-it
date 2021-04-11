---
description: Incapsula un frame di trasformazione in una gerarchia di frame di trasformazione.
ms.assetid: 838d75c2-41b2-4703-961b-893c34104c55
title: Struttura D3DXFRAME (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFRAME
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 152e620f6bf845f1f2528a321e39d8d746e8b893
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235018"
---
# <a name="d3dxframe-structure"></a><span data-ttu-id="bb5f7-103">Struttura D3DXFRAME</span><span class="sxs-lookup"><span data-stu-id="bb5f7-103">D3DXFRAME structure</span></span>

<span data-ttu-id="bb5f7-104">Incapsula un frame di trasformazione in una gerarchia di frame di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="bb5f7-104">Encapsulates a transform frame in a transformation frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb5f7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb5f7-105">Syntax</span></span>


```C++
typedef struct D3DXFRAME {
  LPSTR               Name;
  D3DXMATRIX          TransformationMatrix;
  LPD3DXMESHCONTAINER pMeshContainer;
  D3DXFRAME           *pFrameSibling;
  D3DXFRAME           *pFrameFirstChild;
} D3DXFRAME, *LPD3DXFRAME;
```



## <a name="members"></a><span data-ttu-id="bb5f7-106">Members</span><span class="sxs-lookup"><span data-stu-id="bb5f7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb5f7-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bb5f7-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="bb5f7-108">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="bb5f7-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="bb5f7-109">Nome del frame.</span><span class="sxs-lookup"><span data-stu-id="bb5f7-109">Name of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="bb5f7-110">**TransformationMatrix**</span><span class="sxs-lookup"><span data-stu-id="bb5f7-110">**TransformationMatrix**</span></span>
</dt> <dd>

<span data-ttu-id="bb5f7-111">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="bb5f7-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb5f7-112">Matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="bb5f7-112">Transformation matrix.</span></span>

</dd> <dt>

<span data-ttu-id="bb5f7-113">**pMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="bb5f7-113">**pMeshContainer**</span></span>
</dt> <dd>

<span data-ttu-id="bb5f7-114">Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="bb5f7-114">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bb5f7-115">Puntatore al contenitore mesh.</span><span class="sxs-lookup"><span data-stu-id="bb5f7-115">Pointer to the mesh container.</span></span>

</dd> <dt>

<span data-ttu-id="bb5f7-116">**pFrameSibling**</span><span class="sxs-lookup"><span data-stu-id="bb5f7-116">**pFrameSibling**</span></span>
</dt> <dd>

<span data-ttu-id="bb5f7-117">Tipo: \* \* \* \* D3DXFRAME **\***</span><span class="sxs-lookup"><span data-stu-id="bb5f7-117">Type: \*\*\*\*D3DXFRAME **\***</span></span>

</dd> <dd>

<span data-ttu-id="bb5f7-118">Puntatore a un frame di pari livello.</span><span class="sxs-lookup"><span data-stu-id="bb5f7-118">Pointer to a sibling frame.</span></span>

</dd> <dt>

<span data-ttu-id="bb5f7-119">**pFrameFirstChild**</span><span class="sxs-lookup"><span data-stu-id="bb5f7-119">**pFrameFirstChild**</span></span>
</dt> <dd>

<span data-ttu-id="bb5f7-120">Tipo: \* \* \* \* D3DXFRAME **\***</span><span class="sxs-lookup"><span data-stu-id="bb5f7-120">Type: \*\*\*\*D3DXFRAME **\***</span></span>

</dd> <dd>

<span data-ttu-id="bb5f7-121">Puntatore a un frame figlio.</span><span class="sxs-lookup"><span data-stu-id="bb5f7-121">Pointer to a child frame.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb5f7-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb5f7-122">Remarks</span></span>

<span data-ttu-id="bb5f7-123">Un'applicazione può derivare da questa struttura per aggiungere altri dati.</span><span class="sxs-lookup"><span data-stu-id="bb5f7-123">An application can derive from this structure to add other data.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb5f7-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb5f7-124">Requirements</span></span>



| <span data-ttu-id="bb5f7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb5f7-125">Requirement</span></span> | <span data-ttu-id="bb5f7-126">Valore</span><span class="sxs-lookup"><span data-stu-id="bb5f7-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb5f7-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb5f7-127">Header</span></span><br/> | <dl> <span data-ttu-id="bb5f7-128"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb5f7-128"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb5f7-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb5f7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb5f7-130">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="bb5f7-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




