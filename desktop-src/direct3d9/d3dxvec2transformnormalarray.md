---
description: Trasforma una matrice (x, y, 0, 0) in base a una matrice specificata.
ms.assetid: 9f5d8fdc-f3e1-41dc-be4e-9ffc6be1947f
title: Funzione D3DXVec2TransformNormalArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0aece37f9bebb46bab8a0d2a1c27bf19e0c2b0bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323297"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="208a7-103">Funzione D3DXVec2TransformNormalArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="208a7-103">D3DXVec2TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="208a7-104">Trasforma una matrice (x, y, 0, 0) in base a una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="208a7-104">Transforms an array (x, y, 0, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="208a7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="208a7-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormalArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="208a7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="208a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="208a7-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="208a7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="208a7-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="208a7-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="208a7-109">Puntatore alla struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="208a7-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="208a7-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="208a7-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="208a7-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="208a7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="208a7-112">Stride tra i vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="208a7-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="208a7-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="208a7-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="208a7-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="208a7-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="208a7-115">Puntatore alla matrice [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="208a7-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="208a7-116">*VStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="208a7-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="208a7-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="208a7-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="208a7-118">Stride tra i vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="208a7-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="208a7-119">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="208a7-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="208a7-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="208a7-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="208a7-121">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="208a7-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="208a7-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="208a7-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="208a7-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="208a7-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="208a7-124">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="208a7-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="208a7-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="208a7-125">Return value</span></span>

<span data-ttu-id="208a7-126">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="208a7-126">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="208a7-127">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta la matrice trasformata.</span><span class="sxs-lookup"><span data-stu-id="208a7-127">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="208a7-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="208a7-128">Remarks</span></span>

<span data-ttu-id="208a7-129">Questa funzione trasforma il vettore (*PV-*>x, *PV-*>y, 0, 0) dalla matrice a cui fa riferimento il *PM.*</span><span class="sxs-lookup"><span data-stu-id="208a7-129">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM.*</span></span>

<span data-ttu-id="208a7-130">Se si vuole trasformare un normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice da usare per trasformare un punto.</span><span class="sxs-lookup"><span data-stu-id="208a7-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="208a7-131">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="208a7-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="208a7-132">In questo modo, la funzione **D3DXVec2TransformNormalArray** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="208a7-132">In this way, the **D3DXVec2TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="208a7-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="208a7-133">Requirements</span></span>



| <span data-ttu-id="208a7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="208a7-134">Requirement</span></span> | <span data-ttu-id="208a7-135">Valore</span><span class="sxs-lookup"><span data-stu-id="208a7-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="208a7-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="208a7-136">Header</span></span><br/>  | <dl> <span data-ttu-id="208a7-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="208a7-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="208a7-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="208a7-138">Library</span></span><br/> | <dl> <span data-ttu-id="208a7-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="208a7-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="208a7-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="208a7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="208a7-141">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="208a7-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
