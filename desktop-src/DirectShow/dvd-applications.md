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
# <a name="dvd-applications"></a>Applicazioni DVD

DirectShow fornisce un componente denominato [DVD Navigator](dvd-navigator-filter.md) Source Filter, che semplifica le attività di navigazione su DVD in C++. Il navigatore DVD offre tutte le funzionalità disponibili in un lettore DVD autonomo con funzionalità complete, oltre a funzionalità aggiuntive specifiche per la riproduzione di DVD su personal computer. Grazie a DVD Navigator, gli sviluppatori di script e C++ possono creare applicazioni DVD con funzionalità complete senza fare riferimento alla specifica DVD. Il navigatore DVD, in coordinamento con i filtri del decodificatore, gestisce anche la gestione e la protezione del copyright (CSS e protezione della copia analoga), isolando gli sviluppatori di applicazioni da questi dettagli.

Il filtro per lo strumento di spostamento DVD funziona in un intero volume di DVD-Video, costituito dai file nella \_ directory di Servizi terminal video. Diversamente dalla maggior parte dei filtri origine DirectShow che funzionano con singoli flussi o file, il navigatore DVD usa la struttura DVD-Video di titoli, capitoli e codici temporali. Gli sviluppatori che desiderano riprodurre singoli file MPEG-2 in DirectShow devono usare il [Demultiplexer MPEG-2](mpeg-2-demultiplexer.md) anziché il filtro del navigatore DVD. Per ulteriori informazioni, vedere [supporto MPEG-2 in DirectShow](mpeg-2-support-in-directshow.md) .

> [!Note]  
> Per riprodurre DVD, l'utente deve disporre di un decodificatore MPEG-2.

 

In questa sezione vengono trattati gli argomenti seguenti.

-   [Funzionalità di supporto DVD in DirectShow](dvd-support-features-in-directshow.md)
-   [Nozioni fondamentali sui DVD](dvd-basics.md)
-   [Creazione del grafico del filtro DVD](building-the-dvd-filter-graph.md)
-   [Acquisizione dei puntatori dell'interfaccia DVD](obtaining-the-dvd-interface-pointers.md)
-   [Comandi DVD](dvd-commands.md)
-   [Identificazione di operazioni DVD valide](identifying-valid-dvd-operations.md)
-   [Sincronizzazione dei comandi DVD](synchronizing-dvd-commands.md)
-   [Flusso di dati nel navigatore DVD](data-flow-in-the-dvd-navigator.md)
-   [Gestione delle notifiche degli eventi DVD](handling-dvd-event-notifications.md)
-   [Uso dei menu DVD](working-with-dvd-menus.md)
-   [Flussi audio e immagine subimmagini](audio-and-subpicture-streams.md)
-   [Applicazione dei livelli di gestione padre](enforcing-parental-management-levels.md)
-   [Salvataggio e ripristino di oggetti DvdState](saving-and-restoring-dvdstate-objects.md)
-   [Utilizzo di stringhe di testo DVD](working-with-dvd-text-strings.md)
-   [Riproduzione di flussi audio karaoke](playing-karaoke-audio-streams.md)
-   [Gestione delle espulsioni dei dischi](handling-disc-ejections.md)
-   [Miglioramenti della riproduzione DVD in Windows Vista](dvd-playback-enhancements-in-windows-vista.md)
-   [Configurazione del grafico del filtro DVD](dvd-filter-graph-configuration.md)
-   [Collegamenti alle pagine di riferimento DVD di C++](shortcuts-to-c-dvd-reference-pages.md)

Per informazioni sui riferimenti sullo sviluppo di decoder DVD/MPEG2, vedere [sviluppo di DVD decoder in DirectShow](dvd-decoder-development-in-directshow.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DirectShow](using-directshow.md)
</dt> </dl>

 

 



