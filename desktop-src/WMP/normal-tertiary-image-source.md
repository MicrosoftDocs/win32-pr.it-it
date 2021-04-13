---
title: Origine normale dell'immagine terziaria
description: Origine normale dell'immagine terziaria
ms.assetid: ce0b009a-b008-4e8b-875b-b2ff3c1c0b81
keywords:
- Windows Media Player Mobile Skin, origine immagine pulsante
- interfacce, origine immagine pulsante
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, origine immagine
- origine immagine per interfacce, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109509914c498e950f148caf7c260ef814c1074f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396570"
---
# <a name="normal-tertiary-image-source"></a>Origine normale dell'immagine terziaria

Per la funzione del pulsante PlayPauseStop è necessario definire il percorso dell'immagine normale per lo stato terziario del pulsante. Si tratta dell'immagine visualizzata dagli utenti dopo aver premuto il pulsante PlayPauseStop per avviare lo streaming di una trasmissione live.

Per definire questa immagine, è necessario immettere il tipo di immagine seguito da uno spazio e dal simbolo @ e da un altro spazio. È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine che si vuole usare all'interno del tipo di bitmap da cui si sta disegnando.

Ad esempio, per definire l'immagine normale per un'origine di un'immagine terziaria, se l'immagine si trova all'interno della bitmap di cui è stato eseguito il push, digitare:


```C++
Pushed @ 286,0

```



Gli Stati terziari non possono avere un'immagine disabilitata. Si presuppone che le immagini terziarie siano della stessa larghezza e altezza delle immagini primarie e secondarie.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Pulsanti**](buttons.md)
</dt> </dl>

 

 




