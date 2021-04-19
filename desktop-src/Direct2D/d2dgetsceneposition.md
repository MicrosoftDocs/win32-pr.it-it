---
title: Funzione D2DGetScenePosition (D2d1effecthelpers. h)
description: Restituisce il valore della posizione della scena di input \_ . Disponibile solo quando D2D \_ richiede \_ che \_ la posizione della scena sia dichiarata nel file di origine.
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- Direct2D funzione D2DGetScenePosition
topic_type:
- apiref
api_name:
- D2DGetScenePosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace0ee4d60f8c140825e41ba47de941bca09e67c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332359"
---
# <a name="d2dgetsceneposition-function"></a><span data-ttu-id="72e8d-105">D2DGetScenePosition (funzione)</span><span class="sxs-lookup"><span data-stu-id="72e8d-105">D2DGetScenePosition function</span></span>

<span data-ttu-id="72e8d-106">Restituisce il valore della posizione della scena di input \_ .</span><span class="sxs-lookup"><span data-stu-id="72e8d-106">Returns the value of the input SCENE\_POSITION.</span></span> <span data-ttu-id="72e8d-107">Disponibile solo quando D2D \_ richiede \_ che \_ la posizione della scena sia dichiarata nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="72e8d-107">Only available when D2D\_REQUIRES\_SCENE\_POSITION is declared in the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="72e8d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72e8d-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a><span data-ttu-id="72e8d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="72e8d-109">Parameters</span></span>

<span data-ttu-id="72e8d-110">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="72e8d-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72e8d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72e8d-111">Return value</span></span>

<span data-ttu-id="72e8d-112">La funzione restituisce un **float4** nella posizione della scena del formato \_ .</span><span class="sxs-lookup"><span data-stu-id="72e8d-112">The function returns a **float4** in the format SCENE\_POSITION.</span></span>

## <a name="remarks"></a><span data-ttu-id="72e8d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="72e8d-113">Remarks</span></span>

<span data-ttu-id="72e8d-114">Nell'esempio seguente viene illustrato l'uso della funzione nella generazione di un modello di dissolvenza.</span><span class="sxs-lookup"><span data-stu-id="72e8d-114">The following example shows the use of the function in generating a dissolve pattern.</span></span>

``` syntax
D2D_PS_ENTRY(BlendDissolve)  
{  
    min16float4 dest   = D2DGetInput(0);  
    min16float4 source = D2DGetInput(1);  
  
    min16float4 color = dest;  
  
    if ((source.a > 0.0) && (source.a >= Rand((min16float2)D2DGetScenePosition().xy)))  
    {  
        // TODO: perform  dissovlve math
    }  
  
    return color;  
}  
```

## <a name="requirements"></a><span data-ttu-id="72e8d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72e8d-115">Requirements</span></span>



| <span data-ttu-id="72e8d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="72e8d-116">Requirement</span></span> | <span data-ttu-id="72e8d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="72e8d-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72e8d-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72e8d-118">Header</span></span><br/> | <dl> <span data-ttu-id="72e8d-119"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="72e8d-119"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="72e8d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="72e8d-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="72e8d-121"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72e8d-121"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="72e8d-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72e8d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e8d-123">Collegamento Effect shader</span><span class="sxs-lookup"><span data-stu-id="72e8d-123">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="72e8d-124">Helper HLSL</span><span class="sxs-lookup"><span data-stu-id="72e8d-124">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





