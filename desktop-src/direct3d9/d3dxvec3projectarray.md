---
description: "Funzione D3DXVec3ProjectArray (D3dx9math.h): proietta una matrice (x, y, z, 0) dallo spazio dell'oggetto allo spazio dello schermo."
ms.assetid: cf022741-0bae-4c22-872f-bd94c3721aff
title: Funzione D3DXVec3ProjectArray (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10f0e19ad5bdbff59d7386223c88ed867e8d0d88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097809"
---
# <a name="d3dxvec3projectarray-function-d3dx9mathh"></a><span data-ttu-id="daaf3-103">Funzione D3DXVec3ProjectArray (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="daaf3-103">D3DXVec3ProjectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="daaf3-104">Proietta una matrice (x, y, z, 0) dallo spazio oggetto allo spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="daaf3-104">Projects an array (x, y, z, 0) from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="daaf3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="daaf3-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a><span data-ttu-id="daaf3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="daaf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daaf3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="daaf3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="daaf3-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="daaf3-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="daaf3-109">Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="daaf3-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="daaf3-110">*OutStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="daaf3-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daaf3-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="daaf3-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="daaf3-112">Stride tra vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="daaf3-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="daaf3-113">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="daaf3-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daaf3-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="daaf3-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="daaf3-115">Puntatore alla struttura [**D3DXVECTOR3 di**](d3dxvector3.md) origine.</span><span class="sxs-lookup"><span data-stu-id="daaf3-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="daaf3-116">*VStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="daaf3-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daaf3-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="daaf3-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="daaf3-118">Stride tra vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="daaf3-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="daaf3-119">*pViewport* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="daaf3-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daaf3-120">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="daaf3-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="daaf3-121">Puntatore a [**una struttura D3DVIEWPORT9,**](d3dviewport9.md) che rappresenta il viewport.</span><span class="sxs-lookup"><span data-stu-id="daaf3-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="daaf3-122">*pProjection* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="daaf3-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daaf3-123">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="daaf3-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="daaf3-124">Puntatore a [**una struttura D3DXMATRIX,**](d3dxmatrix.md) che rappresenta la matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="daaf3-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="daaf3-125">*pView* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="daaf3-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daaf3-126">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="daaf3-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="daaf3-127">Puntatore a [**una struttura D3DXMATRIX,**](d3dxmatrix.md) che rappresenta la matrice di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="daaf3-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="daaf3-128">*pWorld* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="daaf3-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daaf3-129">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="daaf3-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="daaf3-130">Puntatore a [**una struttura D3DXMATRIX,**](d3dxmatrix.md) che rappresenta la matrice globale.</span><span class="sxs-lookup"><span data-stu-id="daaf3-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="daaf3-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="daaf3-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daaf3-132">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="daaf3-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="daaf3-133">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="daaf3-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daaf3-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="daaf3-134">Return value</span></span>

<span data-ttu-id="daaf3-135">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="daaf3-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="daaf3-136">Puntatore a [**una struttura D3DXVECTOR3**](d3dxvector3.md) che rappresenta la matrice proiettata dallo spazio oggetto allo spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="daaf3-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="daaf3-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="daaf3-137">Remarks</span></span>

<span data-ttu-id="daaf3-138">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="daaf3-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="daaf3-139">In questo modo, la **funzione D3DXVec3ProjectArray** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="daaf3-139">In this way, the **D3DXVec3ProjectArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="daaf3-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="daaf3-140">Requirements</span></span>



| <span data-ttu-id="daaf3-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="daaf3-141">Requirement</span></span> | <span data-ttu-id="daaf3-142">Valore</span><span class="sxs-lookup"><span data-stu-id="daaf3-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="daaf3-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="daaf3-143">Header</span></span><br/>  | <dl> <span data-ttu-id="daaf3-144"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="daaf3-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="daaf3-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="daaf3-145">Library</span></span><br/> | <dl> <span data-ttu-id="daaf3-146"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="daaf3-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="daaf3-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="daaf3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daaf3-148">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="daaf3-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="daaf3-149">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="daaf3-149">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 
