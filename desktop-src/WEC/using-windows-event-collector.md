---
title: Utilizzo dell'agente di raccolta eventi di Windows
description: In questa sezione sono elencati gli argomenti che illustrano le attività che è possibile eseguire tramite l'SDK di raccolta eventi di Windows. Gli esempi di codice e le spiegazioni per tutte le attività sono inclusi in ciascuno degli argomenti seguenti.
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc618ced4cefc7f17fb63b27bb1e097e65b3adac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298121"
---
# <a name="using-windows-event-collector"></a><span data-ttu-id="c13ab-104">Utilizzo dell'agente di raccolta eventi di Windows</span><span class="sxs-lookup"><span data-stu-id="c13ab-104">Using Windows Event Collector</span></span>

<span data-ttu-id="c13ab-105">In questa sezione sono elencati gli argomenti che illustrano le attività che è possibile eseguire tramite l'SDK di raccolta eventi di Windows.</span><span class="sxs-lookup"><span data-stu-id="c13ab-105">This section lists the topics that explain the tasks that can be accomplished using the Windows Event Collector SDK.</span></span> <span data-ttu-id="c13ab-106">Gli esempi di codice e le spiegazioni per tutte le attività sono inclusi in ciascuno degli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="c13ab-106">Code examples and explanations for all the tasks are included in each of the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c13ab-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c13ab-107">In This Section</span></span>

-   [<span data-ttu-id="c13ab-108">Creazione di una sottoscrizione avviata dall'agente di raccolta</span><span class="sxs-lookup"><span data-stu-id="c13ab-108">Creating a Collector Initiated Subscription</span></span>](creating-an-event-collector-subscription.md)

    <span data-ttu-id="c13ab-109">Vengono fornite informazioni e un esempio di codice C++ per la creazione di una sottoscrizione avviata dall'agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="c13ab-109">Provides information and a C++ code example for creating a collector-initiated subscription.</span></span> <span data-ttu-id="c13ab-110">Una sottoscrizione avviata dall'agente di raccolta consente di ricevere gli eventi in un computer locale, ovvero l'agente di raccolta eventi, che vengono trasmessi da un computer remoto (origine evento).</span><span class="sxs-lookup"><span data-stu-id="c13ab-110">A collector-initiated subscription enables you to receive events on a local computer (the event collector) that are forwarded from a remote computer (an event source).</span></span>

-   [<span data-ttu-id="c13ab-111">Configurazione di una sottoscrizione avviata dall'origine</span><span class="sxs-lookup"><span data-stu-id="c13ab-111">Setting up a Source Initiated Subscription</span></span>](setting-up-a-source-initiated-subscription.md)

    <span data-ttu-id="c13ab-112">Vengono fornite informazioni e un esempio di codice C++ per la creazione di una sottoscrizione avviata dall'origine.</span><span class="sxs-lookup"><span data-stu-id="c13ab-112">Provides information and a C++ code example for creating a source-initiated subscription.</span></span> <span data-ttu-id="c13ab-113">Una sottoscrizione avviata dall'origine consente di ricevere eventi in un computer locale, ovvero l'agente di raccolta eventi, che vengono trasmessi da un computer remoto (origine evento) senza specificare le origini eventi nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c13ab-113">A source-initiated subscription enables you to receive events on a local computer (the event collector) that are forwarded from a remote computer (an event source) without specifying the event sources in the subscription.</span></span>

-   [<span data-ttu-id="c13ab-114">Aggiunta di un'origine evento a una sottoscrizione avviata dall'agente di raccolta</span><span class="sxs-lookup"><span data-stu-id="c13ab-114">Adding an Event Source to a Collector Initiated Subscription</span></span>](adding-an-event-source-to-an-event-collector-subscription.md)

    <span data-ttu-id="c13ab-115">Vengono fornite informazioni e un esempio di codice C++ per l'aggiunta di un'origine evento (computer locale o computer remoto) a una sottoscrizione avviata dall'agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="c13ab-115">Provides information and a C++ code example for adding an event source (local computer or remote computer) to a collector-initiated subscription.</span></span> <span data-ttu-id="c13ab-116">Una sottoscrizione avviata dall'agente di raccolta non può iniziare a raccogliere eventi fino a quando non viene aggiunta un'origine evento alla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c13ab-116">A collector initiated subscription cannot start collecting events until an event source is added to the subscription.</span></span>

-   [<span data-ttu-id="c13ab-117">Creazione di sottoscrizioni di eventi hardware</span><span class="sxs-lookup"><span data-stu-id="c13ab-117">Creating Hardware Event Subscriptions</span></span>](creating-hardware-event-subscriptions.md)

    <span data-ttu-id="c13ab-118">Vengono fornite informazioni su come creare una sottoscrizione di eventi per ricevere eventi hardware da un computer in cui è installato un controller di gestione di battiscopa (BMC).</span><span class="sxs-lookup"><span data-stu-id="c13ab-118">Provides information about how to create an event subscription in order to receive hardware events from a computer that has a Baseboard Management Controller (BMC) installed.</span></span>

-   [<span data-ttu-id="c13ab-119">Eliminazione di una sottoscrizione di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="c13ab-119">Deleting an Event Collector Subscription</span></span>](deleting-an-event-collector-subscription.md)

    <span data-ttu-id="c13ab-120">Fornisce informazioni e un esempio di codice C++ per l'eliminazione di una sottoscrizione di raccolta eventi da un computer locale.</span><span class="sxs-lookup"><span data-stu-id="c13ab-120">Provides information and a C++ code example for deleting an Event Collector subscription from a local computer.</span></span>

-   [<span data-ttu-id="c13ab-121">Visualizzazione delle proprietà di una sottoscrizione di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="c13ab-121">Displaying the Properties of an Event Collector Subscription</span></span>](displaying-the-properties-of-an-event-collector-subscription.md)

    <span data-ttu-id="c13ab-122">Vengono fornite informazioni e un esempio di codice C++ per visualizzare i valori delle proprietà di una sottoscrizione di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="c13ab-122">Provides information and a C++ code example for displaying the property values of an Event Collector subscription.</span></span> <span data-ttu-id="c13ab-123">I valori delle proprietà possono fornire informazioni utili, ad esempio gli indirizzi delle origini eventi, lo stato della sottoscrizione e le origini eventi e le informazioni sulla modalità di recapito degli eventi.</span><span class="sxs-lookup"><span data-stu-id="c13ab-123">Property values can provide useful information, such as the addresses of event sources, the status of the subscription and event sources, and information about how events are delivered.</span></span>

-   [<span data-ttu-id="c13ab-124">Visualizzazione dello stato di una sottoscrizione dell'agente di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="c13ab-124">Displaying the Status of an Event Collector Subscription</span></span>](displaying-the-status-of-an-event-collector-subscription.md)

    <span data-ttu-id="c13ab-125">Fornisce informazioni e un esempio di codice C++ per visualizzare lo stato della fase di esecuzione delle origini eventi associate a una sottoscrizione dell'agente di raccolta eventi.</span><span class="sxs-lookup"><span data-stu-id="c13ab-125">Provides information and a C++ code example for displaying the run time status of events sources that are associated to an Event Collector subscription.</span></span> <span data-ttu-id="c13ab-126">Questo consente di visualizzare i messaggi di errore che consentono di risolvere i problemi che impediscono l'invio di eventi da un'origine evento.</span><span class="sxs-lookup"><span data-stu-id="c13ab-126">This enables you to view error messages that can help solve problems, which prevent an event source from forwarding events.</span></span>

-   [<span data-ttu-id="c13ab-127">Elenco delle sottoscrizioni degli agenti di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="c13ab-127">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)

    <span data-ttu-id="c13ab-128">Vengono fornite informazioni e un esempio di codice C++ per elencare le sottoscrizioni esistenti in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="c13ab-128">Provides information and a C++ code example for listing the subscriptions that exist on a local computer.</span></span> <span data-ttu-id="c13ab-129">È possibile utilizzare i nomi delle sottoscrizioni ottenuti con questo esempio per eliminare una sottoscrizione, aggiungere un'origine evento a una sottoscrizione, recuperare le proprietà di una sottoscrizione o visualizzare lo stato di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c13ab-129">You can use the subscription names that are obtained with this example to delete a subscription, add an event source to a subscription, retrieve the properties of a subscription, or view the status of a subscription.</span></span>

-   [<span data-ttu-id="c13ab-130">Rimozione di un'origine evento da una sottoscrizione avviata dall'agente di raccolta</span><span class="sxs-lookup"><span data-stu-id="c13ab-130">Removing an Event Source from a Collector Initiated Subscription</span></span>](removing-an-event-source-from-an-event-collector-subscription.md)

    <span data-ttu-id="c13ab-131">Vengono fornite informazioni e un esempio di codice C++ per la rimozione di un'origine evento da una sottoscrizione avviata dall'agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="c13ab-131">Provides information and a C++ code example for removing an event source from a collector-initiated subscription.</span></span> <span data-ttu-id="c13ab-132">È possibile rimuovere un'origine evento da una sottoscrizione avviata dall'agente di raccolta senza disabilitare la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c13ab-132">You can remove an event source from a collector-initiated subscription without disabling the subscription.</span></span>

-   [<span data-ttu-id="c13ab-133">Nuovo tentativo di sottoscrizione di un agente di raccolta eventi</span><span class="sxs-lookup"><span data-stu-id="c13ab-133">Retrying an Event Collector Subscription</span></span>](retrying-an-event-collector-subscription.md)

    <span data-ttu-id="c13ab-134">Fornisce informazioni e un esempio di codice C++ per ritentare una sottoscrizione dell'agente di raccolta eventi quando una o più origini evento non sono riuscite.</span><span class="sxs-lookup"><span data-stu-id="c13ab-134">Provides information and a C++ code example for retrying an Event Collector subscription when one or more event sources have failed.</span></span> <span data-ttu-id="c13ab-135">È possibile ritentare una singola origine evento oppure ritentare l'intera sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c13ab-135">You can retry a single event source or you can retry the entire subscription.</span></span>

 

 




