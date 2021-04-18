---
description: Quando un driver di dispositivo ha convertito un intero file journal in comandi di dispositivo non elaborato, il file dei comandi convertiti viene passato nuovamente allo spooler.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Monitoraggi porta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4b00e4171b3fd6e366a66deae8f5e70578ca92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314531"
---
# <a name="port-monitors"></a>Monitoraggi porta

Quando un driver di dispositivo ha convertito un intero file journal in comandi di dispositivo non elaborato, il file dei comandi convertiti viene passato nuovamente allo spooler. Lo spooler invia questi comandi di basso livello a un monitoraggio. Un monitoraggio porta è un file con estensione dll che passa i comandi dei dispositivi non elaborati sulla rete, tramite una porta parallela o tramite una porta seriale al dispositivo di stampa. È possibile installare monitoraggi porta personalizzati per supportare il passaggio dei dati del dispositivo attraverso altre porte di comunicazione.

Usare le funzioni seguenti per lavorare con i monitoraggi delle porte.



| Funzione                               | Descrizione                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [**AddMonitor**](addmonitor.md)       | Installa un monitoraggio porta locale e collega i file di configurazione, dati e monitoraggio. |
| [**DeleteMonitor**](deletemonitor.md) | Rimuove un monitor di porta aggiunto dalla funzione [**AddMonitor**](addmonitor.md) .      |
| [**EnumMonitors**](enummonitors.md)   | Enumera i monitoraggi delle porte installati in un server specificato.                       |



 

 

 



