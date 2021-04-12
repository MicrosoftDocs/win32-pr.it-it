---
description: Incapsula un oggetto mesh in una gerarchia di frame di trasformazione.
ms.assetid: 50e98230-7dc3-468a-92c4-8165e8fe242b
title: Struttura D3DXMESHCONTAINER (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHCONTAINER
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f57daea26f42d8dd680d0259199b0df77badf510
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354179"
---
# <a name="d3dxmeshcontainer-structure"></a><span data-ttu-id="f8b48-103">Struttura D3DXMESHCONTAINER</span><span class="sxs-lookup"><span data-stu-id="f8b48-103">D3DXMESHCONTAINER structure</span></span>

<span data-ttu-id="f8b48-104">Incapsula un oggetto mesh in una gerarchia di frame di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="f8b48-104">Encapsulates a mesh object in a transformation frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8b48-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8b48-105">Syntax</span></span>


```C++
typedef struct D3DXMESHCONTAINER {
  LPSTR                Name;
  D3DXMESHDATA         MeshData;
  LPD3DXMATERIAL       pMaterials;
  LPD3DXEFFECTINSTANCE pEffects;
  DWORD                NumMaterials;
  DWORD                *pAdjacency;
  LPD3DXSKININFO       pSkinInfo;
  D3DXMESHCONTAINER    *pNextMeshContainer;
} D3DXMESHCONTAINER, *LPD3DXMESHCONTAINER;
```



## <a name="members"></a><span data-ttu-id="f8b48-106">Members</span><span class="sxs-lookup"><span data-stu-id="f8b48-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8b48-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f8b48-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="f8b48-108">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="f8b48-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f8b48-109">Nome della rete.</span><span class="sxs-lookup"><span data-stu-id="f8b48-109">Mesh name.</span></span>

</dd> <dt>

<span data-ttu-id="f8b48-110">**MeshData**</span><span class="sxs-lookup"><span data-stu-id="f8b48-110">**MeshData**</span></span>
</dt> <dd>

<span data-ttu-id="f8b48-111">Tipo: **[ **D3DXMESHDATA**](d3dxmeshdata.md)**</span><span class="sxs-lookup"><span data-stu-id="f8b48-111">Type: **[**D3DXMESHDATA**](d3dxmeshdata.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8b48-112">Tipo di dati nella rete.</span><span class="sxs-lookup"><span data-stu-id="f8b48-112">Type of data in the mesh.</span></span> <span data-ttu-id="f8b48-113">Vedere [**D3DXMESHDATA**](d3dxmeshdata.md).</span><span class="sxs-lookup"><span data-stu-id="f8b48-113">See [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8b48-114">**pMaterials**</span><span class="sxs-lookup"><span data-stu-id="f8b48-114">**pMaterials**</span></span>
</dt> <dd>

<span data-ttu-id="f8b48-115">Tipo: **[ **LPD3DXMATERIAL**](d3dxmaterial.md)**</span><span class="sxs-lookup"><span data-stu-id="f8b48-115">Type: **[**LPD3DXMATERIAL**](d3dxmaterial.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8b48-116">Matrice di materiali mesh.</span><span class="sxs-lookup"><span data-stu-id="f8b48-116">Array of mesh materials.</span></span> <span data-ttu-id="f8b48-117">Vedere [**D3DXMATERIAL**](d3dxmaterial.md).</span><span class="sxs-lookup"><span data-stu-id="f8b48-117">See [**D3DXMATERIAL**](d3dxmaterial.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8b48-118">**pEffects**</span><span class="sxs-lookup"><span data-stu-id="f8b48-118">**pEffects**</span></span>
</dt> <dd>

<span data-ttu-id="f8b48-119">Tipo: **[ **LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**</span><span class="sxs-lookup"><span data-stu-id="f8b48-119">Type: **[**LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8b48-120">Puntatore a un set di parametri di effetto predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f8b48-120">Pointer to a set of default effect parameters.</span></span> <span data-ttu-id="f8b48-121">Vedere [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="f8b48-121">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8b48-122">**NumMaterials**</span><span class="sxs-lookup"><span data-stu-id="f8b48-122">**NumMaterials**</span></span>
</dt> <dd>

<span data-ttu-id="f8b48-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8b48-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8b48-124">Numero di materiali nella rete.</span><span class="sxs-lookup"><span data-stu-id="f8b48-124">Number of materials in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="f8b48-125">**pAdjacency**</span><span class="sxs-lookup"><span data-stu-id="f8b48-125">**pAdjacency**</span></span>
</dt> <dd>

<span data-ttu-id="f8b48-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8b48-126">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="f8b48-127">Puntatore a una matrice di tre DWORD per triangolo della mesh che contiene informazioni adiacenza.</span><span class="sxs-lookup"><span data-stu-id="f8b48-127">Pointer to an array of three DWORDs per triangle of the mesh that contains adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="f8b48-128">**pSkinInfo**</span><span class="sxs-lookup"><span data-stu-id="f8b48-128">**pSkinInfo**</span></span>
</dt> <dd>

<span data-ttu-id="f8b48-129">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**</span><span class="sxs-lookup"><span data-stu-id="f8b48-129">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8b48-130">Puntatore all'interfaccia di informazioni sull'interfaccia personalizzata.</span><span class="sxs-lookup"><span data-stu-id="f8b48-130">Pointer to the skin information interface.</span></span> <span data-ttu-id="f8b48-131">Vedere [**ID3DXSkinInfo**](id3dxskininfo.md).</span><span class="sxs-lookup"><span data-stu-id="f8b48-131">See [**ID3DXSkinInfo**](id3dxskininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8b48-132">**pNextMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="f8b48-132">**pNextMeshContainer**</span></span>
</dt> <dd>

<span data-ttu-id="f8b48-133">Tipo: \* \* \* \* D3DXMESHCONTAINER **\***</span><span class="sxs-lookup"><span data-stu-id="f8b48-133">Type: \*\*\*\*D3DXMESHCONTAINER **\***</span></span>

</dd> <dd>

<span data-ttu-id="f8b48-134">Puntatore al contenitore mesh successivo.</span><span class="sxs-lookup"><span data-stu-id="f8b48-134">Pointer to the next mesh container.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8b48-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8b48-135">Remarks</span></span>

<span data-ttu-id="f8b48-136">Un'applicazione può derivare da questa struttura per aggiungere altri dati.</span><span class="sxs-lookup"><span data-stu-id="f8b48-136">An application can derive from this structure to add other data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8b48-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8b48-137">Requirements</span></span>



| <span data-ttu-id="f8b48-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8b48-138">Requirement</span></span> | <span data-ttu-id="f8b48-139">Valore</span><span class="sxs-lookup"><span data-stu-id="f8b48-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b48-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8b48-140">Header</span></span><br/> | <dl> <span data-ttu-id="f8b48-141"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8b48-141"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b48-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8b48-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b48-143">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="f8b48-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
