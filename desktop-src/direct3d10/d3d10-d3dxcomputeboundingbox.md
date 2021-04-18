---
description: Calcola un rettangolo di delimitazione orientato all'asse delle coordinate.
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: Funzione D3DXComputeBoundingBox (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9a93eb4a10f6c2b2fd7eda82afcc21158138a1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323268"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a><span data-ttu-id="42427-103">Funzione D3DXComputeBoundingBox (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="42427-103">D3DXComputeBoundingBox function (D3DX10math.h)</span></span>

<span data-ttu-id="42427-104">Calcola un rettangolo di delimitazione orientato all'asse delle coordinate.</span><span class="sxs-lookup"><span data-stu-id="42427-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="42427-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42427-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="42427-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="42427-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42427-107">*pFirstPosition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42427-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42427-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="42427-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="42427-109">Puntatore alla prima posizione.</span><span class="sxs-lookup"><span data-stu-id="42427-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="42427-110">*NumVertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42427-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42427-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42427-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42427-112">Numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="42427-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="42427-113">*dwStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42427-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42427-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42427-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42427-115">Conteggio o numero di byte tra i vertici.</span><span class="sxs-lookup"><span data-stu-id="42427-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="42427-116">*pMin* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="42427-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42427-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="42427-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="42427-118">Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che descrive l'angolo inferiore sinistro del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="42427-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span>

</dd> <dt>

<span data-ttu-id="42427-119">*pMax* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="42427-119">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42427-120">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="42427-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="42427-121">Puntatore a una struttura [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che descrive l'angolo superiore destro restituito del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="42427-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42427-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42427-122">Return value</span></span>

<span data-ttu-id="42427-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="42427-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="42427-124">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="42427-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="42427-125">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="42427-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="42427-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42427-126">Requirements</span></span>



| <span data-ttu-id="42427-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="42427-127">Requirement</span></span> | <span data-ttu-id="42427-128">Valore</span><span class="sxs-lookup"><span data-stu-id="42427-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42427-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42427-129">Header</span></span><br/>  | <dl> <span data-ttu-id="42427-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="42427-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="42427-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="42427-131">Library</span></span><br/> | <dl> <span data-ttu-id="42427-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42427-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="42427-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42427-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42427-134">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="42427-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
