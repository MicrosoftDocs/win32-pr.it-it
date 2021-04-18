---
title: Struttura degli attributi di intersezione
description: Struttura dichiarata in HLSL per rappresentare gli attributi hit per l'intersezione del triangolo a funzione fissa o il rettangolo di delimitazione allineato all'asse per l'intersezione primitiva procedurale.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f1dd8fee7371f81dd538b6ea6622f22e3bfd3d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "106320435"
---
# <a name="intersection-attributes-structure"></a>Struttura degli attributi di intersezione 

Struttura dichiarata in HLSL per rappresentare gli attributi hit per l'intersezione del triangolo a funzione fissa o il rettangolo di delimitazione allineato all'asse per l'intersezione primitiva procedurale.

## <a name="fixed-function-triangle-intersection"></a>Intersezione del triangolo a funzione fissa

La struttura seguente viene dichiarata in HLSL per rappresentare gli attributi di hit per l'intersezione del triangolo a funzione fissa:


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

[Tutti](any-hit-shader.md) gli hit shader richiamati e [più vicini](closest-hit-shader.md) richiamati usando l'intersezione del triangolo a funzione fissa devono usare questa struttura per gli attributi hit. Dato gli attributi a0, a1 e a2 per i 3 vertici di un triangolo, barycentrics. x è il peso per a1 e barycentrics. y è il peso per a2.  Ad esempio, l'app può interpolare eseguendo: a = a0 + barycentrics. x * (a1-a0) + barycentrics. y * (a2-a0).

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a>Rettangolo di delimitazione allineato all'asse per l'intersezione primitiva procedurale

Quando vengono usati i rettangoli di delimitazione allineati all'asse per l'intersezione con le primitive procedurali, viene attivata un'intersezione shader.  Lo shader fornisce una struttura dell'attributo di intersezione definita dall'utente alla chiamata [**ReportHit**](reporthit-function.md) .  Tutti gli hit e gli hit shader associati nello stesso gruppo di hit con questa intersezione shader devono usare la stessa struttura per gli attributi hit, anche se non si fa riferimento agli attributi.  La dimensione massima della struttura dell'attributo è 32 byte, definita come **D3D12 \_ RAYTRACING \_ Max \_ Attribute \_ size \_ in \_ bytes**.


