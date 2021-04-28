---
description: 'Funzione D3DXVec2TransformCoordArray (D3dx9math.h): trasforma una matrice (x, y, 0, 1) da una determinata matrice e proietta il risultato in w = 1.'
ms.assetid: 23c88bed-344b-4b3a-bb92-e50cbe96daf9
title: Funzione D3DXVec2TransformCoordArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoordArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 257cb77ba97396170f221cff1c512a73eb84179c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097939"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx9mathh"></a><span data-ttu-id="4e983-103">Funzione D3DXVec2TransformCoordArray (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="4e983-103">D3DXVec2TransformCoordArray function (D3dx9math.h)</span></span>

<span data-ttu-id="4e983-104">Trasforma una matrice (x, y, 0, 1) in base a una determinata matrice e proietta il risultato in w = 1.</span><span class="sxs-lookup"><span data-stu-id="4e983-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e983-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e983-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoordArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="4e983-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e983-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e983-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4e983-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e983-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e983-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4e983-109">Puntatore alla [**struttura D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4e983-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4e983-110">*OutStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4e983-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e983-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e983-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e983-112">Stride tra vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="4e983-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="4e983-113">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4e983-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e983-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e983-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4e983-115">Puntatore alla matrice [**D3DXVECTOR2 di**](d3dxvector2.md) origine.</span><span class="sxs-lookup"><span data-stu-id="4e983-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="4e983-116">*VStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4e983-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e983-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e983-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e983-118">Stride tra vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="4e983-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="4e983-119">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4e983-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e983-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e983-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4e983-121">Puntatore alla struttura [**D3DXMATRIX di**](d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="4e983-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4e983-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e983-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e983-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e983-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e983-124">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="4e983-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e983-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e983-125">Return value</span></span>

<span data-ttu-id="4e983-126">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e983-126">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="4e983-127">Puntatore a [**una matrice trasformata D3DXVECTOR4.**](d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="4e983-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e983-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e983-128">Remarks</span></span>

<span data-ttu-id="4e983-129">Questa funzione trasforma la matrice *pV* (x, y, 0, 1) dalla matrice *pM,* proiettando di nuovo il risultato in w = 1.</span><span class="sxs-lookup"><span data-stu-id="4e983-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*, projecting the result back into w = 1.</span></span>

<span data-ttu-id="4e983-130">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="4e983-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4e983-131">In questo modo, la **funzione D3DXVec2TransformCoordArray** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="4e983-131">In this way, the **D3DXVec2TransformCoordArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e983-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e983-132">Requirements</span></span>



| <span data-ttu-id="4e983-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e983-133">Requirement</span></span> | <span data-ttu-id="4e983-134">Valore</span><span class="sxs-lookup"><span data-stu-id="4e983-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e983-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e983-135">Header</span></span><br/>  | <dl> <span data-ttu-id="4e983-136"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="4e983-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4e983-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="4e983-137">Library</span></span><br/> | <dl> <span data-ttu-id="4e983-138"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e983-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4e983-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e983-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e983-140">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="4e983-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
