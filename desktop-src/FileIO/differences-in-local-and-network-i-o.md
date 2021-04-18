---
description: Differenze tra l'i/o locale e l'I/O di rete in Windows.
ms.assetid: 8a8f20bd-fa41-4f1a-b9bf-5f09683cd46c
title: Differenze nell'I/O locale e di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30c4faf6b7358a1c7c134dccdeb12298309c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313892"
---
# <a name="differences-in-local-and-network-io"></a>Differenze nell'I/O locale e di rete

Esistono alcune differenze rilevanti tra I/o locale e I/O di rete in Windows:

-   Il supporto di I/O di rete dipende dal redirector e dal protocollo di rete.
-   Le prestazioni di I/O di rete variano a seconda del numero di operazioni di I/O di rete eseguite e della velocità della connessione di rete. L'applicazione deve essere in grado di gestire le operazioni di I/O di rete con i server che potrebbero essere molto più veloci o più lenti del computer locale, oltre a modifiche temporanee nella capacità di rete. In questi casi, l'applicazione potrebbe dover attendere più tempo per il completamento dell'operazione.
-   Le funzioni utilizzate per eseguire operazioni di I/O su file locali possono comportarsi in modo diverso in rete. È ad esempio possibile che si verifichi il timeout di un'operazione di I/O di rete che richiede molto tempo per il completamento. In alcune situazioni, gli handle di file possono essere lasciati aperti a tempo indefinito a causa di questo. Un altro esempio è che le funzioni possono restituire codici di errore per l'applicazione per l'elaborazione specifiche per l'I/O di rete.

 

 



