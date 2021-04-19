---
title: Funzione D2DSampleInputAtOffset (D2d1effecthelpers. h)
description: Campiona l'input N a un offset di offset dalla coordinata di input. Disponibile solo per gli input complessi.
ms.assetid: 4A01264E-04E3-49BD-9EF8-7834D9B8B0B8
keywords:
- Direct2D funzione D2DSampleInputAtOffset
topic_type:
- apiref
api_name:
- D2DSampleInputAtOffset
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7718f8f48ddfd316d1312dbdff3a5da1f45dfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332785"
---
# <a name="d2dsampleinputatoffset-function"></a><span data-ttu-id="e030e-105">D2DSampleInputAtOffset (funzione)</span><span class="sxs-lookup"><span data-stu-id="e030e-105">D2DSampleInputAtOffset function</span></span>

<span data-ttu-id="e030e-106">Campiona l'input N a un offset di offset dalla coordinata di input.</span><span class="sxs-lookup"><span data-stu-id="e030e-106">Samples input N at an offset of offset from the input coordinate.</span></span> <span data-ttu-id="e030e-107">Disponibile solo per gli input complessi.</span><span class="sxs-lookup"><span data-stu-id="e030e-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="e030e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e030e-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInputAtOffset(
  in uint N,
  in float2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="e030e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e030e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e030e-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e030e-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e030e-111">Numero di input.</span><span class="sxs-lookup"><span data-stu-id="e030e-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="e030e-112">*offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e030e-112">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e030e-113">Offset UV.</span><span class="sxs-lookup"><span data-stu-id="e030e-113">The uv offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e030e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e030e-114">Return value</span></span>

<span data-ttu-id="e030e-115">La funzione restituisce un **float4** nel formato TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="e030e-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="e030e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e030e-116">Remarks</span></span>

<span data-ttu-id="e030e-117">Nell'esempio seguente viene illustrata la funzione utilizzata come parte di una maschera di sfumatura di evidenziazione e ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="e030e-117">The following example shows the function being used as part of a highlighting and shadows gradient mask.</span></span>

``` syntax
  
D2D_PS_ENTRY(HighlightsAndShadowsGradientMask)  
{  
    MIN_TYPE(float4) blurred = D2DGetInput(0);  
  
    // Compute X and Y gradients 
    MIN_TYPE(float) dX1 = D2DSampleInputAtOffset(0, float2(1, 0));
    MIN_TYPE(float) dX2 = D2DSampleInputAtOffset(0, float2(-1, 0));
    MIN_TYPE(float) dY1 = D2DSampleInputAtOffset(0, float2(0, 1));
    MIN_TYPE(float) dY2 = D2DSampleInputAtOffset(0, float2(0, -1));
    
    // TODO: math to calculate shadow gradients

    // Return the value in the alpha channel.  
    blurred.a = // TODO: math to calculate blurred value
  
    return blurred;  
}  
```

## <a name="requirements"></a><span data-ttu-id="e030e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e030e-118">Requirements</span></span>



| <span data-ttu-id="e030e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e030e-119">Requirement</span></span> | <span data-ttu-id="e030e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e030e-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e030e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e030e-121">Header</span></span><br/> | <dl> <span data-ttu-id="e030e-122"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="e030e-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="e030e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e030e-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="e030e-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e030e-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="e030e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e030e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e030e-126">Collegamento Effect shader</span><span class="sxs-lookup"><span data-stu-id="e030e-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="e030e-127">Helper HLSL</span><span class="sxs-lookup"><span data-stu-id="e030e-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





