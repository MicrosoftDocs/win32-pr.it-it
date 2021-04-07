---
description: È possibile utilizzare Microsoft Direct3D per simulare fenomeni naturali che coinvolgono le versioni di energia.
ms.assetid: a16af13d-3a38-42b5-900b-ff58a0c917b2
title: Incendi, flare ed esplosioni (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708730bd8e5f198664bb20c11fa98243ac98f0d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745567"
---
# <a name="fire-flares-and-explosions-direct3d-9"></a>Incendi, flare ed esplosioni (Direct3D 9)

È possibile utilizzare Microsoft Direct3D per simulare fenomeni naturali che coinvolgono le versioni di energia. Ad esempio, un'applicazione può generare l'aspetto di Fire applicando trame simili a una serie di tabelloni. Questa operazione è particolarmente efficace se l'applicazione usa una sequenza di trame di attivazione per animare le fiamme in ogni Billboard nell'incendio. La variazione della velocità della riproduzione dell'animazione da Billboard a Billboard aumenta l'aspetto delle fiamme reali. La somiglianza delle fiamme 3D interfondete può essere realizzata attraverso la sovrapposizione dei cartelloni e delle trame sui tabelloni.

È possibile simulare i bagliori e i flash applicando le mappe più luminose successivamente a tutte le primitive in una scena. Sebbene si tratta di una tecnica a sovraccarico elevato a livello di calcolo, consente all'applicazione di simulare un flare o un flash localizzato. Ovvero la parte della scena in cui ha origine il bagliore o il flash può illuminare prima.

Un'altra tecnica consiste nel posizionare un tabellone davanti alla scena in modo da coprire l'intera area di destinazione del rendering. L'applicazione viene applicata in successione di trame più bianche al tabellone e riduce la trasparenza nel tempo. L'intera scena si dissolve in bianco quando il tempo passa. Si tratta di un metodo con sovraccarico basso per la creazione di un flare. Tuttavia, usando questa tecnica, può essere difficile generare l'aspetto di un flash luminoso da un'unica fonte di luce puntiforme.

Le esplosioni possono essere visualizzate in una procedura di scena 3D simile a quelle usate per l'attivazione, il lampeggio e i flare. Ad esempio, è possibile che l'applicazione utilizzi un tabellone per visualizzare un'onda d'urto e un pennacchio di fumo quando si verifica l'esplosione. Allo stesso tempo, l'applicazione può usare un set di cartelloni per simulare le fiamme. Inoltre, può posizionare un singolo tabellone davanti alla scena per aggiungere un chiaro all'intera scena.

È possibile simulare i raggi di energia usando i tabelloni. L'applicazione può anche visualizzarli usando le primitive definite come elenchi di righe o strisce. Per informazioni dettagliate, vedere [elenchi di linee](line-lists.md) e strisce di [riga](line-strips.md).

L'applicazione può creare campi Force usando tabelloni o primitivi definiti come elenchi di triangolo. Per creare un campo Force dagli elenchi di triangolo, definire un set di triangoli non contigui in un elenco di triangoli equidistanti in base all'area coperta dal campo Force. I gap tra i triangoli consentono all'utente di visualizzare la scena dietro i triangoli, come si può immaginare quando si esamina un campo forzato. Applicare una trama all'elenco di triangolo che fornisce ai triangoli l'aspetto dell'alone con energia. Per ulteriori informazioni, vedere la pagina relativa agli [elenchi di triangolo](triangle-lists.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Alpha](alpha-examples.md)
</dt> </dl>

 

 



