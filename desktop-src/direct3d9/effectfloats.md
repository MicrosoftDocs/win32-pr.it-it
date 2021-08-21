---
description: Definisce un effetto legacy FLOAT. Questo modello è stato sostituito dal modello EffectParamFloats.
ms.assetid: f3d66e23-5c55-478f-921d-3a5bdcfb8679
title: EffettiFloat
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7a847cde48a126e86db47d1df0f9b4e635292862baa5d60b7fa9326703aa21f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951891"
---
# <a name="effectfloats"></a>EffettiFloat

Definisce un effetto legacy FLOAT. Questo modello è stato sostituito [**dal modello EffectParamFloats.**](effectparamfloats.md)

``` syntax
template EffectFloats
{
    < F1CFE2B3-0DE3-4e28-AFA1-155A750A282D >
    DWORD nFloats;
    array float Floats[nFloats];
} 
```

Dove:

-   nFloats: numero di valori float.
-   Floats \[ nFloats: \] matrice di valori float.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



