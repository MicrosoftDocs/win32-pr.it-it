---
title: instance
description: Usare questo attributo per l'istanza di un geometry shader.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4749e11db00b38e5e223e11315de86656b2f6488
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046105"
---
# <a name="instance"></a>instance

Usare questo attributo per l'istanza di un geometry shader.


```
instance(X)   
```



## <a name="remarks"></a>Commenti

X è un indice Integer che indica il numero di istanze da eseguire per ogni elemento disegnato, ad esempio per ogni triangolo. Quando si usa questo attributo, usare [SV \_ GSInstanceID](sv-gsinstanceid.md) per identificare l'istanza di Geometry shader in esecuzione.

Questo attributo è supportato nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        | x        |       |         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi del modello di shader 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




