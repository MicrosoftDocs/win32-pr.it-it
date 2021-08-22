---
description: Le tecniche forniscono il motore di rendering. Una tecnica incapsula lo stato dell'effetto che determina uno stile di rendering. Una tecnica è costituito da uno o più passaggi.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Tecniche e passaggi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9999927d96a914b80f870a2128b0eae12074616e4ae787b011551b6aab919220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044209"
---
# <a name="techniques-and-passes-direct3d-9"></a>Tecniche e passaggi (Direct3D 9)

Le tecniche forniscono il motore di rendering. Una tecnica incapsula lo stato dell'effetto che determina uno stile di rendering. Una tecnica è costituito da uno o più passaggi.

## <a name="techniques"></a>Tecniche

La sintassi per chiamare una tecnica è la seguente:


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



Dove:

-   id è un nome univoco facoltativo.
-   annotation è zero o più parti facoltative di informazioni specifiche dell'utente. Vedere [Aggiungere informazioni ai parametri degli effetti con \_ annotazioni](using-an-effect.md).
-   pass(es) è zero o più passaggi. Ogni passaggio contiene assegnazioni di stato. Vedere qui di seguito.

## <a name="passes"></a>Passa

Un passaggio contiene le assegnazioni di stato necessarie per il rendering.


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



Dove:

-   id è un nome univoco facoltativo.
-   annotation è una o più informazioni facoltative specifiche dell'utente. Vedere [Aggiungere informazioni ai parametri degli effetti con \_ annotazioni](using-an-effect.md).
-   assignment(s) assegna zero o più valori di stato o valuta una o più espressioni. Vedere [Stati degli effetti (Direct3D 9)](effect-states.md) ed Espressioni [(Direct3D 9).](expressions.md)

I passaggi ignorano tutti, ma l'ultima assegnazione in un set di assegnazioni ripetute allo stesso stato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



