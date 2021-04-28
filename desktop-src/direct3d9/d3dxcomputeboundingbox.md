---
description: "Funzione D3DXComputeBoundingBox (D3DX9Mesh.h): calcola un rettangolo di selezione orientato all'asse delle coordinate."
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: Funzione D3DXComputeBoundingBox (D3DX9Mesh.h)
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
ms.openlocfilehash: 39fdf4123781b84d87ec1c9d790eb5ffae058892
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115829"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a><span data-ttu-id="65554-103">Funzione D3DXComputeBoundingBox (D3DX9Mesh.h)</span><span class="sxs-lookup"><span data-stu-id="65554-103">D3DXComputeBoundingBox function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="65554-104">Calcola un rettangolo di selezione orientato all'asse delle coordinate.</span><span class="sxs-lookup"><span data-stu-id="65554-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="65554-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65554-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="65554-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="65554-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65554-107">*pFirstPosition* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="65554-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65554-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="65554-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="65554-109">Puntatore alla prima posizione.</span><span class="sxs-lookup"><span data-stu-id="65554-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="65554-110">*NumVertices* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="65554-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65554-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65554-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65554-112">Numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="65554-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="65554-113">*dwStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="65554-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65554-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="65554-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="65554-115">Numero o numero di byte tra i vertici.</span><span class="sxs-lookup"><span data-stu-id="65554-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="65554-116">*pMin* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="65554-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65554-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="65554-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="65554-118">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che descrive l'angolo inferiore sinistro restituito del rettangolo di selezione.</span><span class="sxs-lookup"><span data-stu-id="65554-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span> <span data-ttu-id="65554-119">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="65554-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="65554-120">*pMax* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="65554-120">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65554-121">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="65554-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="65554-122">Puntatore a [**una struttura D3DXVECTOR3,**](d3dxvector3.md) che descrive l'angolo superiore destro restituito del rettangolo di selezione.</span><span class="sxs-lookup"><span data-stu-id="65554-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span> <span data-ttu-id="65554-123">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="65554-123">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65554-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65554-124">Return value</span></span>

<span data-ttu-id="65554-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="65554-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="65554-126">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="65554-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="65554-127">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="65554-127">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="65554-128">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="65554-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="65554-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65554-129">Requirements</span></span>



| <span data-ttu-id="65554-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="65554-130">Requirement</span></span> | <span data-ttu-id="65554-131">Valore</span><span class="sxs-lookup"><span data-stu-id="65554-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65554-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65554-132">Header</span></span><br/>  | <dl> <span data-ttu-id="65554-133"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="65554-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="65554-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="65554-134">Library</span></span><br/> | <dl> <span data-ttu-id="65554-135"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="65554-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="65554-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65554-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65554-137">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="65554-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
