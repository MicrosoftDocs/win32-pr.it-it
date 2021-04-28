---
description: 'Funzione D3DXMatrixPerspectiveOffCenterRH (D3DX10Math.h): crea una matrice di proiezione prospettica personalizzata e con la mano destra.'
ms.assetid: 51509bfc-2f49-4ba7-8918-3c44d857d4b2
title: Funzione D3DXMatrixPerspectiveOffCenterRH (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3f80c32953dbc591d5d8bc7a95fc707e93fe384c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109039"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="0e6b5-103">Funzione D3DXMatrixPerspectiveOffCenterRH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="0e6b5-103">D3DXMatrixPerspectiveOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="0e6b5-104">Compila una matrice di proiezione prospettica personalizzata con la mano destra.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-104">Builds a customized, right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e6b5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e6b5-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="0e6b5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e6b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e6b5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0e6b5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e6b5-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e6b5-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0e6b5-109">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0e6b5-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e6b5-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e6b5-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e6b5-112">Valore x minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="0e6b5-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e6b5-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e6b5-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e6b5-115">Valore x massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="0e6b5-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e6b5-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e6b5-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e6b5-118">Valore y minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="0e6b5-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e6b5-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e6b5-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e6b5-121">Valore y massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="0e6b5-122">*zn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0e6b5-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e6b5-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e6b5-124">Valore z minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="0e6b5-125">*zf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0e6b5-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e6b5-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e6b5-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e6b5-127">Valore z massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e6b5-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e6b5-128">Return value</span></span>

<span data-ttu-id="0e6b5-129">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e6b5-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0e6b5-130">Puntatore a una struttura D3DXMATRIX che è una matrice di proiezione prospettica personalizzata con la mano destra.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-130">Pointer to a D3DXMATRIX structure that is a customized, right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e6b5-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e6b5-131">Remarks</span></span>

<span data-ttu-id="0e6b5-132">Tutti i parametri della funzione D3DXMatrixPerspectiveOffCenterRH sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-132">All the parameters of the D3DXMatrixPerspectiveOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="0e6b5-133">I parametri descrivono le dimensioni del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="0e6b5-134">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-134">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0e6b5-135">In questo modo, la funzione D3DXMatrixPerspectiveOffCenterRH può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-135">In this way, the D3DXMatrixPerspectiveOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0e6b5-136">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="0e6b5-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a><span data-ttu-id="0e6b5-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e6b5-137">Requirements</span></span>



| <span data-ttu-id="0e6b5-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e6b5-138">Requirement</span></span> | <span data-ttu-id="0e6b5-139">Valore</span><span class="sxs-lookup"><span data-stu-id="0e6b5-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6b5-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e6b5-140">Header</span></span><br/>  | <dl> <span data-ttu-id="0e6b5-141"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0e6b5-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="0e6b5-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="0e6b5-142">Library</span></span><br/> | <dl> <span data-ttu-id="0e6b5-143"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e6b5-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0e6b5-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e6b5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e6b5-145">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="0e6b5-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
