---
description: 'Funzione D3DXVec3TransformNormal (D3dx9math.h): trasforma la normale del vettore 3D in base alla matrice specificata.'
ms.assetid: aa9531e1-b77a-4aad-8d59-2677908cb978
title: Funzione D3DXVec3TransformNormal (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50fb09a4619be9c3dbcff98bc939d6f99ad33bd4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115619"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a><span data-ttu-id="6e917-103">Funzione D3DXVec3TransformNormal (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="6e917-103">D3DXVec3TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="6e917-104">Trasforma la normale del vettore 3D in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="6e917-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e917-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e917-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="6e917-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e917-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e917-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6e917-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e917-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e917-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6e917-109">Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6e917-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6e917-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6e917-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e917-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6e917-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6e917-112">Puntatore alla struttura [**D3DXVECTOR3 di**](d3dxvector3.md) origine.</span><span class="sxs-lookup"><span data-stu-id="6e917-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6e917-113">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6e917-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e917-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6e917-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6e917-115">Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="6e917-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e917-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e917-116">Return value</span></span>

<span data-ttu-id="6e917-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6e917-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6e917-118">Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="6e917-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e917-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e917-119">Remarks</span></span>

<span data-ttu-id="6e917-120">Questa funzione trasforma il vettore (*pV*->x, *pV*->y, *pV*->z, 0) dalla matrice a cui punta *pM*.</span><span class="sxs-lookup"><span data-stu-id="6e917-120">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="6e917-121">Se si vuole trasformare una normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice che si userebbe per trasformare un punto.</span><span class="sxs-lookup"><span data-stu-id="6e917-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="6e917-122">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="6e917-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6e917-123">In questo modo, la **funzione D3DXVec3TransformNormal** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="6e917-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e917-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e917-124">Requirements</span></span>



| <span data-ttu-id="6e917-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e917-125">Requirement</span></span> | <span data-ttu-id="6e917-126">Valore</span><span class="sxs-lookup"><span data-stu-id="6e917-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e917-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e917-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6e917-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6e917-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6e917-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="6e917-129">Library</span></span><br/> | <dl> <span data-ttu-id="6e917-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e917-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6e917-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e917-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e917-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="6e917-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




