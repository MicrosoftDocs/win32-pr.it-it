---
title: earlydepthstencil
description: Forza i test di stencil Depth prima dell'esecuzione di uno shader.
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7dd8507986970f2066538cc00b53af08807910e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993184"
---
# <a name="earlydepthstencil"></a>earlydepthstencil

Forza i test di stencil Depth prima dell'esecuzione di uno shader.


```
earlydepthstencil   
```



## <a name="remarks"></a>Commenti

Il test di stencil depth viene in genere eseguito durante l'elaborazione dei pixel da un pixel shader. La forzatura del test di stencil di profondità anticipato fa sì che il test venga eseguito prima dell'esecuzione dello shader. lo scopo è quello di migliorare le prestazioni per pixel mediante l'abbattimento/riduzione/evitare l'elaborazione di pixel superflui.

Un'applicazione può forzare il testing dello stencil di profondità anticipato fornendo l'attributo o l'hardware può eseguire il test di stencil Depth prima che non venga scritto alcun valore di profondità e non vengono eseguite operazioni di accesso non ordinate in uno shader come ottimizzazione.

Questo attributo è supportato nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi del modello di shader 5](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Modello Shader 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




