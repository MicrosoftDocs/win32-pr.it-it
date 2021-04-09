---
description: Definisce un effetto FLOAT legacy. Questo modello è stato sostituito dal modello EffectParamFloats.
ms.assetid: f3d66e23-5c55-478f-921d-3a5bdcfb8679
title: EffectFloats
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60c59605a6a45d94fa6a005adf0cbe348ada759
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965725"
---
# <a name="effectfloats"></a>EffectFloats

Definisce un effetto FLOAT legacy. Questo modello è stato sostituito dal modello [**EffectParamFloats**](effectparamfloats.md) .

``` syntax
template EffectFloats
{
    < F1CFE2B3-0DE3-4e28-AFA1-155A750A282D >
    DWORD nFloats;
    array float Floats[nFloats];
} 
```

Dove:

-   nFloats: numero di float.
-   Float \[ nFloats \] -matrice di valori float.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



