---
description: Esegue lo schema a mosaico adattivo basato sul criterio a mosaico adattivo basato su z.
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: 'Metodo ID3DXPatchMesh:: TessellateAdaptive (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.TessellateAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4cc6c6b7ff7b0cdb99e56386df49529f26c9166
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323050"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a><span data-ttu-id="25ee4-103">Metodo ID3DXPatchMesh:: TessellateAdaptive</span><span class="sxs-lookup"><span data-stu-id="25ee4-103">ID3DXPatchMesh::TessellateAdaptive method</span></span>

<span data-ttu-id="25ee4-104">Esegue lo schema a mosaico adattivo basato sul criterio a mosaico adattivo basato su z.</span><span class="sxs-lookup"><span data-stu-id="25ee4-104">Performs adaptive tessellation based on the z-based adaptive tessellation criterion.</span></span>

## <a name="syntax"></a><span data-ttu-id="25ee4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25ee4-105">Syntax</span></span>


```C++
HRESULT TessellateAdaptive(
  [in] const D3DXVECTOR4 *pTrans,
  [in]       DWORD       dwMaxTessLevel,
  [in]       DWORD       dwMinTessLevel,
  [in]       LPD3DXMESH  pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="25ee4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="25ee4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25ee4-107">*pTrans* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25ee4-107">*pTrans* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ee4-108">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="25ee4-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="25ee4-109">Specifica un vettore 4D punteggiato con i vertici per ottenere l'importo a mosaico adattivo per vertice.</span><span class="sxs-lookup"><span data-stu-id="25ee4-109">Specifies a 4D vector that is dotted with the vertices to get the per-vertex adaptive tessellation amount.</span></span> <span data-ttu-id="25ee4-110">Ogni bordo è tassellati al valore medio dei livelli a mosaico per i due vertici a cui si connette.</span><span class="sxs-lookup"><span data-stu-id="25ee4-110">Each edge is tessellated to the average value of the tessellation levels for the two vertices it connects.</span></span>

</dd> <dt>

<span data-ttu-id="25ee4-111">*dwMaxTessLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25ee4-111">*dwMaxTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ee4-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25ee4-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25ee4-113">Limite massimo per lo schema a mosaico adattivo.</span><span class="sxs-lookup"><span data-stu-id="25ee4-113">Maximum limit for adaptive tessellation.</span></span> <span data-ttu-id="25ee4-114">Il numero di vertici introdotti tra i vertici esistenti.</span><span class="sxs-lookup"><span data-stu-id="25ee4-114">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="25ee4-115">Questo valore integer può variare da 1 a 32, inclusi.</span><span class="sxs-lookup"><span data-stu-id="25ee4-115">This integer value can range from 1 to 32, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="25ee4-116">*dwMinTessLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25ee4-116">*dwMinTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ee4-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25ee4-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25ee4-118">Limite minimo per lo schema a mosaico adattivo.</span><span class="sxs-lookup"><span data-stu-id="25ee4-118">Minimum limit for adaptive tessellation.</span></span> <span data-ttu-id="25ee4-119">Il numero di vertici introdotti tra i vertici esistenti.</span><span class="sxs-lookup"><span data-stu-id="25ee4-119">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="25ee4-120">Questo valore integer può variare da 1 a 32, inclusi.</span><span class="sxs-lookup"><span data-stu-id="25ee4-120">This integer value can range from 1 to 32, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="25ee4-121">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25ee4-121">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ee4-122">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="25ee4-122">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="25ee4-123">Mesh tassellati risultante.</span><span class="sxs-lookup"><span data-stu-id="25ee4-123">Resulting tessellated mesh.</span></span> <span data-ttu-id="25ee4-124">Vedere [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="25ee4-124">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25ee4-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25ee4-125">Return value</span></span>

<span data-ttu-id="25ee4-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25ee4-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25ee4-127">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="25ee4-127">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="25ee4-128">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="25ee4-128">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="25ee4-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="25ee4-129">Remarks</span></span>

<span data-ttu-id="25ee4-130">Questa funzione verrà eseguita in modo più efficiente se la mesh patch è stata ottimizzata con [**ID3DXPatchMesh:: Optimize**](id3dxpatchmesh--optimize.md).</span><span class="sxs-lookup"><span data-stu-id="25ee4-130">This function will perform more efficiently if the patch mesh has been optimized using [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25ee4-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25ee4-131">Requirements</span></span>



| <span data-ttu-id="25ee4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="25ee4-132">Requirement</span></span> | <span data-ttu-id="25ee4-133">Valore</span><span class="sxs-lookup"><span data-stu-id="25ee4-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25ee4-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25ee4-134">Header</span></span><br/>  | <dl> <span data-ttu-id="25ee4-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="25ee4-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="25ee4-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="25ee4-136">Library</span></span><br/> | <dl> <span data-ttu-id="25ee4-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25ee4-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="25ee4-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25ee4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25ee4-139">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="25ee4-139">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
