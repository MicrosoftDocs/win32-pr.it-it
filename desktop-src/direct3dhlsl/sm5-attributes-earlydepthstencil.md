---
title: earlydepthstencil
description: Forza il test di depth-stencil prima dell'esecuzione di uno shader.
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ed108d4f8e9d8d719d36fc859d5cc01a2317db4756bfbc6b0a548b669d9ca025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986171"
---
# <a name="earlydepthstencil"></a>earlydepthstencil

Forza il test di depth-stencil prima dell'esecuzione di uno shader.


```
earlydepthstencil   
```



## <a name="remarks"></a>Commenti

Il test di depth-stencil viene in genere eseguito durante l'elaborazione dei pixel da un pixel shader. Forzando i primi test di depth-stencil, il test viene eseguito prima dell'esecuzione dello shader; lo scopo è migliorare le prestazioni per pixel mediante l'culling/riduzione/evitare l'elaborazione dei pixel non necessaria.

Un'applicazione può forzare il test iniziale di depth-stencil fornendo l'attributo o l'hardware può eseguire test di profondità-stencil iniziali a condizione che non siano scritti valori di profondità e non venga eseguita alcuna operazione di accesso non ordinato in uno shader come ottimizzazione.

Questo attributo è supportato nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi del modello shader 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modello shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




