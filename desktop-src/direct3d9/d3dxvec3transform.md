---
description: 'Funzione D3DXVec3Transform (D3dx9math.h): trasforma il vettore (x, y, z, 1) in base a una determinata matrice.'
ms.assetid: 5b290c4c-22f1-4086-8e5e-f995757ef193
title: Funzione D3DXVec3Transform (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5128be3fd9e0409b403006fdb1de3c9c48f6aee4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115639"
---
# <a name="d3dxvec3transform-function-d3dx9mathh"></a><span data-ttu-id="1eab8-103">Funzione D3DXVec3Transform (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="1eab8-103">D3DXVec3Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="1eab8-104">Trasforma il vettore (x, y, z, 1) in base a una determinata matrice.</span><span class="sxs-lookup"><span data-stu-id="1eab8-104">Transforms vector (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eab8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1eab8-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="1eab8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1eab8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eab8-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1eab8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eab8-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eab8-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1eab8-109">Puntatore alla [**struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1eab8-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1eab8-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1eab8-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eab8-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1eab8-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1eab8-112">Puntatore alla struttura [**D3DXVECTOR3 di**](d3dxvector3.md) origine.</span><span class="sxs-lookup"><span data-stu-id="1eab8-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1eab8-113">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1eab8-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eab8-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1eab8-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1eab8-115">Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="1eab8-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eab8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1eab8-116">Return value</span></span>

<span data-ttu-id="1eab8-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1eab8-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1eab8-118">Puntatore a [**una struttura D3DXVECTOR4**](d3dxvector4.md) che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="1eab8-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eab8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="1eab8-119">Remarks</span></span>

<span data-ttu-id="1eab8-120">Questa funzione trasforma il *vettore, pV* (x, y, z, 1), dalla matrice *pM*.</span><span class="sxs-lookup"><span data-stu-id="1eab8-120">This function transforms the vector, *pV* (x, y, z, 1), by the matrix *pM*.</span></span>

<span data-ttu-id="1eab8-121">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="1eab8-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1eab8-122">In questo modo, la **funzione D3DXVec3Transform** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="1eab8-122">In this way, the **D3DXVec3Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eab8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1eab8-123">Requirements</span></span>



| <span data-ttu-id="1eab8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1eab8-124">Requirement</span></span> | <span data-ttu-id="1eab8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="1eab8-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eab8-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1eab8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1eab8-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1eab8-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1eab8-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="1eab8-128">Library</span></span><br/> | <dl> <span data-ttu-id="1eab8-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1eab8-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1eab8-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1eab8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eab8-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="1eab8-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




