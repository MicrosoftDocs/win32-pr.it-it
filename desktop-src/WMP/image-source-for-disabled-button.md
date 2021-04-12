---
title: Origine immagine per il pulsante disabilitato
description: Origine immagine per il pulsante disabilitato
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Windows Media Player Mobile Skin, origine immagine pulsante
- interfacce, origine immagine pulsante
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, origine immagine
- origine immagine per interfacce, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ccd0362f3dd11acec71eaf0b92574f2c27c77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396034"
---
# <a name="image-source-for-disabled-button"></a>Origine immagine per il pulsante disabilitato

È necessario definire l'origine dell'immagine che si desidera visualizzare quando un pulsante è disabilitato o presenta uno stato che corrisponde a disattivato. L'immagine deriva dal file definito come disabilitato nella sezione bitmap. È necessario immettere il tipo di immagine seguito da uno spazio e dal simbolo @ e da un altro spazio. È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine che si desidera utilizzare nel file bitmap. Il percorso in cui l'immagine verrà visualizzata deriva dalle coordinate definite per il pulsante rispetto all'immagine di sfondo, ma la posizione da cui deriva è definita dai due numeri che seguono "disabled @" ed è relativo alla bitmap disabilitata da cui si sta leggendo l'immagine.

Ad esempio, per usare un'immagine della bitmap disabilitata presente nel file disabilitato in un percorso superiore e sinistro di 50, 60 pixel, usare il codice seguente:


```C++
Disabled @ 50,60

```



È necessario definire una bitmap disabilitata. Se non si desidera visualizzare un'immagine diversa, è possibile definire la bitmap di sfondo come bitmap disabilitata con un offset di 0, 0:


```C++
Disabled @ 50,60

```



Nell'esempio precedente 50, 60 è la posizione del pulsante che si sta utilizzando nel file disabilitato (in questo caso, la stessa posizione del pulsante nella bitmap di sfondo). È tuttavia consigliabile visualizzare un'immagine disabilitata per tutti i pulsanti per fornire agli utenti un'indicazione visiva, perché molti pulsanti non saranno utilizzabili in determinate condizioni, ad esempio una playlist vuota. Se gli utenti sanno che un pulsante è disabilitato, non continuerà a fare clic su di esso o ritenere che l'interfaccia non funzioni come previsto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Pulsanti**](buttons.md)
</dt> </dl>

 

 




