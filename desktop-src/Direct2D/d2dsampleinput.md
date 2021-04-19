---
title: Funzione D2DSampleInput (D2d1effecthelpers. h)
description: Input di esempio N alla posizione UV. Disponibile solo per gli input complessi.
ms.assetid: 8C1E3B23-D05B-4FCC-B32F-A5870A7C3FEF
keywords:
- Direct2D funzione D2DSampleInput
topic_type:
- apiref
api_name:
- D2DSampleInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5929e9c113e5fa9a7c8a72003357b280a810e49e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332786"
---
# <a name="d2dsampleinput-function"></a><span data-ttu-id="60084-105">D2DSampleInput (funzione)</span><span class="sxs-lookup"><span data-stu-id="60084-105">D2DSampleInput function</span></span>

<span data-ttu-id="60084-106">Input di esempio N alla posizione UV.</span><span class="sxs-lookup"><span data-stu-id="60084-106">Samples input N at position uv.</span></span> <span data-ttu-id="60084-107">Disponibile solo per gli input complessi.</span><span class="sxs-lookup"><span data-stu-id="60084-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="60084-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60084-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInput(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a><span data-ttu-id="60084-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="60084-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60084-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60084-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60084-111">Numero di input.</span><span class="sxs-lookup"><span data-stu-id="60084-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="60084-112">*UV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60084-112">*uv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60084-113">Posizione UV.</span><span class="sxs-lookup"><span data-stu-id="60084-113">The uv position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60084-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60084-114">Return value</span></span>

<span data-ttu-id="60084-115">La funzione restituisce un **float4** nel formato TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="60084-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="60084-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="60084-116">Remarks</span></span>

<span data-ttu-id="60084-117">Nell'esempio seguente viene illustrata la funzione utilizzata per calcolare le normali della superficie.</span><span class="sxs-lookup"><span data-stu-id="60084-117">The following example shows the function being used to calculate surface normals.</span></span>

``` syntax
   
float3 CalculateSurfaceNormal(TAPARGS)  
{  
    float3 normal = float3(0, 0, 1.0);  
  
    // unrolled loop  
    normal.xy += tap1.zw * D2DSampleInput(0, tap1.xy).a;  
    normal.xy += tap2.zw * D2DSampleInput(0, tap2.xy).a;  
    normal.xy += tap3.zw * D2DSampleInput(0, tap3.xy).a;  
    normal.xy += tap4.zw * D2DSampleInput(0, tap4.xy).a;  
    normal.xy += tap5.zw * D2DSampleInput(0, tap5.xy).a;  
    normal.xy += tap6.zw * D2DSampleInput(0, tap6.xy).a;  
  
    normal = normalize(normal);  
      
    return normal;  
}  
```

## <a name="requirements"></a><span data-ttu-id="60084-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60084-118">Requirements</span></span>



| <span data-ttu-id="60084-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="60084-119">Requirement</span></span> | <span data-ttu-id="60084-120">Valore</span><span class="sxs-lookup"><span data-stu-id="60084-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60084-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60084-121">Header</span></span><br/> | <dl> <span data-ttu-id="60084-122"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="60084-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="60084-123">DLL</span><span class="sxs-lookup"><span data-stu-id="60084-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="60084-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60084-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="60084-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60084-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60084-126">Collegamento Effect shader</span><span class="sxs-lookup"><span data-stu-id="60084-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="60084-127">Helper HLSL</span><span class="sxs-lookup"><span data-stu-id="60084-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





