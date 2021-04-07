---
description: Viene creata un'istanza di questo modello in base a mesh, che contiene informazioni sui vertici della mesh che sono duplicati l'uno dall'altro.
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdjacency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2fd0f0b2bb328aa8b5ec39e7481c0b7fd766fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745570"
---
# <a name="faceadjacency"></a>FaceAdjacency

Viene creata un'istanza di questo modello in base a mesh, che contiene informazioni sui vertici della mesh che sono duplicati l'uno dall'altro. Il risultato viene duplicato quando un vertice si trova su un gruppo o un limite di materiale smussato. Lo scopo di questo modello è quello di consentire al caricatore di determinare i vertici che presentano parametri periferici diversi, in realtà gli stessi vertici del modello. Alcune applicazioni (ad esempio, la semplificazione della rete) possono usare queste informazioni.

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

Dove:

-   nIndices: numero di indici nella rete.
-   indici \[ nIndices \] -matrice di indici.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



