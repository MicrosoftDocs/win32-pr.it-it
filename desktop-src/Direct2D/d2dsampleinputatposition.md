---
title: Funzione D2DSampleInputAtPosition (D2d1effecthelpers. h)
description: Campiona l'input N in una posizione assoluta della scena, anziché una posizione relativa all'input. Disponibile solo per gli input complessi.
ms.assetid: E839287F-91D1-4591-8DE7-1DFC3001A23D
keywords:
- Direct2D funzione D2DSampleInputAtPosition
topic_type:
- apiref
api_name:
- D2DSampleInputAtPosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12bba2b83f3956cf4b654c00b0650a6a0ce9a54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332784"
---
# <a name="d2dsampleinputatposition-function"></a><span data-ttu-id="a2a42-105">D2DSampleInputAtPosition (funzione)</span><span class="sxs-lookup"><span data-stu-id="a2a42-105">D2DSampleInputAtPosition function</span></span>

<span data-ttu-id="a2a42-106">Campiona l'input N in una posizione assoluta della scena, anziché una posizione relativa all'input.</span><span class="sxs-lookup"><span data-stu-id="a2a42-106">Samples input N at an absolute scene position, rather than an input-relative position.</span></span> <span data-ttu-id="a2a42-107">Disponibile solo per gli input complessi.</span><span class="sxs-lookup"><span data-stu-id="a2a42-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2a42-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2a42-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInputAtPosition(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a><span data-ttu-id="a2a42-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2a42-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2a42-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2a42-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a42-111">Numero di input.</span><span class="sxs-lookup"><span data-stu-id="a2a42-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="a2a42-112">*UV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a2a42-112">*uv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a42-113">Posizione UV.</span><span class="sxs-lookup"><span data-stu-id="a2a42-113">The uv position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2a42-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2a42-114">Return value</span></span>

<span data-ttu-id="a2a42-115">La funzione restituisce un **float4** nel formato TEXCOORDN.</span><span class="sxs-lookup"><span data-stu-id="a2a42-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2a42-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2a42-116">Remarks</span></span>

<span data-ttu-id="a2a42-117">Nell'esempio seguente viene illustrata la funzione utilizzata in un ritorno a capo circolare.</span><span class="sxs-lookup"><span data-stu-id="a2a42-117">The following example shows the function used in a circular wrap.</span></span>

``` syntax
  
D2D_PS_ENTRY(CircularWrapPS)  
{  
    // TODO: perform math to calculate a circular wrap
  
    // Find the input scene position.  
    float2 inputScenePosition = float2( TODO: add math parameters );  
  
    return D2DSampleInputAtPosition(0, inputScenePosition);  
}
```

## <a name="requirements"></a><span data-ttu-id="a2a42-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2a42-118">Requirements</span></span>



| <span data-ttu-id="a2a42-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2a42-119">Requirement</span></span> | <span data-ttu-id="a2a42-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a2a42-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2a42-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2a42-121">Header</span></span><br/> | <dl> <span data-ttu-id="a2a42-122"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="a2a42-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="a2a42-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a2a42-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="a2a42-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2a42-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="a2a42-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2a42-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2a42-126">Collegamento Effect shader</span><span class="sxs-lookup"><span data-stu-id="a2a42-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="a2a42-127">Helper HLSL</span><span class="sxs-lookup"><span data-stu-id="a2a42-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





