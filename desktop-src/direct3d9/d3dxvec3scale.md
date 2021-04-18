---
description: Ridimensiona un vettore 3D.
ms.assetid: b2483d6e-56e4-4557-a603-d59c0767774d
title: Funzione D3DXVec3Scale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5357b862b9cf82e458429edea27001163eb9635
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323646"
---
# <a name="d3dxvec3scale-function"></a><span data-ttu-id="512df-103">D3DXVec3Scale (funzione)</span><span class="sxs-lookup"><span data-stu-id="512df-103">D3DXVec3Scale function</span></span>

<span data-ttu-id="512df-104">Ridimensiona un vettore 3D.</span><span class="sxs-lookup"><span data-stu-id="512df-104">Scales a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="512df-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="512df-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Scale(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="512df-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="512df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="512df-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="512df-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="512df-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="512df-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="512df-109">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="512df-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="512df-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="512df-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="512df-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="512df-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="512df-112">Puntatore alla struttura [**D3DXVECTOR3**](d3dxvector3.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="512df-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="512df-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="512df-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="512df-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="512df-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="512df-115">Valore di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="512df-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="512df-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="512df-116">Return value</span></span>

<span data-ttu-id="512df-117">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="512df-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="512df-118">Puntatore a una struttura [**D3DXVECTOR3**](d3dxvector3.md) che rappresenta il vettore ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="512df-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="512df-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="512df-119">Remarks</span></span>

<span data-ttu-id="512df-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="512df-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="512df-121">In questo modo, la funzione **D3DXVec3Scale** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="512df-121">In this way, the **D3DXVec3Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="512df-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="512df-122">Requirements</span></span>



| <span data-ttu-id="512df-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="512df-123">Requirement</span></span> | <span data-ttu-id="512df-124">Valore</span><span class="sxs-lookup"><span data-stu-id="512df-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="512df-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="512df-125">Header</span></span><br/>  | <dl> <span data-ttu-id="512df-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="512df-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="512df-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="512df-127">Library</span></span><br/> | <dl> <span data-ttu-id="512df-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="512df-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="512df-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="512df-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="512df-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="512df-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="512df-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="512df-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="512df-132">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="512df-132">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
</dt> </dl>

 

 
