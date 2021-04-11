---
description: Compila un quaternione da una matrice di rotazione.
ms.assetid: 316bf3e0-32ff-4e5e-b771-99f7eea2e27c
title: Funzione D3DXQuaternionRotationMatrix (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1caccf47e03388ffb85f2e12a5d0203f3fe839bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235156"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx10mathh"></a><span data-ttu-id="63127-103">Funzione D3DXQuaternionRotationMatrix (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="63127-103">D3DXQuaternionRotationMatrix function (D3DX10Math.h)</span></span>

<span data-ttu-id="63127-104">Compila un quaternione da una matrice di rotazione.</span><span class="sxs-lookup"><span data-stu-id="63127-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="63127-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63127-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="63127-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="63127-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63127-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="63127-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63127-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="63127-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="63127-109">Puntatore a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="63127-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="63127-110">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63127-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63127-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="63127-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="63127-112">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="63127-112">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63127-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63127-113">Return value</span></span>

<span data-ttu-id="63127-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="63127-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="63127-115">Puntatore alla struttura D3DXQUATERNION compilata da una matrice di rotazione.</span><span class="sxs-lookup"><span data-stu-id="63127-115">Pointer to the D3DXQUATERNION structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="63127-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="63127-116">Remarks</span></span>

<span data-ttu-id="63127-117">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="63127-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="63127-118">In questo modo, la funzione D3DXQuaternionRotationMatrix può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="63127-118">In this way, the D3DXQuaternionRotationMatrix function can be used as a parameter for another function.</span></span>

<span data-ttu-id="63127-119">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="63127-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="63127-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63127-120">Requirements</span></span>



| <span data-ttu-id="63127-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="63127-121">Requirement</span></span> | <span data-ttu-id="63127-122">Valore</span><span class="sxs-lookup"><span data-stu-id="63127-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63127-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63127-123">Header</span></span><br/>  | <dl> <span data-ttu-id="63127-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="63127-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="63127-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="63127-125">Library</span></span><br/> | <dl> <span data-ttu-id="63127-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63127-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="63127-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63127-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63127-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="63127-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
