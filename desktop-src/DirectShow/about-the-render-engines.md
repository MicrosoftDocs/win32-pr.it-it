---
description: Informazioni sui motori di rendering
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: Informazioni sui motori di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fe3a9956bee0d167de9e6618187bfd1f2a6e39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522234"
---
# <a name="about-the-render-engines"></a>Informazioni sui motori di rendering

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Questo articolo descrive come [DirectShow editing Services](directshow-editing-services.md) (des) esegue il rendering di un progetto di modifica video.

In DES un progetto viene rappresentato come sequenza temporale. La sequenza temporale è utile perché semplifica le attività più comuni nella modifica dei video, ad esempio la ridisposizione delle clip di origine e l'aggiunta di effetti video. L'architettura del flusso DirectShow, d'altra parte, richiede un grafico di filtro. Quindi, per eseguire il rendering del progetto, è necessario tradurre una sequenza temporale in un grafico a filtro. Il componente che esegue questa operazione è denominato *motore di rendering*. DirectShow fornisce due motori di rendering:

-   Motore di rendering di base: compila un grafico di filtro che recapita output non compresso.
-   Motore di rendering intelligente: compila un grafico di filtro che recapita l'output compresso.

Il motore di rendering intelligente utilizza la ricompressione intelligente per migliorare le prestazioni. Con la ricompressione intelligente, i file di origine vengono ricompressi solo quando il formato di file originale è diverso dal formato di output finale. Se i formati corrispondono, l'origine non viene mai decompressa. La ricompressione intelligente è supportata solo per la compressione video, non per la compressione audio.

Per l'anteprima, usare il motore di rendering di base. Il motore di rendering intelligente può anche essere visualizzato in anteprima, ma meno efficiente perché deve decomprimere il flusso compresso. Per la scrittura di file, usare il motore di rendering intelligente se si desidera la ricompressione intelligente. In caso contrario, usare il motore di rendering di base. La ricompressione intelligente può ridurre notevolmente il tempo necessario per la scrittura del file.

> [!IMPORTANT]
> Non usare il motore di rendering intelligente per leggere o scrivere file di Windows Media.

 

> [!IMPORTANT]
> Entrambi i motori di rendering creano una finestra invisibile che elabora i messaggi. Il thread che crea il motore di rendering deve disporre di un ciclo di messaggi per inviare i messaggi. Inoltre, il thread non deve uscire finché non vengono rilasciati il motore di rendering e il gestore del grafico dei filtri. In caso contrario, l'applicazione potrebbe verificarsi un deadlock.

 

Creazione del grafico di filtro

Il grafico a filtro è compilato in due fasi. Nella prima fase, il motore di rendering costruisce un "front-end", ovvero un grafico a filtro parziale. Il diagramma seguente illustra un tipico front-end:

![front-end del grafico filtro](images/rendeng1.png)

I sottosistemi contengono diversi filtri specializzati, che vengono assemblati automaticamente dal motore di rendering. Il front-end contiene un pin di output per ogni gruppo nella sequenza temporale. I pin di output restituiscono dati non compressi se si usa il motore di rendering di base o i dati compressi se si usa il motore di rendering intelligente.

Nel secondo passaggio, i pin di output sono connessi ai filtri di rendering. Per l'anteprima, i filtri di rendering sono renderer video e audio. Per la scrittura di file, i filtri di rendering sono filtri multiplexer (MUX) e filtri di file writer.

![completamento del grafico di filtro](images/rendeng2.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Visualizzazione in anteprima di un progetto](previewing-a-project.md)
</dt> <dt>

[Scrittura di un progetto in un file](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



