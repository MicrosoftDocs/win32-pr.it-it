---
description: 'Funzione D3DXVec2TransformCoord (D3dx9math.h): trasforma un vettore 2D da una determinata matrice, proiettando il risultato in w = 1.'
ms.assetid: 0c0efdf8-77df-4f4a-86ce-89e11555f4dc
title: Funzione D3DXVec2TransformCoord (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 717af9eed2c7cedae7ac292a19239e13521dfa74
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115669"
---
# <a name="d3dxvec2transformcoord-function-d3dx9mathh"></a><span data-ttu-id="34a0a-103">Funzione D3DXVec2TransformCoord (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="34a0a-103">D3DXVec2TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="34a0a-104">Trasforma un vettore 2D da una determinata matrice, proiettando il risultato in w = 1.</span><span class="sxs-lookup"><span data-stu-id="34a0a-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="34a0a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34a0a-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="34a0a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="34a0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34a0a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="34a0a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="34a0a-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="34a0a-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="34a0a-109">Puntatore alla [**struttura D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="34a0a-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="34a0a-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="34a0a-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a0a-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="34a0a-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="34a0a-112">Puntatore alla struttura [**D3DXVECTOR2 di**](d3dxvector2.md) origine.</span><span class="sxs-lookup"><span data-stu-id="34a0a-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="34a0a-113">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="34a0a-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34a0a-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="34a0a-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="34a0a-115">Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="34a0a-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34a0a-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34a0a-116">Return value</span></span>

<span data-ttu-id="34a0a-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="34a0a-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="34a0a-118">Puntatore a [**una struttura D3DXVECTOR2**](d3dxvector2.md) che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="34a0a-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="34a0a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="34a0a-119">Remarks</span></span>

<span data-ttu-id="34a0a-120">Questa funzione trasforma il *vettore, pV* (x, y, 0, 1), dalla matrice, *pM,* proiettando il risultato in w=1.</span><span class="sxs-lookup"><span data-stu-id="34a0a-120">This function transforms the vector, *pV* (x, y, 0, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="34a0a-121">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="34a0a-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="34a0a-122">In questo modo, la **funzione D3DXVec2TransformCoord** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="34a0a-122">In this way, the **D3DXVec2TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="34a0a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34a0a-123">Requirements</span></span>



| <span data-ttu-id="34a0a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="34a0a-124">Requirement</span></span> | <span data-ttu-id="34a0a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="34a0a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34a0a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34a0a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="34a0a-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="34a0a-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="34a0a-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="34a0a-128">Library</span></span><br/> | <dl> <span data-ttu-id="34a0a-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="34a0a-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="34a0a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34a0a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34a0a-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="34a0a-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="34a0a-132">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="34a0a-132">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="34a0a-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="34a0a-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




