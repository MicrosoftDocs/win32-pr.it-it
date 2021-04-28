---
description: Funzione D3DXMatrixLookAtRH (D3DX10Math.h) - Compila una matrice di tipo right-handed e look-at.
ms.assetid: 98c8932f-f179-42ed-a361-a89065b71876
title: Funzione D3DXMatrixLookAtRH (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0380207124e4a446b6303dbb377d116b8ae058ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103449"
---
# <a name="d3dxmatrixlookatrh-function-d3dx10mathh"></a><span data-ttu-id="2d12c-103">Funzione D3DXMatrixLookAtRH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="2d12c-103">D3DXMatrixLookAtRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="2d12c-104">Crea una matrice di tipo right-handed e look-at.</span><span class="sxs-lookup"><span data-stu-id="2d12c-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d12c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d12c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="2d12c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d12c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d12c-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2d12c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d12c-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d12c-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2d12c-109">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2d12c-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2d12c-110">*pEye* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2d12c-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d12c-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d12c-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2d12c-112">Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che definisce il punto dell'occhio.</span><span class="sxs-lookup"><span data-stu-id="2d12c-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="2d12c-113">Questo valore viene usato nella traduzione.</span><span class="sxs-lookup"><span data-stu-id="2d12c-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="2d12c-114">*pAt* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2d12c-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d12c-115">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d12c-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2d12c-116">Puntatore alla struttura D3DXVECTOR3 che definisce la destinazione di ricerca della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="2d12c-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="2d12c-117">*pUp* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2d12c-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d12c-118">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d12c-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2d12c-119">Puntatore alla struttura D3DXVECTOR3 che definisce il mondo corrente, in genere \[ 0, 1, \] 0.</span><span class="sxs-lookup"><span data-stu-id="2d12c-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d12c-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d12c-120">Return value</span></span>

<span data-ttu-id="2d12c-121">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d12c-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2d12c-122">Puntatore a una struttura D3DXMATRIX che è una matrice di tipo right-handed.</span><span class="sxs-lookup"><span data-stu-id="2d12c-122">Pointer to a D3DXMATRIX structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d12c-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d12c-123">Remarks</span></span>

<span data-ttu-id="2d12c-124">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="2d12c-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2d12c-125">In questo modo, la funzione D3DXMatrixLookAtRH può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="2d12c-125">In this way, the D3DXMatrixLookAtRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2d12c-126">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="2d12c-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 -xaxis.x           yaxis.x           -zaxis.x          0
 -xaxis.y           yaxis.y           -zaxis.y          0
 -xaxis.z           yaxis.z           -zaxis.z          0
dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="2d12c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d12c-127">Requirements</span></span>



| <span data-ttu-id="2d12c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d12c-128">Requirement</span></span> | <span data-ttu-id="2d12c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="2d12c-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d12c-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d12c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2d12c-131"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="2d12c-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2d12c-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="2d12c-132">Library</span></span><br/> | <dl> <span data-ttu-id="2d12c-133"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d12c-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2d12c-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d12c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d12c-135">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="2d12c-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
