---
description: Data una gerarchia di frame, registra tutte le matrici denominate nel mixer animazione.
ms.assetid: df0560c2-4417-4d54-94c8-031521b32189
title: Funzione D3DXFrameRegisterNamedMatrices (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameRegisterNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8496f467e668939c5d5aa0e90266ab012d436038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322679"
---
# <a name="d3dxframeregisternamedmatrices-function"></a><span data-ttu-id="a8b5c-103">D3DXFrameRegisterNamedMatrices (funzione)</span><span class="sxs-lookup"><span data-stu-id="a8b5c-103">D3DXFrameRegisterNamedMatrices function</span></span>

<span data-ttu-id="a8b5c-104">Data una gerarchia di frame, registra tutte le matrici denominate nel mixer animazione.</span><span class="sxs-lookup"><span data-stu-id="a8b5c-104">Given a frame hierarchy, registers all the named matrices in the animation mixer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b5c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8b5c-105">Syntax</span></span>


```C++
HRESULT D3DXFrameRegisterNamedMatrices(
  _In_ LPD3DXFRAME               pFrameRoot,
  _In_ LPD3DXANIMATIONCONTROLLER pAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="a8b5c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8b5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b5c-107">*pFrameRoot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8b5c-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b5c-108">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="a8b5c-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="a8b5c-109">Nodo di livello superiore nella gerarchia dei frame.</span><span class="sxs-lookup"><span data-stu-id="a8b5c-109">The top level node in the frame hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="a8b5c-110">*pAnimController* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8b5c-110">*pAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b5c-111">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="a8b5c-111">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="a8b5c-112">Puntatore all'oggetto controller di animazione.</span><span class="sxs-lookup"><span data-stu-id="a8b5c-112">Pointer to the animation controller object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b5c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8b5c-113">Return value</span></span>

<span data-ttu-id="a8b5c-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8b5c-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8b5c-115">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a8b5c-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a8b5c-116">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="a8b5c-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b5c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8b5c-117">Requirements</span></span>



| <span data-ttu-id="a8b5c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8b5c-118">Requirement</span></span> | <span data-ttu-id="a8b5c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a8b5c-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b5c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8b5c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a8b5c-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b5c-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a8b5c-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="a8b5c-122">Library</span></span><br/> | <dl> <span data-ttu-id="a8b5c-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8b5c-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8b5c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8b5c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b5c-125">Funzioni di animazione</span><span class="sxs-lookup"><span data-stu-id="a8b5c-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




