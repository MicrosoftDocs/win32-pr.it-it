---
description: Usa l'interpolazione lineare per creare un valore di colore.
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: Funzione D3DXColorLerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorLerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3521ee9e76aecd486093f903d336c08553e0e4ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886291"
---
# <a name="d3dxcolorlerp-function"></a><span data-ttu-id="edddd-103">D3DXColorLerp (funzione)</span><span class="sxs-lookup"><span data-stu-id="edddd-103">D3DXColorLerp function</span></span>

<span data-ttu-id="edddd-104">Usa l'interpolazione lineare per creare un valore di colore.</span><span class="sxs-lookup"><span data-stu-id="edddd-104">Uses linear interpolation to create a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="edddd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="edddd-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorLerp(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="edddd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="edddd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edddd-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="edddd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="edddd-108">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="edddd-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="edddd-109">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che è il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="edddd-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="edddd-110">*pC1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edddd-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edddd-111">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="edddd-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="edddd-112">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="edddd-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="edddd-113">*pC2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edddd-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edddd-114">Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="edddd-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="edddd-115">Puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="edddd-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="edddd-116">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="edddd-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edddd-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="edddd-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="edddd-118">Parametro che esegue l'interpolazione lineare tra i colori, pC1 e pC2, considerandoli entrambi come vettori 4D.</span><span class="sxs-lookup"><span data-stu-id="edddd-118">Parameter that linearly interpolates between the colors, pC1 and pC2, treating them both as 4D vectors.</span></span> <span data-ttu-id="edddd-119">Non sono previsti limiti per il valore di s.</span><span class="sxs-lookup"><span data-stu-id="edddd-119">There are no limits on the value of s.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edddd-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="edddd-120">Return value</span></span>

<span data-ttu-id="edddd-121">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="edddd-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="edddd-122">Questa funzione restituisce un puntatore a una struttura [**D3DXCOLOR**](d3dxcolor.md) che è il risultato dell'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="edddd-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="edddd-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="edddd-123">Remarks</span></span>

<span data-ttu-id="edddd-124">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="edddd-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="edddd-125">In questo modo, la funzione **D3DXColorLerp** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="edddd-125">In this way, the **D3DXColorLerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="edddd-126">Questa funzione esegue l'interpolazione dei componenti rosso, verde, blu e alfa di una struttura [**D3DXCOLOR**](d3dxcolor.md) tra due colori, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="edddd-126">This function interpolates the red, green, blue, and alpha components of a [**D3DXCOLOR**](d3dxcolor.md) structure between two colors, as shown in the following example.</span></span>


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



<span data-ttu-id="edddd-127">Se si esegue l'interpolazione lineare tra i colori A e B e s è 0, il colore risultante è un. Se s è 1, il colore risultante è il colore B.</span><span class="sxs-lookup"><span data-stu-id="edddd-127">If you are linearly interpolating between the colors A and B, and s is 0, the resulting color is A. If s is 1, the resulting color is color B.</span></span>

## <a name="requirements"></a><span data-ttu-id="edddd-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edddd-128">Requirements</span></span>



| <span data-ttu-id="edddd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="edddd-129">Requirement</span></span> | <span data-ttu-id="edddd-130">Valore</span><span class="sxs-lookup"><span data-stu-id="edddd-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edddd-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="edddd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="edddd-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="edddd-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="edddd-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="edddd-133">Library</span></span><br/> | <dl> <span data-ttu-id="edddd-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edddd-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="edddd-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="edddd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edddd-136">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="edddd-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="edddd-137">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="edddd-137">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="edddd-138">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="edddd-138">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> <dt>

[<span data-ttu-id="edddd-139">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="edddd-139">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 
