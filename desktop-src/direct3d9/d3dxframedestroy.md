---
description: Elimina il sottoalbero dei frame sotto la radice, inclusa la radice.
ms.assetid: 0bbb529f-01d8-430b-a72b-4af5f7a71253
title: Funzione D3DXFrameDestroy (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameDestroy
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1c0809ff61abec6f55564ca17a116ad4c826bca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322683"
---
# <a name="d3dxframedestroy-function"></a><span data-ttu-id="a594b-103">D3DXFrameDestroy (funzione)</span><span class="sxs-lookup"><span data-stu-id="a594b-103">D3DXFrameDestroy function</span></span>

<span data-ttu-id="a594b-104">Elimina il sottoalbero dei frame sotto la radice, inclusa la radice.</span><span class="sxs-lookup"><span data-stu-id="a594b-104">Destroys the subtree of frames under the root, including the root.</span></span>

## <a name="syntax"></a><span data-ttu-id="a594b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a594b-105">Syntax</span></span>


```C++
HRESULT D3DXFrameDestroy(
  _In_ LPD3DXFRAME             pFrameRoot,
  _In_ LPD3DXALLOCATEHIERARCHY pAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="a594b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a594b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a594b-107">*pFrameRoot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a594b-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a594b-108">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="a594b-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="a594b-109">Puntatore al nodo radice.</span><span class="sxs-lookup"><span data-stu-id="a594b-109">Pointer to the root node.</span></span>

</dd> <dt>

<span data-ttu-id="a594b-110">*pAlloc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a594b-110">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a594b-111">Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="a594b-111">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="a594b-112">Interfaccia di allocazione utilizzata per deallocare i nodi della gerarchia dei frame.</span><span class="sxs-lookup"><span data-stu-id="a594b-112">Allocation interface used to deallocate nodes of the frame hierarchy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a594b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a594b-113">Return value</span></span>

<span data-ttu-id="a594b-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a594b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a594b-115">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a594b-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a594b-116">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="a594b-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="a594b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a594b-117">Requirements</span></span>



| <span data-ttu-id="a594b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a594b-118">Requirement</span></span> | <span data-ttu-id="a594b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a594b-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a594b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a594b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a594b-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a594b-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a594b-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="a594b-122">Library</span></span><br/> | <dl> <span data-ttu-id="a594b-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a594b-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a594b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a594b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a594b-125">Funzioni di animazione</span><span class="sxs-lookup"><span data-stu-id="a594b-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




