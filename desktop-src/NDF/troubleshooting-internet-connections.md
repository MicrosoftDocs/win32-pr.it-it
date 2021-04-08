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
# <a name="troubleshooting-internet-connections"></a><span data-ttu-id="33ab3-104">Risoluzione dei problemi relativi alle connessioni Internet</span><span class="sxs-lookup"><span data-stu-id="33ab3-104">Troubleshooting Internet Connections</span></span>

<span data-ttu-id="33ab3-105">In questo scenario un utente sta tentando di passare a www.msn.com usando il protocollo HTTPS, ma non è in grado di connettersi.</span><span class="sxs-lookup"><span data-stu-id="33ab3-105">In this scenario, a user is attempting to browse to www.msn.com using the https protocol, but is unable to connect.</span></span> <span data-ttu-id="33ab3-106">È possibile utilizzare Netsh e Network Monitor per raccogliere e visualizzare le tracce per determinare il motivo per cui la connessione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="33ab3-106">You can use Netsh and Network Monitor to collect and view traces in order to help determine why the connection failed.</span></span>

<span data-ttu-id="33ab3-107">In primo luogo, è possibile utilizzare Netsh per avviare una traccia.</span><span class="sxs-lookup"><span data-stu-id="33ab3-107">First, you can use netsh to start a trace.</span></span> <span data-ttu-id="33ab3-108">Digitando **netsh trace start scenario = InternetClient TraceFile = MSN. etl** avvia la traccia per tutti i provider abilitati nello scenario InternetClient, salvando i risultati in un file denominato MSN. etl.</span><span class="sxs-lookup"><span data-stu-id="33ab3-108">Typing **netsh trace start scenario = InternetClient tracefile=msn.etl** starts tracing for all of the providers enabled under the InternetClient scenario, saving the results to a file named msn.etl.</span></span> <span data-ttu-id="33ab3-109">Dopo aver usato un Web browser per tentare di raggiungere www.msn.com, la digitazione di **netsh trace stop** termina e mette in correlazione il file di traccia.</span><span class="sxs-lookup"><span data-stu-id="33ab3-109">After using a web browser to attempt to reach www.msn.com, typing **netsh trace stop** terminates and correlates the trace file.</span></span>

<span data-ttu-id="33ab3-110">È quindi possibile aprire il file MSN. etl in Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="33ab3-110">You can then open the msn.etl file in Network Monitor.</span></span> <span data-ttu-id="33ab3-111">Gli eventi sono raggruppati in base all'ID attività nel riquadro sinistro.</span><span class="sxs-lookup"><span data-stu-id="33ab3-111">The events are grouped by activity ID in the left pane.</span></span> <span data-ttu-id="33ab3-112">Utilizzando la descrizione del filtro **. Contains ("MSN")** mostrerà solo gli eventi che includono la stringa "MSN" nella descrizione del protocollo.</span><span class="sxs-lookup"><span data-stu-id="33ab3-112">Using the filter **description.contains("msn")** will show only those events which include the string "msn" in their protocol description.</span></span>

![risoluzione dei problemi relativi alle connessioni Internet tramite Network Monitor (1)](images/internetclient1.png)

<span data-ttu-id="33ab3-114">Successivamente, è possibile esaminare gli eventi nel riepilogo dei frame per identificare un evento che sembra pertinente.</span><span class="sxs-lookup"><span data-stu-id="33ab3-114">Next, you can review the events in the frame summary to identify an event which looks relevant.</span></span> <span data-ttu-id="33ab3-115">Dopo aver selezionato l'evento, fare clic con il pulsante destro del mouse e scegliere Trova conversazioni, quindi fare clic su UTEvent per selezionare la conversazione a livello di UTEvent.</span><span class="sxs-lookup"><span data-stu-id="33ab3-115">After you select the event, right-click and point to Find Conversations, then click UTEvent to select the conversation at the UTEvent level.</span></span>

![risoluzione dei problemi relativi alle connessioni Internet tramite Network Monitor (2)](images/internetclient2.png)

<span data-ttu-id="33ab3-117">Viene evidenziata l'attività normalizzata associata nel riquadro sinistro, in questo caso UTEvent ActivityID 397.</span><span class="sxs-lookup"><span data-stu-id="33ab3-117">The associated normalized activity in the left pane is then highlighted, in this case UTEvent ActivityID 397.</span></span>

![risoluzione dei problemi relativi alle connessioni Internet tramite Network Monitor (3)](images/internetclient3.png)

<span data-ttu-id="33ab3-119">Utilizzando Network Monitor per visualizzare e filtrare le informazioni di traccia, il numero di eventi da esaminare è stato ridotto da 1989 a 96.</span><span class="sxs-lookup"><span data-stu-id="33ab3-119">By using Network Monitor to view and filter the trace information, the number of events to examine has been reduced from 1989 to 96.</span></span>

 

 




