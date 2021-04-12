---
description: Crea una matrice di proiezione prospettica destrorsa basata su un campo visivo.
ms.assetid: 3f4bc5d8-90af-4fdc-bc0c-931407cd7a9b
title: Funzione D3DXMatrixPerspectiveFovRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da478a027db8c366a2cfec827075d3d4b73ae014
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355414"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx9mathh"></a><span data-ttu-id="5ac34-103">Funzione D3DXMatrixPerspectiveFovRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5ac34-103">D3DXMatrixPerspectiveFovRH function (D3dx9math.h)</span></span>

<span data-ttu-id="5ac34-104">Crea una matrice di proiezione prospettica destrorsa basata su un campo visivo.</span><span class="sxs-lookup"><span data-stu-id="5ac34-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ac34-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ac34-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="5ac34-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ac34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ac34-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5ac34-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ac34-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ac34-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ac34-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5ac34-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5ac34-110">*fovy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ac34-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ac34-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ac34-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ac34-112">Campo di visualizzazione nella direzione y, in radianti.</span><span class="sxs-lookup"><span data-stu-id="5ac34-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="5ac34-113">*Aspetto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ac34-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ac34-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ac34-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ac34-115">Proporzioni, definite come larghezza dello spazio di visualizzazione divisa per l'altezza.</span><span class="sxs-lookup"><span data-stu-id="5ac34-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="5ac34-116">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ac34-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ac34-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ac34-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ac34-118">Valore Z del piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="5ac34-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="5ac34-119">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ac34-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ac34-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ac34-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ac34-121">Valore Z del piano di visualizzazione lontano.</span><span class="sxs-lookup"><span data-stu-id="5ac34-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ac34-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ac34-122">Return value</span></span>

<span data-ttu-id="5ac34-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ac34-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ac34-124">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta una matrice di proiezione prospettica a destra.</span><span class="sxs-lookup"><span data-stu-id="5ac34-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ac34-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ac34-125">Remarks</span></span>

<span data-ttu-id="5ac34-126">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="5ac34-126">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5ac34-127">In questo modo, la funzione **D3DXMatrixPerspectiveFovRH** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="5ac34-127">In this way, the **D3DXMatrixPerspectiveFovRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="5ac34-128">Per modificare l'asse delle proporzioni, usare la formula di calcolo: fovy = 2 \* Math. Atan (Math. Tan (fovy \* 0,5)/aspect).</span><span class="sxs-lookup"><span data-stu-id="5ac34-128">To change the aspect ratio axis, use the calculation formula: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span></span> <span data-ttu-id="5ac34-129">In alternativa, aggiungere variabili di proporzioni X e Y nella struttura per ridimensionare lo spazio di visualizzazione verticale: fovy = 2 \* Math. Atan (Math. Tan (fovy \* 0,5)/aspecty), aspect = aspectX \* aspect Y.</span><span class="sxs-lookup"><span data-stu-id="5ac34-129">Alternatively, add X and Y aspect ratio variables in the structure to scale the vertical view space: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span></span>

<span data-ttu-id="5ac34-130">Questa funzione calcola la matrice restituita come illustrato.</span><span class="sxs-lookup"><span data-stu-id="5ac34-130">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0        0        zf/(zn-zf)        -1
0        0        zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="5ac34-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ac34-131">Requirements</span></span>



| <span data-ttu-id="5ac34-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ac34-132">Requirement</span></span> | <span data-ttu-id="5ac34-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5ac34-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac34-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ac34-134">Header</span></span><br/>  | <dl> <span data-ttu-id="5ac34-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ac34-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5ac34-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="5ac34-136">Library</span></span><br/> | <dl> <span data-ttu-id="5ac34-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ac34-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5ac34-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ac34-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac34-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="5ac34-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5ac34-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="5ac34-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="5ac34-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="5ac34-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="5ac34-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="5ac34-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="5ac34-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="5ac34-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="5ac34-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="5ac34-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
