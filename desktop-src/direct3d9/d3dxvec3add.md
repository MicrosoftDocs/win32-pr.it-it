---
description: Aggiunge due vettori 3D.
ms.assetid: 2979e291-786b-4bc9-b584-421f08db949a
title: Funzione D3DXVec3Add (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16fb06c5e7b32506a94a5828fe7f5e1305afff7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323296"
---
# <a name="d3dxvec3add-function"></a><span data-ttu-id="98c70-103">D3DXVec3Add (funzione)</span><span class="sxs-lookup"><span data-stu-id="98c70-103">D3DXVec3Add function</span></span>

<span data-ttu-id="98c70-104">Aggiunge due vettori 3D.</span><span class="sxs-lookup"><span data-stu-id="98c70-104">Adds two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="98c70-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98c70-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Add(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="98c70-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="98c70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98c70-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="98c70-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98c70-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="98c70-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="98c70-109">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="98c70-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="98c70-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98c70-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c70-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="98c70-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="98c70-112">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="98c70-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="98c70-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98c70-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c70-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="98c70-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="98c70-115">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="98c70-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98c70-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98c70-116">Return value</span></span>

<span data-ttu-id="98c70-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="98c70-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="98c70-118">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che è la somma dei due vettori 3D.</span><span class="sxs-lookup"><span data-stu-id="98c70-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the sum of the two 3D vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="98c70-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="98c70-119">Remarks</span></span>

<span data-ttu-id="98c70-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="98c70-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="98c70-121">In questo modo, la funzione **D3DXVec3Add** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="98c70-121">In this way, the **D3DXVec3Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="98c70-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98c70-122">Requirements</span></span>



| <span data-ttu-id="98c70-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="98c70-123">Requirement</span></span> | <span data-ttu-id="98c70-124">Valore</span><span class="sxs-lookup"><span data-stu-id="98c70-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98c70-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98c70-125">Header</span></span><br/>  | <dl> <span data-ttu-id="98c70-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="98c70-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="98c70-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="98c70-127">Library</span></span><br/> | <dl> <span data-ttu-id="98c70-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98c70-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="98c70-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98c70-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98c70-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="98c70-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="98c70-131">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="98c70-131">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
</dt> <dt>

[<span data-ttu-id="98c70-132">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="98c70-132">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
</dt> </dl>

 

 




