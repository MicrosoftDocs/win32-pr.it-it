---
title: instance
description: Usare questo attributo per creare un'istanza di un geometry shader.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77c19b26107228bb04007d1c2c69ac34b464c7c361966ac9858d9bcdb09b4c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986161"
---
# <a name="instance"></a>instance

Usare questo attributo per creare un'istanza di un geometry shader.


```
instance(X)   
```



## <a name="remarks"></a>Commenti

X è un indice intero che indica il numero di istanze da eseguire per ogni elemento disegnato, ad esempio per ogni triangolo. Quando si usa questo attributo, [usare \_ SV GSInstanceID](sv-gsinstanceid.md) per identificare l'istanza di un geometry shader in esecuzione.

Questo attributo è supportato nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        | x        |       |         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi del modello shader 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




