---
description: Compila una matrice di rotazione da un quaternione.
ms.assetid: e590058c-772b-4eef-aab0-a12bb04c299a
title: Funzione D3DXMatrixRotationQuaternion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275a369da106e9f114ce47286f0f6ea9ce381ecb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323238"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx9mathh"></a><span data-ttu-id="a94e0-103">Funzione D3DXMatrixRotationQuaternion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a94e0-103">D3DXMatrixRotationQuaternion function (D3dx9math.h)</span></span>

<span data-ttu-id="a94e0-104">Compila una matrice di rotazione da un quaternione.</span><span class="sxs-lookup"><span data-stu-id="a94e0-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="a94e0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a94e0-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="a94e0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a94e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a94e0-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a94e0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a94e0-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a94e0-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a94e0-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a94e0-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a94e0-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a94e0-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a94e0-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="a94e0-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="a94e0-112">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="a94e0-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a94e0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a94e0-113">Return value</span></span>

<span data-ttu-id="a94e0-114">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a94e0-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a94e0-115">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) compilata dal quaternione di origine.</span><span class="sxs-lookup"><span data-stu-id="a94e0-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="a94e0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a94e0-116">Remarks</span></span>

<span data-ttu-id="a94e0-117">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="a94e0-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a94e0-118">In questo modo, la funzione **D3DXMatrixRotationQuaternion** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="a94e0-118">In this way, the **D3DXMatrixRotationQuaternion** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a94e0-119">Per informazioni su come calcolare i valori Quaternion da un vettore di direzione (x, y, z) e un angolo di rotazione, vedere [**D3DXQUATERNION**](d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="a94e0-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a94e0-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a94e0-120">Requirements</span></span>



| <span data-ttu-id="a94e0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a94e0-121">Requirement</span></span> | <span data-ttu-id="a94e0-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a94e0-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a94e0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a94e0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a94e0-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a94e0-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a94e0-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="a94e0-125">Library</span></span><br/> | <dl> <span data-ttu-id="a94e0-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a94e0-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a94e0-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a94e0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a94e0-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="a94e0-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a94e0-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="a94e0-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="a94e0-130">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="a94e0-130">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="a94e0-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="a94e0-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="a94e0-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="a94e0-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="a94e0-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="a94e0-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 




