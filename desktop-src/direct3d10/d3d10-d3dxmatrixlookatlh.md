---
description: Compila una matrice di aspetto a sinistra.
ms.assetid: 06888a97-66ef-447f-be8b-ea458ce16b4b
title: Funzione D3DXMatrixLookAtLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a5a7ffa8750fb08174f45b1069f103bfe08be1f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531039"
---
# <a name="d3dxmatrixlookatlh-function-d3dx10mathh"></a><span data-ttu-id="37b56-103">Funzione D3DXMatrixLookAtLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="37b56-103">D3DXMatrixLookAtLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="37b56-104">Compila una matrice di aspetto a sinistra.</span><span class="sxs-lookup"><span data-stu-id="37b56-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="37b56-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37b56-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="37b56-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="37b56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37b56-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="37b56-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="37b56-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="37b56-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="37b56-109">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="37b56-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="37b56-110">*pEye* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37b56-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37b56-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="37b56-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37b56-112">Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che definisce il punto d'occhio.</span><span class="sxs-lookup"><span data-stu-id="37b56-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="37b56-113">Questo valore viene utilizzato nella conversione.</span><span class="sxs-lookup"><span data-stu-id="37b56-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="37b56-114">*pAt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37b56-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37b56-115">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="37b56-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37b56-116">Puntatore alla struttura D3DXVECTOR3 che definisce la destinazione di ricerca della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="37b56-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="37b56-117">*cucciolo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="37b56-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37b56-118">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="37b56-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="37b56-119">Puntatore alla struttura D3DXVECTOR3 che definisce il mondo corrente, in genere \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="37b56-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37b56-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37b56-120">Return value</span></span>

<span data-ttu-id="37b56-121">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="37b56-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="37b56-122">Puntatore a una struttura D3DXMATRIX che è una matrice di aspetto a sinistra.</span><span class="sxs-lookup"><span data-stu-id="37b56-122">Pointer to a D3DXMATRIX structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="37b56-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="37b56-123">Remarks</span></span>

<span data-ttu-id="37b56-124">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="37b56-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="37b56-125">In questo modo, la funzione D3DXMatrixLookAtLH può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="37b56-125">In this way, the D3DXMatrixLookAtLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="37b56-126">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="37b56-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="37b56-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37b56-127">Requirements</span></span>



| <span data-ttu-id="37b56-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="37b56-128">Requirement</span></span> | <span data-ttu-id="37b56-129">Valore</span><span class="sxs-lookup"><span data-stu-id="37b56-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37b56-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37b56-130">Header</span></span><br/>  | <dl> <span data-ttu-id="37b56-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="37b56-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="37b56-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="37b56-132">Library</span></span><br/> | <dl> <span data-ttu-id="37b56-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37b56-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="37b56-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37b56-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b56-135">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="37b56-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
