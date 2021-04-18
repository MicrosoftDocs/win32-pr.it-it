---
description: Trova il frame figlio di un frame radice.
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: Funzione D3DXFrameFind (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameFind
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 82b8c56c93f19c99441b93707fac2a0c150e0c38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322680"
---
# <a name="d3dxframefind-function"></a><span data-ttu-id="3f0ea-103">D3DXFrameFind (funzione)</span><span class="sxs-lookup"><span data-stu-id="3f0ea-103">D3DXFrameFind function</span></span>

<span data-ttu-id="3f0ea-104">Trova il frame figlio di un frame radice.</span><span class="sxs-lookup"><span data-stu-id="3f0ea-104">Finds the child frame of a root frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f0ea-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f0ea-105">Syntax</span></span>


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a><span data-ttu-id="3f0ea-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f0ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f0ea-107">*pFrameRoot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f0ea-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0ea-108">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="3f0ea-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="3f0ea-109">Puntatore al frame radice.</span><span class="sxs-lookup"><span data-stu-id="3f0ea-109">Pointer to the root frame.</span></span> <span data-ttu-id="3f0ea-110">Vedere [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="3f0ea-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="3f0ea-111">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f0ea-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f0ea-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f0ea-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f0ea-113">Nome del fotogramma figlio da trovare.</span><span class="sxs-lookup"><span data-stu-id="3f0ea-113">Name of the child frame to find.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f0ea-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f0ea-114">Return value</span></span>

<span data-ttu-id="3f0ea-115">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="3f0ea-115">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="3f0ea-116">Restituisce il frame figlio se viene trovato; in caso contrario, **null** .</span><span class="sxs-lookup"><span data-stu-id="3f0ea-116">Returns the child frame if it is found, or **NULL** otherwise.</span></span> <span data-ttu-id="3f0ea-117">Vedere [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="3f0ea-117">See [**D3DXFRAME**](d3dxframe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f0ea-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f0ea-118">Requirements</span></span>



| <span data-ttu-id="3f0ea-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f0ea-119">Requirement</span></span> | <span data-ttu-id="3f0ea-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3f0ea-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f0ea-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f0ea-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3f0ea-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f0ea-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3f0ea-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="3f0ea-123">Library</span></span><br/> | <dl> <span data-ttu-id="3f0ea-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f0ea-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3f0ea-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f0ea-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f0ea-126">Funzioni di animazione</span><span class="sxs-lookup"><span data-stu-id="3f0ea-126">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
