---
description: Compila una matrice di ricerca a destra.
ms.assetid: 98c8932f-f179-42ed-a361-a89065b71876
title: Funzione D3DXMatrixLookAtRH (D3DX10Math. h)
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
ms.openlocfilehash: 28c2ad0cc7eb8a3ba98aacadc764bc277a1fdad0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058648"
---
# <a name="d3dxmatrixlookatrh-function-d3dx10mathh"></a><span data-ttu-id="0bd8e-103">Funzione D3DXMatrixLookAtRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="0bd8e-103">D3DXMatrixLookAtRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="0bd8e-104">Compila una matrice di ricerca a destra.</span><span class="sxs-lookup"><span data-stu-id="0bd8e-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bd8e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0bd8e-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="0bd8e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0bd8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bd8e-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0bd8e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bd8e-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bd8e-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0bd8e-109">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0bd8e-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0bd8e-110">*pEye* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bd8e-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bd8e-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bd8e-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0bd8e-112">Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che definisce il punto d'occhio.</span><span class="sxs-lookup"><span data-stu-id="0bd8e-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="0bd8e-113">Questo valore viene utilizzato nella conversione.</span><span class="sxs-lookup"><span data-stu-id="0bd8e-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="0bd8e-114">*pAt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bd8e-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bd8e-115">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bd8e-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0bd8e-116">Puntatore alla struttura D3DXVECTOR3 che definisce la destinazione di ricerca della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="0bd8e-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="0bd8e-117">*cucciolo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bd8e-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bd8e-118">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bd8e-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0bd8e-119">Puntatore alla struttura D3DXVECTOR3 che definisce il mondo corrente, in genere \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="0bd8e-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bd8e-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0bd8e-120">Return value</span></span>

<span data-ttu-id="0bd8e-121">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0bd8e-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0bd8e-122">Puntatore a una struttura D3DXMATRIX che è una matrice di ricerca a destra.</span><span class="sxs-lookup"><span data-stu-id="0bd8e-122">Pointer to a D3DXMATRIX structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bd8e-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="0bd8e-123">Remarks</span></span>

<span data-ttu-id="0bd8e-124">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="0bd8e-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0bd8e-125">In questo modo, la funzione D3DXMatrixLookAtRH può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="0bd8e-125">In this way, the D3DXMatrixLookAtRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0bd8e-126">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="0bd8e-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 -xaxis.x           yaxis.x           -zaxis.x          0
 -xaxis.y           yaxis.y           -zaxis.y          0
 -xaxis.z           yaxis.z           -zaxis.z          0
dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="0bd8e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0bd8e-127">Requirements</span></span>



| <span data-ttu-id="0bd8e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bd8e-128">Requirement</span></span> | <span data-ttu-id="0bd8e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0bd8e-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd8e-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0bd8e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="0bd8e-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bd8e-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="0bd8e-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="0bd8e-132">Library</span></span><br/> | <dl> <span data-ttu-id="0bd8e-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bd8e-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0bd8e-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0bd8e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bd8e-135">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="0bd8e-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
