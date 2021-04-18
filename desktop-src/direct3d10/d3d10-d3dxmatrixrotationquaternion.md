---
description: Compila una matrice di rotazione da un quaternione.
ms.assetid: dcbf8696-b959-4475-a250-6094dd5fe358
title: Funzione D3DXMatrixRotationQuaternion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationQuaternion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 44cd4a5982b322c2d207263fb490c898ed9fa76e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323341"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx10mathh"></a><span data-ttu-id="e462c-103">Funzione D3DXMatrixRotationQuaternion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e462c-103">D3DXMatrixRotationQuaternion function (D3DX10Math.h)</span></span>

<span data-ttu-id="e462c-104">Compila una matrice di rotazione da un quaternione.</span><span class="sxs-lookup"><span data-stu-id="e462c-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="e462c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e462c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="e462c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e462c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e462c-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e462c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e462c-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e462c-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e462c-109">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e462c-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e462c-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e462c-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e462c-111">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e462c-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e462c-112">Puntatore alla struttura D3DXQUATERNION di origine.</span><span class="sxs-lookup"><span data-stu-id="e462c-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e462c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e462c-113">Return value</span></span>

<span data-ttu-id="e462c-114">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e462c-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e462c-115">Puntatore a una struttura D3DXMATRIX compilata dal quaternione di origine.</span><span class="sxs-lookup"><span data-stu-id="e462c-115">Pointer to a D3DXMATRIX structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="e462c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e462c-116">Remarks</span></span>

<span data-ttu-id="e462c-117">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="e462c-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e462c-118">In questo modo, la funzione D3DXMatrixRotationQuaternion può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="e462c-118">In this way, the D3DXMatrixRotationQuaternion function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e462c-119">Per informazioni su come calcolare i valori Quaternion da un vettore di direzione (x, y, z) e un angolo di rotazione, vedere [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="e462c-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e462c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e462c-120">Requirements</span></span>



| <span data-ttu-id="e462c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e462c-121">Requirement</span></span> | <span data-ttu-id="e462c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e462c-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e462c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e462c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e462c-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e462c-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e462c-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="e462c-125">Library</span></span><br/> | <dl> <span data-ttu-id="e462c-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e462c-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e462c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e462c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e462c-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="e462c-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
