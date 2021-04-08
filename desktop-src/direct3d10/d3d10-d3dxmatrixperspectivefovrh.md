---
description: Crea una matrice di proiezione prospettica destrorsa basata su un campo visivo.
ms.assetid: a75e6666-e6c0-4a54-bc88-835fa012542f
title: Funzione D3DXMatrixPerspectiveFovRH (D3DX10Math. h)
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
ms.openlocfilehash: baad02b5840af8e244cd562def4aeb8f9ac2988a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969432"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx10mathh"></a><span data-ttu-id="54453-103">Funzione D3DXMatrixPerspectiveFovRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="54453-103">D3DXMatrixPerspectiveFovRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="54453-104">Crea una matrice di proiezione prospettica destrorsa basata su un campo visivo.</span><span class="sxs-lookup"><span data-stu-id="54453-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="54453-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54453-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="54453-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="54453-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54453-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="54453-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54453-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="54453-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="54453-109">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="54453-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="54453-110">*fovy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54453-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54453-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54453-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54453-112">Campo di visualizzazione nella direzione y, in radianti.</span><span class="sxs-lookup"><span data-stu-id="54453-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="54453-113">*Aspetto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54453-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54453-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54453-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54453-115">Proporzioni, definite come larghezza dello spazio di visualizzazione divisa per l'altezza.</span><span class="sxs-lookup"><span data-stu-id="54453-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="54453-116">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54453-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54453-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54453-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54453-118">Valore Z del piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="54453-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="54453-119">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54453-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54453-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54453-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54453-121">Valore Z del piano di visualizzazione lontano.</span><span class="sxs-lookup"><span data-stu-id="54453-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54453-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54453-122">Return value</span></span>

<span data-ttu-id="54453-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="54453-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="54453-124">Puntatore a una struttura D3DXMATRIX che rappresenta una matrice di proiezione prospettica a destra.</span><span class="sxs-lookup"><span data-stu-id="54453-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="54453-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="54453-125">Remarks</span></span>

<span data-ttu-id="54453-126">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="54453-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="54453-127">In questo modo, la funzione D3DXMatrixPerspectiveFovRH può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="54453-127">In this way, the D3DXMatrixPerspectiveFovRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="54453-128">Questa funzione calcola la matrice restituita come illustrato.</span><span class="sxs-lookup"><span data-stu-id="54453-128">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0          0      zf/(zn-zf)        -1
0          0      zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="54453-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54453-129">Requirements</span></span>



| <span data-ttu-id="54453-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="54453-130">Requirement</span></span> | <span data-ttu-id="54453-131">Valore</span><span class="sxs-lookup"><span data-stu-id="54453-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54453-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54453-132">Header</span></span><br/>  | <dl> <span data-ttu-id="54453-133"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="54453-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="54453-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="54453-134">Library</span></span><br/> | <dl> <span data-ttu-id="54453-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54453-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="54453-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54453-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54453-137">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="54453-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
