---
description: Dopo che un driver di dispositivo ha convertito un intero file journal in comandi di dispositivo non elaborati, il file dei comandi convertiti viene passato nuovamente nello spooler.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Monitoraggi porte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8334da48fb147a41924be2cf090f55d7955cb1d7913c43b302a312fd4447602f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470931"
---
# <a name="port-monitors"></a>Monitoraggi porte

Dopo che un driver di dispositivo ha convertito un intero file journal in comandi di dispositivo non elaborati, il file dei comandi convertiti viene passato nuovamente nello spooler. Lo spooler invia questi comandi di basso livello a un monitoraggio. Un monitoraggio porte è un .dll che passa i comandi del dispositivo non elaborato in rete, tramite una porta parallela o tramite una porta seriale al dispositivo della stampante. È possibile installare monitoraggi delle porte personalizzati per supportare il passaggio dei dati del dispositivo tramite altre porte di comunicazione.

Usare le funzioni seguenti per usare i monitoraggi delle porte.



| Funzione                               | Descrizione                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [**AddMonitor**](addmonitor.md)       | Installa un monitoraggio porta locale e collega i file di configurazione, dati e monitoraggio. |
| [**DeleteMonitor**](deletemonitor.md) | Rimuove un monitoraggio delle porte aggiunto dalla [**funzione AddMonitor.**](addmonitor.md)      |
| [**EnumMonitors**](enummonitors.md)   | Enumera i monitoraggi delle porte installati in un server specificato.                       |



 

 

 



