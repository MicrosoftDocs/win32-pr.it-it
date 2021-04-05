---
title: Origine dell'immagine terziaria push
description: Origine dell'immagine terziaria push
ms.assetid: e2d41729-87c5-4cec-931c-8702585930f2
keywords:
- Windows Media Player Mobile Skin, origine immagine pulsante
- interfacce, origine immagine pulsante
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, origine immagine
- origine immagine per interfacce, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a37f79ab3c5fbf02eed1f0a02219a517b12ce1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955495"
---
# <a name="pushed-tertiary-image-source"></a>Origine dell'immagine terziaria push

Per la funzione del pulsante PlayPauseStop è necessario definire il percorso dell'immagine push per lo stato terziario del pulsante. Si tratta dell'immagine visualizzata dagli utenti quando eseguono il push del pulsante PlayPauseStop durante lo streaming di una trasmissione live.

Per definire questa immagine, è necessario immettere il tipo di immagine seguito da uno spazio e dal simbolo @ e da un altro spazio. È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine che si vuole usare all'interno del tipo di bitmap da cui si sta disegnando.

Ad esempio, per definire l'immagine push per un'origine di un'immagine terziaria, se l'immagine si trova all'interno della bitmap di cui è stato eseguito il push, digitare:


```C++
Pushed @ 324,0

```



Gli Stati terziari non possono avere un'immagine disabilitata. Si presuppone che le immagini terziarie siano della stessa larghezza e altezza delle immagini primarie e secondarie.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Pulsanti**](buttons.md)
</dt> </dl>

 

 




