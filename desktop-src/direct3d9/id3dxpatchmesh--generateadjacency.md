---
description: Generare un elenco di bordi della rete e le patch che condividono ogni bordo.
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: 'Metodo ID3DXPatchMesh:: GenerateAdjacency (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68de2a77b9d27391c57ec299ceb87d29166ee248
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401932"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a><span data-ttu-id="05e1b-103">Metodo ID3DXPatchMesh:: GenerateAdjacency</span><span class="sxs-lookup"><span data-stu-id="05e1b-103">ID3DXPatchMesh::GenerateAdjacency method</span></span>

<span data-ttu-id="05e1b-104">Generare un elenco di bordi della rete e le patch che condividono ogni bordo.</span><span class="sxs-lookup"><span data-stu-id="05e1b-104">Generate a list of mesh edges and the patches that share each edge.</span></span>

## <a name="syntax"></a><span data-ttu-id="05e1b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05e1b-105">Syntax</span></span>


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a><span data-ttu-id="05e1b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="05e1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05e1b-107">*fTolerance* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05e1b-107">*fTolerance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05e1b-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="05e1b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="05e1b-109">Specifica che i vertici che differiscono in base a un numero inferiore rispetto alla tolleranza devono essere considerati coincidenti.</span><span class="sxs-lookup"><span data-stu-id="05e1b-109">Specifies that vertices that differ in position by less than the tolerance should be treated as coincident.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05e1b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="05e1b-110">Return value</span></span>

<span data-ttu-id="05e1b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="05e1b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="05e1b-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="05e1b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="05e1b-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="05e1b-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="05e1b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="05e1b-114">Remarks</span></span>

<span data-ttu-id="05e1b-115">Quando un'applicazione genera informazioni adiacenza per una mesh, i dati della mesh possono essere ottimizzati per migliorare le prestazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="05e1b-115">After an application generates adjacency information for a mesh, the mesh data can be optimized for better drawing performance.</span></span> <span data-ttu-id="05e1b-116">Questo metodo determina quali patch sono adiacenti (entro la tolleranza fornita).</span><span class="sxs-lookup"><span data-stu-id="05e1b-116">This method determines which patches are adjacent (within the provided tolerance).</span></span> <span data-ttu-id="05e1b-117">Queste informazioni vengono utilizzate internamente per ottimizzare la suddivisione a mosaico.</span><span class="sxs-lookup"><span data-stu-id="05e1b-117">This information is used internally to optimize tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="05e1b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05e1b-118">Requirements</span></span>



| <span data-ttu-id="05e1b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="05e1b-119">Requirement</span></span> | <span data-ttu-id="05e1b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="05e1b-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05e1b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05e1b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="05e1b-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="05e1b-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="05e1b-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="05e1b-123">Library</span></span><br/> | <dl> <span data-ttu-id="05e1b-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05e1b-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="05e1b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05e1b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05e1b-126">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="05e1b-126">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="05e1b-127">**ID3DXPatchMesh:: Optimize**</span><span class="sxs-lookup"><span data-stu-id="05e1b-127">**ID3DXPatchMesh::Optimize**</span></span>](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 
