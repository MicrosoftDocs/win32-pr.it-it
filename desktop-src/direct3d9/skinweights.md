---
description: Viene creata un'istanza di questo modello in base alla rete.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: SkinWeights
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759239a3a7ec8ebb608cf9ede6624105cee321b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520882"
---
# <a name="skinweights"></a>SkinWeights

Viene creata un'istanza di questo modello in base alla rete. All'interno di una mesh, viene visualizzata una sequenza di n istanze di questo modello, dove n è il numero di ossa (X file frame) che influenzano i vertici nella rete. Ogni istanza del modello definisce fondamentalmente l'influenza di un particolare osso sulla rete. È presente un elenco di indici dei vertici e un elenco corrispondente di pesi.

``` syntax
template SkinWeights 
{ 
    < 6F0D123B-BAD2-4167-A0D0-80224F25FABB > 
    STRING transformNodeName; 
    DWORD nWeights; 
    array DWORD vertexIndices[nWeights]; 
    array float weights[nWeights]; 
    Matrix4x4 matrixOffset; 
} 
```

Dove:

-   Il nome dell'osso la cui influenza viene definita è transformNodeName e nWeights è il numero di vertici interessati da questo osso.
-   I vertici influenzati da questo osso sono contenuti in vertexIndices e i pesi per ogni vertice influenzato da questo osso sono contenuti in pesi.
-   La matrice matrixOffset trasforma i vertici della mesh nello spazio dell'osso. Una volta concatenato alla trasformazione dell'osso, fornisce le coordinate dello spazio globale della mesh interessate dall'osso. Vedere [**Matrix4x4**](matrix4x4.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



