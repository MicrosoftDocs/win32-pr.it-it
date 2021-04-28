---
description: 'Funzione D3DXComputeBoundingSphere (D3DX9Mesh.h): calcola una sfera di delimitazione per la mesh.'
ms.assetid: efa1365b-fe3a-4165-a3cb-bc1cd2ba03c0
title: Funzione D3DXComputeBoundingSphere (D3DX9Mesh.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dbfccb13dfe15b06de98ddba114cdc62c5f4ec05
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115819"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx9meshh"></a><span data-ttu-id="3a817-103">Funzione D3DXComputeBoundingSphere (D3DX9Mesh.h)</span><span class="sxs-lookup"><span data-stu-id="3a817-103">D3DXComputeBoundingSphere function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="3a817-104">Calcola una sfera di delimitazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="3a817-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a817-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a817-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pCenter,
  _Out_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="3a817-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a817-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a817-107">*pFirstPosition* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3a817-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a817-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3a817-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3a817-109">Puntatore alla prima posizione.</span><span class="sxs-lookup"><span data-stu-id="3a817-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="3a817-110">*NumVertices* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3a817-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a817-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a817-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a817-112">Numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="3a817-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="3a817-113">*dwStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3a817-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a817-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a817-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a817-115">Numero di byte tra i vettori di posizione.</span><span class="sxs-lookup"><span data-stu-id="3a817-115">Number of bytes between position vectors.</span></span> <span data-ttu-id="3a817-116">Usare [**GetNumBytesPerVertex,**](id3dxbasemesh--getnumbytespervertex.md) [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md)o [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) per ottenere lo stride del vertice.</span><span class="sxs-lookup"><span data-stu-id="3a817-116">Use [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md), or [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) to get the vertex stride.</span></span>

</dd> <dt>

<span data-ttu-id="3a817-117">*pCenter* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3a817-117">*pCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a817-118">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="3a817-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3a817-119">[**Struttura D3DXVECTOR3,**](d3dxvector3.md) che definisce il centro delle coordinate della sfera di delimitazione restituita.</span><span class="sxs-lookup"><span data-stu-id="3a817-119">[**D3DXVECTOR3**](d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="3a817-120">*pRadius* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3a817-120">*pRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a817-121">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3a817-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3a817-122">Raggio della sfera di delimitazione restituita.</span><span class="sxs-lookup"><span data-stu-id="3a817-122">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a817-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a817-123">Return value</span></span>

<span data-ttu-id="3a817-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a817-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a817-125">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3a817-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3a817-126">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3a817-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a817-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a817-127">Requirements</span></span>



| <span data-ttu-id="3a817-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a817-128">Requirement</span></span> | <span data-ttu-id="3a817-129">Valore</span><span class="sxs-lookup"><span data-stu-id="3a817-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a817-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a817-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3a817-131"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="3a817-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3a817-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="3a817-132">Library</span></span><br/> | <dl> <span data-ttu-id="3a817-133"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a817-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3a817-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a817-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a817-135">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="3a817-135">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
