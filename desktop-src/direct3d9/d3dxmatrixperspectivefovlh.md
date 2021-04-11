---
description: Crea una matrice di proiezione prospettica sinistrorsa basata su un campo visivo.
ms.assetid: 90328798-f124-4b61-90a9-971946066b02
title: Funzione D3DXMatrixPerspectiveFovLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91b25a2e319236485c2c290b55acb94954a4791d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235139"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx9mathh"></a><span data-ttu-id="f6ea1-103">Funzione D3DXMatrixPerspectiveFovLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f6ea1-103">D3DXMatrixPerspectiveFovLH function (D3dx9math.h)</span></span>

<span data-ttu-id="f6ea1-104">Crea una matrice di proiezione prospettica sinistrorsa basata su un campo visivo.</span><span class="sxs-lookup"><span data-stu-id="f6ea1-104">Builds a left-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6ea1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6ea1-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="f6ea1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6ea1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6ea1-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f6ea1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ea1-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f6ea1-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f6ea1-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f6ea1-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f6ea1-110">*fovy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6ea1-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ea1-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6ea1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6ea1-112">Campo di visualizzazione nella direzione y, in radianti.</span><span class="sxs-lookup"><span data-stu-id="f6ea1-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="f6ea1-113">*Aspetto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6ea1-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ea1-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6ea1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6ea1-115">Proporzioni, definite come larghezza dello spazio di visualizzazione divisa per l'altezza.</span><span class="sxs-lookup"><span data-stu-id="f6ea1-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="f6ea1-116">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6ea1-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ea1-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6ea1-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6ea1-118">Valore Z del piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="f6ea1-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="f6ea1-119">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6ea1-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ea1-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6ea1-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6ea1-121">Valore Z del piano di visualizzazione lontano.</span><span class="sxs-lookup"><span data-stu-id="f6ea1-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6ea1-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6ea1-122">Return value</span></span>

<span data-ttu-id="f6ea1-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f6ea1-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f6ea1-124">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta una matrice di proiezione prospettica a sinistra.</span><span class="sxs-lookup"><span data-stu-id="f6ea1-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6ea1-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6ea1-125">Remarks</span></span>

<span data-ttu-id="f6ea1-126">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="f6ea1-126">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f6ea1-127">In questo modo, la funzione **D3DXMatrixPerspectiveFovLH** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="f6ea1-127">In this way, the **D3DXMatrixPerspectiveFovLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f6ea1-128">Per modificare l'asse delle proporzioni, usare la formula di calcolo: fovy = 2 \* Math. Atan (Math. Tan (fovy \* 0,5)/aspect).</span><span class="sxs-lookup"><span data-stu-id="f6ea1-128">To change the aspect ratio axis, use the calculation formula: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span></span> <span data-ttu-id="f6ea1-129">In alternativa, aggiungere variabili di proporzioni X e Y nella struttura per ridimensionare lo spazio di visualizzazione verticale: fovy = 2 \* Math. Atan (Math. Tan (fovy \* 0,5)/aspecty), aspect = aspectX \* aspect Y.</span><span class="sxs-lookup"><span data-stu-id="f6ea1-129">Alternatively, add X and Y aspect ratio variables in the structure to scale the vertical view space: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span></span>

<span data-ttu-id="f6ea1-130">Questa funzione calcola la matrice restituita come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f6ea1-130">This function computes the returned matrix as shown:</span></span>


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="f6ea1-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6ea1-131">Requirements</span></span>



| <span data-ttu-id="f6ea1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6ea1-132">Requirement</span></span> | <span data-ttu-id="f6ea1-133">Valore</span><span class="sxs-lookup"><span data-stu-id="f6ea1-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6ea1-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6ea1-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f6ea1-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6ea1-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f6ea1-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="f6ea1-136">Library</span></span><br/> | <dl> <span data-ttu-id="f6ea1-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6ea1-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f6ea1-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6ea1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6ea1-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="f6ea1-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f6ea1-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="f6ea1-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="f6ea1-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="f6ea1-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="f6ea1-142">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="f6ea1-142">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="f6ea1-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="f6ea1-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="f6ea1-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="f6ea1-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
