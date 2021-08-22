---
title: Origine immagine di cui è stato push
description: Origine immagine di cui è stato push
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Windows Media Player Interfaccia per dispositivi mobili, origine immagine pulsante
- skins, origine dell'immagine del pulsante
- informazioni di riferimento per le interfaccia, pulsanti
- pulsanti nelle interfaccia, origine dell'immagine
- origine dell'immagine per le interfaccia, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b336f19900b53a4ae9fff39ce76af9fe52daac4de9e94fb09dcf7b0561f1dde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861841"
---
# <a name="pushed-image-source"></a>Origine immagine di cui è stato push

È necessario definire l'origine dell'immagine da visualizzare quando l'utente preme un pulsante. L'immagine proviene dal file definito come Push nella sezione Bitmap. È necessario immettere il tipo di immagine seguito da uno spazio, il simbolo @ e un altro spazio. È quindi necessario immettere due numeri interi positivi che definiscono le coordinate superiore e sinistra (in pixel) dell'immagine da usare all'interno del file di immagine push. La posizione in cui verrà visualizzata l'immagine proviene dalle coordinate definite per il pulsante rispetto all'immagine di sfondo. ma la posizione da cui proviene è definita dai due numeri che segue "Pushed @" ed è relativa all'immagine push da cui si sta leggendo l'immagine.

Ad esempio, per usare un'immagine dell'immagine push nel file push la cui posizione superiore sinistra è 50,60, usare il codice seguente:


```C++
Pushed @ 50,60

```



Se non si vuole visualizzare un'immagine diversa, è possibile definire la bitmap Di sfondo come bitmap di cui è stato push. A tale scopo, specificare il file In background come file di cui è stato premuto il push e specificare l'offset nell'angolo superiore sinistro del pulsante:


```C++
Pushed @ 50,60

```



In questo caso, nessuno dei pulsanti può visualizzare un'immagine push. È consigliabile visualizzare un'immagine push per tutti i pulsanti per fornire all'utente un'indicazione visiva, perché non è sempre chiaro se un tocco produce un risultato, soprattutto quando la musica è in riproduzione o il suono toccando è disattivato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Pulsanti**](buttons.md)
</dt> </dl>

 

 




