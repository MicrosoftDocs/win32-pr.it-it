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
# <a name="effectparamfloats"></a>EffectParamFloats

Definisce i numeri a virgola mobile effetto. Questo modello sostituisce il modello [**EffectFloats**](effectfloats.md) .

``` syntax
template EffectParamFloats
{
    < 3014B9A0-62F5-478c-9B86-E4AC9F4E418B >
    STRING ParamName;
    DWORD nFloats;
    array float Floats[nFloats];
} 
```

Dove:

-   ParamName: nome della matrice di float.
-   nFloats: numero di valori a virgola mobile nella matrice.
-   Float \[ nFloats \] -matrice di valori a virgola mobile.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



