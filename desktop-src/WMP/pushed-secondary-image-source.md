---
title: Origine immagine secondaria di cui è stato push
description: Origine immagine secondaria di cui è stato push
ms.assetid: f2a2380d-c876-456b-837b-01b3997d81f2
keywords:
- Windows Media Player Interfaccia per dispositivi mobili, origine immagine pulsante
- skins, origine dell'immagine del pulsante
- informazioni di riferimento per le interfaccia, i pulsanti
- pulsanti nelle interfaccia, origine dell'immagine
- origine dell'immagine per le interfaccia, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37045da71b8417856ec72ac7e57a6a787426ba486993b9fef03910b4d32e663d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861831"
---
# <a name="pushed-secondary-image-source"></a>Origine immagine secondaria di cui è stato push

A seconda della funzione del pulsante, potrebbe essere necessario definire la posizione dell'immagine inserita per lo stato secondario del pulsante. Questa sarà l'immagine che gli utenti vedono quando esegono il push di un pulsante della funzione PlayPause la seconda volta.

Per definire questa immagine, è necessario immettere il tipo di immagine seguito da uno spazio, il simbolo @ e un altro spazio. È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine da usare all'interno del tipo di immagine da cui si sta disegnando.

Ad esempio, per definire l'immagine push per un'origine immagine secondaria, se l'immagine si trova all'interno della bitmap push, digitare:


```C++
Pushed @ 248,0

```



Gli stati secondari non possono avere un'immagine Disabilitata. Si presuppone che le immagini secondarie siano della stessa larghezza e altezza dell'immagine primaria.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Pulsanti**](buttons.md)
</dt> </dl>

 

 




