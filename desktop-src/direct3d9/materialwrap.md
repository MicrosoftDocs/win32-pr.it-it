---
description: Definisce un set di due valori booleani usati nel modello MeshFaceWraps per definire la topologia di trama di un singolo viso. Usare invece di Boolean2d quando le coordinate della trama (u, v) si estendono nell'intervallo da 0 a 2 anziché da 0 a 1.
ms.assetid: 0d1755fc-66cb-4372-b9d0-fb320c55d6a7
title: MaterialWrap
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 656c5f7d4eaad52a75cffca0189a1e6fa36e3e89714d8ee0225a3aeec21c8e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798922"
---
# <a name="materialwrap"></a>MaterialWrap

Definisce un set di due valori booleani usati nel [**modello MeshFaceWraps**](meshfacewraps.md) per definire la topologia di trama di un singolo viso. Usare invece di [**Boolean2d**](boolean2d.md) quando le coordinate della trama (u, v) si estendono nell'intervallo da 0 a 2 anziché da 0 a 1.

``` syntax
template MaterialWrap
{
    < 4885ae60-78e8-11cf-8f52-0040333594a3 >
    Boolean u;
    Boolean v;
} 
```

Dove:

-   u : valore booleano. Vedere [**Boolean**](boolean.md).
-   v : valore booleano. Vedere [**Boolean**](boolean.md).

> [!Note]  
> Il [**modello MeshFaceWraps**](meshfacewraps.md) non viene più usato.

 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



