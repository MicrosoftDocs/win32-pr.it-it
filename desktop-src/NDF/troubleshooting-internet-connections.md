---
title: Risoluzione dei problemi relativi alle connessioni Internet
description: In questo scenario un utente sta tentando di passare a www.msn.com usando il protocollo HTTPS, ma non è in grado di connettersi. È possibile utilizzare Netsh e Network Monitor per raccogliere e visualizzare le tracce per determinare il motivo per cui la connessione non è riuscita.
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753636c1186243a96e3cef5a4ab73244556daec4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855913"
---
# <a name="troubleshooting-internet-connections"></a>Risoluzione dei problemi relativi alle connessioni Internet

In questo scenario un utente sta tentando di passare a www.msn.com usando il protocollo HTTPS, ma non è in grado di connettersi. È possibile utilizzare Netsh e Network Monitor per raccogliere e visualizzare le tracce per determinare il motivo per cui la connessione non è riuscita.

In primo luogo, è possibile utilizzare Netsh per avviare una traccia. Digitando **netsh trace start scenario = InternetClient TraceFile = MSN. etl** avvia la traccia per tutti i provider abilitati nello scenario InternetClient, salvando i risultati in un file denominato MSN. etl. Dopo aver usato un Web browser per tentare di raggiungere www.msn.com, la digitazione di **netsh trace stop** termina e mette in correlazione il file di traccia.

È quindi possibile aprire il file MSN. etl in Network Monitor. Gli eventi sono raggruppati in base all'ID attività nel riquadro sinistro. Utilizzando la descrizione del filtro **. Contains ("MSN")** mostrerà solo gli eventi che includono la stringa "MSN" nella descrizione del protocollo.

![risoluzione dei problemi relativi alle connessioni Internet tramite Network Monitor (1)](images/internetclient1.png)

Successivamente, è possibile esaminare gli eventi nel riepilogo dei frame per identificare un evento che sembra pertinente. Dopo aver selezionato l'evento, fare clic con il pulsante destro del mouse e scegliere Trova conversazioni, quindi fare clic su UTEvent per selezionare la conversazione a livello di UTEvent.

![risoluzione dei problemi relativi alle connessioni Internet tramite Network Monitor (2)](images/internetclient2.png)

Viene evidenziata l'attività normalizzata associata nel riquadro sinistro, in questo caso UTEvent ActivityID 397.

![risoluzione dei problemi relativi alle connessioni Internet tramite Network Monitor (3)](images/internetclient3.png)

Utilizzando Network Monitor per visualizzare e filtrare le informazioni di traccia, il numero di eventi da esaminare è stato ridotto da 1989 a 96.

 

 




