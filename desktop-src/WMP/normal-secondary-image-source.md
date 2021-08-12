---
title: Origine immagine secondaria normale
description: Origine immagine secondaria normale
ms.assetid: fe5c0da2-0c40-456f-ab56-ac61ed69ff2d
keywords:
- Windows Media Player Skin per dispositivi mobili, origine immagine pulsante
- skins,origine immagine pulsante
- informazioni di riferimento su skin, pulsanti
- pulsanti nelle skin, origine immagine
- origine dell'immagine per le skin, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f6aeb48ceabc873d4aeb0db910db896712fe16377aa0f67b76205ad8a39c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573731"
---
# <a name="normal-secondary-image-source"></a>Origine immagine secondaria normale

A seconda della funzione del pulsante, potrebbe essere necessario definire la posizione dell'immagine normale per lo stato secondario del pulsante. Questa sarà l'immagine che gli utenti vedono quando esegono il push di un pulsante di funzione PlayPause la prima volta.

Per definire questa immagine, è necessario immettere il tipo di immagine seguito da uno spazio, il simbolo @ e un altro spazio. È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine da usare all'interno del tipo di bitmap da cui si sta disegnando.

Ad esempio, per definire l'immagine normale per un'origine immagine secondaria, se l'immagine si trova all'interno della bitmap con push, digitare:


```C++
Pushed @ 210,0

```



Gli stati secondari non possono avere un'immagine Disabilitata. Si presuppone che le immagini secondarie siano la stessa larghezza e altezza dell'immagine primaria.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Pulsanti**](buttons.md)
</dt> </dl>

 

 




