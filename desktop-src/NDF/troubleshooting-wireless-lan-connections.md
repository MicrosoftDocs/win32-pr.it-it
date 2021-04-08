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
# <a name="troubleshooting-wireless-lan-connections"></a><span data-ttu-id="70364-104">Risoluzione dei problemi relativi alle connessioni LAN wireless</span><span class="sxs-lookup"><span data-stu-id="70364-104">Troubleshooting Wireless LAN Connections</span></span>

<span data-ttu-id="70364-105">In questo scenario un utente sta tentando di connettersi a una LAN wireless, ma non è in grado di connettersi.</span><span class="sxs-lookup"><span data-stu-id="70364-105">In this scenario, a user is attempting to connect to a wireless LAN, but is unable to connect.</span></span> <span data-ttu-id="70364-106">È possibile utilizzare Netsh e Network Monitor per raccogliere e visualizzare le tracce per determinare il motivo per cui la connessione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="70364-106">You can use Netsh and Network Monitor to collect and view traces in order to help determine why the connection failed.</span></span>

<span data-ttu-id="70364-107">In primo luogo, è possibile utilizzare Netsh per avviare una traccia.</span><span class="sxs-lookup"><span data-stu-id="70364-107">First, you can use netsh to start a trace.</span></span> <span data-ttu-id="70364-108">Digitando **netsh trace start scenario = WLAN TraceFile = wlanwpp. etl** avvia la traccia per tutti i provider abilitati nello scenario WLAN, salvando i risultati in un file denominato wlanwpp. etl.</span><span class="sxs-lookup"><span data-stu-id="70364-108">Typing **netsh trace start scenario = wlan tracefile=wlanwpp.etl** starts tracing for all of the providers enabled under the WLAN scenario, saving the results to a file named wlanwpp.etl.</span></span> <span data-ttu-id="70364-109">Dopo aver tentato di connettersi alla LAN wireless, digitando **netsh trace stop** viene terminato e correlato il file di traccia.</span><span class="sxs-lookup"><span data-stu-id="70364-109">After attempting to connect to the wireless LAN, typing **netsh trace stop** terminates and correlates the trace file.</span></span>

<span data-ttu-id="70364-110">È quindi possibile aprire il file wlanwpp. etl in Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="70364-110">You can then open the wlanwpp.etl file in Network Monitor.</span></span> <span data-ttu-id="70364-111">Gli eventi sono raggruppati in base all'ID attività nel riquadro sinistro.</span><span class="sxs-lookup"><span data-stu-id="70364-111">The events are grouped by activity ID in the left pane.</span></span>

![risoluzione dei problemi relativi alle connessioni LAN wireless tramite Network Monitor (1)](images/1wlan.png)

<span data-ttu-id="70364-113">ETL contiene numerose tracce di altri provider di rete abilitati.</span><span class="sxs-lookup"><span data-stu-id="70364-113">The ETL contains lot of traces from other network providers that are enabled.</span></span> <span data-ttu-id="70364-114">È possibile applicare un filtro per visualizzare solo gli eventi rilevanti per il provider **\_ MicrosoftWindowsWlanAutoConfig WLAN** .</span><span class="sxs-lookup"><span data-stu-id="70364-114">You can apply a filter to display only those events which are relevant to the **WLAN\_MicrosoftWindowsWlanAutoConfig** provider.</span></span>

![risoluzione dei problemi relativi alle connessioni LAN wireless tramite Network Monitor (2)](images/2wlan.png)

<span data-ttu-id="70364-116">Dopo aver applicato il filtro, è possibile esaminare gli eventi nel riepilogo del frame per identificare un evento che sembra pertinente.</span><span class="sxs-lookup"><span data-stu-id="70364-116">After the filter has been applied, you can review the events in the frame summary to identify an event which looks relevant.</span></span> <span data-ttu-id="70364-117">Dopo aver selezionato l'evento, fare clic con il pulsante destro del mouse e scegliere Trova conversazioni, quindi fare clic su NetEvent.</span><span class="sxs-lookup"><span data-stu-id="70364-117">After you select the event, right-click and point to Find Conversations, then click NetEvent.</span></span>

![risoluzione dei problemi relativi alle connessioni LAN wireless tramite Network Monitor (3)](images/3wlan.png)

<span data-ttu-id="70364-119">Espandendo gli elementi sotto un ID attività nel riquadro sinistro, sarà possibile visualizzare tutti gli altri provider rilevanti per il tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="70364-119">Expanding the items under an activity ID in the left pane will allow you to view all of the other relevant providers for the connection attempt.</span></span> <span data-ttu-id="70364-120">Per visualizzare gli eventi di altri provider, tutti i filtri vengono rimossi facendo clic su **Rimuovi** nel riquadro **filtro di visualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="70364-120">To view the events from other providers, all filters are removed by clicking **Remove** in the **Display Filter** pane.</span></span> <span data-ttu-id="70364-121">Le tracce possono essere analizzate scorrendo il riepilogo del frame, selezionando gli eventi aggiuntivi necessari per raccogliere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="70364-121">The traces can be analyzed by scrolling through the frame summary, selecting additional events as needed to gather more information.</span></span> <span data-ttu-id="70364-122">In questo caso, il riquadro dei dettagli del frame fornisce informazioni che l'errore è dovuto a un errore di scambio delle chiavi, probabilmente a causa dell'impossibilità di immettere la chiave di passaggio errata.</span><span class="sxs-lookup"><span data-stu-id="70364-122">In this case, the Frame Details pane provides information that the failure is due to key exchange failure, most likely due to the user entering the wrong pass key.</span></span>

 

 




