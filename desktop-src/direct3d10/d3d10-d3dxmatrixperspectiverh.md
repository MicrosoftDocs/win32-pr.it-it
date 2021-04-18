---
description: Crea una matrice di proiezione prospettica destrorsa.
ms.assetid: 324c8a21-24ef-4b3a-aac1-a753e26076d4
title: Funzione D3DXMatrixPerspectiveRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eb1c2b4b876fb2dda842912d2f18f845a3167406
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323404"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx10mathh"></a><span data-ttu-id="b28fe-103">Funzione D3DXMatrixPerspectiveRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b28fe-103">D3DXMatrixPerspectiveRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="b28fe-104">Crea una matrice di proiezione prospettica destrorsa.</span><span class="sxs-lookup"><span data-stu-id="b28fe-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b28fe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b28fe-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="b28fe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b28fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b28fe-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b28fe-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b28fe-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b28fe-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b28fe-109">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b28fe-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b28fe-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b28fe-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b28fe-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b28fe-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b28fe-112">Larghezza del volume di visualizzazione nel piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="b28fe-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="b28fe-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b28fe-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b28fe-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b28fe-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b28fe-115">Altezza del volume di visualizzazione nel piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="b28fe-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="b28fe-116">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b28fe-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b28fe-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b28fe-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b28fe-118">Valore Z del piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="b28fe-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="b28fe-119">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b28fe-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b28fe-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b28fe-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b28fe-121">Valore Z del piano di visualizzazione lontano.</span><span class="sxs-lookup"><span data-stu-id="b28fe-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b28fe-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b28fe-122">Return value</span></span>

<span data-ttu-id="b28fe-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b28fe-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b28fe-124">Puntatore a una struttura D3DXMATRIX che rappresenta una matrice di proiezione prospettica a destra.</span><span class="sxs-lookup"><span data-stu-id="b28fe-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b28fe-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="b28fe-125">Remarks</span></span>

<span data-ttu-id="b28fe-126">Tutti i parametri della funzione D3DXMatrixPerspectiveRH sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="b28fe-126">All the parameters of the D3DXMatrixPerspectiveRH function are distances in camera space.</span></span> <span data-ttu-id="b28fe-127">I parametri descrivono le dimensioni del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b28fe-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="b28fe-128">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="b28fe-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b28fe-129">In questo modo, la funzione D3DXMatrixPerspectiveRH può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="b28fe-129">In this way, the D3DXMatrixPerspectiveRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b28fe-130">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="b28fe-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="b28fe-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b28fe-131">Requirements</span></span>



| <span data-ttu-id="b28fe-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b28fe-132">Requirement</span></span> | <span data-ttu-id="b28fe-133">Valore</span><span class="sxs-lookup"><span data-stu-id="b28fe-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b28fe-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b28fe-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b28fe-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b28fe-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b28fe-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="b28fe-136">Library</span></span><br/> | <dl> <span data-ttu-id="b28fe-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b28fe-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b28fe-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b28fe-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b28fe-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="b28fe-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
