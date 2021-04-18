---
description: Durante il rendering, la pipeline interpola i dati dei vertici in ogni triangolo.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Interpolazione di triangolo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 405cbecd6123145d412a3e7f58f727bdf5b5a3e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304364"
---
# <a name="triangle-interpolation-direct3d-9"></a>Interpolazione di triangolo (Direct3D 9)

Durante il rendering, la pipeline interpola i dati dei vertici in ogni triangolo. I dati dei vertici possono essere un'ampia varietà di dati e possono includere (ma non limitati): il colore diffuso, il colore speculare, l'alfa diffusa (opacità del triangolo), l'alfa speculare e un fattore di nebbia (tratto da Alpha speculare per la pipeline Vertex della funzione fissa e dal registro di nebbia per la pipeline dei vertici programmabile). I dati dei vertici vengono definiti dalla [dichiarazione del vertice (Direct3D 9)](vertex-declaration.md).

Per alcuni dati dei vertici, l'interpolazione dipende dalla modalità di ombreggiatura corrente, come illustrato nella tabella seguente.



| Modalità ombreggiatura | Descrizione                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Semplice         | Solo il fattore di nebbia viene interpolato in modalità ombreggiatura piatta. Per tutti gli altri valori interpolati, il colore del primo vertice nel triangolo viene applicato nell'intero quadrante. |
| Gouraud      | L'interpolazione lineare viene eseguita tra tutti e tre i vertici.                                                                                                               |



 

Il colore e il colore speculare sono trattati in modo diverso, a seconda del modello colori. Nel modello di colore RGB, il sistema usa i componenti di colore rosso, verde e blu nell'interpolazione.

Il componente alfa di un colore viene considerato come un valore interpolato separato perché i driver di dispositivo possono implementare la trasparenza in due modi diversi: usando la combinazione di trame o l'uso di punteggiatura.

Usare il membro ShadeCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per determinare le forme di interpolazione supportate dal driver di dispositivo corrente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistemi di coordinate e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



