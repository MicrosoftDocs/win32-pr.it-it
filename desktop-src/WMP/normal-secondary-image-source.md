---
title: Origine normale dell'immagine secondaria
description: Origine normale dell'immagine secondaria
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Windows Media Player Mobile Skin, origine immagine pulsante
- interfacce, origine immagine pulsante
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, origine immagine
- origine immagine per interfacce, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff828f6d0f0c8348453cb00fef04ab31718693
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298702"
---
# <a name="normal-secondary-image-source"></a>Origine normale dell'immagine secondaria

A seconda della funzione Button, potrebbe essere necessario definire il percorso dell'immagine normale per lo stato secondario del pulsante. Si tratta dell'immagine visualizzata dagli utenti quando eseguono il push di un pulsante della funzione come playpause la prima volta.

Per definire questa immagine, è necessario immettere il tipo di immagine seguito da uno spazio e dal simbolo @ e da un altro spazio. È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine che si vuole usare all'interno del tipo di bitmap da cui si sta disegnando.

Ad esempio, per definire l'immagine normale per un'origine di un'immagine secondaria, se l'immagine si trova all'interno della bitmap di cui è stato eseguito il push, digitare:


```C++
Pushed @ 210,0

```



Gli stati secondari non possono avere un'immagine disabilitata. Si presuppone che le immagini secondarie siano della stessa larghezza e altezza dell'immagine principale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Pulsanti**](buttons.md)
</dt> </dl>

 

 




