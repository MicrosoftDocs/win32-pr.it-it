---
description: Avviare il disegno di ogni faccia di una mappa dell'ambiente.
ms.assetid: c100e138-c5a8-49bb-9a91-e7f70410470f
title: 'Metodo ID3DXRenderToEnvMap:: Face (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.Face
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 452933c0d85a7aad2987011796ff47eff41dc32b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762346"
---
# <a name="id3dxrendertoenvmapface-method"></a><span data-ttu-id="7937f-103">Metodo ID3DXRenderToEnvMap:: Face</span><span class="sxs-lookup"><span data-stu-id="7937f-103">ID3DXRenderToEnvMap::Face method</span></span>

<span data-ttu-id="7937f-104">Avviare il disegno di ogni faccia di una mappa dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="7937f-104">Initiate the drawing of each face of an environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="7937f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7937f-105">Syntax</span></span>


```C++
HRESULT Face(
  [in] D3DCUBEMAP_FACES Face,
  [in] DWORD            MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="7937f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7937f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7937f-107">*Faccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7937f-107">*Face* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7937f-108">Tipo: **[ **D3DCUBEMAP \_ visi**](./d3dcubemap-faces.md)**</span><span class="sxs-lookup"><span data-stu-id="7937f-108">Type: **[**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md)**</span></span>

<span data-ttu-id="7937f-109">Prima faccia della mappa del cubo ambientale.</span><span class="sxs-lookup"><span data-stu-id="7937f-109">The first face of the environmental cube map.</span></span> <span data-ttu-id="7937f-110">Vedere [**D3DCUBEMAP \_ visi**](./d3dcubemap-faces.md).</span><span class="sxs-lookup"><span data-stu-id="7937f-110">See [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md).</span></span>

</dd> <dt>

<span data-ttu-id="7937f-111">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7937f-111">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7937f-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7937f-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7937f-113">Combinazione valida di uno o più flag [di \_ filtro D3DX](d3dx-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="7937f-113">A valid combination of one or more [D3DX\_FILTER](d3dx-filter.md) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7937f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7937f-114">Return value</span></span>

<span data-ttu-id="7937f-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7937f-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7937f-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7937f-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7937f-117">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="7937f-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7937f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7937f-118">Remarks</span></span>

<span data-ttu-id="7937f-119">Questo metodo deve essere chiamato una volta per ogni tipo di mappa dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="7937f-119">This method must be called once for each type of environment map.</span></span> <span data-ttu-id="7937f-120">L'unica eccezione è rappresentata da una mappa dell'ambiente cubica che richiede che questo metodo venga chiamato sei volte, una volta per ogni viso in D3DCUBEMAP \_ visi.</span><span class="sxs-lookup"><span data-stu-id="7937f-120">The only exception is a cubic environment map which requires this method to be called six times, once for each face in D3DCUBEMAP\_FACES.</span></span> <span data-ttu-id="7937f-121">Per altre informazioni, vedere [mapping dell'ambiente (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="7937f-121">For more information, see [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7937f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7937f-122">Requirements</span></span>



| <span data-ttu-id="7937f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7937f-123">Requirement</span></span> | <span data-ttu-id="7937f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7937f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7937f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7937f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7937f-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7937f-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="7937f-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="7937f-127">Library</span></span><br/> | <dl> <span data-ttu-id="7937f-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7937f-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7937f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7937f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7937f-130">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="7937f-130">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
