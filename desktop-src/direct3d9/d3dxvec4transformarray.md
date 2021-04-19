---
description: Trasforma una matrice (x, y, 0, 1) in base a una matrice specificata.
ms.assetid: 11d69f65-2aef-46f4-b274-e173a11382a8
title: Funzione D3DXVec4TransformArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3102d1766ba43525829e045503c1838a19d4b0e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323753"
---
# <a name="d3dxvec4transformarray-function-d3dx9mathh"></a><span data-ttu-id="63e13-103">Funzione D3DXVec4TransformArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="63e13-103">D3DXVec4TransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="63e13-104">Trasforma una matrice (x, y, 0, 1) in base a una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="63e13-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e13-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63e13-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR4 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="63e13-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="63e13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63e13-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="63e13-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63e13-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="63e13-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="63e13-109">Puntatore alla matrice [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="63e13-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="63e13-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63e13-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e13-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63e13-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63e13-112">Stride tra i vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="63e13-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="63e13-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63e13-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e13-114">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="63e13-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="63e13-115">Puntatore alla matrice [**D3DXVECTOR4**](d3dxvector4.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="63e13-115">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="63e13-116">*VStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63e13-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e13-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63e13-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63e13-118">Stride tra i vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="63e13-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="63e13-119">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63e13-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e13-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="63e13-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="63e13-121">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="63e13-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="63e13-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63e13-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e13-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63e13-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63e13-124">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="63e13-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63e13-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63e13-125">Return value</span></span>

<span data-ttu-id="63e13-126">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="63e13-126">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="63e13-127">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta la matrice trasformata.</span><span class="sxs-lookup"><span data-stu-id="63e13-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="63e13-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="63e13-128">Remarks</span></span>

<span data-ttu-id="63e13-129">Questa funzione trasforma la matrice *PV* (x, y, 0, 1) dalle *PM* della matrice.</span><span class="sxs-lookup"><span data-stu-id="63e13-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="63e13-130">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="63e13-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="63e13-131">In questo modo, la funzione **D3DXVec4TransformArray** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="63e13-131">In this way, the **D3DXVec4TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="63e13-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63e13-132">Requirements</span></span>



| <span data-ttu-id="63e13-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="63e13-133">Requirement</span></span> | <span data-ttu-id="63e13-134">Valore</span><span class="sxs-lookup"><span data-stu-id="63e13-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63e13-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63e13-135">Header</span></span><br/>  | <dl> <span data-ttu-id="63e13-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="63e13-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="63e13-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="63e13-137">Library</span></span><br/> | <dl> <span data-ttu-id="63e13-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63e13-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="63e13-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63e13-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e13-140">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="63e13-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
