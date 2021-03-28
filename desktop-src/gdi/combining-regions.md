---
description: Un'applicazione combina due aree chiamando la funzione CombineRgn.
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: Combinazione di aree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51db22daea448acfb02120844ca2859a5ba11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566839"
---
# <a name="combining-regions"></a>Combinazione di aree

Un'applicazione combina due aree chiamando la funzione [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) . Utilizzando questa funzione, un'applicazione può combinare le parti intersecanti di due aree, tutte tranne le parti intersecanti di due aree, le due aree originali e così via. Di seguito sono riportati cinque valori che definiscono le combinazioni di aree.



| Valore     | Significato                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| RGN \_ e  | Le parti che intersecano due aree originali definiscono una nuova regione.                   |
| copia di RGN \_ | Una copia della prima (delle due aree originali) definisce una nuova area.               |
| \_diff RGN | La parte della prima area che non interseca la seconda definisce una nuova area. |
| RGN \_ o   | Le due aree originali definiscono una nuova area.                                         |
| \_Xor RGN  | Le parti delle due aree originali che non si sovrappongono definiscono una nuova area.      |



 

Nella figura seguente sono illustrate le cinque combinazioni possibili di un quadrato e di un'area circolare risultante da una chiamata a [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).

![illustrazione che illustra i risultati descritti nella tabella precedente](images/csrgn-02.png)

 

 



