---
title: RaytracingAccelerationStructure
description: Tipo di risorsa che può essere dichiarata in HLSL e passata in TraceRay per indicare la risorsa di accelerazione di primo livello compilata con BuildRaytracingAccelerationStructure.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: beb6f5e397126223e9c0e6959e16a6cca3145517
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "106320447"
---
# <a name="raytracingaccelerationstructure"></a>RaytracingAccelerationStructure

Tipo di risorsa che può essere dichiarata in HLSL e passata in [**TraceRay**](traceray-function.md) per indicare la risorsa di accelerazione di primo livello compilata con **BuildRaytracingAccelerationStructure**. Viene associato come SRV buffer non elaborato in una tabella descrittore o in un descrittore radice SRV.  La dichiarazione in HLSL è la seguente:


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

In questo esempio viene illustrata una matrice di dimensioni non vincolate di strutture di accelerazione, che implica la provenienza da un heap dei descrittori poiché i descrittori radice non possono essere indicizzati.

**RaytracingAccelerationStructure** è una risorsa opaca senza metodi disponibili per gli shader.


 

 




