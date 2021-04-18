---
description: Definisce un set di due valori booleani utilizzati nel modello MeshFaceWraps per definire la topologia di trama di una singola faccia. Usare anziché Boolean2d quando le coordinate di trama (u, v) si estendono nell'intervallo da 0 a 2 anziché da 0 a 1.
ms.assetid: 0d1755fc-66cb-4372-b9d0-fb320c55d6a7
title: MaterialWrap
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6797719919a4f52421751a5cad008aa8a581089a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303845"
---
# <a name="materialwrap"></a>MaterialWrap

Definisce un set di due valori booleani utilizzati nel modello [**MeshFaceWraps**](meshfacewraps.md) per definire la topologia di trama di una singola faccia. Usare anziché [**Boolean2d**](boolean2d.md) quando le coordinate di trama (u, v) si estendono nell'intervallo da 0 a 2 anziché da 0 a 1.

``` syntax
template MaterialWrap
{
    < 4885ae60-78e8-11cf-8f52-0040333594a3 >
    Boolean u;
    Boolean v;
} 
```

Dove:

-   valore u-Boolean. Vedere [**valore booleano**](boolean.md).
-   v: valore booleano. Vedere [**valore booleano**](boolean.md).

> [!Note]  
> Il modello [**MeshFaceWraps**](meshfacewraps.md) non viene più usato.

 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



