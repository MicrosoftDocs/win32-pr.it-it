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
# <a name="raytracingaccelerationstructure"></a><span data-ttu-id="8926a-103">RaytracingAccelerationStructure</span><span class="sxs-lookup"><span data-stu-id="8926a-103">RaytracingAccelerationStructure</span></span>

<span data-ttu-id="8926a-104">Tipo di risorsa che può essere dichiarata in HLSL e passata in [**TraceRay**](traceray-function.md) per indicare la risorsa di accelerazione di primo livello compilata con **BuildRaytracingAccelerationStructure**.</span><span class="sxs-lookup"><span data-stu-id="8926a-104">A resource type that can be declared in HLSL and passed into [**TraceRay**](traceray-function.md) to indicate the top-level acceleration resource built using **BuildRaytracingAccelerationStructure**.</span></span> <span data-ttu-id="8926a-105">Viene associato come SRV buffer non elaborato in una tabella descrittore o in un descrittore radice SRV.</span><span class="sxs-lookup"><span data-stu-id="8926a-105">It is bound as a raw buffer SRV in a descriptor table or root descriptor SRV.</span></span>  <span data-ttu-id="8926a-106">La dichiarazione in HLSL è la seguente:</span><span class="sxs-lookup"><span data-stu-id="8926a-106">The declaration in HLSL is as follows:</span></span>


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

<span data-ttu-id="8926a-107">In questo esempio viene illustrata una matrice di dimensioni non vincolate di strutture di accelerazione, che implica la provenienza da un heap dei descrittori poiché i descrittori radice non possono essere indicizzati.</span><span class="sxs-lookup"><span data-stu-id="8926a-107">This example shows an unbounded size array of acceleration structures, which implies coming from a descriptor heap since root descriptors can’t be indexed.</span></span>

<span data-ttu-id="8926a-108">**RaytracingAccelerationStructure** è una risorsa opaca senza metodi disponibili per gli shader.</span><span class="sxs-lookup"><span data-stu-id="8926a-108">**RaytracingAccelerationStructure** is an opaque resource with no methods available to shaders.</span></span>


 

 




