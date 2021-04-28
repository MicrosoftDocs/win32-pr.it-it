---
description: 'Funzione D3DXMatrixPerspectiveRH (D3dx9math.h): crea una matrice di proiezione prospettica con la mano destra.'
ms.assetid: dd9b041b-922b-43df-a6e9-46c97204338a
title: Funzione D3DXMatrixPerspectiveRH (D3dx9math.h)
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
ms.openlocfilehash: 3c583b74366a0a00054bbeced1ece2bd3d1c1cd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118239"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx9mathh"></a><span data-ttu-id="6a5c7-103">Funzione D3DXMatrixPerspectiveRH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="6a5c7-103">D3DXMatrixPerspectiveRH function (D3dx9math.h)</span></span>

<span data-ttu-id="6a5c7-104">Crea una matrice di proiezione prospettica destrorsa.</span><span class="sxs-lookup"><span data-stu-id="6a5c7-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a5c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a5c7-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="6a5c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a5c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a5c7-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6a5c7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5c7-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a5c7-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6a5c7-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6a5c7-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6a5c7-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a5c7-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5c7-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a5c7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a5c7-112">Larghezza del volume di visualizzazione nel piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="6a5c7-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="6a5c7-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a5c7-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5c7-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a5c7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a5c7-115">Altezza del volume di visualizzazione nel piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="6a5c7-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="6a5c7-116">*zn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6a5c7-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5c7-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a5c7-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a5c7-118">Valore Z del piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="6a5c7-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="6a5c7-119">*zf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6a5c7-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5c7-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a5c7-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a5c7-121">Valore Z del piano di visualizzazione lontano.</span><span class="sxs-lookup"><span data-stu-id="6a5c7-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a5c7-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a5c7-122">Return value</span></span>

<span data-ttu-id="6a5c7-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a5c7-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6a5c7-124">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta una matrice di proiezione prospettica con la mano destra.</span><span class="sxs-lookup"><span data-stu-id="6a5c7-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a5c7-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a5c7-125">Remarks</span></span>

<span data-ttu-id="6a5c7-126">Tutti i parametri della **funzione D3DXMatrixPerspectiveRH** sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="6a5c7-126">All the parameters of the **D3DXMatrixPerspectiveRH** function are distances in camera space.</span></span> <span data-ttu-id="6a5c7-127">I parametri descrivono le dimensioni del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="6a5c7-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="6a5c7-128">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="6a5c7-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6a5c7-129">In questo modo, la **funzione D3DXMatrixPerspectiveRH** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="6a5c7-129">In this way, the **D3DXMatrixPerspectiveRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="6a5c7-130">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="6a5c7-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="6a5c7-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a5c7-131">Requirements</span></span>



| <span data-ttu-id="6a5c7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a5c7-132">Requirement</span></span> | <span data-ttu-id="6a5c7-133">Valore</span><span class="sxs-lookup"><span data-stu-id="6a5c7-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a5c7-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a5c7-134">Header</span></span><br/>  | <dl> <span data-ttu-id="6a5c7-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6a5c7-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6a5c7-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="6a5c7-136">Library</span></span><br/> | <dl> <span data-ttu-id="6a5c7-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a5c7-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a5c7-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a5c7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a5c7-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="6a5c7-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6a5c7-140">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="6a5c7-140">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="6a5c7-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="6a5c7-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="6a5c7-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="6a5c7-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="6a5c7-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="6a5c7-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="6a5c7-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="6a5c7-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
