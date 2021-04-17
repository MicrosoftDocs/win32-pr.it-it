---
description: Trasforma il vettore (x, y, z,1) in base a una matrice specificata.
ms.assetid: 5b290c4c-22f1-4086-8e5e-f995757ef193
title: Funzione D3DXVec3Transform (D3dx9math. h)
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
ms.openlocfilehash: b653eeb7ea3797a3c385efda73ac974e2f4fbd97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355969"
---
# <a name="d3dxvec3transform-function-d3dx9mathh"></a><span data-ttu-id="d1933-103">Funzione D3DXVec3Transform (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d1933-103">D3DXVec3Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="d1933-104">Trasforma il vettore (x, y, z,1) in base a una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="d1933-104">Transforms vector (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1933-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1933-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d1933-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1933-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1933-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d1933-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1933-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1933-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d1933-109">Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d1933-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d1933-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1933-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1933-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d1933-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d1933-112">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="d1933-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d1933-113">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1933-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1933-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d1933-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d1933-115">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="d1933-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1933-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1933-116">Return value</span></span>

<span data-ttu-id="d1933-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d1933-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d1933-118">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="d1933-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1933-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1933-119">Remarks</span></span>

<span data-ttu-id="d1933-120">Questa funzione trasforma il vettore, *PV* (x, y, z, 1), dal *PM* della matrice.</span><span class="sxs-lookup"><span data-stu-id="d1933-120">This function transforms the vector, *pV* (x, y, z, 1), by the matrix *pM*.</span></span>

<span data-ttu-id="d1933-121">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="d1933-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d1933-122">In questo modo, la funzione **D3DXVec3Transform** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="d1933-122">In this way, the **D3DXVec3Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1933-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1933-123">Requirements</span></span>



| <span data-ttu-id="d1933-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1933-124">Requirement</span></span> | <span data-ttu-id="d1933-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d1933-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1933-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1933-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d1933-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1933-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d1933-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="d1933-128">Library</span></span><br/> | <dl> <span data-ttu-id="d1933-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1933-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d1933-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1933-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1933-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="d1933-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




