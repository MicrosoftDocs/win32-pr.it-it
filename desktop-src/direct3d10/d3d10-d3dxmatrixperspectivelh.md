---
description: 'Funzione D3DXMatrixPerspectiveLH (D3DX10Math.h): crea una matrice di proiezione prospettica mancino'
ms.assetid: 5fd8da67-ff12-42fa-b915-b50fa2680b32
title: Funzione D3DXMatrixPerspectiveLH (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0f6c976f64fe64d3ca583351ae5c7c32aa958fd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109099"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx10mathh"></a><span data-ttu-id="4a6de-103">Funzione D3DXMatrixPerspectiveLH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="4a6de-103">D3DXMatrixPerspectiveLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="4a6de-104">Compila una matrice di proiezione prospettica mancino</span><span class="sxs-lookup"><span data-stu-id="4a6de-104">Builds a left-handed perspective projection matrix</span></span>

## <a name="syntax"></a><span data-ttu-id="4a6de-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a6de-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="4a6de-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a6de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a6de-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4a6de-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6de-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a6de-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4a6de-109">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4a6de-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4a6de-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a6de-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6de-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a6de-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4a6de-112">Larghezza del volume di visualizzazione nel piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="4a6de-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="4a6de-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a6de-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6de-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a6de-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4a6de-115">Altezza del volume di visualizzazione nel piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="4a6de-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="4a6de-116">*zn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4a6de-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6de-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a6de-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4a6de-118">Valore Z del piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="4a6de-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="4a6de-119">*zf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4a6de-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6de-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a6de-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4a6de-121">Valore Z del piano di visualizzazione lontano.</span><span class="sxs-lookup"><span data-stu-id="4a6de-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a6de-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a6de-122">Return value</span></span>

<span data-ttu-id="4a6de-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a6de-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4a6de-124">Puntatore a una struttura D3DXMATRIX che è una matrice di proiezione prospettica mancino.</span><span class="sxs-lookup"><span data-stu-id="4a6de-124">Pointer to a D3DXMATRIX structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a6de-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a6de-125">Remarks</span></span>

<span data-ttu-id="4a6de-126">Tutti i parametri della funzione D3DXMatrixPerspectiveLH sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="4a6de-126">All the parameters of the D3DXMatrixPerspectiveLH function are distances in camera space.</span></span> <span data-ttu-id="4a6de-127">I parametri descrivono le dimensioni del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="4a6de-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="4a6de-128">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="4a6de-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="4a6de-129">In questo modo, la funzione D3DXMatrixPerspectiveLH può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="4a6de-129">In this way, the D3DXMatrixPerspectiveLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4a6de-130">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="4a6de-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="4a6de-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a6de-131">Requirements</span></span>



| <span data-ttu-id="4a6de-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a6de-132">Requirement</span></span> | <span data-ttu-id="4a6de-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4a6de-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a6de-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a6de-134">Header</span></span><br/>  | <dl> <span data-ttu-id="4a6de-135"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="4a6de-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4a6de-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="4a6de-136">Library</span></span><br/> | <dl> <span data-ttu-id="4a6de-137"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a6de-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4a6de-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a6de-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a6de-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="4a6de-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
