---
description: Determina il prodotto scalare di due vettori 2D.
ms.assetid: ae77ff29-44be-4b67-9c63-aaffa4fe8d59
title: Funzione D3DXVec2Dot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 79b65127c415695b3df9f927b6edff8fcdd5c58d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322462"
---
# <a name="d3dxvec2dot-function"></a><span data-ttu-id="2048d-103">D3DXVec2Dot (funzione)</span><span class="sxs-lookup"><span data-stu-id="2048d-103">D3DXVec2Dot function</span></span>

<span data-ttu-id="2048d-104">Determina il prodotto scalare di due vettori 2D.</span><span class="sxs-lookup"><span data-stu-id="2048d-104">Determines the dot product of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="2048d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2048d-105">Syntax</span></span>


```C++
FLOAT D3DXVec2Dot(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="2048d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2048d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2048d-107">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2048d-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2048d-108">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="2048d-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2048d-109">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="2048d-109">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2048d-110">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2048d-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2048d-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="2048d-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2048d-112">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="2048d-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2048d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2048d-113">Return value</span></span>

<span data-ttu-id="2048d-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2048d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2048d-115">Prodotto scalare.</span><span class="sxs-lookup"><span data-stu-id="2048d-115">The dot product.</span></span>

## <a name="requirements"></a><span data-ttu-id="2048d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2048d-116">Requirements</span></span>



| <span data-ttu-id="2048d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2048d-117">Requirement</span></span> | <span data-ttu-id="2048d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2048d-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2048d-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2048d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2048d-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2048d-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2048d-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="2048d-121">Library</span></span><br/> | <dl> <span data-ttu-id="2048d-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2048d-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2048d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2048d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2048d-124">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="2048d-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2048d-125">**D3DXVec2CCW**</span><span class="sxs-lookup"><span data-stu-id="2048d-125">**D3DXVec2CCW**</span></span>](d3dxvec2ccw.md)
</dt> </dl>

 

 
