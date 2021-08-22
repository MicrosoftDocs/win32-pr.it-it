---
description: I provider di pacchetti di rete forniscono interfacce COM chiamate dalle applicazioni NPP e Network Monitor.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: Interfacce NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fc38bd5db91354c81f88d9f0fe0a6ad23ce3ccb3ecd4a08c4b6335e25ddd33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676981"
---
# <a name="npp-interfaces"></a>Interfacce NPP

I provider di pacchetti di rete forniscono interfacce COM chiamate dalle applicazioni NPP e Network Monitor. Quando si chiama [CreateNPPInterface,](createnppinterface.md)tenere presente che ogni NPP è rappresentato come un singolo oggetto COM in-process. Le applicazioni possono creare un'istanza di un numero qualsiasi di oggetti NPP. Tuttavia, ogni oggetto di cui è stata creata un'istanza deve usare una sola delle cinque interfacce NPP.

Si noti anche che diverse interfacce NPP forniscono dati di rete in varie forme. Ad esempio, Network Monitor usa **l'interfaccia IDelaydC** per acquisire il traffico di rete e salvarlo in un file di acquisizione. mentre i monitor usano **l'interfaccia IRTC** per acquisire il traffico di rete in tempo reale. La tabella seguente descrive Network Monitor NPP.



| Interfaccia                | Descrizione                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IDelaydC](idelaydc.md) | Acquisisce il traffico di rete archiviato in un file di acquisizione. Questa interfaccia viene usata dalle applicazioni Network Monitor e NPP.                                          |
| [IESP](iesp.md)         | Acquisisce il traffico di rete archiviato in un file di acquisizione e fornisce statistiche avanzate in un formato di file ESP speciale. Questa interfaccia viene usata dalle applicazioni NPP |
| [IRTC](irtc.md)         | Acquisisce il traffico di rete in tempo reale e attiva gli eventi quando si verificano. Questa interfaccia viene usata dai [*monitoraggi e*](m.md) dalle applicazioni NPP.     |
| [IStats](istats.md)     | Recupera le statistiche come dati non elaborati anziché come frame. Questa interfaccia viene usata dalle applicazioni NPP, ad esempio [*Perfmon.*](p.md)                     |



 

 

 



