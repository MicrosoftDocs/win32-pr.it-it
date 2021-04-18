---
description: Facendo clic su Esegui esperti dalla finestra Experts dell'interfaccia utente di Network Monitor, vengono avviati gli esperti selezionati per il file di acquisizione e viene chiamata la funzione Run. Quando viene avviato, l'esperto analizza il file di acquisizione usando diverse funzioni di frame di esperti.
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: Avvio ed esecuzione di esperti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bd41472d286727541d26bade1942eb3b6b5c593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318966"
---
# <a name="starting-and-running-experts"></a><span data-ttu-id="601f2-104">Avvio ed esecuzione di esperti</span><span class="sxs-lookup"><span data-stu-id="601f2-104">Starting and Running Experts</span></span>

<span data-ttu-id="601f2-105">Facendo clic su **Esegui esperti** dalla finestra Experts dell'interfaccia utente di Network Monitor, vengono avviati gli esperti selezionati per il file di acquisizione e viene chiamata la funzione [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="601f2-105">Clicking **Run Experts** from the Experts window of the Network Monitor UI starts the experts selected for the capture file and calls the [**Run**](run.md) function.</span></span> <span data-ttu-id="601f2-106">Quando viene avviato, l'esperto analizza il file di acquisizione usando diverse funzioni di frame di esperti.</span><span class="sxs-lookup"><span data-stu-id="601f2-106">When started, the expert analyzes the capture file by using several expert frame functions.</span></span>

<span data-ttu-id="601f2-107">La funzione [**ExpertIndicateStatus**](expertindicatestatus.md) fornisce informazioni sullo stato dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="601f2-107">The [**ExpertIndicateStatus**](expertindicatestatus.md) function provides status information from the expert.</span></span> <span data-ttu-id="601f2-108">Quando si esegue un esperto con Network Monitor, nella finestra di visualizzazione stato esperto vengono visualizzate le informazioni aggiornate sullo stato aggiornate (dal 0 al 100% di completamento).</span><span class="sxs-lookup"><span data-stu-id="601f2-108">When you run an expert with Network Monitor, the Expert Status View window displays periodically updated status information (from 0 to 100 percent completion).</span></span>

![finestra di visualizzazione stato esperto](images/exview.png)

<span data-ttu-id="601f2-110">L'esperto è attivo fino al completamento del passaggio dei dati tramite il file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="601f2-110">The expert is active until the data completes its pass though the capture file.</span></span> <span data-ttu-id="601f2-111">Al termine del passaggio, viene visualizzata una finestra Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="601f2-111">When the pass is complete, an Event Viewer window appears.</span></span> <span data-ttu-id="601f2-112">Le informazioni contenute in questa finestra dipendono dal tipo di esperto che ha analizzato i dati.</span><span class="sxs-lookup"><span data-stu-id="601f2-112">The information in this window depends on the type of expert that analyzed the data.</span></span> <span data-ttu-id="601f2-113">Nella figura seguente è illustrata una visualizzazione di esperti di distribuzione delle proprietà, che riepiloga i dati del frame analizzati dall'esperto.</span><span class="sxs-lookup"><span data-stu-id="601f2-113">The following illustration shows a Property Distribution Expert view, which summarizes the frame data that the expert analyzed.</span></span>

![visualizzazione esperto distribuzione proprietà](images/exview1.png)

<span data-ttu-id="601f2-115">Un secondo report (non visualizzato) riepiloga i risultati dell'esperto di ritrasmissione del Transmission Control Protocol (TCP).</span><span class="sxs-lookup"><span data-stu-id="601f2-115">A second report (not shown), summarizes the results of the Transmission Control Protocol (TCP) Retransmit expert.</span></span>

<span data-ttu-id="601f2-116">È anche possibile:</span><span class="sxs-lookup"><span data-stu-id="601f2-116">You can also:</span></span>

-   <span data-ttu-id="601f2-117">Creare una voce per una pagina di riferimento evento (ERP) che informa l'utente di condizioni o problemi rilevati (come illustrato nella finestra di analisi).</span><span class="sxs-lookup"><span data-stu-id="601f2-117">Create an entry for an event reference page (ERP) that advises the user of detected conditions or problems (as shown in the Analysis window).</span></span>
-   <span data-ttu-id="601f2-118">Creare voci per le correzioni suggerite o i dati esplicativi che forniscono informazioni aggiuntive (come illustrato nella finestra di risoluzione).</span><span class="sxs-lookup"><span data-stu-id="601f2-118">Create entries for suggested fixes or explanatory data that provide additional information (as shown in the Resolution window).</span></span>

<span data-ttu-id="601f2-119">Dopo che l'esperto ha completato l'attività, Network Monitor rimuove l'esperto dalla memoria attiva.</span><span class="sxs-lookup"><span data-stu-id="601f2-119">After the expert completes its task, Network Monitor removes the expert from active memory.</span></span> <span data-ttu-id="601f2-120">Gli esperti devono usare le funzioni di memoria protette incluse nel Software Development Kit (SDK) della piattaforma; Queste funzioni ripuliscono la memoria se gli esperti hanno esito negativo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="601f2-120">Experts should use the protected memory functions included in the Platform Software Development Kit (SDK); these functions clean up memory if the experts fail during run time.</span></span>

 

 



