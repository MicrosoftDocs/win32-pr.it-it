---
description: Proietta una matrice (x, y, z,0) dallo spazio dell'oggetto nello spazio dello schermo.
ms.assetid: cf022741-0bae-4c22-872f-bd94c3721aff
title: Funzione D3DXVec3ProjectArray (D3dx9math. h)
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
ms.openlocfilehash: f802d8ab564f2cbfe1cc60ad6aed13959bef9383
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323648"
---
# <a name="d3dxvec3projectarray-function-d3dx9mathh"></a><span data-ttu-id="67173-103">Funzione D3DXVec3ProjectArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="67173-103">D3DXVec3ProjectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="67173-104">Proietta una matrice (x, y, z,0) dallo spazio dell'oggetto nello spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="67173-104">Projects an array (x, y, z, 0) from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="67173-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67173-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="67173-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="67173-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67173-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="67173-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="67173-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="67173-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="67173-109">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="67173-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="67173-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67173-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67173-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67173-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67173-112">Stride tra i vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="67173-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="67173-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67173-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67173-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="67173-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="67173-115">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="67173-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="67173-116">*VStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67173-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67173-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67173-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67173-118">Stride tra i vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="67173-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="67173-119">*pViewport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67173-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67173-120">Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="67173-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="67173-121">Puntatore a una struttura [**D3DVIEWPORT9**](d3dviewport9.md) che rappresenta il viewport.</span><span class="sxs-lookup"><span data-stu-id="67173-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="67173-122">*pProjection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67173-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67173-123">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="67173-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="67173-124">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) , che rappresenta la matrice di proiezione.</span><span class="sxs-lookup"><span data-stu-id="67173-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="67173-125">*pview* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67173-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67173-126">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="67173-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="67173-127">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta la matrice di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="67173-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="67173-128">*pWorld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67173-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67173-129">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="67173-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="67173-130">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) , che rappresenta la matrice mondiale.</span><span class="sxs-lookup"><span data-stu-id="67173-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="67173-131">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67173-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67173-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67173-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67173-133">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="67173-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67173-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67173-134">Return value</span></span>

<span data-ttu-id="67173-135">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="67173-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="67173-136">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta la matrice proiettata dallo spazio oggetto allo spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="67173-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="67173-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="67173-137">Remarks</span></span>

<span data-ttu-id="67173-138">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="67173-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="67173-139">In questo modo, la funzione **D3DXVec3ProjectArray** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="67173-139">In this way, the **D3DXVec3ProjectArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="67173-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67173-140">Requirements</span></span>



| <span data-ttu-id="67173-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="67173-141">Requirement</span></span> | <span data-ttu-id="67173-142">Valore</span><span class="sxs-lookup"><span data-stu-id="67173-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67173-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67173-143">Header</span></span><br/>  | <dl> <span data-ttu-id="67173-144"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="67173-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="67173-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="67173-145">Library</span></span><br/> | <dl> <span data-ttu-id="67173-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67173-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="67173-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67173-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67173-148">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="67173-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="67173-149">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="67173-149">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 
