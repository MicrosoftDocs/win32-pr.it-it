---
description: Aggiunge due valori di colore per creare un nuovo valore di colore.
ms.assetid: 7743392d-4676-4408-93e9-f92d4bf02411
title: Funzione D3DXColorAdd (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f326c9bec4802a9a94accc76b825cd1c6ea28fd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323015"
---
# <a name="d3dxcoloradd-function"></a><span data-ttu-id="5785b-103">D3DXColorAdd (funzione)</span><span class="sxs-lookup"><span data-stu-id="5785b-103">D3DXColorAdd function</span></span>

<span data-ttu-id="5785b-104">Aggiunge due valori di colore per creare un nuovo valore di colore.</span><span class="sxs-lookup"><span data-stu-id="5785b-104">Adds two color values together to create a new color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5785b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5785b-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdd(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="5785b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5785b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5785b-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5785b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5785b-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="5785b-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="5785b-109">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5785b-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5785b-110">*pC1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5785b-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5785b-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="5785b-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="5785b-112">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="5785b-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5785b-113">*pC2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5785b-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5785b-114">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="5785b-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="5785b-115">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="5785b-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5785b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5785b-116">Return value</span></span>

<span data-ttu-id="5785b-117">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="5785b-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="5785b-118">Questa funzione restituisce un puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che è la somma di due valori di colore.</span><span class="sxs-lookup"><span data-stu-id="5785b-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the sum of two color values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5785b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5785b-119">Remarks</span></span>

<span data-ttu-id="5785b-120">Il valore restituito per questa funzione è lo stesso valore restituito in broncio.</span><span class="sxs-lookup"><span data-stu-id="5785b-120">The return value for this function is the same value returned in pOut.</span></span> <span data-ttu-id="5785b-121">In questo modo, la funzione **D3DXColorAdd** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="5785b-121">In this way, the **D3DXColorAdd** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5785b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5785b-122">Requirements</span></span>



| <span data-ttu-id="5785b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5785b-123">Requirement</span></span> | <span data-ttu-id="5785b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5785b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5785b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5785b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5785b-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5785b-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5785b-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="5785b-127">Library</span></span><br/> | <dl> <span data-ttu-id="5785b-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5785b-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5785b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5785b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5785b-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="5785b-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5785b-131">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="5785b-131">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="5785b-132">**D3DXColorSubtract**</span><span class="sxs-lookup"><span data-stu-id="5785b-132">**D3DXColorSubtract**</span></span>](d3dxcolorsubtract.md)
</dt> </dl>

 

 




