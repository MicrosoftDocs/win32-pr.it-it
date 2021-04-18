---
title: Origine immagine per TrackBar disabilitato
description: Origine immagine per TrackBar disabilitato
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Windows Media Player Mobile Skins, trackbars
- interfacce, TrackBar
- riferimento per Skin, trackbars
- TrackBar in interfacce, origine immagine
- origine immagine per Skin, trackbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbae540f97c7d1f7241035b074f45e6267e51615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298237"
---
# <a name="image-source-for-disabled-trackbar"></a>Origine immagine per TrackBar disabilitato

È necessario definire l'origine dell'immagine che si desidera visualizzare quando un TrackBar è disabilitato, utilizzando il tipo di bitmap da cui si desidera creare l'immagine. L'immagine visualizzata si trova in genere all'interno del file con privilegi avanzati o se si sta creando un'interfaccia per Windows Media Player 10 Mobile, l'immagine si trova all'interno del file SeekThumb. È necessario immettere il tipo di immagine seguito da uno spazio e dal simbolo @ e da un altro spazio. È quindi necessario immettere due numeri interi positivi che definiscono le coordinate in alto a sinistra (in pixel) dell'immagine che si vuole usare all'interno del tipo di bitmap da cui si sta disegnando.

Ad esempio, per usare un'immagine dalla bitmap SeekThumb con una posizione superiore e sinistra di 50, 60 pixel, digitare:


```C++
Disabled @ 50,60

```



È necessario definire un percorso immagine per un'immagine TrackBar disabilitata. Se non si vuole visualizzare una nuova immagine, è possibile definire l'immagine di sfondo come immagine disabilitata con un offset di 0, 0:


```C++
Disabled @ 50,60

```



Nell'esempio precedente, 50, 60 rappresenta la posizione del pulsante che si sta utilizzando nel file SeekThumb (in questo caso, la stessa posizione del pulsante nella bitmap di sfondo). Tuttavia, si consiglia di visualizzare un'immagine disabilitata per tutti i TrackBar per fornire all'utente un'indicazione visiva, perché i TrackBar non saranno utilizzabili in determinate condizioni. Ad esempio, la ricerca di TrackBar può essere disabilitata quando la playlist corrente è vuota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**TrackBar**](trackbars.md)
</dt> </dl>

 

 




