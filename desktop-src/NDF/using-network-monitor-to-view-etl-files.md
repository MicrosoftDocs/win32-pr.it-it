---
title: Utilizzo di Network Monitor per visualizzare i file ETL
description: Network Monitor 3,3 consente agli utenti di analizzare, filtrare e visualizzare un file ETL (utilizzando Windows Vista o versione successiva).
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04120f860654f4859aa930f32a4711999682eaf8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "103968793"
---
# <a name="using-network-monitor-to-view-etl-files"></a><span data-ttu-id="b489d-103">Utilizzo di Network Monitor per visualizzare i file ETL</span><span class="sxs-lookup"><span data-stu-id="b489d-103">Using Network Monitor to View ETL Files</span></span>

<span data-ttu-id="b489d-104">[Network Monitor 3,3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) consente agli utenti di analizzare, filtrare e visualizzare un file ETL (utilizzando Windows Vista o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="b489d-104">[Network Monitor 3.3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) enables users to parse, filter, and view an ETL file (using Windows Vista or later).</span></span> <span data-ttu-id="b489d-105">Se si utilizza Network Monitor 3,2, sarà necessario scaricare e installare parser aggiuntivi da [codeplex](https://www.codeplex.com/NMParsers) per eseguire il rendering degli eventi di traccia di rete.</span><span class="sxs-lookup"><span data-stu-id="b489d-105">(If using Network Monitor 3.2, you will need to download and install additional parsers from [CodePlex](https://www.codeplex.com/NMParsers) in order to render the network tracing events.)</span></span>

<span data-ttu-id="b489d-106">I file ETL correlati raggruppano insieme gli eventi rilevanti.</span><span class="sxs-lookup"><span data-stu-id="b489d-106">Correlated ETL files group the relevant events together.</span></span> <span data-ttu-id="b489d-107">Il ScrollBar seguente mostra un file correlato aperto in Network Monitor, con la conversazione abilitata.</span><span class="sxs-lookup"><span data-stu-id="b489d-107">The illlustration below shows a correlated file opened in Network Monitor, with conversation enabled.</span></span>

![Screenshot che mostra la Network Monitor, con eventi correlati evidenziati nella finestra a sinistra e UTEvent evidenziati dall'elenco a discesa.](images/ut-netmon1.png)

<span data-ttu-id="b489d-109">Gli eventi correlati vengono raggruppati per attività nel riquadro sinistro.</span><span class="sxs-lookup"><span data-stu-id="b489d-109">Correlated events are grouped by activity in the left pane.</span></span> <span data-ttu-id="b489d-110">È possibile selezionare un evento nel riquadro Riepilogo Frame, quindi fare clic con il pulsante destro del mouse per selezionare la conversazione a livello di evento di rete.</span><span class="sxs-lookup"><span data-stu-id="b489d-110">You can select an event in the Frame Summary pane, then right-click to select the conversation at the network event level.</span></span> <span data-ttu-id="b489d-111">Verrà visualizzata un'attività correlata nel riquadro sinistro.</span><span class="sxs-lookup"><span data-stu-id="b489d-111">This will display a related activity in the left pane.</span></span>

<span data-ttu-id="b489d-112">Se si seleziona una determinata attività dal riquadro a sinistra per espanderla, verrà visualizzato l'elenco dei provider per gli eventi correlati.</span><span class="sxs-lookup"><span data-stu-id="b489d-112">Selecting a particular activity from the left pane and expanding it will show the list of providers for the correlated events.</span></span>

![Screenshot che mostra la Network Monitor con un'attività selezionata nel riquadro sinistro e gli eventi corrispondenti a tale evento nel riquadro di destra.](images/ut-netmon2.png)

<span data-ttu-id="b489d-114">Quando si seleziona un provider specifico nel riquadro a sinistra, nel riquadro Riepilogo frame verrà visualizzato un elenco di eventi specifici del provider e dell'attività.</span><span class="sxs-lookup"><span data-stu-id="b489d-114">When you select a specific provider in the left pane, a list of events specific to that provider and activity will be displayed in the Frame Summary pane.</span></span>

![Screenshot che mostra un provider specifico selezionato nel riquadro a sinistra e un elenco di eventi specifici del provider evidenziato nel riquadro superiore destro.](images/ut-netmon3.png)

<span data-ttu-id="b489d-116">I filtri possono essere applicati in Network Monitor per semplificare la visualizzazione e la ricerca degli eventi o dei pacchetti corretti.</span><span class="sxs-lookup"><span data-stu-id="b489d-116">Filters can be applied in Network Monitor to make it easier to view and find the right events or packet.</span></span> <span data-ttu-id="b489d-117">Ad esempio, è possibile applicare un filtro agli eventi di errore selezionati (ad esempio, **UTEvent. Header. Descriptor. Level = = 2**) per visualizzarli in un determinato colore.</span><span class="sxs-lookup"><span data-stu-id="b489d-117">For example, you can apply a filter to selected error events (for example, **UTEvent.Header.Descriptor.Level == 2**) to display them in a certain color.</span></span>

![Screenshot che mostra la finestra di dialogo "modifica filtro colori".](images/ut-netmon4.png)

<span data-ttu-id="b489d-119">I filtri possono essere applicati anche per contrassegnare diversi provider in colori diversi, in modo da semplificare la visualizzazione dei risultati.</span><span class="sxs-lookup"><span data-stu-id="b489d-119">Filters can also be applied to mark different providers in different colors so that the results are easier to view.</span></span>

![Screenshot che mostra un esempio di provider diversi contrassegnati con colori diversi.](images/ut-netmon5.png)

<span data-ttu-id="b489d-121">Per applicare un filtro, fare clic su **ColorFilters** nel menu **filtri** .</span><span class="sxs-lookup"><span data-stu-id="b489d-121">To apply a filter, click **ColorFilters** on the **Filters** menu.</span></span>

<span data-ttu-id="b489d-122">Nella tabella seguente vengono illustrati alcuni esempi di filtri utili.</span><span class="sxs-lookup"><span data-stu-id="b489d-122">The following table shows some examples of useful filters.</span></span>



| <span data-ttu-id="b489d-123">Filtra</span><span class="sxs-lookup"><span data-stu-id="b489d-123">Filter</span></span>                                                                        | <span data-ttu-id="b489d-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b489d-124">Description</span></span>                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="b489d-125">UTEvent. Header. Descriptor. Level = = 2</span><span class="sxs-lookup"><span data-stu-id="b489d-125">UTEvent.Header.Descriptor.Level == 2</span></span>                                          | <span data-ttu-id="b489d-126">Filtra solo gli eventi di errore.</span><span class="sxs-lookup"><span data-stu-id="b489d-126">Filters only error events.</span></span>                                        |
| <span data-ttu-id="b489d-127">UTEvent. Header. Descriptor. Level = = 3</span><span class="sxs-lookup"><span data-stu-id="b489d-127">UTEvent.Header.Descriptor.Level == 3</span></span>                                          | <span data-ttu-id="b489d-128">Filtra solo gli eventi di avviso.</span><span class="sxs-lookup"><span data-stu-id="b489d-128">Filters only warning events.</span></span>                                      |
| <span data-ttu-id="b489d-129">UTEvent.Header.Descriptor.Id = = 2001</span><span class="sxs-lookup"><span data-stu-id="b489d-129">UTEvent.Header.Descriptor.Id == 2001</span></span>                                          | <span data-ttu-id="b489d-130">Filtra solo gli eventi con ID evento 2001.</span><span class="sxs-lookup"><span data-stu-id="b489d-130">Filters only events with event ID 2001.</span></span>                           |
| <span data-ttu-id="b489d-131">\_MICROSOFTWINDOWSWLANAUTOCONFIG WLAN</span><span class="sxs-lookup"><span data-stu-id="b489d-131">WLAN\_MicrosoftWindowsWLANAutoConfig</span></span>                                          | <span data-ttu-id="b489d-132">Filtra solo gli eventi del servizio WLAN.</span><span class="sxs-lookup"><span data-stu-id="b489d-132">Filters only events from WLAN service.</span></span>                            |
| <span data-ttu-id="b489d-133">\_MicrosoftWindowsNWiFi N802</span><span class="sxs-lookup"><span data-stu-id="b489d-133">N802\_MicrosoftWindowsNWiFi</span></span>                                                   | <span data-ttu-id="b489d-134">Filtra solo gli eventi dal driver WiFi nativo.</span><span class="sxs-lookup"><span data-stu-id="b489d-134">Filters only events from the Native Wifi driver.</span></span>                  |
| <span data-ttu-id="b489d-135">WLAN \_ MICROSOFTWINDOWSWLANAUTOCONFIG e UTEvent.Header.Descriptor.ID = = 2001</span><span class="sxs-lookup"><span data-stu-id="b489d-135">WLAN\_MicrosoftWindowsWLANAutoConfig AND UTEvent.Header.Descriptor.Id == 2001</span></span> | <span data-ttu-id="b489d-136">Filtra solo gli eventi con ID evento 2001 generati dal servizio WLAN.</span><span class="sxs-lookup"><span data-stu-id="b489d-136">Filters only events with event ID 2001 emitted from WLAN service.</span></span> |



 

 

 




