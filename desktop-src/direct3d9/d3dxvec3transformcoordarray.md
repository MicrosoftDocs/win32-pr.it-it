---
description: Trasforma una matrice (x, y, z,1) in base a una matrice specificata e proietta il risultato di nuovo in w = 1.
ms.assetid: f1595861-d8cb-4787-8078-b9ba6f76507e
title: Funzione D3DXVec3TransformCoordArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoordArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 414fd17c3d7077b4aeb399b734b4a6c811a8a291
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969510"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx9mathh"></a><span data-ttu-id="d5326-103">Funzione D3DXVec3TransformCoordArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d5326-103">D3DXVec3TransformCoordArray function (D3dx9math.h)</span></span>

<span data-ttu-id="d5326-104">Trasforma una matrice (x, y, z,1) in base a una matrice specificata e proietta il risultato di nuovo in w = 1.</span><span class="sxs-lookup"><span data-stu-id="d5326-104">Transforms an array (x, y, z, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5326-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5326-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoordArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="d5326-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5326-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5326-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d5326-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5326-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d5326-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d5326-109">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d5326-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d5326-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5326-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5326-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5326-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5326-112">Stride tra i vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="d5326-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="d5326-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5326-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5326-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d5326-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d5326-115">Puntatore alla matrice [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="d5326-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="d5326-116">*VStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5326-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5326-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5326-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5326-118">Stride tra i vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="d5326-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="d5326-119">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5326-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5326-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d5326-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d5326-121">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="d5326-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d5326-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5326-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5326-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5326-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5326-124">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="d5326-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5326-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5326-125">Return value</span></span>

<span data-ttu-id="d5326-126">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d5326-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d5326-127">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta la matrice trasformata.</span><span class="sxs-lookup"><span data-stu-id="d5326-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5326-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5326-128">Remarks</span></span>

<span data-ttu-id="d5326-129">Questa funzione trasforma la matrice *PV (* x, y, z,1) dalle *PM* della matrice, proiettando il risultato in w = 1.</span><span class="sxs-lookup"><span data-stu-id="d5326-129">This function transforms the array *pV (* x, y, z, 1) by the matrix *pM*, projecting the result back into w = 1.</span></span>

<span data-ttu-id="d5326-130">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="d5326-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d5326-131">In questo modo, la funzione [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md) può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="d5326-131">In this way, the [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5326-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5326-132">Requirements</span></span>



| <span data-ttu-id="d5326-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5326-133">Requirement</span></span> | <span data-ttu-id="d5326-134">Valore</span><span class="sxs-lookup"><span data-stu-id="d5326-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5326-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5326-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d5326-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5326-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d5326-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="d5326-137">Library</span></span><br/> | <dl> <span data-ttu-id="d5326-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5326-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d5326-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5326-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5326-140">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="d5326-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
