---
description: Recupera i parametri della superficie di rendering.
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: 'Metodo ID3DXRenderToSurface:: getdesc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00824c6b418a3e6707ebfd588d8d32d4e38f173d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235192"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a><span data-ttu-id="b2a2b-103">Metodo ID3DXRenderToSurface:: getdesc</span><span class="sxs-lookup"><span data-stu-id="b2a2b-103">ID3DXRenderToSurface::GetDesc method</span></span>

<span data-ttu-id="b2a2b-104">Recupera i parametri della superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="b2a2b-104">Retrieves the parameters of the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2a2b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2a2b-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a><span data-ttu-id="b2a2b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2a2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2a2b-107">*pParameters* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b2a2b-107">*pParameters* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2a2b-108">Tipo: **[ **D3DXRTS \_ desc**](d3dxrts-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="b2a2b-108">Type: **[**D3DXRTS\_DESC**](d3dxrts-desc.md)\***</span></span>

<span data-ttu-id="b2a2b-109">Puntatore a una struttura [**D3DXRTS \_ desc**](d3dxrts-desc.md) , che descrive i parametri della superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="b2a2b-109">Pointer to a [**D3DXRTS\_DESC**](d3dxrts-desc.md) structure, describing the parameters of the render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2a2b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2a2b-110">Return value</span></span>

<span data-ttu-id="b2a2b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2a2b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2a2b-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b2a2b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b2a2b-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b2a2b-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2a2b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2a2b-114">Requirements</span></span>



| <span data-ttu-id="b2a2b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2a2b-115">Requirement</span></span> | <span data-ttu-id="b2a2b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b2a2b-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a2b-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2a2b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b2a2b-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2a2b-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="b2a2b-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="b2a2b-119">Library</span></span><br/> | <dl> <span data-ttu-id="b2a2b-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2a2b-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b2a2b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2a2b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2a2b-122">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="b2a2b-122">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 




