---
description: 'Funzione D3DXVec3TransformCoord (D3dx9math.h): trasforma un vettore 3D in base a una determinata matrice, proiettando di nuovo il risultato in w = 1.'
ms.assetid: 4075b067-1e64-46c9-be73-5fa765c9cb9d
title: Funzione D3DXVec3TransformCoord (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4e3514d4717262a7afab7ae808d747de3a1b635
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115629"
---
# <a name="d3dxvec3transformcoord-function-d3dx9mathh"></a><span data-ttu-id="5e3ad-103">Funzione D3DXVec3TransformCoord (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="5e3ad-103">D3DXVec3TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="5e3ad-104">Trasforma un vettore 3D in base a una determinata matrice, proiettando il risultato in w = 1.</span><span class="sxs-lookup"><span data-stu-id="5e3ad-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e3ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e3ad-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="5e3ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e3ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e3ad-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5e3ad-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3ad-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5e3ad-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5e3ad-109">Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5e3ad-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5e3ad-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5e3ad-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3ad-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5e3ad-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5e3ad-112">Puntatore alla struttura [**D3DXVECTOR3 di**](d3dxvector3.md) origine.</span><span class="sxs-lookup"><span data-stu-id="5e3ad-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5e3ad-113">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5e3ad-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e3ad-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5e3ad-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5e3ad-115">Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="5e3ad-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e3ad-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e3ad-116">Return value</span></span>

<span data-ttu-id="5e3ad-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5e3ad-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5e3ad-118">Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="5e3ad-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e3ad-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e3ad-119">Remarks</span></span>

<span data-ttu-id="5e3ad-120">Questa funzione trasforma il *vettore, pV* (x, y, z, 1), dalla matrice, *pM,* proiettando il risultato di nuovo in w=1.</span><span class="sxs-lookup"><span data-stu-id="5e3ad-120">This function transforms the vector, *pV* (x, y, z, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="5e3ad-121">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="5e3ad-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5e3ad-122">In questo modo, la **funzione D3DXVec3TransformCoord** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="5e3ad-122">In this way, the **D3DXVec3TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e3ad-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e3ad-123">Requirements</span></span>



| <span data-ttu-id="5e3ad-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e3ad-124">Requirement</span></span> | <span data-ttu-id="5e3ad-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5e3ad-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e3ad-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e3ad-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5e3ad-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5e3ad-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5e3ad-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="5e3ad-128">Library</span></span><br/> | <dl> <span data-ttu-id="5e3ad-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e3ad-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5e3ad-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e3ad-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e3ad-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="5e3ad-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5e3ad-132">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="5e3ad-132">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
</dt> <dt>

[<span data-ttu-id="5e3ad-133">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="5e3ad-133">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
</dt> </dl>

 

 




