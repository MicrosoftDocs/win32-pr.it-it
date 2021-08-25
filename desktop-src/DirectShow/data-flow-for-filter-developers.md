---
description: Dati Flow per sviluppatori di filtri
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Dati Flow per sviluppatori di filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ced9507856d7a6b8aea2acaea86c20b393b8d937ab4427bf522596a29ba690
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749371"
---
# <a name="data-flow-for-filter-developers"></a>Dati Flow per sviluppatori di filtri

Questa sezione descrive in dettaglio lo spostamento dei dati nel grafico dei filtri. Si concentra sul trasporto di memoria locale usando [**l'interfaccia IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) o [**IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) È destinato agli sviluppatori che scrivono filtri personalizzati. Per un'introduzione generale al modo in cui Microsoft DirectShow gestisce il flusso di dati, vedere [Data Flow in Filter Graph](data-flow-in-the-filter-graph.md).

Molti dati si spostano attraverso un grafico di filtro. Rientra approssimativamente in due categorie: dati multimediali e dati di controllo. In generale, i dati multimediali viaggiano a valle e i dati di controllo viaggiano a monte. I dati multimediali includono fotogrammi video, campioni audio, pacchetti MPEG e così via che costituiscono un flusso, ma includono anche comandi di scaricamento, notifiche di fine flusso e altri dati che viaggiano con il flusso. I dati di controllo non fanno parte del flusso multimediale. Esempi di dati di controllo sono le richieste di controllo qualità e i comandi di ricerca.

Questa sezione contiene gli articoli seguenti.

-   [Distribuzione di esempi](delivering-samples.md)
-   [Elaborazione dei dati](processing-data.md)
-   [Notifiche di fine flusso](end-of-stream-notifications.md)
-   [Nuovi segmenti](new-segments.md)
-   [Flushing](flushing.md)
-   [riercare](seeking.md)
-   [Modifiche al formato dinamico](dynamic-format-changes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione del controllo di qualità](quality-control-management.md)
</dt> <dt>

[Thread e sezioni critiche](threads-and-critical-sections.md)
</dt> <dt>

[Scrittura DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



