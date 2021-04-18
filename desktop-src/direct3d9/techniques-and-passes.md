---
description: Le tecniche forniscono il muscolo di rendering. Una tecnica incapsula lo stato dell'effetto che determina uno stile di rendering. Una tecnica è costituita da uno o più passaggi.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Tecniche e passaggi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3a68ac40db16b3e6819adf6fcd1f8a6f790325
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304374"
---
# <a name="techniques-and-passes-direct3d-9"></a>Tecniche e passaggi (Direct3D 9)

Le tecniche forniscono il muscolo di rendering. Una tecnica incapsula lo stato dell'effetto che determina uno stile di rendering. Una tecnica è costituita da uno o più passaggi.

## <a name="techniques"></a>Tecniche

La sintassi per la chiamata di una tecnica è la seguente:


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



Dove:

-   ID è un nome univoco facoltativo.
-   l'annotazione è zero o più parti facoltative delle informazioni specifiche dell'utente. Vedere [aggiungere informazioni ai parametri di effetto con le \_ annotazioni](using-an-effect.md).
-   i pass (es) sono pari a zero o più sessioni. Ogni sessione contiene le assegnazioni di stato. Vedere qui di seguito.

## <a name="passes"></a>Passa

Un passaggio contiene le assegnazioni di stato necessarie per il rendering.


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



Dove:

-   ID è un nome univoco facoltativo.
-   l'annotazione è una o più informazioni facoltative specifiche dell'utente. Vedere [aggiungere informazioni ai parametri di effetto con le \_ annotazioni](using-an-effect.md).
-   assegnazione/i assegna zero o più valori di stato oppure valuta una o più espressioni. Vedere [gli Stati degli effetti (Direct3D 9)](effect-states.md) ed [espressioni (Direct3D 9)](expressions.md).

Passa Ignora tutto tranne l'ultima assegnazione in un set di assegnazioni ripetute allo stesso stato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



