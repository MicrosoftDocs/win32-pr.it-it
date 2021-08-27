---
description: Definisce una patch di controllo&\# B 233;zier. La matrice definisce i punti di controllo per la patch.
ms.assetid: vs|directx_sdk|~\patch.htm
title: Patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f57ac0cec68a1e8d1651c0e6ad2aabde6f1f6b949b085aa0dc35bd6e02c82a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118632"
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

-   nControlIndices: numero di indici del punto di controllo.
-   array DWORD controlIndices \[ nControlIndices \] : matrice di indici del punto di controllo.

Il tipo di patch è definito dal numero di punti di controllo, come illustrato nella tabella seguente.



| Numero di punti di controllo | Tipo                              |
|--------------------------|-----------------------------------|
| 10                       | Patch triangolare di Bézier cubica     |
| 15                       | Patch triangolare di Quartic Bézier   |
| 16                       | Patch rettangolo quad di Bézier cubica |



 

L'ordine dei punti di controllo è indicato in un modello di blocco, come illustrato nei diagrammi seguenti per le patch triangolari e rettangolari.

Le patch triangolari usano il modello seguente.

![Diagramma del modello per le patch triangolari](images/tripatch.png)

Le patch rettangolari usano il modello seguente.

![Diagramma del modello per le patch rettangolari](images/quadpatch.png)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



