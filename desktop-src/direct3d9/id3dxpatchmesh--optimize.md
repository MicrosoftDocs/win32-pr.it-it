---
description: Ottimizza la mesh della patch per un efficiente mosaico.
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: 'Metodo ID3DXPatchMesh:: Optimize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fa66aadd0ef1f9f9f65747694fc311f80172449
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969518"
---
# <a name="id3dxpatchmeshoptimize-method"></a><span data-ttu-id="41cec-103">Metodo ID3DXPatchMesh:: Optimize</span><span class="sxs-lookup"><span data-stu-id="41cec-103">ID3DXPatchMesh::Optimize method</span></span>

<span data-ttu-id="41cec-104">Ottimizza la mesh della patch per un efficiente mosaico.</span><span class="sxs-lookup"><span data-stu-id="41cec-104">Optimizes the patch mesh for efficient tessellation.</span></span>

## <a name="syntax"></a><span data-ttu-id="41cec-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41cec-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="41cec-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="41cec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41cec-107">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41cec-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41cec-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="41cec-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="41cec-109">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="41cec-109">Currently unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41cec-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41cec-110">Return value</span></span>

<span data-ttu-id="41cec-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="41cec-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="41cec-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="41cec-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="41cec-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT.</span><span class="sxs-lookup"><span data-stu-id="41cec-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_CANNOTATTRSORT.</span></span>

## <a name="remarks"></a><span data-ttu-id="41cec-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="41cec-114">Remarks</span></span>

<span data-ttu-id="41cec-115">Quando un'applicazione genera informazioni adiacenza per una mesh, i dati della mesh possono essere ottimizzati (riordinati) per migliorare le prestazioni del disegno.</span><span class="sxs-lookup"><span data-stu-id="41cec-115">After an application generates adjacency information for a mesh, the mesh data can be optimized (reordered) for better drawing performance.</span></span> <span data-ttu-id="41cec-116">Questo metodo determina quali patch sono adiacenti (entro la tolleranza fornita).</span><span class="sxs-lookup"><span data-stu-id="41cec-116">This method determines which patches are adjacent (within the provided tolerance).</span></span>

<span data-ttu-id="41cec-117">Le informazioni adiacenza vengono usate anche per ottimizzare la suddivisione a mosaico.</span><span class="sxs-lookup"><span data-stu-id="41cec-117">Adjacency information is also used to optimize tessellation.</span></span> <span data-ttu-id="41cec-118">Generare le informazioni adiacenza una sola volta e conteggiarla suddividerla ripetutamente chiamando [**ID3DXPatchMesh:: conteggiarla suddividerla**](id3dxpatchmesh--tessellate.md).</span><span class="sxs-lookup"><span data-stu-id="41cec-118">Generate adjacency information once and tessellate repeatedly by calling [**ID3DXPatchMesh::Tessellate**](id3dxpatchmesh--tessellate.md).</span></span> <span data-ttu-id="41cec-119">L'ottimizzazione eseguita è indipendente dal livello di mosaico effettivo utilizzato.</span><span class="sxs-lookup"><span data-stu-id="41cec-119">The optimization performed is independent of the actual tessellation level used.</span></span> <span data-ttu-id="41cec-120">Tuttavia, se i vertici della mesh vengono modificati, è necessario rigenerare le informazioni adiacenza.</span><span class="sxs-lookup"><span data-stu-id="41cec-120">However, if the mesh vertices are changed, you must regenerate the adjacency information.</span></span>

## <a name="requirements"></a><span data-ttu-id="41cec-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41cec-121">Requirements</span></span>



| <span data-ttu-id="41cec-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="41cec-122">Requirement</span></span> | <span data-ttu-id="41cec-123">Valore</span><span class="sxs-lookup"><span data-stu-id="41cec-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41cec-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41cec-124">Header</span></span><br/>  | <dl> <span data-ttu-id="41cec-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="41cec-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="41cec-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="41cec-126">Library</span></span><br/> | <dl> <span data-ttu-id="41cec-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41cec-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41cec-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41cec-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41cec-129">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="41cec-129">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="41cec-130">**ID3DXPatchMesh:: GenerateAdjacency**</span><span class="sxs-lookup"><span data-stu-id="41cec-130">**ID3DXPatchMesh::GenerateAdjacency**</span></span>](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 
