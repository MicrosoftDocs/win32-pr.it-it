---
title: Aggiunta di un dispositivo di scorrimento
description: Aggiunta di un dispositivo di scorrimento
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- creazione di interfacce, dispositivi di scorrimento
- Interfacce di Media Player Windows, dispositivi di scorrimento
- interfacce, dispositivi di scorrimento
- dispositivi di scorrimento nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efcae55b3826b69a7c88fed5a23a262526c9dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044968"
---
# <a name="adding-a-slider"></a>Aggiunta di un dispositivo di scorrimento

È possibile aggiungere un dispositivo di scorrimento per visualizzare la posizione corrente del supporto e consentire anche all'utente di modificare la posizione nel file multimediale corrente.

Prima di tutto è necessario aggiungere l'elemento **Slider** :


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



Viene impostato un valore massimo in base alla durata del file multimediale corrente. Viene usata una bitmap di immagini Thumb minuscola che è solo un quadrato verde di 10 pixel per 10 pixel. Lo sfondo del dispositivo di scorrimento sarà rosso e il primo piano sarà blu. Quando l'utente trascina l'immagine del cursore in una nuova posizione e consente di passare al pulsante del mouse, il supporto viene modificato in tale posizione.

Il dispositivo di scorrimento, tuttavia, non si sposta da solo a meno che non si misuri la posizione corrente con l'attributo **\_ OnChange CurrentPosition** dell'elemento **Controls** , che è incorporato nell'elemento **Player** .


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



Quando viene modificata la posizione del supporto, viene generato un evento che esegue quindi la riga di codice che modifica il valore del dispositivo di scorrimento in base alla posizione corrente del supporto.

Nella sezione di esempio dell'SDK è possibile visualizzare un'interfaccia del dispositivo di scorrimento funzionante simile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla creazione dell'interfaccia**](skin-creation-guide.md)
</dt> </dl>

 

 




