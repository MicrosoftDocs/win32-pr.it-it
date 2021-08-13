---
description: Dopo che un driver di dispositivo ha convertito un intero file journal in comandi di dispositivo non elaborati, il file dei comandi convertiti viene passato di nuovo al spooler.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Monitoraggi delle porte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8334da48fb147a41924be2cf090f55d7955cb1d7913c43b302a312fd4447602f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470931"
---
# <a name="port-monitors"></a>Monitoraggi delle porte

Dopo che un driver di dispositivo ha convertito un intero file journal in comandi di dispositivo non elaborati, il file dei comandi convertiti viene passato di nuovo al spooler. Lo spooler invia questi comandi di basso livello a un monitoraggio. Un monitor di porta è un .dll che passa i comandi del dispositivo non elaborato in rete, tramite una porta parallela o tramite una porta seriale al dispositivo stampante. È possibile installare monitor di porta personalizzati per supportare il passaggio dei dati del dispositivo attraverso altre porte di comunicazione.

Usare le funzioni seguenti per usare i monitor di porta.



| Funzione                               | Descrizione                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [**AddMonitor**](addmonitor.md)       | Installa un monitor di porta locale e collega i file di configurazione, di dati e di monitoraggio. |
| [**DeleteMonitor**](deletemonitor.md) | Rimuove un monitor di porta aggiunto dalla [**funzione AddMonitor.**](addmonitor.md)      |
| [**EnumMonitors**](enummonitors.md)   | Enumera i monitoraggi delle porte installati in un server specificato.                       |



 

 

 



