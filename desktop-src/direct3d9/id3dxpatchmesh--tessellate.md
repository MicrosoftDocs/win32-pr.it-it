---
description: Esegue lo schema a mosaico uniforme in base al livello del mosaico.
ms.assetid: 0fc701b4-0636-450e-b8e0-e7a490871316
title: 'Metodo ID3DXPatchMesh:: conteggiarla suddividerla (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Tessellate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b94b79a9decd2f44fa1675e257a2401e2ae8f7a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323714"
---
# <a name="id3dxpatchmeshtessellate-method"></a><span data-ttu-id="aff99-103">Metodo ID3DXPatchMesh:: conteggiarla suddividerla</span><span class="sxs-lookup"><span data-stu-id="aff99-103">ID3DXPatchMesh::Tessellate method</span></span>

<span data-ttu-id="aff99-104">Esegue lo schema a mosaico uniforme in base al livello del mosaico.</span><span class="sxs-lookup"><span data-stu-id="aff99-104">Performs uniform tessellation based on the tessellation level.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff99-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aff99-105">Syntax</span></span>


```C++
HRESULT Tessellate(
  [in] FLOAT      fTessLevel,
  [in] LPD3DXMESH pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="aff99-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aff99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aff99-107">*fTessLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aff99-107">*fTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aff99-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aff99-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aff99-109">Livello mosaico.</span><span class="sxs-lookup"><span data-stu-id="aff99-109">Tessellation level.</span></span> <span data-ttu-id="aff99-110">Il numero di vertici introdotti tra i vertici esistenti.</span><span class="sxs-lookup"><span data-stu-id="aff99-110">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="aff99-111">L'intervallo di questo parametro float è 0 < fTessLevel <= 32.</span><span class="sxs-lookup"><span data-stu-id="aff99-111">The range of this float parameter is 0 < fTessLevel <= 32.</span></span>

</dd> <dt>

<span data-ttu-id="aff99-112">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aff99-112">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aff99-113">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="aff99-113">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="aff99-114">Mesh tassellati risultante.</span><span class="sxs-lookup"><span data-stu-id="aff99-114">Resulting tessellated mesh.</span></span> <span data-ttu-id="aff99-115">Vedere [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="aff99-115">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aff99-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aff99-116">Return value</span></span>

<span data-ttu-id="aff99-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aff99-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aff99-118">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="aff99-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="aff99-119">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="aff99-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="aff99-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="aff99-120">Remarks</span></span>

<span data-ttu-id="aff99-121">Questa funzione verrà eseguita in modo più efficiente se la mesh patch è stata ottimizzata con [**ID3DXPatchMesh:: Optimize**](id3dxpatchmesh--optimize.md).</span><span class="sxs-lookup"><span data-stu-id="aff99-121">This function will perform more efficiently if the patch mesh has been optimized using [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aff99-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aff99-122">Requirements</span></span>



| <span data-ttu-id="aff99-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="aff99-123">Requirement</span></span> | <span data-ttu-id="aff99-124">Valore</span><span class="sxs-lookup"><span data-stu-id="aff99-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aff99-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aff99-125">Header</span></span><br/>  | <dl> <span data-ttu-id="aff99-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff99-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="aff99-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="aff99-127">Library</span></span><br/> | <dl> <span data-ttu-id="aff99-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aff99-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aff99-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aff99-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff99-130">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="aff99-130">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
