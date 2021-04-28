---
description: 'Funzione D3DXVec3TransformNormalArray (D3dx9math.h): trasforma una matrice (x, y, z, 0) in base a una determinata matrice.'
ms.assetid: c12fad52-d541-483f-a919-e6031aa4f761
title: Funzione D3DXVec3TransformNormalArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74da959002bfbd0c488e630f09c89e848708b1b1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097729"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="50411-103">Funzione D3DXVec3TransformNormalArray (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="50411-103">D3DXVec3TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="50411-104">Trasforma una matrice (x, y, z, 0) in base a una determinata matrice.</span><span class="sxs-lookup"><span data-stu-id="50411-104">Transforms an array (x, y, z, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="50411-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50411-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormalArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="50411-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="50411-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50411-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="50411-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50411-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="50411-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="50411-109">Puntatore alla [**matrice D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="50411-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="50411-110">*OutStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="50411-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50411-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50411-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50411-112">Stride tra vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="50411-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="50411-113">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="50411-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50411-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="50411-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="50411-115">Puntatore alla matrice [**D3DXVECTOR3 di**](d3dxvector3.md) origine.</span><span class="sxs-lookup"><span data-stu-id="50411-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="50411-116">*VStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="50411-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50411-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50411-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50411-118">Stride tra vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="50411-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="50411-119">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="50411-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50411-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="50411-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="50411-121">Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="50411-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="50411-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50411-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50411-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50411-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50411-124">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="50411-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50411-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50411-125">Return value</span></span>

<span data-ttu-id="50411-126">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="50411-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="50411-127">Puntatore a [**una matrice D3DXVECTOR3**](d3dxvector3.md) che rappresenta la matrice trasformata.</span><span class="sxs-lookup"><span data-stu-id="50411-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) array that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="50411-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="50411-128">Remarks</span></span>

<span data-ttu-id="50411-129">Questa funzione trasforma il vettore (*pV*->x, *pV*->y, *pV*->z, 0) dalla matrice a cui punta *pM*.</span><span class="sxs-lookup"><span data-stu-id="50411-129">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="50411-130">Se si vuole trasformare una normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice che si userebbe per trasformare un punto.</span><span class="sxs-lookup"><span data-stu-id="50411-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="50411-131">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="50411-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="50411-132">In questo modo, la **funzione D3DXVec3TransformNormalArray** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="50411-132">In this way, the **D3DXVec3TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="50411-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50411-133">Requirements</span></span>



| <span data-ttu-id="50411-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="50411-134">Requirement</span></span> | <span data-ttu-id="50411-135">Valore</span><span class="sxs-lookup"><span data-stu-id="50411-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50411-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50411-136">Header</span></span><br/>  | <dl> <span data-ttu-id="50411-137"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="50411-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="50411-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="50411-138">Library</span></span><br/> | <dl> <span data-ttu-id="50411-139"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="50411-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50411-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50411-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50411-141">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="50411-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
