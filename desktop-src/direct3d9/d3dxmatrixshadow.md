---
description: Compila una matrice che appiattisce la geometria in un piano.
ms.assetid: 8f283ff9-c879-476c-8057-f4fe77a7a9e7
title: Funzione D3DXMatrixShadow (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6bf1639adb7364536cce5c0dead9ef58ae10bea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322637"
---
# <a name="d3dxmatrixshadow-function-d3dx9mathh"></a><span data-ttu-id="007e0-103">Funzione D3DXMatrixShadow (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="007e0-103">D3DXMatrixShadow function (D3dx9math.h)</span></span>

<span data-ttu-id="007e0-104">Compila una matrice che appiattisce la geometria in un piano.</span><span class="sxs-lookup"><span data-stu-id="007e0-104">Builds a matrix that flattens geometry into a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="007e0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="007e0-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="007e0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="007e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="007e0-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="007e0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="007e0-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="007e0-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="007e0-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="007e0-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="007e0-110">*situazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="007e0-110">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="007e0-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="007e0-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="007e0-112">Puntatore a una struttura [**D3DXVECTOR4**](d3dxvector4.md) che descrive la posizione della luce.</span><span class="sxs-lookup"><span data-stu-id="007e0-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure describing the light's position.</span></span>

</dd> <dt>

<span data-ttu-id="007e0-113">*pPlane* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="007e0-113">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="007e0-114">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="007e0-114">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="007e0-115">Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="007e0-115">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="007e0-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="007e0-116">Return value</span></span>

<span data-ttu-id="007e0-117">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="007e0-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="007e0-118">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che appiattisce la geometria in un piano.</span><span class="sxs-lookup"><span data-stu-id="007e0-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that flattens geometry into a plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="007e0-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="007e0-119">Remarks</span></span>

<span data-ttu-id="007e0-120">La funzione **D3DXMatrixShadow** rende flat la geometria in un piano, come se si proiettasse un'ombreggiatura da una luce.</span><span class="sxs-lookup"><span data-stu-id="007e0-120">The **D3DXMatrixShadow** function flattens geometry into a plane, as if casting a shadow from a light.</span></span>

<span data-ttu-id="007e0-121">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="007e0-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="007e0-122">In questo modo, la funzione **D3DXMatrixShadow** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="007e0-122">In this way, the **D3DXMatrixShadow** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="007e0-123">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="007e0-123">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
L = Light;
d = -dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



<span data-ttu-id="007e0-124">Se il componente w della luce è 0, il raggio dall'origine alla luce rappresenta una luce direzionale.</span><span class="sxs-lookup"><span data-stu-id="007e0-124">If the light's w-component is 0, the ray from the origin to the light represents a directional light.</span></span> <span data-ttu-id="007e0-125">Se è 1, la luce è una luce puntiforme.</span><span class="sxs-lookup"><span data-stu-id="007e0-125">If it is 1, the light is a point light.</span></span>

## <a name="requirements"></a><span data-ttu-id="007e0-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="007e0-126">Requirements</span></span>



| <span data-ttu-id="007e0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="007e0-127">Requirement</span></span> | <span data-ttu-id="007e0-128">Valore</span><span class="sxs-lookup"><span data-stu-id="007e0-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="007e0-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="007e0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="007e0-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="007e0-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="007e0-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="007e0-131">Library</span></span><br/> | <dl> <span data-ttu-id="007e0-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="007e0-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="007e0-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="007e0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="007e0-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="007e0-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




