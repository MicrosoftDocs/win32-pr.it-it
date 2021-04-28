---
description: 'Funzione D3DXComputeBoundingSphere (D3DX10math.h): calcola una sfera di delimitazione per la mesh.'
ms.assetid: 54f486d2-45e9-4fc1-90a3-97488ed4d900
title: Funzione D3DXComputeBoundingSphere (D3DX10math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0041d775b21d1af37bc51d6ec2f432e616b2abd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113299"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx10mathh"></a><span data-ttu-id="8442b-103">Funzione D3DXComputeBoundingSphere (D3DX10math.h)</span><span class="sxs-lookup"><span data-stu-id="8442b-103">D3DXComputeBoundingSphere function (D3DX10math.h)</span></span>

<span data-ttu-id="8442b-104">Calcola una sfera di delimitazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="8442b-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="8442b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8442b-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_ const D3DXVECTOR3 *pFirstPosition,
  _In_       DWORD       NumVertices,
  _In_       DWORD       dwStride,
  _In_       D3DXVECTOR3 *pCenter,
  _In_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="8442b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8442b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8442b-107">*pFirstPosition* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8442b-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8442b-108">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8442b-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8442b-109">Puntatore alla prima posizione.</span><span class="sxs-lookup"><span data-stu-id="8442b-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="8442b-110">*NumVertices* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8442b-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8442b-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8442b-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8442b-112">Numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="8442b-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="8442b-113">*dwStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8442b-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8442b-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8442b-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8442b-115">Numero di byte tra i vettori di posizione.</span><span class="sxs-lookup"><span data-stu-id="8442b-115">Number of bytes between position vectors.</span></span>

</dd> <dt>

<span data-ttu-id="8442b-116">*pCenter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8442b-116">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8442b-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="8442b-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8442b-118">[**Struttura D3DXVECTOR3,**](d3d10-d3dxvector3.md) che definisce il centro delle coordinate della sfera di delimitazione restituita.</span><span class="sxs-lookup"><span data-stu-id="8442b-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="8442b-119">*pRadius* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8442b-119">*pRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8442b-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8442b-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8442b-121">Raggio della sfera di delimitazione restituita.</span><span class="sxs-lookup"><span data-stu-id="8442b-121">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8442b-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8442b-122">Return value</span></span>

<span data-ttu-id="8442b-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8442b-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8442b-124">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8442b-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8442b-125">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8442b-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8442b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8442b-126">Requirements</span></span>



| <span data-ttu-id="8442b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8442b-127">Requirement</span></span> | <span data-ttu-id="8442b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8442b-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8442b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8442b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="8442b-130"><dt>D3DX10math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8442b-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="8442b-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="8442b-131">Library</span></span><br/> | <dl> <span data-ttu-id="8442b-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8442b-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8442b-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8442b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8442b-134">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="8442b-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
