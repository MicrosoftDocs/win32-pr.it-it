---
title: Funzione D2DGetInputCoordinate (D2d1effecthelpers. h)
description: Restituisce il valore di TEXCOORDN di input. Disponibile solo per gli input complessi.
ms.assetid: 60125E23-53B3-45ED-89FE-684E79004F6B
keywords:
- Direct2D funzione D2DGetInputCoordinate
topic_type:
- apiref
api_name:
- D2DGetInputCoordinate
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5d9ee759de12bb8b017d582026dd5b5ca8c3fb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332365"
---
# <a name="d2dgetinputcoordinate-function"></a><span data-ttu-id="26c09-105">D2DGetInputCoordinate (funzione)</span><span class="sxs-lookup"><span data-stu-id="26c09-105">D2DGetInputCoordinate function</span></span>

<span data-ttu-id="26c09-106">Restituisce il valore di TEXCOORDN di input.</span><span class="sxs-lookup"><span data-stu-id="26c09-106">Returns the value of the input TEXCOORDN.</span></span> <span data-ttu-id="26c09-107">Disponibile solo per gli input complessi.</span><span class="sxs-lookup"><span data-stu-id="26c09-107">Available only for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="26c09-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26c09-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a><span data-ttu-id="26c09-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="26c09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26c09-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26c09-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26c09-111">Numero di input.</span><span class="sxs-lookup"><span data-stu-id="26c09-111">The input number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26c09-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26c09-112">Return value</span></span>

<span data-ttu-id="26c09-113">La funzione restituisce un **float4** nel formato TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="26c09-113">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="26c09-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="26c09-114">Remarks</span></span>

<span data-ttu-id="26c09-115">La coordinata restituita da questa funzione è nello spazio Texel.</span><span class="sxs-lookup"><span data-stu-id="26c09-115">The coordinate returned by this function is in texel space.</span></span> <span data-ttu-id="26c09-116">Uno shader non deve prendere alcuna dipendenza dal modo in cui questo valore viene calcolato.</span><span class="sxs-lookup"><span data-stu-id="26c09-116">A shader shouldn't take any dependencies on how this value is calculated.</span></span> <span data-ttu-id="26c09-117">Deve utilizzarlo solo per campionare l'input del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="26c09-117">It should use it only to sample the pixel shader's input.</span></span> <span data-ttu-id="26c09-118">Per altre informazioni, vedere [aggiunta di un pixel shader a una trasformazione personalizzata](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).</span><span class="sxs-lookup"><span data-stu-id="26c09-118">For more info, see [Adding a pixel shader to a custom transform](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).</span></span>

<span data-ttu-id="26c09-119">Nell'esempio seguente viene illustrata la funzione utilizzata per un effetto Mappa di spostamento.</span><span class="sxs-lookup"><span data-stu-id="26c09-119">The following example shows the function used for a displacement map effect.</span></span>

``` syntax
float2 GetDisplacementOffset(float4 uv0, float4 uv1)  
{  
    // TODO: return the displacement offset 
}  
  
D2D_PS_ENTRY(DisplacementMapBilinear)  
{  
    const float4 coord0 = D2DGetInputCoordinate(0);  
    const float4 coord1 = D2DGetInputCoordinate(1);  
    return D2DSampleInput(0, GetDisplacementOffset(coord0, coord1) * coord0.zw + coord0.xy);  
}  
```

## <a name="requirements"></a><span data-ttu-id="26c09-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26c09-120">Requirements</span></span>



| <span data-ttu-id="26c09-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="26c09-121">Requirement</span></span> | <span data-ttu-id="26c09-122">Valore</span><span class="sxs-lookup"><span data-stu-id="26c09-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26c09-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26c09-123">Header</span></span><br/> | <dl> <span data-ttu-id="26c09-124"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="26c09-124"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="26c09-125">DLL</span><span class="sxs-lookup"><span data-stu-id="26c09-125">DLL</span></span><br/>    | <dl> <span data-ttu-id="26c09-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26c09-126"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="26c09-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26c09-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c09-128">Collegamento Effect shader</span><span class="sxs-lookup"><span data-stu-id="26c09-128">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="26c09-129">Helper HLSL</span><span class="sxs-lookup"><span data-stu-id="26c09-129">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

