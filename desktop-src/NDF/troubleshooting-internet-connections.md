---
title: Risoluzione dei problemi relativi alle connessioni Internet
description: In questo scenario, un utente sta tentando di passare www.msn.com usando il protocollo https, ma non è in grado di connettersi. È possibile usare Netsh e Network Monitor per raccogliere e visualizzare le tracce per determinare il motivo per cui la connessione non è riuscita.
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fadeefe0413a5a6be5d3ec7f5676ef346e21bc1f4b9e4c3cca026b54d761784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133401"
---
# <a name="troubleshooting-internet-connections"></a>Risoluzione dei problemi relativi alle connessioni Internet

In questo scenario, un utente sta tentando di passare www.msn.com usando il protocollo https, ma non è in grado di connettersi. È possibile usare Netsh e Network Monitor per raccogliere e visualizzare le tracce per determinare il motivo per cui la connessione non è riuscita.

In primo luogo, è possibile usare netsh per avviare una traccia. Digitando **netsh trace start scenario = InternetClient tracefile=msn.etl** viene avviata la traccia per tutti i provider abilitati nello scenario InternetClient, salvando i risultati in un file denominato msn.etl. Dopo aver utilizzato un Web browser per tentare di raggiungere www.msn.com, la digitazione di **netsh trace stop** termina e mette in correlazione il file di traccia.

È quindi possibile aprire il file msn.etl in Network Monitor. Gli eventi vengono raggruppati in base all'ID attività nel riquadro sinistro. Usando la **descrizione del filtro.contains("msn")** verranno visualizzati solo gli eventi che includono la stringa "msn" nella descrizione del protocollo.

![risoluzione dei problemi relativi alle connessioni Internet tramite Network Monitor (1)](images/internetclient1.png)

Successivamente, è possibile esaminare gli eventi nel riepilogo dei fotogrammi per identificare un evento che sembra pertinente. Dopo aver selezionato l'evento, fare clic con il pulsante destro del mouse e scegliere Trova conversazioni, quindi fare clic su UTEvent per selezionare la conversazione a livello di UTEvent.

![risoluzione dei problemi relativi alle connessioni Internet tramite network monitor (2)](images/internetclient2.png)

L'attività normalizzata associata nel riquadro sinistro viene quindi evidenziata, in questo caso UTEvent ActivityID 397.

![risoluzione dei problemi relativi alle connessioni Internet tramite Network Monitor (3)](images/internetclient3.png)

Se si Network Monitor visualizzare e filtrare le informazioni di traccia, il numero di eventi da esaminare è stato ridotto da 1989 a 96.

 

 




