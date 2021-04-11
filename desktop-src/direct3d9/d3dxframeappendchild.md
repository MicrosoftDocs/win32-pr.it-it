---
description: Aggiunge un frame figlio a un frame.
ms.assetid: a04c9bbe-8e54-467a-8e02-27c6469f4dac
title: Funzione D3DXFrameAppendChild (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameAppendChild
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a27c8b31abf982c7cfaaa2a53d49d8859fa2c8bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235017"
---
# <a name="d3dxframeappendchild-function"></a><span data-ttu-id="e26fd-103">D3DXFrameAppendChild (funzione)</span><span class="sxs-lookup"><span data-stu-id="e26fd-103">D3DXFrameAppendChild function</span></span>

<span data-ttu-id="e26fd-104">Aggiunge un frame figlio a un frame.</span><span class="sxs-lookup"><span data-stu-id="e26fd-104">Adds a child frame to a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="e26fd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e26fd-105">Syntax</span></span>


```C++
HRESULT D3DXFrameAppendChild(
  _In_       LPD3DXFRAME pFrameParent,
  _In_ const D3DXFRAME   *pFrameChild
);
```



## <a name="parameters"></a><span data-ttu-id="e26fd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e26fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e26fd-107">*pFrameParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e26fd-107">*pFrameParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e26fd-108">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="e26fd-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="e26fd-109">Puntatore al nodo padre.</span><span class="sxs-lookup"><span data-stu-id="e26fd-109">Pointer to the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="e26fd-110">*pFrameChild* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e26fd-110">*pFrameChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e26fd-111">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="e26fd-111">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="e26fd-112">Puntatore al nodo figlio.</span><span class="sxs-lookup"><span data-stu-id="e26fd-112">Pointer to the child node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e26fd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e26fd-113">Return value</span></span>

<span data-ttu-id="e26fd-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e26fd-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e26fd-115">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e26fd-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e26fd-116">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="e26fd-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e26fd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e26fd-117">Requirements</span></span>



| <span data-ttu-id="e26fd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e26fd-118">Requirement</span></span> | <span data-ttu-id="e26fd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e26fd-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e26fd-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e26fd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e26fd-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e26fd-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e26fd-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="e26fd-122">Library</span></span><br/> | <dl> <span data-ttu-id="e26fd-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e26fd-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e26fd-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e26fd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e26fd-125">Funzioni di animazione</span><span class="sxs-lookup"><span data-stu-id="e26fd-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




