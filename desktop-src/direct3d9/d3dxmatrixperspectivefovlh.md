---
description: 'Funzione D3DXMatrixPerspectiveFovLH (D3dx9math.h): crea una matrice di proiezione prospettica sinistra basata su un campo di visualizzazione.'
ms.assetid: 90328798-f124-4b61-90a9-971946066b02
title: Funzione D3DXMatrixPerspectiveFovLH (D3dx9math.h)
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
ms.openlocfilehash: eec478fec30567fbf301054ddfa60f1689bfee8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118349"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx9mathh"></a><span data-ttu-id="87cc3-103">Funzione D3DXMatrixPerspectiveFovLH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="87cc3-103">D3DXMatrixPerspectiveFovLH function (D3dx9math.h)</span></span>

<span data-ttu-id="87cc3-104">Crea una matrice di proiezione prospettica sinistrorsa basata su un campo visivo.</span><span class="sxs-lookup"><span data-stu-id="87cc3-104">Builds a left-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="87cc3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87cc3-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="87cc3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="87cc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87cc3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="87cc3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="87cc3-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="87cc3-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="87cc3-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="87cc3-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="87cc3-110">*fovy* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="87cc3-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87cc3-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87cc3-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87cc3-112">Campo di visualizzazione nella direzione y, espresso in radianti.</span><span class="sxs-lookup"><span data-stu-id="87cc3-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="87cc3-113">*Aspetto* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="87cc3-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87cc3-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87cc3-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87cc3-115">Proporzioni, definite come larghezza dello spazio di visualizzazione divisa per altezza.</span><span class="sxs-lookup"><span data-stu-id="87cc3-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="87cc3-116">*zn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="87cc3-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87cc3-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87cc3-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87cc3-118">Valore Z del piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="87cc3-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="87cc3-119">*zf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="87cc3-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87cc3-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87cc3-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87cc3-121">Valore Z del piano di visualizzazione lontano.</span><span class="sxs-lookup"><span data-stu-id="87cc3-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87cc3-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87cc3-122">Return value</span></span>

<span data-ttu-id="87cc3-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="87cc3-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="87cc3-124">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta una matrice di proiezione prospettica mancino.</span><span class="sxs-lookup"><span data-stu-id="87cc3-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="87cc3-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="87cc3-125">Remarks</span></span>

<span data-ttu-id="87cc3-126">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="87cc3-126">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="87cc3-127">In questo modo, la **funzione D3DXMatrixPerspectiveFovLH** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="87cc3-127">In this way, the **D3DXMatrixPerspectiveFovLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="87cc3-128">Per modificare l'asse delle proporzioni, usare la formula di calcolo: fovy = 2 \* math.atan(math.tan(fovy \* 0,5) /aspect).</span><span class="sxs-lookup"><span data-stu-id="87cc3-128">To change the aspect ratio axis, use the calculation formula: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span></span> <span data-ttu-id="87cc3-129">In alternativa, aggiungere le variabili delle proporzioni X e Y nella struttura per ridimensionare lo spazio di visualizzazione verticale: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) /aspectY), aspect = aspectX \* aspect Y.</span><span class="sxs-lookup"><span data-stu-id="87cc3-129">Alternatively, add X and Y aspect ratio variables in the structure to scale the vertical view space: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span></span>

<span data-ttu-id="87cc3-130">Questa funzione calcola la matrice restituita come illustrato:</span><span class="sxs-lookup"><span data-stu-id="87cc3-130">This function computes the returned matrix as shown:</span></span>


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="87cc3-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87cc3-131">Requirements</span></span>



| <span data-ttu-id="87cc3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="87cc3-132">Requirement</span></span> | <span data-ttu-id="87cc3-133">Valore</span><span class="sxs-lookup"><span data-stu-id="87cc3-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87cc3-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87cc3-134">Header</span></span><br/>  | <dl> <span data-ttu-id="87cc3-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="87cc3-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="87cc3-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="87cc3-136">Library</span></span><br/> | <dl> <span data-ttu-id="87cc3-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="87cc3-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="87cc3-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87cc3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87cc3-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="87cc3-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="87cc3-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="87cc3-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="87cc3-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="87cc3-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="87cc3-142">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="87cc3-142">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="87cc3-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="87cc3-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="87cc3-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="87cc3-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
