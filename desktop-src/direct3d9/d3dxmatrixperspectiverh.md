---
description: Crea una matrice di proiezione prospettica destrorsa.
ms.assetid: dd9b041b-922b-43df-a6e9-46c97204338a
title: Funzione D3DXMatrixPerspectiveRH (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3bcec04202ecb2de15c479ac4ce84d4ee86c99a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234945"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx9mathh"></a><span data-ttu-id="398c6-103">Funzione D3DXMatrixPerspectiveRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="398c6-103">D3DXMatrixPerspectiveRH function (D3dx9math.h)</span></span>

<span data-ttu-id="398c6-104">Crea una matrice di proiezione prospettica destrorsa.</span><span class="sxs-lookup"><span data-stu-id="398c6-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="398c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="398c6-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="398c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="398c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="398c6-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="398c6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="398c6-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="398c6-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="398c6-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="398c6-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="398c6-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="398c6-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="398c6-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="398c6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="398c6-112">Larghezza del volume di visualizzazione nel piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="398c6-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="398c6-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="398c6-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="398c6-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="398c6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="398c6-115">Altezza del volume di visualizzazione nel piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="398c6-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="398c6-116">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="398c6-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="398c6-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="398c6-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="398c6-118">Valore Z del piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="398c6-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="398c6-119">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="398c6-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="398c6-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="398c6-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="398c6-121">Valore Z del piano di visualizzazione lontano.</span><span class="sxs-lookup"><span data-stu-id="398c6-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="398c6-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="398c6-122">Return value</span></span>

<span data-ttu-id="398c6-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="398c6-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="398c6-124">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta una matrice di proiezione prospettica a destra.</span><span class="sxs-lookup"><span data-stu-id="398c6-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="398c6-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="398c6-125">Remarks</span></span>

<span data-ttu-id="398c6-126">Tutti i parametri della funzione **D3DXMatrixPerspectiveRH** sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="398c6-126">All the parameters of the **D3DXMatrixPerspectiveRH** function are distances in camera space.</span></span> <span data-ttu-id="398c6-127">I parametri descrivono le dimensioni del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="398c6-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="398c6-128">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="398c6-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="398c6-129">In questo modo, la funzione **D3DXMatrixPerspectiveRH** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="398c6-129">In this way, the **D3DXMatrixPerspectiveRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="398c6-130">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="398c6-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="398c6-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="398c6-131">Requirements</span></span>



| <span data-ttu-id="398c6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="398c6-132">Requirement</span></span> | <span data-ttu-id="398c6-133">Valore</span><span class="sxs-lookup"><span data-stu-id="398c6-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="398c6-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="398c6-134">Header</span></span><br/>  | <dl> <span data-ttu-id="398c6-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="398c6-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="398c6-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="398c6-136">Library</span></span><br/> | <dl> <span data-ttu-id="398c6-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="398c6-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="398c6-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="398c6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="398c6-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="398c6-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="398c6-140">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="398c6-140">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="398c6-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="398c6-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="398c6-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="398c6-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="398c6-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="398c6-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="398c6-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="398c6-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
