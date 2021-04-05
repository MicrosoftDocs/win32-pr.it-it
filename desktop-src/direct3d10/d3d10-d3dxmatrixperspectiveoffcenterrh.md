---
description: Compila una matrice di proiezione prospettica personalizzata e a destra.
ms.assetid: 51509bfc-2f49-4ba7-8918-3c44d857d4b2
title: Funzione D3DXMatrixPerspectiveOffCenterRH (D3DX10Math. h)
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
ms.openlocfilehash: 54fc98658d5466acd69d3245af7488c40cd352c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058669"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="3ade2-103">Funzione D3DXMatrixPerspectiveOffCenterRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="3ade2-103">D3DXMatrixPerspectiveOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="3ade2-104">Compila una matrice di proiezione prospettica personalizzata e a destra.</span><span class="sxs-lookup"><span data-stu-id="3ade2-104">Builds a customized, right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ade2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ade2-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="3ade2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ade2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ade2-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="3ade2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ade2-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="3ade2-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3ade2-109">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3ade2-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3ade2-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ade2-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ade2-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ade2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ade2-112">Valore x minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ade2-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="3ade2-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ade2-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ade2-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ade2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ade2-115">Valore x massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ade2-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="3ade2-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ade2-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ade2-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ade2-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ade2-118">Valore y minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ade2-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="3ade2-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ade2-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ade2-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ade2-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ade2-121">Valore y massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ade2-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="3ade2-122">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ade2-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ade2-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ade2-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ade2-124">Valore z minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ade2-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="3ade2-125">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ade2-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ade2-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ade2-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ade2-127">Valore z massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ade2-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ade2-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ade2-128">Return value</span></span>

<span data-ttu-id="3ade2-129">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="3ade2-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3ade2-130">Puntatore a una struttura D3DXMATRIX che è una matrice di proiezione prospettica personalizzata e a destra.</span><span class="sxs-lookup"><span data-stu-id="3ade2-130">Pointer to a D3DXMATRIX structure that is a customized, right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ade2-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ade2-131">Remarks</span></span>

<span data-ttu-id="3ade2-132">Tutti i parametri della funzione D3DXMatrixPerspectiveOffCenterRH sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="3ade2-132">All the parameters of the D3DXMatrixPerspectiveOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="3ade2-133">I parametri descrivono le dimensioni del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3ade2-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="3ade2-134">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="3ade2-134">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="3ade2-135">In questo modo, la funzione D3DXMatrixPerspectiveOffCenterRH può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="3ade2-135">In this way, the D3DXMatrixPerspectiveOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="3ade2-136">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="3ade2-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a><span data-ttu-id="3ade2-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ade2-137">Requirements</span></span>



| <span data-ttu-id="3ade2-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ade2-138">Requirement</span></span> | <span data-ttu-id="3ade2-139">Valore</span><span class="sxs-lookup"><span data-stu-id="3ade2-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ade2-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ade2-140">Header</span></span><br/>  | <dl> <span data-ttu-id="3ade2-141"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ade2-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="3ade2-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="3ade2-142">Library</span></span><br/> | <dl> <span data-ttu-id="3ade2-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ade2-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3ade2-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ade2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ade2-145">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="3ade2-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
