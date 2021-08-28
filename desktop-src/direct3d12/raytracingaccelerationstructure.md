---
title: RaytracingAccelerationStructure
description: Tipo di risorsa che può essere dichiarato in HLSL e passato a TraceRay per indicare la risorsa di accelerazione di primo livello compilata con BuildRaytracingAccelerationStructure.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 4728e167fe9fbc353c51accaa92d9b9d4086a0bfff3f098f43b93523cd63a792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123619"
---
# <a name="raytracingaccelerationstructure"></a>RaytracingAccelerationStructure

Tipo di risorsa che può essere dichiarato in HLSL e passato a [**TraceRay**](traceray-function.md) per indicare la risorsa di accelerazione di primo livello compilata con **BuildRaytracingAccelerationStructure.** Viene associato come SRV del buffer non elaborato in una tabella di descrittori o in una SRV del descrittore radice.  La dichiarazione in HLSL è la seguente:


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

Questo esempio illustra una matrice di dimensioni illimitate di strutture di accelerazione, che implica la derivazione da un heap descrittore perché i descrittori radice non possono essere indicizzati.

**RaytracingAccelerationStructure è** una risorsa opaca senza metodi disponibili per gli shader.


 

 




