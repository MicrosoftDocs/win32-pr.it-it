---
description: Recupera la descrizione della superficie di rendering.
ms.assetid: 3c2612fa-540d-4d7a-9821-bf37fa3b6da4
title: 'Metodo ID3DXRenderToEnvMap:: getdesc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0b9faf5bdd4c57f7320749aef2010f457dd682e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761998"
---
# <a name="id3dxrendertoenvmapgetdesc-method"></a><span data-ttu-id="ea1ba-103">Metodo ID3DXRenderToEnvMap:: getdesc</span><span class="sxs-lookup"><span data-stu-id="ea1ba-103">ID3DXRenderToEnvMap::GetDesc method</span></span>

<span data-ttu-id="ea1ba-104">Recupera la descrizione della superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="ea1ba-104">Retrieves the description of the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea1ba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea1ba-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXRTE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="ea1ba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea1ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea1ba-107">*pDesc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ea1ba-107">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea1ba-108">Tipo: **[ **D3DXRTE \_ desc**](d3dxrte-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea1ba-108">Type: **[**D3DXRTE\_DESC**](d3dxrte-desc.md)\***</span></span>

<span data-ttu-id="ea1ba-109">Puntatore a una struttura [**D3DXRTE \_ desc**](d3dxrte-desc.md) che descrive la superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="ea1ba-109">Pointer to a [**D3DXRTE\_DESC**](d3dxrte-desc.md) structure that describes the rendering surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea1ba-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea1ba-110">Return value</span></span>

<span data-ttu-id="ea1ba-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea1ba-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea1ba-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea1ba-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ea1ba-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ea1ba-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea1ba-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea1ba-114">Requirements</span></span>



| <span data-ttu-id="ea1ba-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea1ba-115">Requirement</span></span> | <span data-ttu-id="ea1ba-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ea1ba-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea1ba-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea1ba-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ea1ba-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea1ba-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ea1ba-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="ea1ba-119">Library</span></span><br/> | <dl> <span data-ttu-id="ea1ba-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea1ba-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ea1ba-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea1ba-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea1ba-122">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="ea1ba-122">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




