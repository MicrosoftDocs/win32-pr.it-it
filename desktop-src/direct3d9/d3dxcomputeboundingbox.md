---
description: Calcola un rettangolo di delimitazione orientato all'asse delle coordinate.
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: Funzione D3DXComputeBoundingBox (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df0376428153cfc02e499c9e26226cce81154023
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235059"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a><span data-ttu-id="d4d15-103">Funzione D3DXComputeBoundingBox (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="d4d15-103">D3DXComputeBoundingBox function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="d4d15-104">Calcola un rettangolo di delimitazione orientato all'asse delle coordinate.</span><span class="sxs-lookup"><span data-stu-id="d4d15-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d15-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4d15-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="d4d15-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4d15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4d15-107">*pFirstPosition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4d15-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d15-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d4d15-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d4d15-109">Puntatore alla prima posizione.</span><span class="sxs-lookup"><span data-stu-id="d4d15-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="d4d15-110">*NumVertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4d15-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d15-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4d15-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4d15-112">Numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="d4d15-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d4d15-113">*dwStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4d15-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d15-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4d15-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4d15-115">Conteggio o numero di byte tra i vertici.</span><span class="sxs-lookup"><span data-stu-id="d4d15-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d4d15-116">*pMin* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d4d15-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d15-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4d15-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d4d15-118">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che descrive l'angolo inferiore sinistro del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="d4d15-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span> <span data-ttu-id="d4d15-119">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d4d15-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d4d15-120">*pMax* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d4d15-120">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d15-121">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4d15-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d4d15-122">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che descrive l'angolo superiore destro restituito del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="d4d15-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span> <span data-ttu-id="d4d15-123">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d4d15-123">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4d15-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4d15-124">Return value</span></span>

<span data-ttu-id="d4d15-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4d15-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4d15-126">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d4d15-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d4d15-127">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d4d15-127">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4d15-128">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d4d15-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d15-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4d15-129">Requirements</span></span>



| <span data-ttu-id="d4d15-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4d15-130">Requirement</span></span> | <span data-ttu-id="d4d15-131">Valore</span><span class="sxs-lookup"><span data-stu-id="d4d15-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d15-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4d15-132">Header</span></span><br/>  | <dl> <span data-ttu-id="d4d15-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d15-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d4d15-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="d4d15-134">Library</span></span><br/> | <dl> <span data-ttu-id="d4d15-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4d15-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4d15-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4d15-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d15-137">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="d4d15-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
