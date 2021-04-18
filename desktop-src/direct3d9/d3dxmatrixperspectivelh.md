---
description: Compila una matrice di proiezione prospettica a sinistra
ms.assetid: 07bbbca8-ad1e-4177-97d4-601b33179b47
title: Funzione D3DXMatrixPerspectiveLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf7e6a446202a86e126b2cea0c4a09f19bf6ffa0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323239"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx9mathh"></a><span data-ttu-id="0738c-103">Funzione D3DXMatrixPerspectiveLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0738c-103">D3DXMatrixPerspectiveLH function (D3dx9math.h)</span></span>

<span data-ttu-id="0738c-104">Compila una matrice di proiezione prospettica a sinistra</span><span class="sxs-lookup"><span data-stu-id="0738c-104">Builds a left-handed perspective projection matrix</span></span>

## <a name="syntax"></a><span data-ttu-id="0738c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0738c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="0738c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0738c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0738c-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0738c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0738c-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0738c-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0738c-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0738c-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0738c-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0738c-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0738c-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0738c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0738c-112">Larghezza del volume di visualizzazione nel piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="0738c-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="0738c-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0738c-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0738c-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0738c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0738c-115">Altezza del volume di visualizzazione nel piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="0738c-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="0738c-116">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0738c-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0738c-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0738c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0738c-118">Valore Z del piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="0738c-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="0738c-119">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0738c-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0738c-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0738c-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0738c-121">Valore Z del piano di visualizzazione lontano.</span><span class="sxs-lookup"><span data-stu-id="0738c-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0738c-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0738c-122">Return value</span></span>

<span data-ttu-id="0738c-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0738c-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0738c-124">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta una matrice di proiezione prospettica a sinistra.</span><span class="sxs-lookup"><span data-stu-id="0738c-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="0738c-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="0738c-125">Remarks</span></span>

<span data-ttu-id="0738c-126">Tutti i parametri della funzione **D3DXMatrixPerspectiveLH** sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="0738c-126">All the parameters of the **D3DXMatrixPerspectiveLH** function are distances in camera space.</span></span> <span data-ttu-id="0738c-127">I parametri descrivono le dimensioni del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0738c-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="0738c-128">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="0738c-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0738c-129">In questo modo, la funzione **D3DXMatrixPerspectiveLH** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="0738c-129">In this way, the **D3DXMatrixPerspectiveLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0738c-130">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="0738c-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="0738c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0738c-131">Requirements</span></span>



| <span data-ttu-id="0738c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0738c-132">Requirement</span></span> | <span data-ttu-id="0738c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0738c-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0738c-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0738c-134">Header</span></span><br/>  | <dl> <span data-ttu-id="0738c-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0738c-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0738c-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="0738c-136">Library</span></span><br/> | <dl> <span data-ttu-id="0738c-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0738c-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0738c-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0738c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0738c-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="0738c-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0738c-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="0738c-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="0738c-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="0738c-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="0738c-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="0738c-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="0738c-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="0738c-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="0738c-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="0738c-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
