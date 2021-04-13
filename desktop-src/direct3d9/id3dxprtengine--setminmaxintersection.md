---
description: Imposta le distanze minime e massime di intersezione tra oggetti 3D.
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: 'Metodo ID3DXPRTEngine:: SetMinMaxIntersection (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68845f713289c524afc844037ca305909e5b89b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355149"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a><span data-ttu-id="a8e8e-103">Metodo ID3DXPRTEngine:: SetMinMaxIntersection</span><span class="sxs-lookup"><span data-stu-id="a8e8e-103">ID3DXPRTEngine::SetMinMaxIntersection method</span></span>

<span data-ttu-id="a8e8e-104">Imposta le distanze minime e massime di intersezione tra oggetti 3D.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-104">Sets the minimum and maximum distances of intersection between 3D objects.</span></span> <span data-ttu-id="a8e8e-105">Questi valori di distanza possono essere utilizzati per controllare la distanza minima o massima che gli oggetti possono nascondere o rispecchiare la luce.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-105">These distance values can be used to control the minimum or maximum distance that objects can shadow or reflect light.</span></span> <span data-ttu-id="a8e8e-106">Ad esempio, il metodo può essere usato per limitare l'ombreggiatura delle funzionalità vicine di un modello 3D.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-106">For example, the method can be used to limit the shadowing of nearby features of a 3D model.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8e8e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8e8e-107">Syntax</span></span>


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a><span data-ttu-id="a8e8e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8e8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8e8e-109">*fMin* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8e8e-109">*fMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8e8e-110">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8e8e-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8e8e-111">Distanza di intersezione minima.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-111">Minimum intersection distance.</span></span> <span data-ttu-id="a8e8e-112">Deve essere positivo e minore di fMax.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-112">Must be positive and less than fMax.</span></span>

</dd> <dt>

<span data-ttu-id="a8e8e-113">*fMax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8e8e-113">*fMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8e8e-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8e8e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8e8e-115">Distanza di intersezione massima.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-115">Maximum intersection distance.</span></span> <span data-ttu-id="a8e8e-116">Se 0,0 f, verrà utilizzato il valore precedente; in caso contrario, deve essere maggiore di fMin.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-116">If 0.0f, the previous value will be used; otherwise, must be greater than fMin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8e8e-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8e8e-117">Return value</span></span>

<span data-ttu-id="a8e8e-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8e8e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8e8e-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a8e8e-120">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8e8e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8e8e-121">Remarks</span></span>

<span data-ttu-id="a8e8e-122">Questo metodo non può essere usato nelle simulazioni dei PRT (pre-Computed Radiance Transfer) eseguite nella GPU.</span><span class="sxs-lookup"><span data-stu-id="a8e8e-122">This method cannot be used in precomputed radiance transfer (PRT) simulations that run in the GPU.</span></span> <span data-ttu-id="a8e8e-123">Vedere [**ID3DXPRTEngine:: ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).</span><span class="sxs-lookup"><span data-stu-id="a8e8e-123">See [**ID3DXPRTEngine::ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8e8e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8e8e-124">Requirements</span></span>



| <span data-ttu-id="a8e8e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8e8e-125">Requirement</span></span> | <span data-ttu-id="a8e8e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a8e8e-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e8e-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8e8e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a8e8e-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8e8e-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a8e8e-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="a8e8e-129">Library</span></span><br/> | <dl> <span data-ttu-id="a8e8e-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8e8e-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8e8e-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8e8e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e8e-132">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="a8e8e-132">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
