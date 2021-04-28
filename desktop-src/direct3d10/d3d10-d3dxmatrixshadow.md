---
description: 'Funzione D3DXMatrixShadow (D3DX10Math.h): compila una matrice che appiatti la geometria in un piano.'
ms.assetid: 83c9e7d6-fc6c-48e7-bbf2-6aa10868351d
title: Funzione D3DXMatrixShadow (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixShadow
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d3a5bff99552a4c5d65267c390c25a2892d3d32f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103349"
---
# <a name="d3dxmatrixshadow-function-d3dx10mathh"></a><span data-ttu-id="0d13f-103">Funzione D3DXMatrixShadow (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="0d13f-103">D3DXMatrixShadow function (D3DX10Math.h)</span></span>

<span data-ttu-id="0d13f-104">Compila una matrice che appiattise la geometria in un piano.</span><span class="sxs-lookup"><span data-stu-id="0d13f-104">Builds a matrix that flattens geometry into a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d13f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d13f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="0d13f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d13f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d13f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0d13f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d13f-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d13f-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0d13f-109">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0d13f-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0d13f-110">*pLight* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0d13f-110">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d13f-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="0d13f-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="0d13f-112">Puntatore a [**un oggetto D3DXVECTOR4**](d3d10-d3dxvector4.md) che descrive la posizione della luce.</span><span class="sxs-lookup"><span data-stu-id="0d13f-112">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) describing the light's position.</span></span>

</dd> <dt>

<span data-ttu-id="0d13f-113">*pPlane* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0d13f-113">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d13f-114">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="0d13f-114">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="0d13f-115">Puntatore [**all'oggetto D3DXPLANE di origine.**](d3d10-d3dxplane.md)</span><span class="sxs-lookup"><span data-stu-id="0d13f-115">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d13f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d13f-116">Return value</span></span>

<span data-ttu-id="0d13f-117">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d13f-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0d13f-118">Puntatore a una struttura D3DXMATRIX che appiattirà la geometria in un piano.</span><span class="sxs-lookup"><span data-stu-id="0d13f-118">Pointer to a D3DXMATRIX structure that flattens geometry into a plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d13f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d13f-119">Remarks</span></span>

<span data-ttu-id="0d13f-120">La **funzione D3DXMatrixShadow** appiattise la geometria in un piano, come se proiettassi un'ombreggiatura da una luce.</span><span class="sxs-lookup"><span data-stu-id="0d13f-120">The **D3DXMatrixShadow** function flattens geometry into a plane, as if casting a shadow from a light.</span></span>

<span data-ttu-id="0d13f-121">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="0d13f-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0d13f-122">In questo modo, la **funzione D3DXMatrixShadow** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="0d13f-122">In this way, the **D3DXMatrixShadow** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0d13f-123">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="0d13f-123">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
L = Light;
d = dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



<span data-ttu-id="0d13f-124">Se il componente w della luce è 0, il raggio dall'origine alla luce rappresenta una luce direzionale.</span><span class="sxs-lookup"><span data-stu-id="0d13f-124">If the light's w-component is 0, the ray from the origin to the light represents a directional light.</span></span> <span data-ttu-id="0d13f-125">Se è 1, la luce è una luce punto.</span><span class="sxs-lookup"><span data-stu-id="0d13f-125">If it is 1, the light is a point light.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d13f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d13f-126">Requirements</span></span>



| <span data-ttu-id="0d13f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d13f-127">Requirement</span></span> | <span data-ttu-id="0d13f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0d13f-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d13f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d13f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0d13f-130"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0d13f-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="0d13f-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="0d13f-131">Library</span></span><br/> | <dl> <span data-ttu-id="0d13f-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d13f-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0d13f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d13f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d13f-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="0d13f-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
