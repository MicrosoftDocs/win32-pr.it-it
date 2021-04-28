---
description: 'Funzione D3DXVec3TransformCoordArray (D3dx9math.h): trasforma una matrice (x, y, z, 1) da una determinata matrice e proietta il risultato in w = 1.'
ms.assetid: f1595861-d8cb-4787-8078-b9ba6f76507e
title: Funzione D3DXVec3TransformCoordArray (D3dx9math.h)
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
ms.openlocfilehash: c373705307b2529b3d05609fc4b6ffb47d3abcc2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097749"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx9mathh"></a><span data-ttu-id="1a36f-103">Funzione D3DXVec3TransformCoordArray (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="1a36f-103">D3DXVec3TransformCoordArray function (D3dx9math.h)</span></span>

<span data-ttu-id="1a36f-104">Trasforma una matrice (x, y, z, 1) in base a una determinata matrice e proietta il risultato in w = 1.</span><span class="sxs-lookup"><span data-stu-id="1a36f-104">Transforms an array (x, y, z, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a36f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a36f-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1a36f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a36f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a36f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1a36f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a36f-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a36f-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1a36f-109">Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1a36f-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1a36f-110">*OutStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1a36f-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a36f-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a36f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a36f-112">Stride tra vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="1a36f-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="1a36f-113">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1a36f-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a36f-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a36f-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1a36f-115">Puntatore alla matrice [**D3DXVECTOR3 di**](d3dxvector3.md) origine.</span><span class="sxs-lookup"><span data-stu-id="1a36f-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="1a36f-116">*VStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1a36f-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a36f-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a36f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a36f-118">Stride tra vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="1a36f-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="1a36f-119">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1a36f-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a36f-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1a36f-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1a36f-121">Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="1a36f-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1a36f-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a36f-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a36f-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1a36f-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1a36f-124">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="1a36f-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a36f-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a36f-125">Return value</span></span>

<span data-ttu-id="1a36f-126">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1a36f-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1a36f-127">Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta la matrice trasformata.</span><span class="sxs-lookup"><span data-stu-id="1a36f-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a36f-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a36f-128">Remarks</span></span>

<span data-ttu-id="1a36f-129">Questa funzione trasforma la matrice *pV (x,* y, z, 1) dalla matrice *pM,* proiettando il risultato di nuovo in w = 1.</span><span class="sxs-lookup"><span data-stu-id="1a36f-129">This function transforms the array *pV (* x, y, z, 1) by the matrix *pM*, projecting the result back into w = 1.</span></span>

<span data-ttu-id="1a36f-130">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="1a36f-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1a36f-131">In questo modo, la [**funzione D3DXVec3TransformCoord**](d3dxvec3transformcoord.md) può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="1a36f-131">In this way, the [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a36f-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a36f-132">Requirements</span></span>



| <span data-ttu-id="1a36f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a36f-133">Requirement</span></span> | <span data-ttu-id="1a36f-134">Valore</span><span class="sxs-lookup"><span data-stu-id="1a36f-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a36f-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a36f-135">Header</span></span><br/>  | <dl> <span data-ttu-id="1a36f-136"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1a36f-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1a36f-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="1a36f-137">Library</span></span><br/> | <dl> <span data-ttu-id="1a36f-138"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a36f-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1a36f-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a36f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a36f-140">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="1a36f-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
