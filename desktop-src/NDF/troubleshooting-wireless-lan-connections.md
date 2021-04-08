---
title: Risoluzione dei problemi relativi alle connessioni LAN wireless
description: In questo scenario un utente sta tentando di connettersi a una LAN wireless, ma non è in grado di connettersi. È possibile utilizzare Netsh e Network Monitor per raccogliere e visualizzare le tracce per determinare il motivo per cui la connessione non è riuscita.
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55878afcee0091634415d4dbc465d1b143f46057
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045187"
---
# <a name="troubleshooting-wireless-lan-connections"></a>Risoluzione dei problemi relativi alle connessioni LAN wireless

In questo scenario un utente sta tentando di connettersi a una LAN wireless, ma non è in grado di connettersi. È possibile utilizzare Netsh e Network Monitor per raccogliere e visualizzare le tracce per determinare il motivo per cui la connessione non è riuscita.

In primo luogo, è possibile utilizzare Netsh per avviare una traccia. Digitando **netsh trace start scenario = WLAN TraceFile = wlanwpp. etl** avvia la traccia per tutti i provider abilitati nello scenario WLAN, salvando i risultati in un file denominato wlanwpp. etl. Dopo aver tentato di connettersi alla LAN wireless, digitando **netsh trace stop** viene terminato e correlato il file di traccia.

È quindi possibile aprire il file wlanwpp. etl in Network Monitor. Gli eventi sono raggruppati in base all'ID attività nel riquadro sinistro.

![risoluzione dei problemi relativi alle connessioni LAN wireless tramite Network Monitor (1)](images/1wlan.png)

ETL contiene numerose tracce di altri provider di rete abilitati. È possibile applicare un filtro per visualizzare solo gli eventi rilevanti per il provider **\_ MicrosoftWindowsWlanAutoConfig WLAN** .

![risoluzione dei problemi relativi alle connessioni LAN wireless tramite Network Monitor (2)](images/2wlan.png)

Dopo aver applicato il filtro, è possibile esaminare gli eventi nel riepilogo del frame per identificare un evento che sembra pertinente. Dopo aver selezionato l'evento, fare clic con il pulsante destro del mouse e scegliere Trova conversazioni, quindi fare clic su NetEvent.

![risoluzione dei problemi relativi alle connessioni LAN wireless tramite Network Monitor (3)](images/3wlan.png)

Espandendo gli elementi sotto un ID attività nel riquadro sinistro, sarà possibile visualizzare tutti gli altri provider rilevanti per il tentativo di connessione. Per visualizzare gli eventi di altri provider, tutti i filtri vengono rimossi facendo clic su **Rimuovi** nel riquadro **filtro di visualizzazione** . Le tracce possono essere analizzate scorrendo il riepilogo del frame, selezionando gli eventi aggiuntivi necessari per raccogliere ulteriori informazioni. In questo caso, il riquadro dei dettagli del frame fornisce informazioni che l'errore è dovuto a un errore di scambio delle chiavi, probabilmente a causa dell'impossibilità di immettere la chiave di passaggio errata.

 

 




