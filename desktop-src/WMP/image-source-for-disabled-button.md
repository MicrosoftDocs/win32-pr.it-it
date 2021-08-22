---
title: Origine immagine per il pulsante Disabilitato
description: Origine immagine per il pulsante Disabilitato
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Windows Media Player Skin per dispositivi mobili, origine immagine pulsante
- skins,origine immagine pulsante
- informazioni di riferimento per le skin, i pulsanti
- pulsanti nelle skin, origine immagine
- origine dell'immagine per le skin, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a3b31a25eb40d82d33f241a6eaebf690fe11aa2128528739a7e7bbb4dc217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509261"
---
# <a name="image-source-for-disabled-button"></a>Origine immagine per il pulsante Disabilitato

È necessario definire l'origine dell'immagine da visualizzare quando un pulsante è disabilitato o ha uno stato corrispondente a off. L'immagine proviene dal file definito come Disabilitato nella sezione Bitmap. È necessario immettere il tipo di immagine seguito da uno spazio, il simbolo @ e un altro spazio. È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine da usare all'interno del file bitmap. La posizione in cui verrà visualizzata l'immagine proviene dalle coordinate definite per il pulsante rispetto all'immagine di sfondo, ma la posizione da cui proviene è definita dai due numeri che segue "Disabled @" ed è relativa alla bitmap Disabled da cui si sta leggendo l'immagine.

Ad esempio, per usare un'immagine della bitmap Disabled che si trova nel file Disabled in una posizione superiore e sinistra di 50,60 pixel, usare il codice seguente:


```C++
Disabled @ 50,60

```



È necessario definire una bitmap Disabilitata. Se non si vuole visualizzare un'immagine diversa, è possibile definire la bitmap Di sfondo come bitmap disabilitata con un offset di 0,0:


```C++
Disabled @ 50,60

```



Nell'esempio precedente, 50,60 è il percorso del pulsante che si sta lavorando nel file Disabled (in questo caso, lo stesso percorso del pulsante nella bitmap Background). Tuttavia, è consigliabile visualizzare un'immagine disabilitata per tutti i pulsanti per fornire agli utenti un'indicazione visiva, perché molti pulsanti non saranno utilizzabili in determinate condizioni, ad esempio una playlist vuota. Se gli utenti sanno che un pulsante è disabilitato, non continueranno a fare clic su di esso o a pensare che l'interfaccia non funzioni come previsto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Pulsanti**](buttons.md)
</dt> </dl>

 

 




