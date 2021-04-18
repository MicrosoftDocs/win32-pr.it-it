---
description: I provider di pacchetti di rete (centrali) forniscono interfacce COM chiamate da applicazioni NPP e Network Monitor.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: Interfacce NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3146d34798c57aea0bbd0f4bfec0037ed2ac879c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308161"
---
# <a name="npp-interfaces"></a>Interfacce NPP

I provider di pacchetti di rete (centrali) forniscono interfacce COM chiamate da applicazioni NPP e Network Monitor. Quando si chiama [CreateNPPInterface](createnppinterface.md), tenere presente che ogni npp è rappresentato come un singolo oggetto com in-process. Le applicazioni possono creare un'istanza di un numero qualsiasi di oggetti NPP. Tuttavia, ogni oggetto di cui è stata creata un'istanza deve utilizzarne uno, e solo uno, delle cinque interfacce NPP.

Si noti inoltre che diverse interfacce NPP forniscono dati di rete in vari formati. Ad esempio, Network Monitor usa l'interfaccia **IDelaydC** per acquisire il traffico di rete e salvarlo in un file di acquisizione. mentre i monitoraggi usano l'interfaccia **IRTC** per acquisire il traffico di rete in tempo reale. Nella tabella seguente vengono descritte Network Monitor le interfacce NPP.



| Interfaccia                | Descrizione                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IDelaydC](idelaydc.md) | Acquisisce il traffico di rete archiviato in un file di acquisizione. Questa interfaccia viene utilizzata dalle applicazioni Network Monitor e NPP.                                          |
| [IESP](iesp.md)         | Acquisisce il traffico di rete archiviato in un file di acquisizione e fornisce statistiche avanzate in un formato di file ESP speciale. Questa interfaccia viene utilizzata dalle applicazioni NPP |
| [IRTC](irtc.md)         | Acquisisce il traffico di rete in tempo reale e attiva gli eventi quando si verificano. Questa interfaccia viene utilizzata dai [*monitoraggi*](m.md) e dalle applicazioni NPP.     |
| [IStats](istats.md)     | Recupera le statistiche come dati non elaborati anziché come frame. Questa interfaccia viene utilizzata dalle applicazioni NPP come [*PerfMon*](p.md).                     |



 

 

 



