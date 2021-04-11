---
description: Membro della decl del vertice su cui eseguire il Skinning del software. Viene usato con l'API ID3DX10SkinInfo::D oSoftwareSkinning.
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: Struttura D3DX10_SKINNING_CHANNEL (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SKINNING_CHANNEL
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 79f5807dc2539d770d3caa41bddf7aa4960ce682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235078"
---
# <a name="d3dx10_skinning_channel-structure"></a><span data-ttu-id="d89c3-104">\_Struttura del canale di skinning d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="d89c3-104">D3DX10\_SKINNING\_CHANNEL structure</span></span>

<span data-ttu-id="d89c3-105">Membro della decl del vertice su cui eseguire il Skinning del software.</span><span class="sxs-lookup"><span data-stu-id="d89c3-105">The member of the vertex decl to do the software skinning on.</span></span> <span data-ttu-id="d89c3-106">Viene usato con l'API [**ID3DX10SkinInfo::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) .</span><span class="sxs-lookup"><span data-stu-id="d89c3-106">This is used with the [**ID3DX10SkinInfo::DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md) API.</span></span>

## <a name="syntax"></a><span data-ttu-id="d89c3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d89c3-107">Syntax</span></span>


```C++
typedef struct D3DX10_SKINNING_CHANNEL {
  UINT SrcOffset;
  UINT DestOffset;
  BOOL IsNormal;
} D3DX10_SKINNING_CHANNEL, *LPD3DX10_SKINNING_CHANNEL;
```



## <a name="members"></a><span data-ttu-id="d89c3-108">Members</span><span class="sxs-lookup"><span data-stu-id="d89c3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d89c3-109">**SrcOffset**</span><span class="sxs-lookup"><span data-stu-id="d89c3-109">**SrcOffset**</span></span>
</dt> <dd>

<span data-ttu-id="d89c3-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d89c3-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d89c3-111">Offset dall'inizio di ogni vertice di origine.</span><span class="sxs-lookup"><span data-stu-id="d89c3-111">Offset from the beginning of each source vertex.</span></span>

</dd> <dt>

<span data-ttu-id="d89c3-112">**DestOffset**</span><span class="sxs-lookup"><span data-stu-id="d89c3-112">**DestOffset**</span></span>
</dt> <dd>

<span data-ttu-id="d89c3-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d89c3-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d89c3-114">Offset dall'inizio di ogni vertice di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d89c3-114">Offset from the beginning of each destination vertex.</span></span>

</dd> <dt>

<span data-ttu-id="d89c3-115">**Normale**</span><span class="sxs-lookup"><span data-stu-id="d89c3-115">**IsNormal**</span></span>
</dt> <dd>

<span data-ttu-id="d89c3-116">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d89c3-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d89c3-117">Determina la matrice di matrici da usare nell'API [**ID3DX10SkinInfo::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) .</span><span class="sxs-lookup"><span data-stu-id="d89c3-117">Determines which array of matrices to use in the [**ID3DX10SkinInfo::DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md) API.</span></span> <span data-ttu-id="d89c3-118">Se il valore è true, verrà utilizzato *pInverseTransposeBoneMatrices* . in caso contrario, verrà utilizzato *pBoneMatrices* .</span><span class="sxs-lookup"><span data-stu-id="d89c3-118">If this is true, the *pInverseTransposeBoneMatrices* will be used, otherwise *pBoneMatrices* will be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d89c3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d89c3-119">Requirements</span></span>



| <span data-ttu-id="d89c3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d89c3-120">Requirement</span></span> | <span data-ttu-id="d89c3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d89c3-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d89c3-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d89c3-122">Header</span></span><br/> | <dl> <span data-ttu-id="d89c3-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d89c3-123"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d89c3-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d89c3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d89c3-125">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="d89c3-125">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
