---
description: Suddivide i visi su una mesh, consentendo il campionamento adattivo conservativo che non eliminerà le funzionalità sulla rete.
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: 'Metodo ID3DXPRTEngine:: RobustMeshRefine (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.RobustMeshRefine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65d49fcec3072956365ce1ed8dc5d7a11ce6c826
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323437"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a><span data-ttu-id="fd1f0-103">Metodo ID3DXPRTEngine:: RobustMeshRefine</span><span class="sxs-lookup"><span data-stu-id="fd1f0-103">ID3DXPRTEngine::RobustMeshRefine method</span></span>

<span data-ttu-id="fd1f0-104">Suddivide i visi su una mesh, consentendo il campionamento adattivo conservativo che non eliminerà le funzionalità sulla rete.</span><span class="sxs-lookup"><span data-stu-id="fd1f0-104">Subdivides faces on a mesh, allowing for conservative adaptive sampling that will not eliminate features on the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd1f0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd1f0-105">Syntax</span></span>


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a><span data-ttu-id="fd1f0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd1f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd1f0-107">*MinEdgeLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd1f0-107">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd1f0-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd1f0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd1f0-109">Lunghezza minima del bordo della superficie che verrà generata nel campionamento adattivo.</span><span class="sxs-lookup"><span data-stu-id="fd1f0-109">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="fd1f0-110">Se è zero, verrà sostituito un valore predefinito ragionevole.</span><span class="sxs-lookup"><span data-stu-id="fd1f0-110">If zero, a reasonable default value will be substituted.</span></span>

</dd> <dt>

<span data-ttu-id="fd1f0-111">*MaxSubdiv* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd1f0-111">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd1f0-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd1f0-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd1f0-113">Livello massimo di suddivisione di una faccia che verrà utilizzata nel campionamento adattivo.</span><span class="sxs-lookup"><span data-stu-id="fd1f0-113">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span> <span data-ttu-id="fd1f0-114">Se è zero, verrà sostituito un valore predefinito di 5.</span><span class="sxs-lookup"><span data-stu-id="fd1f0-114">If zero, a default value of 5 will be substituted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd1f0-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd1f0-115">Return value</span></span>

<span data-ttu-id="fd1f0-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fd1f0-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fd1f0-117">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fd1f0-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fd1f0-118">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="fd1f0-118">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd1f0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd1f0-119">Requirements</span></span>



| <span data-ttu-id="fd1f0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd1f0-120">Requirement</span></span> | <span data-ttu-id="fd1f0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="fd1f0-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd1f0-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd1f0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="fd1f0-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd1f0-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fd1f0-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="fd1f0-124">Library</span></span><br/> | <dl> <span data-ttu-id="fd1f0-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd1f0-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fd1f0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd1f0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd1f0-127">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="fd1f0-127">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="fd1f0-128">**ID3DXPRTEngine::ComputeBounceAdaptive**</span><span class="sxs-lookup"><span data-stu-id="fd1f0-128">**ID3DXPRTEngine::ComputeBounceAdaptive**</span></span>](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[<span data-ttu-id="fd1f0-129">**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**</span><span class="sxs-lookup"><span data-stu-id="fd1f0-129">**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**</span></span>](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
