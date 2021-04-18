---
description: Modello di sequenza temporale
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: Modello di sequenza temporale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac01f90e8ca827bde41f2ad36e1ab32b3d429437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104549802"
---
# <a name="the-timeline-model"></a>Modello di sequenza temporale

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Una *sequenza temporale* è un oggetto usato da [DirectShow editing Services](directshow-editing-services.md) (des) per rappresentare un progetto di modifica video. Un progetto di modifica viene avviato come raccolta di clip di origine, estratti da file video, file audio o file di immagine ancora. Una sequenza lineare di clip costituisce una *traccia*. In DirectShow editing Services (DES), audio e video vengono posizionati in tracce separate.

Le tracce possono anche essere sovrapposte. Più tracce audio vengono combinate insieme e possono includere effetti audio, ad esempio Fades o Reverb. Per la creazione di transizioni vengono usate più tracce video. Ad esempio, è possibile creare una cancellazione da un clip a un altro. Un altro esempio è una chiave Chroma, in cui lo sfondo di una clip viene dismesso e sostituito da un'altra traccia. (Il Forecaster Meteo davanti a un'immagine satellite è un esempio di chiave Chroma).

DES usa una struttura ad albero per rappresentare una modifica:

-   I clip audio e video formano i nodi foglia o gli oggetti di *origine* .
-   Una raccolta di origini con un tipo di supporto uniforme (audio o video) è una *traccia*.
-   Una raccolta di tracce è una *composizione*. Viene eseguito il rendering di una composizione come composto di tutte le tracce in esso contenute. Le composizioni possono contenere altre composizioni, che consentono di organizzare in modo complesso le tracce.
-   Una raccolta di livello superiore di composizioni e tracce (tutti che rappresentano lo stesso tipo di supporto) è un *gruppo*.
-   Un set di uno o più gruppi costituisce una *sequenza temporale*. La sequenza temporale è il nodo radice nell'albero.

Una sequenza temporale deve contenere almeno un gruppo. Ogni gruppo rappresenta un singolo flusso nell'ambiente di produzione finale. Un progetto tipico include un gruppo video e un gruppo audio. Le composizioni sono facoltative; esistono per fornire una maggiore struttura, se necessario.

Nella figura seguente sono illustrate le relazioni padre-figlio che costituiscono una sequenza temporale:

![struttura del nodo](images/timeline1.png)

Di seguito viene illustrata una sequenza temporale come sequenza temporale:

![illustrazione della sequenza temporale](images/timeline2.png)

La freccia nella parte superiore rappresenta la direzione della sequenza temporale, a partire dal tempo zero. All'interno del gruppo video, Track 1 ha una priorità più alta rispetto a Track 0. Gli oggetti di origine in Track 1 nascondono quelli nella traccia 0. Dove Track 1 è vuoto, Track 0 "shows through". Come indicato in precedenza, le tracce audio sono semplicemente combinate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con i servizi di modifica DirectShow](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Creazione di una sequenza temporale](constructing-a-timeline.md)
</dt> </dl>

 

 



