---
description: Struttura D3DXSHPRTSPLITMESHCLUSTERDATA
ms.assetid: 6a53420c-06bc-4f52-ac2e-5adda5e34cb2
title: Struttura D3DXSHPRTSPLITMESHCLUSTERDATA (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHCLUSTERDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7b1bc23606dbf08f5a924860e12c9c09d719287
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322473"
---
# <a name="d3dxshprtsplitmeshclusterdata-structure"></a><span data-ttu-id="7d55b-103">Struttura D3DXSHPRTSPLITMESHCLUSTERDATA</span><span class="sxs-lookup"><span data-stu-id="7d55b-103">D3DXSHPRTSPLITMESHCLUSTERDATA structure</span></span>

## <a name="syntax"></a><span data-ttu-id="7d55b-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d55b-104">Syntax</span></span>


```C++
typedef struct D3DXSHPRTSPLITMESHCLUSTERDATA {
  UINT uVertStart;
  UINT uVertLength;
  UINT uFaceStart;
  UINT uFaceLength;
  UINT uClusterStart;
  UINT uClusterLength;
} D3DXSHPRTSPLITMESHCLUSTERDATA, *LPD3DXSHPRTSPLITMESHCLUSTERDATA;
```



## <a name="members"></a><span data-ttu-id="7d55b-105">Members</span><span class="sxs-lookup"><span data-stu-id="7d55b-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="7d55b-106">**uVertStart**</span><span class="sxs-lookup"><span data-stu-id="7d55b-106">**uVertStart**</span></span>
</dt> <dd>

<span data-ttu-id="7d55b-107">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d55b-107">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d55b-108">Vertice iniziale in una matrice di vertici con mapping.</span><span class="sxs-lookup"><span data-stu-id="7d55b-108">Initial vertex into remapped vertex array.</span></span>

</dd> <dt>

<span data-ttu-id="7d55b-109">**uVertLength**</span><span class="sxs-lookup"><span data-stu-id="7d55b-109">**uVertLength**</span></span>
</dt> <dd>

<span data-ttu-id="7d55b-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d55b-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d55b-111">Numero di vertici in questo Supercluster.</span><span class="sxs-lookup"><span data-stu-id="7d55b-111">Number of vertices in this supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="7d55b-112">**uFaceStart**</span><span class="sxs-lookup"><span data-stu-id="7d55b-112">**uFaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="7d55b-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d55b-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d55b-114">Indice iniziale nella matrice della superficie.</span><span class="sxs-lookup"><span data-stu-id="7d55b-114">Initial index into face array.</span></span>

</dd> <dt>

<span data-ttu-id="7d55b-115">**uFaceLength**</span><span class="sxs-lookup"><span data-stu-id="7d55b-115">**uFaceLength**</span></span>
</dt> <dd>

<span data-ttu-id="7d55b-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d55b-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d55b-117">Numero di visi in questo Supercluster.</span><span class="sxs-lookup"><span data-stu-id="7d55b-117">Number of faces in this supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="7d55b-118">**uClusterStart**</span><span class="sxs-lookup"><span data-stu-id="7d55b-118">**uClusterStart**</span></span>
</dt> <dd>

<span data-ttu-id="7d55b-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d55b-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d55b-120">Indice iniziale nella matrice del cluster.</span><span class="sxs-lookup"><span data-stu-id="7d55b-120">Initial index into cluster array.</span></span>

</dd> <dt>

<span data-ttu-id="7d55b-121">**uClusterLength**</span><span class="sxs-lookup"><span data-stu-id="7d55b-121">**uClusterLength**</span></span>
</dt> <dd>

<span data-ttu-id="7d55b-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d55b-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d55b-123">Numero di cluster in questa matrice di Supercluster.</span><span class="sxs-lookup"><span data-stu-id="7d55b-123">Number of clusters in this supercluster array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d55b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d55b-124">Requirements</span></span>



| <span data-ttu-id="7d55b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d55b-125">Requirement</span></span> | <span data-ttu-id="7d55b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7d55b-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d55b-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d55b-127">Header</span></span><br/> | <dl> <span data-ttu-id="7d55b-128"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d55b-128"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d55b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d55b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d55b-130">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="7d55b-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="7d55b-131">**D3DXSHPRTCompSplitMeshSC**</span><span class="sxs-lookup"><span data-stu-id="7d55b-131">**D3DXSHPRTCompSplitMeshSC**</span></span>](d3dxshprtcompsplitmeshsc.md)
</dt> </dl>

 

 
