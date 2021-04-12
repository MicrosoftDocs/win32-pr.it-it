---
description: Tecniche di Graph-Building generali
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: Tecniche di Graph-Building generali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225319"
---
# <a name="general-graph-building-techniques"></a>Tecniche di Graph-Building generali

Ogni applicazione DirectShow inizia con la creazione di un grafico a filtro. Quando si leggono gli argomenti della panoramica nella documentazione di DirectShow, si noterà che la maggior parte dei casi descrive il tipo di grafico filtro necessario. In alcuni casi, è disponibile un metodo o un oggetto helper appositamente progettato per la compilazione di questo tipo di grafico. Ad esempio, l'oggetto [Generatore di DVD Graph](dvd-graph-builder.md) compila i grafici di riproduzione DVD. In altri casi, l'applicazione deve creare il grafico aggiungendo filtri e connetterli.

In questa sezione vengono presentate alcune funzioni helper che implementano operazioni di base per la creazione di grafici. Possono essere usati da qualsiasi applicazione DirectShow che deve compilare o modificare un grafico di filtro. Questa sezione contiene i seguenti argomenti:

-   [Aggiungere un filtro in base al CLSID](add-a-filter-by-clsid.md)
-   [Trovare un PIN non connesso in un filtro](find-an-unconnected-pin-on-a-filter.md)
-   [Connetti due filtri](connect-two-filters.md)
-   [Trovare un'interfaccia su un filtro o un pin](find-an-interface-on-a-filter-or-pin.md)
-   [Trovare il peer di un filtro](find-a-filters-peer.md)
-   [Rimuovere tutti i filtri nel grafico](remove-all-the-filters-in-the-graph.md)
-   [Creazione di grafici con il generatore di grafici di acquisizione](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività DirectShow di base](basic-directshow-tasks.md)
</dt> <dt>

[Enumerazione dei dispositivi e dei filtri](enumerating-devices-and-filters.md)
</dt> <dt>

[Enumerazione di oggetti in un grafico di filtro](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Connessione intelligente](intelligent-connect.md)
</dt> </dl>

 

 



