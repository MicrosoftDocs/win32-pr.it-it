---
description: Viene creata un'istanza di questo modello in base a mesh, che contiene informazioni sui vertici della mesh che sono duplicati l'uno dall'altro.
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d62278c206032c9a2dfed6ce9b2cd36c5e7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303673"
---
# <a name="vertexduplicationindices"></a>VertexDuplicationIndices

Viene creata un'istanza di questo modello in base a mesh, che contiene informazioni sui vertici della mesh che sono duplicati l'uno dall'altro. Il risultato viene duplicato quando un vertice si trova su un gruppo o un limite di materiale smussato. Lo scopo di questo modello è quello di consentire al caricatore di determinare i vertici che presentano parametri periferici diversi, in realtà gli stessi vertici del modello. Alcune applicazioni (ad esempio, la semplificazione della rete) possono usare queste informazioni.

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

Dove:

-   nIndices: numero di indici dei vertici. Il numero di vertici nella rete.
-   nOriginalVertices: numero di vertici nella mesh prima che si verifichi la duplicazione.
-   Gli indici di valore \[ n \] contengono l'indice dei vertici \[ per il vertice n \] nella matrice di vertici per la mesh se non si sono verificate duplicazioni. Gli indici in questa matrice, pertanto, indicano i vertici duplicati.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



