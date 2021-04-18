---
description: È possibile modellare un provider di classi come provider push o pull, che specifica come un provider prevede di interagire con WMI.
ms.assetid: d1852784-8440-4b8a-9cdd-896e51cdee98
ms.tgt_platform: multiple
title: Determinazione dello stato di push o pull
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee037b4c81e43080ee119540b05568eb00cdc70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310372"
---
# <a name="determining-push-or-pull-status"></a>Determinazione dello stato di push o pull

È possibile modellare un provider di classi come provider push o pull, che specifica come un provider prevede di interagire con WMI. I provider pull ricevono una richiesta da WMI e soddisfano la richiesta generando i dati in modo dinamico o recuperando i dati da una cache locale. I provider pull devono inoltre implementare un numero elevato di interfacce.

Un provider di pull genera in modo dinamico le definizioni delle classi. In genere, i dati gestiti da un provider di pull cambiano di frequente, richiedendo al provider di generare la classe in modo dinamico o recuperare la classe da una cache locale ogni volta che un'applicazione invia una richiesta. Un provider di pull deve implementare i propri meccanismi di recupero dati, cache e notifica degli eventi. Poiché la maggior parte dei provider è provider di pull, la documentazione in questo file presuppone che si stia compilando un provider di pull se non diversamente specificato in modo esplicito.

WMI utilizza invece i dati nel repository WMI per gestire tutte le richieste di applicazioni per i provider di push. I provider di push utilizzano anche un minor numero di metodi di interfaccia e pertanto sono più facili da implementare. Un provider di push utilizza il repository WMI come area di archiviazione per ottenere informazioni sull'oggetto gestito e aggiorna tali informazioni solo durante l'inizializzazione. Il provider di classi WDM incluso nella sezione WMI di Microsoft Windows Software Development Kit (SDK), ad esempio, è modellato come provider di push.

Utilizzando il repository WMI come area di archiviazione, un provider di push ottiene i vantaggi seguenti rispetto a un provider di pull:

-   Non è necessario che il provider implementi una cache locale per archiviare i dati.
-   Non è necessario che il provider supporti il recupero dei dati; il provider può invece avvalersi di WMI per fornire supporto per il recupero.
-   Quando un'applicazione richiede i dati forniti dal provider, WMI soddisfa la richiesta.
-   Il provider può inoltre basarsi su WMI per supportare la notifica degli eventi.

Tuttavia, poiché un provider di push viene aggiornato solo durante l'inizializzazione, le eventuali modifiche apportate a una classe potrebbero non essere riflesse nel repository WMI per un certo periodo di tempo. Pertanto, il modello del provider di Push funziona meglio con le classi che cambiano poco o altrimenti sono completamente statiche.

 

 



