---
title: Risoluzione dei problemi relativi alle connessioni LAN wireless
description: In questo scenario, un utente sta tentando di connettersi a una rete LAN wireless, ma non è in grado di connettersi. È possibile usare Netsh e Network Monitor per raccogliere e visualizzare le tracce per determinare il motivo per cui la connessione non è riuscita.
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3749b3e3a45ef68cb33b7d3658ca346dd4c6e0a8ba8ea11626573f4da6edfbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801835"
---
# <a name="troubleshooting-wireless-lan-connections"></a>Risoluzione dei problemi relativi alle connessioni LAN wireless

In questo scenario, un utente sta tentando di connettersi a una rete LAN wireless, ma non è in grado di connettersi. È possibile usare Netsh e Network Monitor per raccogliere e visualizzare le tracce per determinare il motivo per cui la connessione non è riuscita.

In primo luogo, è possibile usare netsh per avviare una traccia. Digitando **netsh trace start scenario = wlan tracefile=wlanwpp.etl** viene avviata la traccia per tutti i provider abilitati nello scenario WLAN, salvando i risultati in un file denominato wlanwpp.etl. Dopo aver tentato di connettersi alla rete LAN wireless, **digitando netsh trace stop** termina e correla il file di traccia.

È quindi possibile aprire il file wlanwpp.etl in Network Monitor. Gli eventi vengono raggruppati in base all'ID attività nel riquadro sinistro.

![risoluzione dei problemi relativi alle connessioni lan wireless tramite Network Monitor (1)](images/1wlan.png)

L'ETL contiene molte tracce di altri provider di rete abilitati. È possibile applicare un filtro per visualizzare solo gli eventi rilevanti per il provider **\_ MicrosoftWindowsWlanAutoConfig WLAN.**

![risoluzione dei problemi relativi alle connessioni lan wireless tramite Network Monitor (2)](images/2wlan.png)

Dopo aver applicato il filtro, è possibile esaminare gli eventi nel riepilogo dei frame per identificare un evento che sembra pertinente. Dopo aver selezionato l'evento, fare clic con il pulsante destro del mouse e scegliere Trova conversazioni, quindi fare clic su NetEvent.

![risoluzione dei problemi relativi alle connessioni lan wireless tramite Network Monitor (3)](images/3wlan.png)

Espandendo gli elementi sotto un ID attività nel riquadro sinistro sarà possibile visualizzare tutti gli altri provider rilevanti per il tentativo di connessione. Per visualizzare gli eventi di altri provider, tutti i filtri vengono rimossi facendo clic **su Rimuovi** nel **riquadro Filtro** di visualizzazione. Le tracce possono essere analizzate scorrendo il riepilogo dei frame, selezionando eventi aggiuntivi in base alle esigenze per raccogliere altre informazioni. In questo caso, il riquadro Dettagli frame fornisce informazioni che l'errore è dovuto a un errore di scambio della chiave, molto probabilmente a causa dell'immissione della pass key errata da parte dell'utente.

 

 




