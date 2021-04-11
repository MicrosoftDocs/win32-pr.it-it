---
description: Applicazioni DVD
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: Applicazioni DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acaddc683078acff84b7c90689f82becfb7b1d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341851"
---
# <a name="dvd-applications"></a><span data-ttu-id="95f74-103">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="95f74-103">DVD Applications</span></span>

<span data-ttu-id="95f74-104">DirectShow fornisce un componente denominato [DVD Navigator](dvd-navigator-filter.md) Source Filter, che semplifica le attività di navigazione su DVD in C++.</span><span class="sxs-lookup"><span data-stu-id="95f74-104">DirectShow provides a component called the [DVD Navigator](dvd-navigator-filter.md) source filter which simplifies DVD navigation tasks in C++.</span></span> <span data-ttu-id="95f74-105">Il navigatore DVD offre tutte le funzionalità disponibili in un lettore DVD autonomo con funzionalità complete, oltre a funzionalità aggiuntive specifiche per la riproduzione di DVD su personal computer.</span><span class="sxs-lookup"><span data-stu-id="95f74-105">The DVD Navigator has all the capabilities that you find on a full-featured stand-alone DVD player, plus additional capabilities specific to playing DVDs on personal computers.</span></span> <span data-ttu-id="95f74-106">Grazie a DVD Navigator, gli sviluppatori di script e C++ possono creare applicazioni DVD con funzionalità complete senza fare riferimento alla specifica DVD.</span><span class="sxs-lookup"><span data-stu-id="95f74-106">Using the DVD Navigator, C++ and scripting developers can create full-featured DVD applications without referring to the DVD specification.</span></span> <span data-ttu-id="95f74-107">Il navigatore DVD, in coordinamento con i filtri del decodificatore, gestisce anche la gestione e la protezione del copyright (CSS e protezione della copia analoga), isolando gli sviluppatori di applicazioni da questi dettagli.</span><span class="sxs-lookup"><span data-stu-id="95f74-107">The DVD Navigator, in coordination with the decoder filters, also handles regional management and copyright protection (CSS and analog copy protection), isolating application developers from these details.</span></span>

<span data-ttu-id="95f74-108">Il filtro per lo strumento di spostamento DVD funziona in un intero volume di DVD-Video, costituito dai file nella \_ directory di Servizi terminal video.</span><span class="sxs-lookup"><span data-stu-id="95f74-108">The DVD Navigator filter works across an entire DVD-Video volume, which consists of the files in the VIDEO\_TS directory.</span></span> <span data-ttu-id="95f74-109">Diversamente dalla maggior parte dei filtri origine DirectShow che funzionano con singoli flussi o file, il navigatore DVD usa la struttura DVD-Video di titoli, capitoli e codici temporali.</span><span class="sxs-lookup"><span data-stu-id="95f74-109">Unlike most DirectShow source filters that work with individual streams or files, the DVD Navigator uses the DVD-Video structure of titles, chapters, and time codes.</span></span> <span data-ttu-id="95f74-110">Gli sviluppatori che desiderano riprodurre singoli file MPEG-2 in DirectShow devono usare il [Demultiplexer MPEG-2](mpeg-2-demultiplexer.md) anziché il filtro del navigatore DVD.</span><span class="sxs-lookup"><span data-stu-id="95f74-110">Developers wishing to play individual MPEG-2 files in DirectShow should use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead of the DVD Navigator filter.</span></span> <span data-ttu-id="95f74-111">Per ulteriori informazioni, vedere [supporto MPEG-2 in DirectShow](mpeg-2-support-in-directshow.md) .</span><span class="sxs-lookup"><span data-stu-id="95f74-111">See [MPEG-2 Support in DirectShow](mpeg-2-support-in-directshow.md) for more information.</span></span>

> [!Note]  
> <span data-ttu-id="95f74-112">Per riprodurre DVD, l'utente deve disporre di un decodificatore MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="95f74-112">To play DVDs, the user must have an MPEG-2 decoder.</span></span>

 

<span data-ttu-id="95f74-113">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="95f74-113">This section contains the following topics.</span></span>

-   [<span data-ttu-id="95f74-114">Funzionalità di supporto DVD in DirectShow</span><span class="sxs-lookup"><span data-stu-id="95f74-114">DVD Support Features in DirectShow</span></span>](dvd-support-features-in-directshow.md)
-   [<span data-ttu-id="95f74-115">Nozioni fondamentali sui DVD</span><span class="sxs-lookup"><span data-stu-id="95f74-115">DVD Basics</span></span>](dvd-basics.md)
-   [<span data-ttu-id="95f74-116">Creazione del grafico del filtro DVD</span><span class="sxs-lookup"><span data-stu-id="95f74-116">Building the DVD Filter Graph</span></span>](building-the-dvd-filter-graph.md)
-   [<span data-ttu-id="95f74-117">Acquisizione dei puntatori dell'interfaccia DVD</span><span class="sxs-lookup"><span data-stu-id="95f74-117">Obtaining the DVD Interface Pointers</span></span>](obtaining-the-dvd-interface-pointers.md)
-   [<span data-ttu-id="95f74-118">Comandi DVD</span><span class="sxs-lookup"><span data-stu-id="95f74-118">DVD Commands</span></span>](dvd-commands.md)
-   [<span data-ttu-id="95f74-119">Identificazione di operazioni DVD valide</span><span class="sxs-lookup"><span data-stu-id="95f74-119">Identifying Valid DVD Operations</span></span>](identifying-valid-dvd-operations.md)
-   [<span data-ttu-id="95f74-120">Sincronizzazione dei comandi DVD</span><span class="sxs-lookup"><span data-stu-id="95f74-120">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
-   [<span data-ttu-id="95f74-121">Flusso di dati nel navigatore DVD</span><span class="sxs-lookup"><span data-stu-id="95f74-121">Data Flow in the DVD Navigator</span></span>](data-flow-in-the-dvd-navigator.md)
-   [<span data-ttu-id="95f74-122">Gestione delle notifiche degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="95f74-122">Handling DVD Event Notifications</span></span>](handling-dvd-event-notifications.md)
-   [<span data-ttu-id="95f74-123">Uso dei menu DVD</span><span class="sxs-lookup"><span data-stu-id="95f74-123">Working With DVD Menus</span></span>](working-with-dvd-menus.md)
-   [<span data-ttu-id="95f74-124">Flussi audio e immagine subimmagini</span><span class="sxs-lookup"><span data-stu-id="95f74-124">Audio and Subpicture Streams</span></span>](audio-and-subpicture-streams.md)
-   [<span data-ttu-id="95f74-125">Applicazione dei livelli di gestione padre</span><span class="sxs-lookup"><span data-stu-id="95f74-125">Enforcing Parental Management Levels</span></span>](enforcing-parental-management-levels.md)
-   [<span data-ttu-id="95f74-126">Salvataggio e ripristino di oggetti DvdState</span><span class="sxs-lookup"><span data-stu-id="95f74-126">Saving and Restoring DvdState Objects</span></span>](saving-and-restoring-dvdstate-objects.md)
-   [<span data-ttu-id="95f74-127">Utilizzo di stringhe di testo DVD</span><span class="sxs-lookup"><span data-stu-id="95f74-127">Working with DVD Text Strings</span></span>](working-with-dvd-text-strings.md)
-   [<span data-ttu-id="95f74-128">Riproduzione di flussi audio karaoke</span><span class="sxs-lookup"><span data-stu-id="95f74-128">Playing Karaoke Audio Streams</span></span>](playing-karaoke-audio-streams.md)
-   [<span data-ttu-id="95f74-129">Gestione delle espulsioni dei dischi</span><span class="sxs-lookup"><span data-stu-id="95f74-129">Handling Disc Ejections</span></span>](handling-disc-ejections.md)
-   [<span data-ttu-id="95f74-130">Miglioramenti della riproduzione DVD in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95f74-130">DVD Playback Enhancements in Windows Vista</span></span>](dvd-playback-enhancements-in-windows-vista.md)
-   [<span data-ttu-id="95f74-131">Configurazione del grafico del filtro DVD</span><span class="sxs-lookup"><span data-stu-id="95f74-131">DVD Filter Graph Configuration</span></span>](dvd-filter-graph-configuration.md)
-   [<span data-ttu-id="95f74-132">Collegamenti alle pagine di riferimento DVD di C++</span><span class="sxs-lookup"><span data-stu-id="95f74-132">Shortcuts to C++ DVD Reference Pages</span></span>](shortcuts-to-c-dvd-reference-pages.md)

<span data-ttu-id="95f74-133">Per informazioni sui riferimenti sullo sviluppo di decoder DVD/MPEG2, vedere [sviluppo di DVD decoder in DirectShow](dvd-decoder-development-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="95f74-133">For references on DVD/MPEG2 decoder development, see [DVD Decoder Development in DirectShow](dvd-decoder-development-in-directshow.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="95f74-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="95f74-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95f74-135">Uso di DirectShow</span><span class="sxs-lookup"><span data-stu-id="95f74-135">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



