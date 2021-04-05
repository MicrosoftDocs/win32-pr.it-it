---
description: Trasforma una matrice (x, y, 0, 1) in base a una matrice specificata.
ms.assetid: ba8c1983-bd65-4249-9451-69d813e4a3a4
title: Funzione D3DXVec2TransformArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf95c4b8ffd9fd2804b4168609e60ff7278d1209
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762011"
---
# <a name="d3dxvec2transformarray-function-d3dx9mathh"></a><span data-ttu-id="04b47-103">Funzione D3DXVec2TransformArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="04b47-103">D3DXVec2TransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="04b47-104">Trasforma una matrice (x, y, 0, 1) in base a una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="04b47-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="04b47-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04b47-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="04b47-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04b47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04b47-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="04b47-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="04b47-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="04b47-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="04b47-109">Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="04b47-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="04b47-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04b47-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04b47-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04b47-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04b47-112">Stride tra i vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="04b47-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="04b47-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04b47-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04b47-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="04b47-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="04b47-115">Puntatore alla struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="04b47-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="04b47-116">*VStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04b47-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04b47-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04b47-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04b47-118">Stride tra i vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="04b47-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="04b47-119">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04b47-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04b47-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="04b47-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="04b47-121">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="04b47-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="04b47-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04b47-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04b47-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04b47-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04b47-124">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="04b47-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04b47-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04b47-125">Return value</span></span>

<span data-ttu-id="04b47-126">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="04b47-126">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="04b47-127">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta la matrice trasformata.</span><span class="sxs-lookup"><span data-stu-id="04b47-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="04b47-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="04b47-128">Remarks</span></span>

<span data-ttu-id="04b47-129">Questa funzione trasforma la matrice *PV* (x, y, 0, 1) dalle *PM* della matrice.</span><span class="sxs-lookup"><span data-stu-id="04b47-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="04b47-130">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="04b47-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="04b47-131">In questo modo, la funzione [**D3DXVec2Transform**](d3dxvec2transform.md) può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="04b47-131">In this way, the [**D3DXVec2Transform**](d3dxvec2transform.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="04b47-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04b47-132">Requirements</span></span>



| <span data-ttu-id="04b47-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="04b47-133">Requirement</span></span> | <span data-ttu-id="04b47-134">Valore</span><span class="sxs-lookup"><span data-stu-id="04b47-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04b47-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04b47-135">Header</span></span><br/>  | <dl> <span data-ttu-id="04b47-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="04b47-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="04b47-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="04b47-137">Library</span></span><br/> | <dl> <span data-ttu-id="04b47-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04b47-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="04b47-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04b47-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04b47-140">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="04b47-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="04b47-141">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="04b47-141">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> <dt>

[<span data-ttu-id="04b47-142">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="04b47-142">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 
