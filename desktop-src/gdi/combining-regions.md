---
description: Un'applicazione combina due aree chiamando la funzione CombineRgn.
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: Combinazione di aree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6550f260a70bc0f49e6b181f9e1c82a64ce4eadbe643214362444d0dcbfccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887521"
---
# <a name="combining-regions"></a>Combinazione di aree

Un'applicazione combina due aree chiamando la [**funzione CombineRgn.**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) Usando questa funzione, un'applicazione può combinare le parti intersecate di due aree, tutte le parti che si intersecano di due aree, le due aree originali nella loro interezza e così via. Di seguito sono riportati cinque valori che definiscono le combinazioni di aree.



| Valore     | Significato                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| RGN \_ AND  | Le parti intersecate di due aree originali definiscono una nuova area.                   |
| RGN \_ COPY | Una copia della prima (delle due aree originali) definisce una nuova area.               |
| RGN \_ DIFF | La parte della prima area che non interseca la seconda definisce una nuova area. |
| RGN \_ OR   | Le due aree originali definiscono una nuova area.                                         |
| RGN \_ XOR  | Le parti delle due aree originali che non si sovrappongono definiscono una nuova area.      |



 

La figura seguente illustra le cinque possibili combinazioni di un quadrato e di un'area circolare risultanti da una chiamata a [**CombineRgn.**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn)

![illustrazione che illustra i risultati descritti nella tabella precedente](images/csrgn-02.png)

 

 



