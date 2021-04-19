---
description: Ridimensiona un vettore 4D.
ms.assetid: b185a9b9-f768-4b50-aa6c-667c71eac39a
title: Funzione D3DXVec4Scale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a29ee7b8519c802deb0542b6b7ba3ea22692f36d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322856"
---
# <a name="d3dxvec4scale-function"></a><span data-ttu-id="1dbd2-103">D3DXVec4Scale (funzione)</span><span class="sxs-lookup"><span data-stu-id="1dbd2-103">D3DXVec4Scale function</span></span>

<span data-ttu-id="1dbd2-104">Ridimensiona un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="1dbd2-104">Scales a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dbd2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1dbd2-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Scale(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="1dbd2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1dbd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dbd2-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1dbd2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dbd2-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1dbd2-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1dbd2-109">Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1dbd2-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1dbd2-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dbd2-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dbd2-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1dbd2-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1dbd2-112">Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="1dbd2-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1dbd2-113">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dbd2-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dbd2-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1dbd2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1dbd2-115">Valore di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="1dbd2-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dbd2-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1dbd2-116">Return value</span></span>

<span data-ttu-id="1dbd2-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="1dbd2-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1dbd2-118">Puntatore alla struttura [**D3DXVECTOR4**](d3dxvector4.md) che rappresenta il vettore ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="1dbd2-118">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dbd2-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="1dbd2-119">Remarks</span></span>

<span data-ttu-id="1dbd2-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="1dbd2-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1dbd2-121">In questo modo, la funzione **D3DXVec4Scale** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="1dbd2-121">In this way, the **D3DXVec4Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dbd2-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dbd2-122">Requirements</span></span>



| <span data-ttu-id="1dbd2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dbd2-123">Requirement</span></span> | <span data-ttu-id="1dbd2-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1dbd2-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dbd2-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1dbd2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1dbd2-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dbd2-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1dbd2-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="1dbd2-127">Library</span></span><br/> | <dl> <span data-ttu-id="1dbd2-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1dbd2-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1dbd2-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1dbd2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dbd2-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="1dbd2-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1dbd2-131">**D3DXVec4Add**</span><span class="sxs-lookup"><span data-stu-id="1dbd2-131">**D3DXVec4Add**</span></span>](d3dxvec4add.md)
</dt> <dt>

[<span data-ttu-id="1dbd2-132">**D3DXVec4Subtract**</span><span class="sxs-lookup"><span data-stu-id="1dbd2-132">**D3DXVec4Subtract**</span></span>](d3dxvec4subtract.md)
</dt> </dl>

 

 
