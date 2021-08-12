---
title: Struttura degli attributi di intersezione
description: Struttura dichiarata in HLSL per rappresentare gli attributi di hit per l'intersezione di triangoli a funzione fissa o il riquadro delimitatore allineato all'asse per l'intersezione primitiva procedurale.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: fea10edb8402f07431d488ff9d28d1de539259e51bc1893d20e76e8f4cc3cdab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528119"
---
# <a name="intersection-attributes-structure"></a>Struttura degli attributi di intersezione 

Struttura dichiarata in HLSL per rappresentare gli attributi di hit per l'intersezione di triangoli a funzione fissa o il riquadro delimitatore allineato all'asse per l'intersezione primitiva procedurale.

## <a name="fixed-function-triangle-intersection"></a>Intersezione di triangoli a funzione fissa

La struttura seguente viene dichiarata in HLSL per rappresentare gli attributi di hit per l'intersezione del triangolo a funzione fissa:


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

[Tutti gli hit](any-hit-shader.md) shader [e gli hit](closest-hit-shader.md) shader più vicini richiamati usando l'intersezione di triangoli a funzione fissa devono usare questa struttura per gli attributi di hit. Dato gli attributi a0, a1 e a2 per i 3 vertici di un triangolo, barycentrics.x è il peso per a1 e barycentrics.y è il peso per a2.  Ad esempio, l'app può eseguire l'interpolazione eseguendo: a = a0 + barycentrics.x * (a1-a0) + barycentrics.y* (a2 - a0).

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a>Rettangolo di selezione allineato all'asse per l'intersezione delle primitive procedurali

Quando vengono usati relimitati allineati all'asse per l'intersezione con primitive procedurali, viene attivato uno shader di intersezione.  Lo shader fornisce una struttura dell'attributo di intersezione definita dall'utente alla [**chiamata a ReportHit.**](reporthit-function.md)  Gli eventuali hit shader e hit shader più vicini associati nello stesso gruppo di hit con questo intersection shader devono usare la stessa struttura per gli attributi di hit, anche se non viene fatto riferimento agli attributi.  La dimensione massima della struttura dell'attributo è di 32 byte, definita come **D3D12 \_ RAYTRACING \_ MAX ATTRIBUTE SIZE IN \_ \_ \_ \_ BYTES**.


