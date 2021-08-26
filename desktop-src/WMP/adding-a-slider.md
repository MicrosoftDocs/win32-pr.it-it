---
title: Aggiunta di un dispositivo di scorrimento
description: Aggiunta di un dispositivo di scorrimento
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- creazione di skin, dispositivi di scorrimento
- Windows Media Player, dispositivi di scorrimento
- skin, dispositivi di scorrimento
- dispositivi di scorrimento nelle skin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c3644e1b243188664295bbc00101a74377cbef17632217ff0a81dac0d377a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004380"
---
# <a name="adding-a-slider"></a>Aggiunta di un dispositivo di scorrimento

È possibile aggiungere un dispositivo di scorrimento per visualizzare la posizione corrente del supporto e consentire all'utente di modificare la posizione nel file multimediale corrente.

Prima di tutto è necessario aggiungere **l'elemento SLIDER:**


```C++
<SLIDER
  id = "myslider"
  min = "0"
  max = "wmpprop:player.currentMedia.duration"
  onmouseup = "player.controls.currentPosition = myslider.value; "
  tooltip = "current position"
  height = "10"
  width = "180"
  top = "150"
  left = "88"
  backgroundColor = "red"
  foregroundColor = "blue"
  thumbImage = "thumb.bmp"/>

```



In questo modo viene impostato un valore massimo in base alla durata del file multimediale corrente. Viene utilizzata una piccola bitmap dell'immagine del pollice che è un quadrato verde di 10 pixel per 10 pixel. Lo sfondo del dispositivo di scorrimento sarà rosso e il primo piano sarà blu. Quando l'utente trascina l'immagine del cursore in una nuova posizione e lascia andare il pulsante del mouse, il supporto passa a tale posizione.

Tuttavia, il dispositivo di scorrimento non si sposterà da solo a meno che non si misura la posizione corrente con l'attributo **currentPosition \_ onchange** dell'elemento **CONTROLS,** incorporato nell'elemento **PLAYER.**


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



Quando la posizione del supporto cambia, viene generato un evento che esegue quindi la riga di codice che modifica il valore del dispositivo di scorrimento nella posizione corrente del supporto.

È possibile visualizzare un'interfaccia del dispositivo di scorrimento funzionante simile nella sezione di esempio dell'SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla creazione dell'interfaccia**](skin-creation-guide.md)
</dt> </dl>

 

 




