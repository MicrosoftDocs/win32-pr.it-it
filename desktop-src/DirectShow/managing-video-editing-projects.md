---
description: Gestione dei progetti di modifica video
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Gestione dei progetti di modifica video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491cfcb9a6e94874d2cae43567b61666bbd43cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303852"
---
# <a name="managing-video-editing-projects"></a>Gestione dei progetti di modifica video

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

I suggerimenti seguenti consentono di gestire i progetti in [servizi di modifica DirectShow](directshow-editing-services.md).

Modifiche alla sequenza temporale

-   Se si modifica la sequenza temporale dopo aver compilato il grafico del filtro, chiamare di nuovo [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) per ricompilare il front-end. In genere, ciò non influisce sul resto del grafo. In alcuni casi, tuttavia, il motore di rendering deve eliminare l'intero grafico prima di ricompilare il front-end. Questa situazione si verifica, ad esempio, se si aggiunge o si rimuove un gruppo. Il metodo **ConnectFrontEnd** restituisce \_ un avviso \_ OUTPUTRESET per segnalare che il grafo è stato eliminato. In tal caso, l'applicazione deve ricompilare la sezione di rendering del grafico.
-   Per rimuovere completamente tutti gli oggetti dalla sequenza temporale, chiamare il metodo [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md) .

**Pulizia**

-   Al termine dell'utilizzo di un motore di rendering, chiamare il metodo [**IRenderEngine:: ScrapIt**](irenderengine-scrapit.md) . Come per qualsiasi oggetto COM, assicurarsi di rilasciare ogni puntatore a interfaccia al termine dell'uso.
-   Il motore di rendering non mantiene un conteggio dei riferimenti nella sequenza temporale. Non rilasciare la sequenza temporale prima di procedere con l'uso e chiamare sempre **ScrapIt** sul motore di rendering.
-   Se si rilasciano tutti i riferimenti a una sequenza temporale, non usare alcuno degli oggetti in tale sequenza temporale, anche se sono presenti conteggi dei riferimenti su di essi.

**Più istanze della sequenza temporale**

-   Non spostare oggetti sequenza temporale tra sequenze temporali. Ogni oggetto in una sequenza temporale deve essere creato da tale sequenza temporale. La sequenza temporale include una cache interna con informazioni sugli oggetti creati; lo stato di avanzamento degli oggetti Timeline può compromettere la cache.
-   Non usare mai la stessa istanza di un motore di rendering con più di una sequenza temporale. Il motore di rendering include una cache con informazioni sulla sequenza temporale. Più sequenze temporali comprometteranno la cache e causeranno risultati imprevedibili. Se sono necessarie due sequenze temporali attive, creare istanze separate dei motori di rendering per ogni sequenza temporale.
-   Una sequenza temporale può usare più di un motore di rendering, ma non nello stesso momento. Eliminare il motore di rendering precedente prima di utilizzare un altro motore di rendering. Questa operazione viene eseguita in genere quando si passa dall'utilizzo del motore di rendering di base per l'anteprima al motore di rendering intelligente per la scrittura di file.

**Persistenza**

-   Il grafico del filtro non è permanente quando si salva il progetto in un file XML. Pertanto, si perderanno tutte le informazioni relative al ricompressione intelligente, al formato di compressione o ai parametri di compressione. Al termine del caricamento di un progetto, l'applicazione deve ripristinare questi parametri.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei servizi di modifica DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



