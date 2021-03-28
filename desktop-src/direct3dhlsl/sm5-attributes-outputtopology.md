---
title: outputtopology
description: Definisce il tipo primitivo di output per mosaico.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 917a927ff80d4abe1b6509fd41281992a998c945
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103956075"
---
# <a name="outputtopology"></a>outputtopology

Definisce il tipo primitivo di output per mosaico.


```
outputtopology(X)      
```



## <a name="remarks"></a>Commenti

X deve essere un [**punto**](dx-graphics-hlsl-geometry-shader.md), **una linea**, un **triangolo in \_ senso orario** o un **triangolo \_ CCW** e deve essere racchiuso tra virgolette. Di seguito sono riportate le opzioni valide per l'attributo:


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



Questo attributo è supportato nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi del modello di shader 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




