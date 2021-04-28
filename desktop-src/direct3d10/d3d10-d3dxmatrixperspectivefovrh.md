---
description: 'Funzione D3DXMatrixPerspectiveFovRH (D3DX10Math.h): compila una matrice di proiezione prospettica con mano destra in base a un campo di visualizzazione.'
ms.assetid: a75e6666-e6c0-4a54-bc88-835fa012542f
title: Funzione D3DXMatrixPerspectiveFovRH (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 38d48789bab9b968b6bcf657459c408abdba774b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109109"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx10mathh"></a><span data-ttu-id="a0105-103">Funzione D3DXMatrixPerspectiveFovRH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="a0105-103">D3DXMatrixPerspectiveFovRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="a0105-104">Crea una matrice di proiezione prospettica destrorsa basata su un campo visivo.</span><span class="sxs-lookup"><span data-stu-id="a0105-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0105-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0105-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="a0105-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0105-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0105-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a0105-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0105-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0105-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a0105-109">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a0105-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a0105-110">*fovy* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a0105-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0105-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0105-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0105-112">Campo di visualizzazione nella direzione y, espresso in radianti.</span><span class="sxs-lookup"><span data-stu-id="a0105-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="a0105-113">*Aspetto* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a0105-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0105-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0105-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0105-115">Proporzioni, definite come larghezza dello spazio di visualizzazione diviso per altezza.</span><span class="sxs-lookup"><span data-stu-id="a0105-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="a0105-116">*zn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a0105-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0105-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0105-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0105-118">Valore Z del piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="a0105-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="a0105-119">*zf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a0105-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0105-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0105-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0105-121">Valore Z del piano di visualizzazione lontano.</span><span class="sxs-lookup"><span data-stu-id="a0105-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0105-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0105-122">Return value</span></span>

<span data-ttu-id="a0105-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0105-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a0105-124">Puntatore a una struttura D3DXMATRIX che è una matrice di proiezione prospettica con mano destra.</span><span class="sxs-lookup"><span data-stu-id="a0105-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0105-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0105-125">Remarks</span></span>

<span data-ttu-id="a0105-126">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="a0105-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a0105-127">In questo modo, la funzione D3DXMatrixPerspectiveFovRH può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="a0105-127">In this way, the D3DXMatrixPerspectiveFovRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a0105-128">Questa funzione calcola la matrice restituita come illustrato.</span><span class="sxs-lookup"><span data-stu-id="a0105-128">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0          0      zf/(zn-zf)        -1
0          0      zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="a0105-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0105-129">Requirements</span></span>



| <span data-ttu-id="a0105-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0105-130">Requirement</span></span> | <span data-ttu-id="a0105-131">Valore</span><span class="sxs-lookup"><span data-stu-id="a0105-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0105-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0105-132">Header</span></span><br/>  | <dl> <span data-ttu-id="a0105-133"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a0105-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a0105-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0105-134">Library</span></span><br/> | <dl> <span data-ttu-id="a0105-135"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0105-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0105-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0105-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0105-137">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="a0105-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
