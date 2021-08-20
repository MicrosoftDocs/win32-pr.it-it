---
title: topologia di output
description: Definisce il tipo primitivo di output per il tessellatore.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d718b11c23fcf77f452e224a51439f7d6f422d3c81d5238167cbf87c7c3014a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725415"
---
# <a name="outputtopology"></a>topologia di output

Definisce il tipo primitivo di output per il tessellatore.


```
outputtopology(X)      
```



## <a name="remarks"></a>Commenti

X deve essere un [**punto, una**](dx-graphics-hlsl-geometry-shader.md) **linea,** **un triangolo \_ cw** o un **\_ ccw** triangolo e deve essere racchiuso tra virgolette. Ecco le opzioni valide per questo attributo:


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



Questo attributo è supportato nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi del modello shader 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




