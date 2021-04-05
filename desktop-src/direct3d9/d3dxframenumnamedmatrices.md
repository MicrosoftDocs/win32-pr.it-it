---
description: Conta il numero di frame in un sottoalbero con nomi non null.
ms.assetid: bc1cb985-acd1-4ba0-bb3c-3e86fea559da
title: Funzione D3DXFrameNumNamedMatrices (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameNumNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c2d535a41d15987df7816cfc23f1bb213b6adc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969354"
---
# <a name="d3dxframenumnamedmatrices-function"></a><span data-ttu-id="f5aa3-103">D3DXFrameNumNamedMatrices (funzione)</span><span class="sxs-lookup"><span data-stu-id="f5aa3-103">D3DXFrameNumNamedMatrices function</span></span>

<span data-ttu-id="f5aa3-104">Conta il numero di frame in un sottoalbero con nomi non null.</span><span class="sxs-lookup"><span data-stu-id="f5aa3-104">Counts number of frames in a subtree that have non-null names.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5aa3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5aa3-105">Syntax</span></span>


```C++
UINT D3DXFrameNumNamedMatrices(
  _In_ const D3DXFRAME *pFrameRoot
);
```



## <a name="parameters"></a><span data-ttu-id="f5aa3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5aa3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5aa3-107">*pFrameRoot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5aa3-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5aa3-108">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="f5aa3-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="f5aa3-109">Puntatore al nodo radice del sottoalbero.</span><span class="sxs-lookup"><span data-stu-id="f5aa3-109">Pointer to the root node of the subtree.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5aa3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5aa3-110">Return value</span></span>

<span data-ttu-id="f5aa3-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5aa3-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f5aa3-112">Restituisce il numero di frame.</span><span class="sxs-lookup"><span data-stu-id="f5aa3-112">Returns the frame count.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5aa3-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5aa3-113">Requirements</span></span>



| <span data-ttu-id="f5aa3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5aa3-114">Requirement</span></span> | <span data-ttu-id="f5aa3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f5aa3-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5aa3-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5aa3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f5aa3-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5aa3-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f5aa3-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="f5aa3-118">Library</span></span><br/> | <dl> <span data-ttu-id="f5aa3-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5aa3-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f5aa3-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5aa3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5aa3-121">Funzioni di animazione</span><span class="sxs-lookup"><span data-stu-id="f5aa3-121">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
