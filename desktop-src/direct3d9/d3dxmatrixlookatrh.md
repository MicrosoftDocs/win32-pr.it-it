---
description: Compila una matrice di ricerca a destra.
ms.assetid: 10198bb9-a77e-4482-be6e-cc5f76eff30b
title: Funzione D3DXMatrixLookAtRH (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f09b57d46c6c5dea51c9b55ce6fe507d5bfe415
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354204"
---
# <a name="d3dxmatrixlookatrh-function-d3dx9mathh"></a><span data-ttu-id="99bcf-103">Funzione D3DXMatrixLookAtRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="99bcf-103">D3DXMatrixLookAtRH function (D3dx9math.h)</span></span>

<span data-ttu-id="99bcf-104">Compila una matrice di ricerca a destra.</span><span class="sxs-lookup"><span data-stu-id="99bcf-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="99bcf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99bcf-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="99bcf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="99bcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99bcf-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="99bcf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99bcf-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="99bcf-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="99bcf-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="99bcf-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="99bcf-110">*pEye* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99bcf-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99bcf-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="99bcf-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="99bcf-112">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che definisce il punto d'occhio.</span><span class="sxs-lookup"><span data-stu-id="99bcf-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="99bcf-113">Questo valore viene utilizzato nella conversione.</span><span class="sxs-lookup"><span data-stu-id="99bcf-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="99bcf-114">*pAt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99bcf-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99bcf-115">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="99bcf-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="99bcf-116">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che definisce la destinazione di ricerca della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="99bcf-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="99bcf-117">*cucciolo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99bcf-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99bcf-118">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="99bcf-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="99bcf-119">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che definisce il mondo corrente, in genere \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="99bcf-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99bcf-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99bcf-120">Return value</span></span>

<span data-ttu-id="99bcf-121">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="99bcf-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="99bcf-122">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che è una matrice di ricerca a destra.</span><span class="sxs-lookup"><span data-stu-id="99bcf-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="99bcf-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="99bcf-123">Remarks</span></span>

<span data-ttu-id="99bcf-124">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="99bcf-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="99bcf-125">In questo modo, la funzione **D3DXMatrixLookAtRH** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="99bcf-125">In this way, the **D3DXMatrixLookAtRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="99bcf-126">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="99bcf-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
 dot(xaxis, eye)   dot(yaxis, eye)   dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="99bcf-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99bcf-127">Requirements</span></span>



| <span data-ttu-id="99bcf-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="99bcf-128">Requirement</span></span> | <span data-ttu-id="99bcf-129">Valore</span><span class="sxs-lookup"><span data-stu-id="99bcf-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99bcf-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99bcf-130">Header</span></span><br/>  | <dl> <span data-ttu-id="99bcf-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="99bcf-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="99bcf-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="99bcf-132">Library</span></span><br/> | <dl> <span data-ttu-id="99bcf-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99bcf-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="99bcf-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99bcf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99bcf-135">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="99bcf-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="99bcf-136">**D3DXMatrixLookAtLH**</span><span class="sxs-lookup"><span data-stu-id="99bcf-136">**D3DXMatrixLookAtLH**</span></span>](d3dxmatrixlookatlh.md)
</dt> </dl>

 

 




