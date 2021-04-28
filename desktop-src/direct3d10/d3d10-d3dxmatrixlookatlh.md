---
description: 'Funzione D3DXMatrixLookAtLH (D3DX10Math.h): compila una matrice di tipo left-handed e look-at.'
ms.assetid: 06888a97-66ef-447f-be8b-ea458ce16b4b
title: Funzione D3DXMatrixLookAtLH (D3DX10Math.h)
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
ms.openlocfilehash: 3590d2cbdeead9e1b9b2547b2344163b81f05d11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109169"
---
# <a name="d3dxmatrixlookatlh-function-d3dx10mathh"></a><span data-ttu-id="03576-103">Funzione D3DXMatrixLookAtLH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="03576-103">D3DXMatrixLookAtLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="03576-104">Compila una matrice di tipo left-handed e look-at.</span><span class="sxs-lookup"><span data-stu-id="03576-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="03576-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03576-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="03576-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="03576-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03576-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="03576-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="03576-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="03576-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="03576-109">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="03576-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="03576-110">*pEye* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="03576-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03576-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="03576-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="03576-112">Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che definisce il punto dell'occhio.</span><span class="sxs-lookup"><span data-stu-id="03576-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="03576-113">Questo valore viene usato nella traduzione.</span><span class="sxs-lookup"><span data-stu-id="03576-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="03576-114">*pAt* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="03576-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03576-115">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="03576-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="03576-116">Puntatore alla struttura D3DXVECTOR3 che definisce la destinazione di ricerca della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="03576-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="03576-117">*pUp* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="03576-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03576-118">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="03576-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="03576-119">Puntatore alla struttura D3DXVECTOR3 che definisce il mondo corrente, in genere \[ 0, 1, \] 0.</span><span class="sxs-lookup"><span data-stu-id="03576-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03576-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03576-120">Return value</span></span>

<span data-ttu-id="03576-121">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="03576-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="03576-122">Puntatore a una struttura D3DXMATRIX che è una matrice di tipo left-handed.</span><span class="sxs-lookup"><span data-stu-id="03576-122">Pointer to a D3DXMATRIX structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="03576-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="03576-123">Remarks</span></span>

<span data-ttu-id="03576-124">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="03576-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="03576-125">In questo modo, la funzione D3DXMatrixLookAtLH può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="03576-125">In this way, the D3DXMatrixLookAtLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="03576-126">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="03576-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="03576-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03576-127">Requirements</span></span>



| <span data-ttu-id="03576-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="03576-128">Requirement</span></span> | <span data-ttu-id="03576-129">Valore</span><span class="sxs-lookup"><span data-stu-id="03576-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03576-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03576-130">Header</span></span><br/>  | <dl> <span data-ttu-id="03576-131"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="03576-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="03576-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="03576-132">Library</span></span><br/> | <dl> <span data-ttu-id="03576-133"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="03576-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="03576-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03576-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03576-135">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="03576-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
