---
description: Restituisce il numero di set di animazioni attualmente registrati nel controller di animazione.
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: 'Metodo ID3DXAnimationController:: GetNumAnimationSets (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetNumAnimationSets
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5baedb0ea30d51cbd659e597cb000a434ec1632
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322147"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a><span data-ttu-id="2d5fe-103">Metodo ID3DXAnimationController:: GetNumAnimationSets</span><span class="sxs-lookup"><span data-stu-id="2d5fe-103">ID3DXAnimationController::GetNumAnimationSets method</span></span>

<span data-ttu-id="2d5fe-104">Restituisce il numero di set di animazioni attualmente registrati nel controller di animazione.</span><span class="sxs-lookup"><span data-stu-id="2d5fe-104">Returns the number of animation sets currently registered in the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d5fe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d5fe-105">Syntax</span></span>


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a><span data-ttu-id="2d5fe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d5fe-106">Parameters</span></span>

<span data-ttu-id="2d5fe-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2d5fe-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2d5fe-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d5fe-108">Return value</span></span>

<span data-ttu-id="2d5fe-109">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d5fe-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d5fe-110">Numero di set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="2d5fe-110">Number of animation sets.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d5fe-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d5fe-111">Remarks</span></span>

<span data-ttu-id="2d5fe-112">Il controller contiene un numero qualsiasi di set di animazioni e tracce.</span><span class="sxs-lookup"><span data-stu-id="2d5fe-112">The controller contains any number of animations sets and tracks.</span></span> <span data-ttu-id="2d5fe-113">I set di animazioni possono essere registrati con [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md).</span><span class="sxs-lookup"><span data-stu-id="2d5fe-113">Animation sets can be registered with [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md).</span></span> <span data-ttu-id="2d5fe-114">Un controller di animazione creato da una chiamata a [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) registrerà automaticamente i set di animazioni caricati.</span><span class="sxs-lookup"><span data-stu-id="2d5fe-114">An animation controller created by a call to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) will automatically register loaded animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d5fe-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d5fe-115">Requirements</span></span>



| <span data-ttu-id="2d5fe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d5fe-116">Requirement</span></span> | <span data-ttu-id="2d5fe-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2d5fe-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d5fe-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d5fe-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2d5fe-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d5fe-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2d5fe-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="2d5fe-120">Library</span></span><br/> | <dl> <span data-ttu-id="2d5fe-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d5fe-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2d5fe-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d5fe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d5fe-123">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="2d5fe-123">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
