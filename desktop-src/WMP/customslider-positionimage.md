---
title: CUSTOMSLIDER. dimensione positionImage
description: L'attributo dimensione positionImage specifica o recupera la mappa immagine utilizzata per determinare l'immagine della posizione dal file di immagine da visualizzare.
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- Media Player Windows CUSTOMSLIDER. dimensione positionImage
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc92a9c263e2b450e64d526ccfc7976fdd6227a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324102"
---
# <a name="customsliderpositionimage"></a>CUSTOMSLIDER. dimensione positionImage

L'attributo **dimensione positionImage** specifica o recupera la mappa immagine utilizzata per determinare l'immagine della posizione dal file di immagine da visualizzare.

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente il nome di un file di immagine.

## <a name="remarks"></a>Commenti

Questo attributo è obbligatorio e deve essere specificato.

**Dimensione positionImage** non viene visualizzato. Al contrario, funge da mappa che definisce le aree selezionabili dell'immagine visualizzata. L'immagine visualizzata è una delle immagini secondarie del file di immagine e rappresenta lo stato effettivo del dispositivo di scorrimento. Il **dimensione positionImage** include un numero di aree di scala grigie uguale al numero di queste immagini secondarie. Le immagini secondarie devono avere le stesse dimensioni di **dimensione positionImage** o il dispositivo di scorrimento personalizzato non funzionerà correttamente.

Non sarà possibile fare clic su un'area che non è in scala di grigi. Le aree selezionabili devono essere impostate su valori di colore che variano uniformemente nello spettro della scala grigia da nero a bianco, in cui la prima area è nera pura e l'ultima area è bianca. I valori dei colori di ogni area successiva devono essere incrementati di un valore uguale a 255 diviso per il numero totale di aree meno uno, arrotondando al numero intero più vicino.

Se ad esempio sono presenti sei aree, l'incremento è 51 (255 diviso per 5) e i sei valori della scala di grigi sarebbero 0, 51, 102, 153, 204 e 255. I valori esadecimali dei colori per le sei aree sono quindi \# 000000, \# 333333, \# 666666, \# 999999, \# cccccc e \# FFFFFF.

In questo modo, le aree avranno una sequenza dettata dai valori dei colori della scala grigia e questa sequenza corrisponderà alla sequenza di immagini secondarie nel file di immagine. Quando si fa clic su una delle aree, viene visualizzata l'immagine secondaria corrispondente e il **valore** del dispositivo di scorrimento personalizzato viene aggiornato di conseguenza.

I tipi di file di immagine supportati sono BMP, JPG, PNG e GIF (escluse le gif animate).

## <a name="examples"></a>Esempio

Di seguito è riportato un esempio di un dispositivo di scorrimento **dimensione positionImage** personalizzato. L'immagine corrispondente è illustrata nella sezione esempio della proprietà **Image** .

![immagine di dimensione positionImage di esempio](images/dialmap.png)

Il codice seguente illustra l'uso degli attributi **CUSTOMSLIDER** .


```XML
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >

    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    >
      <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition;"
      />
    </PLAYER>

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
      thumbImage = "thumb.bmp"
    />

    <CUSTOMSLIDER
      top = "120"
      left = "23"
      min = "0"
      max = "100"
      borderSize = "10"
      toolTip = "volume control"
      image = "dial.bmp"
      transparencyColor = "#00FFFF"
      positionImage = "dialmap.bmp"
      enabled = "true"
      value = "wmpprop:player.settings.volume"
      value_onchange = "player.settings.volume = value"
    />

    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "100"
    />

    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    > 

      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />

      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />

    </BUTTONGROUP>

  </VIEW>
</THEME>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER. image**](customslider-image.md)
</dt> </dl>

 

 





