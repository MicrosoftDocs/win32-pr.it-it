---
description: Ripristinare tutte le destinazioni di rendering e, se necessario, comporre tutti i visi sottoposti a rendering nella superficie della mappa dell'ambiente.
ms.assetid: 57c73787-36e7-4088-b5ff-78894e3a5d90
title: 'Metodo ID3DXRenderToEnvMap:: end (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20e62a9d794738ae81ae84a665165f6034958f0c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354564"
---
# <a name="id3dxrendertoenvmapend-method"></a><span data-ttu-id="a94c4-103">Metodo ID3DXRenderToEnvMap:: end</span><span class="sxs-lookup"><span data-stu-id="a94c4-103">ID3DXRenderToEnvMap::End method</span></span>

<span data-ttu-id="a94c4-104">Ripristinare tutte le destinazioni di rendering e, se necessario, comporre tutti i visi sottoposti a rendering nella superficie della mappa dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="a94c4-104">Restore all render targets and, if needed, compose all the rendered faces into the environment map surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a94c4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a94c4-105">Syntax</span></span>


```C++
HRESULT End(
  [in] DWORD MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="a94c4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a94c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a94c4-107">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a94c4-107">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a94c4-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a94c4-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a94c4-109">Combinazione valida di uno o più flag [di \_ filtro D3DX](d3dx-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="a94c4-109">A valid combination of one or more [D3DX\_FILTER](d3dx-filter.md) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a94c4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a94c4-110">Return value</span></span>

<span data-ttu-id="a94c4-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a94c4-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a94c4-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a94c4-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a94c4-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a94c4-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a94c4-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a94c4-114">Requirements</span></span>



| <span data-ttu-id="a94c4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a94c4-115">Requirement</span></span> | <span data-ttu-id="a94c4-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a94c4-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a94c4-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a94c4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a94c4-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a94c4-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a94c4-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="a94c4-119">Library</span></span><br/> | <dl> <span data-ttu-id="a94c4-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a94c4-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a94c4-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a94c4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a94c4-122">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="a94c4-122">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> <dt>

[<span data-ttu-id="a94c4-123">**ID3DXRenderToEnvMap:: Face**</span><span class="sxs-lookup"><span data-stu-id="a94c4-123">**ID3DXRenderToEnvMap::Face**</span></span>](id3dxrendertoenvmap--face.md)
</dt> </dl>

 

 
