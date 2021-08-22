---
description: Informazioni sui motori di rendering
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: Informazioni sui motori di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a398cbe342ed2e92fc23e7da034dd69cae492208e3201b3419b3999594a135
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664379"
---
# <a name="about-the-render-engines"></a>Informazioni sui motori di rendering

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Questo articolo descrive in che modo [DirectShow Servizi di](directshow-editing-services.md) modifica (DES) esegue il rendering di un progetto di modifica video.

In DES un progetto è rappresentato come sequenza temporale. La sequenza temporale è utile perché semplifica le attività più comuni nella modifica video, ad esempio la riorganizzazione delle clip sorgente e l'aggiunta di effetti video. L DirectShow di flusso, d'altra parte, richiede un grafico di filtro. Pertanto, per eseguire il rendering del progetto, è necessario convertire una sequenza temporale in un grafico di filtro. Il componente che esegue questa operazione è denominato motore *di rendering*. DirectShow fornisce due motori di rendering:

-   Motore di rendering di base: compila un grafo di filtro che fornisce output non compresso.
-   Motore di rendering intelligente: compila un grafo di filtro che fornisce l'output compresso.

Il motore di rendering intelligente usa la ricompressione intelligente per migliorare le prestazioni. Con la ricompressione intelligente, i file di origine vengono compressi nuovamente solo quando il formato del file originale è diverso dal formato di output finale. Se i formati corrispondono, l'origine non viene mai decompressa. La ricompressione intelligente è supportata solo per la compressione video, non per la compressione audio.

Per l'anteprima, usare il motore di rendering di base. Il motore di rendering intelligente può anche essere visualizzato in anteprima, ma meno efficiente perché deve decomprimere il flusso compresso. Per la scrittura di file, usare il motore di rendering intelligente se si vuole una ricompressione intelligente. In caso contrario, usare il motore di rendering di base. La ricompressione intelligente può ridurre notevolmente il tempo necessario per scrivere il file.

> [!IMPORTANT]
> Non usare il motore di rendering intelligente per leggere o scrivere Windows file multimediali.

 

> [!IMPORTANT]
> Entrambi i motori di rendering creano una finestra invisibile che elabora i messaggi. Il thread che crea il motore di rendering deve avere un ciclo di messaggi per inviare messaggi. Inoltre, tale thread non deve uscire fino a quando non vengono rilasciati il motore di rendering e Graph Gestione filtri. In caso contrario, l'applicazione potrebbe deadlock.

 

Costruzione del filtro Graph

Il grafico dei filtri è compilato in due fasi. Nella prima fase, il motore di rendering costruisce un "front-end", ovvero un grafico di filtro parziale. Il diagramma seguente illustra un front-end tipico:

![front-end del grafo di filtro](images/rendeng1.png)

I sottosistemi contengono vari filtri specializzati, assemblati automaticamente dal motore di rendering. Il front-end contiene un pin di output per ogni gruppo nella sequenza temporale. I pin di output forniscono dati non compressi se si usa il motore di rendering di base o dati compressi se si usa il motore di rendering intelligente.

Nel secondo passaggio, i pin di output sono connessi ai filtri di rendering. Per l'anteprima, i filtri di rendering sono renderer video e audio. Per la scrittura di file, i filtri di rendering sono filtri multiplexer (mux) e filtri di scrittura file.

![completamento del grafico dei filtri](images/rendeng2.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Anteprima di un Project](previewing-a-project.md)
</dt> <dt>

[Scrittura di Project in un file](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



