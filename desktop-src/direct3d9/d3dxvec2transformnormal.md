---
description: 'Funzione D3DXVec2TransformNormal (D3dx9math.h): trasforma la normale vettore 2D in base alla matrice specificata.'
ms.assetid: aa9adf6d-5aae-4acf-bbd9-f5c14d90470e
title: Funzione D3DXVec2TransformNormal (D3dx9math.h)
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
ms.openlocfilehash: c8ed31300027fcb2e827988809cce1c50dbf77de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097909"
---
# <a name="d3dxvec2transformnormal-function-d3dx9mathh"></a><span data-ttu-id="32c94-103">Funzione D3DXVec2TransformNormal (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="32c94-103">D3DXVec2TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="32c94-104">Trasforma la normale del vettore 2D in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="32c94-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="32c94-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32c94-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="32c94-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="32c94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32c94-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="32c94-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="32c94-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="32c94-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="32c94-109">Puntatore alla [**struttura D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="32c94-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="32c94-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="32c94-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32c94-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="32c94-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="32c94-112">Puntatore alla struttura [**D3DXVECTOR2 di**](d3dxvector2.md) origine.</span><span class="sxs-lookup"><span data-stu-id="32c94-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="32c94-113">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="32c94-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32c94-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="32c94-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="32c94-115">Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="32c94-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32c94-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32c94-116">Return value</span></span>

<span data-ttu-id="32c94-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="32c94-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="32c94-118">Puntatore a [**una struttura D3DXVECTOR2**](d3dxvector2.md) che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="32c94-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="32c94-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="32c94-119">Remarks</span></span>

<span data-ttu-id="32c94-120">Questa funzione trasforma il vettore (*pV-*>x, *pV-*>y, 0, 0) dalla matrice a cui punta *pM*.</span><span class="sxs-lookup"><span data-stu-id="32c94-120">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="32c94-121">Se si vuole trasformare una normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice da usare per trasformare un punto.</span><span class="sxs-lookup"><span data-stu-id="32c94-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="32c94-122">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="32c94-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="32c94-123">In questo modo, la **funzione D3DXVec2TransformNormal** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="32c94-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="32c94-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32c94-124">Requirements</span></span>



| <span data-ttu-id="32c94-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="32c94-125">Requirement</span></span> | <span data-ttu-id="32c94-126">Valore</span><span class="sxs-lookup"><span data-stu-id="32c94-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32c94-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32c94-127">Header</span></span><br/>  | <dl> <span data-ttu-id="32c94-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="32c94-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="32c94-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="32c94-129">Library</span></span><br/> | <dl> <span data-ttu-id="32c94-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="32c94-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="32c94-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32c94-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32c94-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="32c94-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="32c94-133">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="32c94-133">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="32c94-134">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="32c94-134">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> </dl>

 

 




