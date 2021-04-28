---
description: 'Funzione D3DXVec3TransformArray (D3dx9math.h): trasforma una matrice (x, y, z, 1) in base a una determinata matrice.'
ms.assetid: fd7ab674-5e42-4265-afad-ae5a00dabcdb
title: Funzione D3DXVec3TransformArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 440869f42769d5c20e26083acf3fad1203e20a22
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097769"
---
# <a name="d3dxvec3transformarray-function-d3dx9mathh"></a><span data-ttu-id="de293-103">Funzione D3DXVec3TransformArray (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="de293-103">D3DXVec3TransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="de293-104">Trasforma una matrice (x, y, z, 1) in base a una determinata matrice.</span><span class="sxs-lookup"><span data-stu-id="de293-104">Transforms an array (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="de293-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de293-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="de293-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de293-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de293-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="de293-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="de293-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="de293-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="de293-109">Puntatore alla [**matrice D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="de293-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="de293-110">*OutStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="de293-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de293-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="de293-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="de293-112">Stride tra vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="de293-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="de293-113">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="de293-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de293-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="de293-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="de293-115">Puntatore alla matrice [**D3DXVECTOR3 di**](d3dxvector3.md) origine.</span><span class="sxs-lookup"><span data-stu-id="de293-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="de293-116">*VStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="de293-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de293-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="de293-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="de293-118">Stride tra i vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="de293-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="de293-119">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="de293-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de293-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="de293-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="de293-121">Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="de293-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="de293-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de293-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de293-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="de293-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="de293-124">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="de293-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de293-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de293-125">Return value</span></span>

<span data-ttu-id="de293-126">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="de293-126">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="de293-127">Puntatore a [**una matrice trasformata D3DXVECTOR4.**](d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="de293-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="de293-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="de293-128">Remarks</span></span>

<span data-ttu-id="de293-129">Questa funzione trasforma la matrice *pV* (x, y, z, 1) dalla matrice *pM*.</span><span class="sxs-lookup"><span data-stu-id="de293-129">This function transforms the array *pV* (x, y, z, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="de293-130">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="de293-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="de293-131">In questo modo, la **funzione D3DXVec3TransformArray** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="de293-131">In this way, the **D3DXVec3TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="de293-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de293-132">Requirements</span></span>



| <span data-ttu-id="de293-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="de293-133">Requirement</span></span> | <span data-ttu-id="de293-134">Valore</span><span class="sxs-lookup"><span data-stu-id="de293-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de293-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de293-135">Header</span></span><br/>  | <dl> <span data-ttu-id="de293-136"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="de293-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="de293-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="de293-137">Library</span></span><br/> | <dl> <span data-ttu-id="de293-138"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="de293-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="de293-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de293-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de293-140">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="de293-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
