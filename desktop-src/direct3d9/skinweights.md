---
description: Viene creata un'istanza di questo modello per ogni mesh.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: SkinWeights
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bb76b1c0860e64f2e1e8b42cb7ed4d2af984cc043425b97e03cf997714d0e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627911"
---
# <a name="skinweights"></a>SkinWeights

Viene creata un'istanza di questo modello per ogni mesh. All'interno di una mesh verrà visualizzata una sequenza di n istanze di questo modello, dove n è il numero di elementi (frame di file X) che influenzano i vertici nella mesh. Ogni istanza del modello definisce fondamentalmente l'influenza di un particolare elemento nella mesh. È disponibile un elenco di indici dei vertici e un elenco corrispondente di pesi.

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

-   Il nome dell'ente di cui viene definita l'influenza è transformNodeName e nWeights è il numero di vertici interessati da questo gruppo.
-   I vertici influenzati da questo vertice sono contenuti in vertexIndices e i pesi per ognuno dei vertici influenzati da questo vertice sono contenuti in pesi.
-   La matrice matrixOffset trasforma i vertici della mesh nello spazio dell'oggetto . In caso di concatenazione alla trasformazione del campione, questo fornisce le coordinate dello spazio del mondo della mesh interessate dall'affondo. Vedere [**Matrix4x4.**](matrix4x4.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



