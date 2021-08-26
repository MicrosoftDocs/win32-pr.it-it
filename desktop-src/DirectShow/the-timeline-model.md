---
description: Modello di sequenza temporale
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: Modello di sequenza temporale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e5eeb60dce31fa466a518476bb3da341a3d2fda4fdeaa47ca58a89a904dded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903813"
---
# <a name="the-timeline-model"></a>Modello di sequenza temporale

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Una *sequenza temporale* è un oggetto che DirectShow Servizi [di](directshow-editing-services.md) modifica (DES) usa per rappresentare un progetto di modifica video. Un progetto di modifica viene avviato come raccolta di clip di origine, prese da file video, file audio o file di immagine. Una sequenza lineare di clip forma una *traccia*. In DirectShow Servizi di modifica (DES), audio e video vengono inseriti in tracce separate.

Le tracce possono anche essere su più livelli. Più tracce audio vengono miste e possono includere effetti audio, ad esempio dissolvenze o riverbero. Per creare transizioni vengono usate più tracce video. Ad esempio, è possibile creare una cancellazione da un clip a un altro. Un altro esempio è una chiave chroma, in cui lo sfondo di una clip viene ritagliato e sostituito da una traccia diversa. Il meteorografo davanti a un'immagine satelite è un esempio di keying della croma.

DES usa una struttura ad albero per rappresentare una modifica:

-   I clip audio e video formano i nodi foglia o gli *oggetti di* origine.
-   Una raccolta di origini con un tipo di supporto uniforme (audio o video) è una *traccia*.
-   Una raccolta di tracce è una *composizione*. Viene eseguito il rendering di una composizione come composito di tutte le tracce in essa contenute. Le composizioni possono contenere altre composizioni, che consentono una disposizione complessa delle tracce.
-   Una raccolta di primo livello di composizioni e tracce (tutte che rappresentano lo stesso tipo di supporto) è un *gruppo*.
-   Un set di uno o più gruppi forma una sequenza *temporale.* La sequenza temporale è il nodo radice nell'albero.

Una sequenza temporale deve contenere almeno un gruppo. Ogni gruppo rappresenta un singolo flusso nell'ambiente di produzione finale. Un progetto tipico include un gruppo di video e un gruppo audio. Le composizioni sono facoltative. esistono per fornire una maggiore struttura, se necessario.

La figura seguente mostra le relazioni padre-figlio che costituiscono una sequenza temporale:

![struttura del nodo](images/timeline1.png)

Di seguito viene illustrata una sequenza temporale come sequenza temporale:

![Illustrazione della sequenza temporale](images/timeline2.png)

La freccia nella parte superiore rappresenta la direzione della sequenza temporale, a partire dall'ora zero. All'interno del gruppo di video, la traccia 1 ha una priorità più alta rispetto alla traccia 0. Gli oggetti di origine nella traccia 1 oscurano quelli nella traccia 0. Dove la traccia 1 è vuota, la traccia 0 "mostra". Come accennato in precedenza, le tracce audio vengono semplicemente miste tra loro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con i DirectShow di modifica](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Costruzione di una sequenza temporale](constructing-a-timeline.md)
</dt> </dl>

 

 



