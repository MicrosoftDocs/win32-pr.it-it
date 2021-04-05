---
description: Trasforma il vettore 2D normale in base alla matrice specificata.
ms.assetid: aa9adf6d-5aae-4acf-bbd9-f5c14d90470e
title: Funzione D3DXVec2TransformNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 154268b272f6cac00acb1d770d3c919cf65d6297
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969380"
---
# <a name="d3dxvec2transformnormal-function-d3dx9mathh"></a><span data-ttu-id="dae47-103">Funzione D3DXVec2TransformNormal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="dae47-103">D3DXVec2TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="dae47-104">Trasforma il vettore 2D normale in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="dae47-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="dae47-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dae47-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="dae47-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dae47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dae47-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="dae47-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dae47-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="dae47-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="dae47-109">Puntatore alla struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dae47-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="dae47-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dae47-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dae47-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="dae47-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="dae47-112">Puntatore alla struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="dae47-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dae47-113">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dae47-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dae47-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="dae47-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="dae47-115">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="dae47-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dae47-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dae47-116">Return value</span></span>

<span data-ttu-id="dae47-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="dae47-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="dae47-118">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="dae47-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="dae47-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="dae47-119">Remarks</span></span>

<span data-ttu-id="dae47-120">Questa funzione trasforma il vettore (*PV-*>x, *PV-*>y, 0, 0) dalla matrice a cui fa riferimento il *PM*.</span><span class="sxs-lookup"><span data-stu-id="dae47-120">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="dae47-121">Se si vuole trasformare un normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice da usare per trasformare un punto.</span><span class="sxs-lookup"><span data-stu-id="dae47-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="dae47-122">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="dae47-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="dae47-123">In questo modo, la funzione **D3DXVec2TransformNormal** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="dae47-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dae47-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dae47-124">Requirements</span></span>



| <span data-ttu-id="dae47-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="dae47-125">Requirement</span></span> | <span data-ttu-id="dae47-126">Valore</span><span class="sxs-lookup"><span data-stu-id="dae47-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dae47-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dae47-127">Header</span></span><br/>  | <dl> <span data-ttu-id="dae47-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="dae47-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="dae47-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="dae47-129">Library</span></span><br/> | <dl> <span data-ttu-id="dae47-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dae47-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dae47-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dae47-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae47-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="dae47-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="dae47-133">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="dae47-133">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="dae47-134">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="dae47-134">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> </dl>

 

 




