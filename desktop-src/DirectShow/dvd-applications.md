---
description: Applicazioni DVD
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: Applicazioni DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d601fdbf94ef2a2d9a70d1f28f68854200b58f9fb44d23c3738994f3001e3a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102961"
---
# <a name="dvd-applications"></a>Applicazioni DVD

DirectShow fornisce un componente denominato filtro di origine [dvd Navigator](dvd-navigator-filter.md) che semplifica le attività di navigazione dvd in C++. Lo strumento di navigazione DVD include tutte le funzionalità disponibili in un lettore DVD autonomo completo, oltre a funzionalità aggiuntive specifiche per la riproduzione di DVD nei personal computer. Usando lo strumento di navigazione DVD, gli sviluppatori C++ e di scripting possono creare applicazioni DVD complete senza fare riferimento alla specifica DVD. Lo strumento di navigazione DVD, in coordinamento con i filtri del decodificatore, gestisce anche la gestione a livello di area e la protezione del copyright (PROTEZIONE CSS e copia analoga), isolando gli sviluppatori di applicazioni da questi dettagli.

Il filtro DVD Navigator funziona in un intero volume DVD-Video, costituito dai file nella directory VIDEO \_ TS. A differenza DirectShow filtri di origine che funzionano con singoli flussi o file, lo strumento di navigazione DVD usa la struttura DVD-Video di titoli, capitoli e codici temporizzato. Gli sviluppatori che vogliono riprodurre singoli file MPEG-2 in DirectShow usare il [demultiplexer MPEG-2](mpeg-2-demultiplexer.md) anziché il filtro DVD Navigator. Per altre informazioni, vedere Supporto [MPEG-2 in DirectShow.](mpeg-2-support-in-directshow.md)

> [!Note]  
> Per riprodurre i DVD, l'utente deve avere un decodificatore MPEG-2.

 

In questa sezione vengono trattati gli argomenti seguenti.

-   [Funzionalità di supporto DVD in DirectShow](dvd-support-features-in-directshow.md)
-   [Nozioni di base su DVD](dvd-basics.md)
-   [Compilazione del filtro DVD Graph](building-the-dvd-filter-graph.md)
-   [Recupero dei puntatori di interfaccia DVD](obtaining-the-dvd-interface-pointers.md)
-   [Comandi DVD](dvd-commands.md)
-   [Identificazione di operazioni DVD valide](identifying-valid-dvd-operations.md)
-   [Sincronizzazione dei comandi DVD](synchronizing-dvd-commands.md)
-   [Dati Flow nello strumento di navigazione DVD](data-flow-in-the-dvd-navigator.md)
-   [Gestione delle notifiche degli eventi DVD](handling-dvd-event-notifications.md)
-   [Uso dei menu DVD](working-with-dvd-menus.md)
-   [Audio e immagini secondarie Flussi](audio-and-subpicture-streams.md)
-   [Applicazione dei livelli di gestione dei genitori](enforcing-parental-management-levels.md)
-   [Salvataggio e ripristino di oggetti DvdState](saving-and-restoring-dvdstate-objects.md)
-   [Uso di stringhe di testo DVD](working-with-dvd-text-strings.md)
-   [Riproduzione di contenuti audio per il Flussi](playing-karaoke-audio-streams.md)
-   [Gestione degli espulsioni di dischi](handling-disc-ejections.md)
-   [Miglioramenti della riproduzione di DVD in Windows Vista](dvd-playback-enhancements-in-windows-vista.md)
-   [Configurazione del filtro DVD Graph](dvd-filter-graph-configuration.md)
-   [Collegamenti alle pagine di riferimento dei DVD C++](shortcuts-to-c-dvd-reference-pages.md)

Per informazioni di riferimento sullo sviluppo di decodificatori DVD/MPEG2, vedere Sviluppo di decodificatori [DVD in DirectShow](dvd-decoder-development-in-directshow.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DirectShow](using-directshow.md)
</dt> </dl>

 

 



