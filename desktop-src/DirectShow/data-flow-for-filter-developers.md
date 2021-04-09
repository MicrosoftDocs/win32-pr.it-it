---
description: Flusso di dati per sviluppatori di filtri
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Flusso di dati per sviluppatori di filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb4e4123e8617190a459ff500d1100c0dbbb8ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049054"
---
# <a name="data-flow-for-filter-developers"></a>Flusso di dati per sviluppatori di filtri

In questa sezione viene descritto in dettaglio il modo in cui i dati vengono spostati attraverso il grafico dei filtri. Si concentra sul trasporto di memoria locale usando l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) o [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . È destinato agli sviluppatori che scrivono filtri personalizzati. Per un'introduzione generale al modo in cui Microsoft DirectShow gestisce il flusso di dati, vedere [flusso di dati nel grafico del filtro](data-flow-in-the-filter-graph.md).

Una grande quantità di dati viene spostata attraverso un grafico a filtro. Rientra approssimativamente in due categorie: dati multimediali e dati di controllo. In generale, i dati multimediali viaggiano a valle e i dati di controllo viaggiano a Monte. I dati multimediali includono i fotogrammi video, gli esempi audio, i pacchetti MPEG e così via che costituiscono un flusso, ma includono anche comandi di scaricamento, notifiche di fine flusso e altri dati che viaggiano con il flusso. I dati del controllo non fanno parte del flusso multimediale. Esempi di dati di controllo sono richieste di controllo della qualità e comandi di ricerca.

Questa sezione contiene gli articoli seguenti.

-   [Distribuzione di esempi](delivering-samples.md)
-   [Elaborazione dei dati](processing-data.md)
-   [Notifiche di fine flusso](end-of-stream-notifications.md)
-   [Nuovi segmenti](new-segments.md)
-   [Flushing](flushing.md)
-   [La ricerca](seeking.md)
-   [Modifiche al formato dinamico](dynamic-format-changes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione controllo qualità](quality-control-management.md)
</dt> <dt>

[Thread e sezioni critiche](threads-and-critical-sections.md)
</dt> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



