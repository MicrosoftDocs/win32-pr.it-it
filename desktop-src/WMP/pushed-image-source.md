---
title: Origine immagine push
description: Origine immagine push
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Windows Media Player Mobile Skin, origine immagine pulsante
- interfacce, origine immagine pulsante
- riferimento per le interfacce, i pulsanti
- pulsanti in interfacce, origine immagine
- origine immagine per interfacce, pulsanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021c77a305e0f6981823c8a1e471862554c32e08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711554"
---
# <a name="pushed-image-source"></a>Origine immagine push

È necessario definire l'origine dell'immagine che si desidera visualizzare quando l'utente preme un pulsante. L'immagine deriva dal file definito come inserito nella sezione bitmap. È necessario immettere il tipo di immagine seguito da uno spazio e dal simbolo @ e da un altro spazio. È quindi necessario immettere due numeri interi positivi che definiscono le coordinate superiore e sinistra (in pixel) dell'immagine che si vuole usare all'interno del file di immagine di cui è stato eseguito il push. La posizione in cui verrà visualizzata l'immagine deriva dalle coordinate definite per il pulsante rispetto all'immagine di sfondo; ma il percorso da cui deriva è definito dai due numeri che seguono "pushed @" ed è relativo all'immagine push da cui viene letta l'immagine.

Ad esempio, per usare un'immagine dall'immagine push presente nel file di cui è stato eseguito il push, il cui percorso superiore sinistro è 50, 60 usare il codice seguente:


```C++
Pushed @ 50,60

```



Se non si desidera visualizzare un'immagine diversa, è possibile definire la bitmap di sfondo come bitmap sottoposta a push. A tale scopo, specificare il file di sfondo come file di cui è stato eseguito il push e specificare l'offset nell'angolo superiore sinistro del pulsante:


```C++
Pushed @ 50,60

```



In tal caso, nessuno dei pulsanti può visualizzare un'immagine inserita. Si consiglia di visualizzare un'immagine push per tutti i pulsanti per fornire all'utente un'indicazione visiva, perché non è sempre chiaro se un tocco produce un risultato, soprattutto quando la musica viene riprodotta o se il suono di tocco è disattivato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Pulsanti**](buttons.md)
</dt> </dl>

 

 




