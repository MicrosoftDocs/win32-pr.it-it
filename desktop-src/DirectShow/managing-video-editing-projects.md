---
description: Gestione dei progetti di modifica video
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Gestione dei progetti di modifica video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe226f4fdc43889daac8e978086c67bd81c5d8d822902e7c041bf500f2836fb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584451"
---
# <a name="managing-video-editing-projects"></a>Gestione dei progetti di modifica video

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

I suggerimenti seguenti consentono di gestire i progetti in [DirectShow Servizi di modifica](directshow-editing-services.md).

Modifiche alla sequenza temporale

-   Se si modifica la sequenza temporale dopo aver compilato il grafico dei filtri, chiamare di nuovo [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) per ricompilare il front-end. In genere, ciò non influisce sul resto del grafico. In alcuni casi, tuttavia, il motore di rendering deve eliminare l'intero grafico prima di ricompilare il front-end. Ad esempio, ciò si verifica se si aggiunge o si rimuove un gruppo. Il **metodo ConnectFrontEnd** restituisce S \_ WARN \_ OUTPUTRESET per segnalare l'eliminazione del grafico. In questo caso, l'applicazione deve ricompilare la sezione di rendering del grafo.
-   Per rimuovere completamente tutti gli oggetti dalla sequenza temporale, chiamare il [**metodo IAMTimeline::ClearAllGroups.**](iamtimeline-clearallgroups.md)

**Pulizia**

-   Dopo aver terminato di usare un motore di rendering, chiamare il [**metodo IRenderEngine::ScrapIt.**](irenderengine-scrapit.md) Come per qualsiasi oggetto COM, assicurarsi di rilasciare ogni puntatore di interfaccia al termine dell'uso.
-   Il motore di rendering non mantiene un conteggio dei riferimenti nella sequenza temporale. Non rilasciare la sequenza temporale prima di aver finito di usarla e chiamare **sempre ScrapIt** prima sul motore di rendering.
-   Se si rilasciano tutti i riferimenti a una sequenza temporale, non usare alcuno degli oggetti in tale sequenza temporale, anche se sono presenti conteggi dei riferimenti su di essi.

**Più istanze della sequenza temporale**

-   Non spostare gli oggetti sequenza temporale tra le sequenze temporali. Ogni oggetto in una sequenza temporale deve essere creato da tale sequenza temporale. La sequenza temporale contiene una cache interna con informazioni sugli oggetti creati. lo spostamento di oggetti della sequenza temporale può interrompere la cache.
-   Non usare mai la stessa istanza di un motore di rendering con più di una sequenza temporale. Il motore di rendering contiene una cache con informazioni sulla sequenza temporale. Più sequenze temporali interromperanno la cache e causeranno risultati imprevedibili. Se sono necessarie due sequenze temporali attive, creare istanze separate dei motori di rendering per ogni sequenza temporale.
-   Una sequenza temporale può usare più motori di rendering, ma non contemporaneamente. Eliminare il motore di rendering precedente prima di usare un altro motore di rendering. Questa operazione viene in genere eseguito quando si passa dall'uso del motore di rendering di base per l'anteprima al motore di rendering intelligente per la scrittura di file.

**Persistenza**

-   Il grafico dei filtri non è persistente quando si salva il progetto in un file XML. Di conseguenza, si perdono tutte le informazioni relative alla ricocompressione intelligente, al formato di compressione o ai parametri di compressione. È l'applicazione a ripristinare questi parametri dopo il caricamento di un progetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DirectShow di modifica](using-directshow-editing-services.md)
</dt> </dl>

 

 



