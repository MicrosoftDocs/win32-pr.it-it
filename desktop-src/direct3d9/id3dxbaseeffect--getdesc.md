---
description: Ottiene la descrizione dell'effetto.
ms.assetid: 96b53b8a-0c20-4bfd-af45-626f6e0305d2
title: 'Metodo ID3DXBaseEffect:: getdesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 35fcb62e9461d419e6643c99c1879efa28fa78c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323610"
---
# <a name="id3dxbaseeffectgetdesc-method"></a><span data-ttu-id="52fe2-103">Metodo ID3DXBaseEffect:: getdesc</span><span class="sxs-lookup"><span data-stu-id="52fe2-103">ID3DXBaseEffect::GetDesc method</span></span>

<span data-ttu-id="52fe2-104">Ottiene la descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="52fe2-104">Gets the effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="52fe2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52fe2-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXEFFECT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="52fe2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="52fe2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52fe2-107">*pDesc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="52fe2-107">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52fe2-108">Tipo: **[ **D3DXEFFECT \_ desc**](d3dxeffect-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="52fe2-108">Type: **[**D3DXEFFECT\_DESC**](d3dxeffect-desc.md)\***</span></span>

<span data-ttu-id="52fe2-109">Restituisce una descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="52fe2-109">Returns a description of the effect.</span></span> <span data-ttu-id="52fe2-110">Vedere [**D3DXEFFECT \_ desc**](d3dxeffect-desc.md).</span><span class="sxs-lookup"><span data-stu-id="52fe2-110">See [**D3DXEFFECT\_DESC**](d3dxeffect-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52fe2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52fe2-111">Return value</span></span>

<span data-ttu-id="52fe2-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52fe2-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52fe2-113">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52fe2-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="52fe2-114">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="52fe2-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="52fe2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52fe2-115">Requirements</span></span>



| <span data-ttu-id="52fe2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="52fe2-116">Requirement</span></span> | <span data-ttu-id="52fe2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="52fe2-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="52fe2-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52fe2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="52fe2-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="52fe2-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="52fe2-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="52fe2-120">Library</span></span><br/> | <dl> <span data-ttu-id="52fe2-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52fe2-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="52fe2-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52fe2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52fe2-123">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="52fe2-123">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




