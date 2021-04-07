---
description: Definisce i numeri a virgola mobile effetto. Questo modello sostituisce il modello EffectFloats.
ms.assetid: 7b41d0dc-209f-4ade-a7ed-aa54f421e520
title: EffectParamFloats
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0954ce7679691920c2e104277d12a48f7a34ddf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048941"
---
# <a name="effectparamfloats"></a><span data-ttu-id="9091d-104">EffectParamFloats</span><span class="sxs-lookup"><span data-stu-id="9091d-104">EffectParamFloats</span></span>

<span data-ttu-id="9091d-105">Definisce i numeri a virgola mobile effetto.</span><span class="sxs-lookup"><span data-stu-id="9091d-105">Defines effect floating-point numbers.</span></span> <span data-ttu-id="9091d-106">Questo modello sostituisce il modello [**EffectFloats**](effectfloats.md) .</span><span class="sxs-lookup"><span data-stu-id="9091d-106">This template replaces the [**EffectFloats**](effectfloats.md) template.</span></span>

``` syntax
template EffectParamFloats
{
    < 3014B9A0-62F5-478c-9B86-E4AC9F4E418B >
    STRING ParamName;
    DWORD nFloats;
    array float Floats[nFloats];
} 
```

<span data-ttu-id="9091d-107">Dove:</span><span class="sxs-lookup"><span data-stu-id="9091d-107">Where:</span></span>

-   <span data-ttu-id="9091d-108">ParamName: nome della matrice di float.</span><span class="sxs-lookup"><span data-stu-id="9091d-108">ParamName - Name of the array of floats.</span></span>
-   <span data-ttu-id="9091d-109">nFloats: numero di valori a virgola mobile nella matrice.</span><span class="sxs-lookup"><span data-stu-id="9091d-109">nFloats - Number of floating-point values in the array.</span></span>
-   <span data-ttu-id="9091d-110">Float \[ nFloats \] -matrice di valori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="9091d-110">Floats\[nFloats\] - Array of floating-point values.</span></span>

## <a name="see-also"></a><span data-ttu-id="9091d-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9091d-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9091d-112">Modelli</span><span class="sxs-lookup"><span data-stu-id="9091d-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



