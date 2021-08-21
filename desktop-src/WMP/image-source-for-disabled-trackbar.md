---
title: Origine immagine per trackbar disabilitato
description: Origine immagine per trackbar disabilitato
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Windows Media Player Skin per dispositivi mobili, trackbar
- skin, trackbar
- informazioni di riferimento su skin, trackbar
- trackbar nelle skin, origine immagine
- origine immagine per skin, trackbar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b3f5f58198d55f2dcd17b23b102c91eb4dff4787489e13775c6be71faa3223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338946"
---
# <a name="image-source-for-disabled-trackbar"></a>Origine immagine per trackbar disabilitato

È necessario definire l'origine dell'immagine da visualizzare quando un trackbar è disabilitato, usando il tipo di bitmap da cui si vuole disegnare l'immagine. L'immagine visualizzata si trova in genere all'interno del file Super o se si crea un'interfaccia per Windows Media Player 10 Mobile, l'immagine si trova all'interno del file SeekThumb. È necessario immettere il tipo di immagine seguito da uno spazio, il simbolo @ e un altro spazio. È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine da usare all'interno del tipo di bitmap da cui si sta disegnando.

Ad esempio, per usare un'immagine della bitmap SeekThumb con una posizione superiore e sinistra di 50,60 pixel, digitare:


```C++
Disabled @ 50,60

```



È necessario definire una posizione dell'immagine per un'immagine del trackbar disabilitata. Se non si vuole visualizzare una nuova immagine, è possibile definire l'immagine di sfondo come immagine disabilitata con un offset di 0,0:


```C++
Disabled @ 50,60

```



Nell'esempio precedente, 50,60 rappresenta il percorso del pulsante che si sta lavorando nel file SeekThumb (in questo caso, la stessa posizione del pulsante sulla bitmap Background). Tuttavia, è consigliabile visualizzare un'immagine disabilitata per tutti i trackbar per fornire all'utente un'indicazione visiva, perché i trackbar non saranno utilizzabili in determinate condizioni. Ad esempio, i trackbar Seek possono essere disabilitati quando la playlist corrente è vuota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Trackbar**](trackbars.md)
</dt> </dl>

 

 




