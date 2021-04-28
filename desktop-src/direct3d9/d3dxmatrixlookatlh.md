---
description: 'Funzione D3DXMatrixLookAtLH (D3dx9math.h): compila una matrice di tipo left-handed e look-at.'
ms.assetid: bf34d3d8-725d-4fc1-b4c8-6c98f9dac329
title: Funzione D3DXMatrixLookAtLH (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94a423e700c4a42e2ae7f7e522d83a5a4bd9bf3a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107589"
---
# <a name="d3dxmatrixlookatlh-function-d3dx9mathh"></a><span data-ttu-id="c5f8a-103">Funzione D3DXMatrixLookAtLH (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="c5f8a-103">D3DXMatrixLookAtLH function (D3dx9math.h)</span></span>

<span data-ttu-id="c5f8a-104">Compila una matrice di tipo left-handed e look-at.</span><span class="sxs-lookup"><span data-stu-id="c5f8a-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5f8a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5f8a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="c5f8a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5f8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5f8a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c5f8a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f8a-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5f8a-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c5f8a-109">Puntatore alla [**struttura D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c5f8a-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c5f8a-110">*pEye* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c5f8a-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f8a-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c5f8a-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c5f8a-112">Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che definisce il punto dell'occhio.</span><span class="sxs-lookup"><span data-stu-id="c5f8a-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="c5f8a-113">Questo valore viene usato nella conversione.</span><span class="sxs-lookup"><span data-stu-id="c5f8a-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="c5f8a-114">*pAt* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c5f8a-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f8a-115">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c5f8a-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c5f8a-116">Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che definisce la destinazione di ricerca della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="c5f8a-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="c5f8a-117">*pUp* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c5f8a-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f8a-118">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c5f8a-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c5f8a-119">Puntatore alla [**struttura D3DXVECTOR3**](d3dxvector3.md) che definisce il mondo corrente verso l'alto, in genere \[ 0, 1, \] 0.</span><span class="sxs-lookup"><span data-stu-id="c5f8a-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5f8a-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5f8a-120">Return value</span></span>

<span data-ttu-id="c5f8a-121">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5f8a-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c5f8a-122">Puntatore a [**una struttura D3DXMATRIX**](d3dxmatrix.md) che è una matrice di tipo left-handed.</span><span class="sxs-lookup"><span data-stu-id="c5f8a-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5f8a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5f8a-123">Remarks</span></span>

<span data-ttu-id="c5f8a-124">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="c5f8a-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c5f8a-125">In questo modo, la **funzione D3DXMatrixLookAtLH** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="c5f8a-125">In this way, the **D3DXMatrixLookAtLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c5f8a-126">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="c5f8a-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="c5f8a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5f8a-127">Requirements</span></span>



| <span data-ttu-id="c5f8a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5f8a-128">Requirement</span></span> | <span data-ttu-id="c5f8a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c5f8a-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5f8a-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5f8a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c5f8a-131"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c5f8a-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c5f8a-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="c5f8a-132">Library</span></span><br/> | <dl> <span data-ttu-id="c5f8a-133"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5f8a-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c5f8a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5f8a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5f8a-135">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="c5f8a-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c5f8a-136">**D3DXMatrixLookAtRH**</span><span class="sxs-lookup"><span data-stu-id="c5f8a-136">**D3DXMatrixLookAtRH**</span></span>](d3dxmatrixlookatrh.md)
</dt> </dl>

 

 




