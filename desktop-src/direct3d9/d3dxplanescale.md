---
description: Ridimensionare il piano con il fattore di scala specificato.
ms.assetid: 3a0454ef-2821-472f-b7a4-5e49bb5f556e
title: Funzione D3DXPlaneScale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39bd80ceebaee915b8175f2adf13b3b200000fa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322097"
---
# <a name="d3dxplanescale-function"></a><span data-ttu-id="73c23-103">D3DXPlaneScale (funzione)</span><span class="sxs-lookup"><span data-stu-id="73c23-103">D3DXPlaneScale function</span></span>

<span data-ttu-id="73c23-104">Ridimensionare il piano con il fattore di scala specificato.</span><span class="sxs-lookup"><span data-stu-id="73c23-104">Scale the plane with the given scaling factor.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c23-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73c23-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneScale(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="73c23-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="73c23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73c23-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="73c23-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="73c23-108">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="73c23-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="73c23-109">Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="73c23-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="73c23-110">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73c23-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c23-111">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="73c23-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="73c23-112">Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="73c23-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="73c23-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73c23-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c23-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c23-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="73c23-115">Fattore di scala.</span><span class="sxs-lookup"><span data-stu-id="73c23-115">Scale factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73c23-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73c23-116">Return value</span></span>

<span data-ttu-id="73c23-117">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="73c23-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="73c23-118">Puntatore a una struttura [**D3DXPLANE**](d3dxplane.md) che rappresenta il piano ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="73c23-118">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure that represents the scaled plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="73c23-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="73c23-119">Remarks</span></span>

<span data-ttu-id="73c23-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="73c23-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="73c23-121">Questa funzione può pertanto essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="73c23-121">Therefore, this function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="73c23-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73c23-122">Requirements</span></span>



| <span data-ttu-id="73c23-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="73c23-123">Requirement</span></span> | <span data-ttu-id="73c23-124">Valore</span><span class="sxs-lookup"><span data-stu-id="73c23-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73c23-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73c23-125">Header</span></span><br/>  | <dl> <span data-ttu-id="73c23-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="73c23-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="73c23-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="73c23-127">Library</span></span><br/> | <dl> <span data-ttu-id="73c23-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73c23-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="73c23-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73c23-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c23-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="73c23-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
