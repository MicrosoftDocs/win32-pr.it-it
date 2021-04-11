---
description: Ridimensiona un vettore 2D.
ms.assetid: 1887bc48-3766-42d7-840b-1e29d78db4ce
title: Funzione D3DXVec2Scale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 941e85763b15724e3c810c0416b5b142c9d95913
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354599"
---
# <a name="d3dxvec2scale-function"></a><span data-ttu-id="4300d-103">D3DXVec2Scale (funzione)</span><span class="sxs-lookup"><span data-stu-id="4300d-103">D3DXVec2Scale function</span></span>

<span data-ttu-id="4300d-104">Ridimensiona un vettore 2D.</span><span class="sxs-lookup"><span data-stu-id="4300d-104">Scales a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="4300d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4300d-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Scale(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="4300d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4300d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4300d-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4300d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4300d-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="4300d-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4300d-109">Puntatore alla struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4300d-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4300d-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4300d-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4300d-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="4300d-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4300d-112">Puntatore alla struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="4300d-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4300d-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4300d-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4300d-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4300d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4300d-115">Valore di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="4300d-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4300d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4300d-116">Return value</span></span>

<span data-ttu-id="4300d-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="4300d-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4300d-118">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta il vettore ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="4300d-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="4300d-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="4300d-119">Remarks</span></span>

<span data-ttu-id="4300d-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="4300d-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4300d-121">In questo modo, la funzione **D3DXVec2Scale** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="4300d-121">In this way, the **D3DXVec2Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4300d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4300d-122">Requirements</span></span>



| <span data-ttu-id="4300d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4300d-123">Requirement</span></span> | <span data-ttu-id="4300d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4300d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4300d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4300d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4300d-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4300d-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4300d-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="4300d-127">Library</span></span><br/> | <dl> <span data-ttu-id="4300d-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4300d-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4300d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4300d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4300d-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="4300d-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4300d-131">**D3DXVec2Add**</span><span class="sxs-lookup"><span data-stu-id="4300d-131">**D3DXVec2Add**</span></span>](d3dxvec2add.md)
</dt> <dt>

[<span data-ttu-id="4300d-132">**D3DXVec2Subtract**</span><span class="sxs-lookup"><span data-stu-id="4300d-132">**D3DXVec2Subtract**</span></span>](d3dxvec2subtract.md)
</dt> </dl>

 

 
