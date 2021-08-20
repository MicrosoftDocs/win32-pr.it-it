---
description: Differenze tra I/O locale e I/O di rete Windows.
ms.assetid: 8a8f20bd-fa41-4f1a-b9bf-5f09683cd46c
title: Differenze nell'I/O locale e di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 445f41115d95d138e9a3dae8cf25df3c63555ff0435e857ba69f80d717d626f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998021"
---
# <a name="differences-in-local-and-network-io"></a>Differenze nell'I/O locale e di rete

Esistono alcune differenze significative tra l'I/O locale e l'I/O di rete Windows:

-   Il supporto dell'I/O di rete dipende dal redirector e dal protocollo di rete.
-   Le prestazioni di I/O di rete dipendono dal numero di operazioni di I/O di rete in corso e dalla velocità della connessione di rete. L'applicazione deve essere in grado di gestire le operazioni di I/O di rete con server molto più veloci o più lenti rispetto al computer locale, nonché modifiche temporanee nella capacità di rete. In questi casi, l'applicazione potrebbe dover concedere più tempo per il completamento dell'operazione.
-   Le funzioni usate per eseguire operazioni di I/O di file locali possono comportarsi in modo diverso in rete. Ad esempio, può verificarsi il timeout di un'operazione di I/O di rete che richiede molto tempo. In alcune situazioni, gli handle di file possono essere lasciati aperti per un periodo illimitato. Un altro esempio è che le funzioni possono restituire codici di errore specifici dell'I/O di rete per l'applicazione.

 

 



