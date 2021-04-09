---
description: Definisce una patch di \# controllo Zier B&233;. La matrice definisce i punti di controllo per la patch.
ms.assetid: vs|directx_sdk|~\patch.htm
title: Patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480457b3dd3800aca8b23210e3fe653b4e713e94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875966"
---
# <a name="patch"></a>Patch

Definisce una patch di controllo di Bézier. La matrice definisce i punti di controllo per la patch.

``` syntax
template Patch
{
    < A3EB5D44-FC22-429D-9AFB-3221CB9719A6 >
    DWORD nControlIndices;
    array DWORD controlIndices[nControlIndices];
} 
```

Dove:

-   nControlIndices: numero di indici dei punti di controllo.
-   Array DWORD controlIndices \[ nControlIndices \] -matrice di indici di punti di controllo.

Il tipo di patch è definito dal numero di punti di controllo, come illustrato nella tabella seguente.



| Numero di punti di controllo | Tipo                              |
|--------------------------|-----------------------------------|
| 10                       | Patch triangolare Bézier cubica     |
| 15                       | Patch triangolare Béziers quartica   |
| 16                       | Patch rettangolare di Bézier a cubi quadre |



 

L'ordine dei punti di controllo viene fornito in un modello a spirale, come illustrato nei diagrammi seguenti per le patch triangolari e rettangolari.

Le patch triangolari usano il modello seguente.

![diagramma del modello per le patch triangolari](images/tripatch.png)

Le patch rettangolari usano il modello seguente.

![diagramma del modello per le patch rettangolari](images/quadpatch.png)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



