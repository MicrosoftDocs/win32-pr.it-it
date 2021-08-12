---
title: Controls.currentMarker
description: La proprietà currentMarker specifica o recupera il numero del marcatore corrente.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Controlli.currentMarker Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentMarker
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcc11f79460661b6622da529b0de025672794af660aeb27bf56c7910a6d5a50b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580307"
---
# <a name="controlscurrentmarker"></a>Controls.currentMarker

La **proprietà currentMarker** specifica o recupera il numero del marcatore corrente.

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un numero di **lettura/scrittura** (**long**) con un valore predefinito pari a zero.

## <a name="remarks"></a>Commenti

Se **si imposta currentMarker,** la riproduzione viene avviata dal marcatore specificato. Prima di tentare di impostare **currentMarker,** determinare se un file contiene marcatori e il numero di marcatori usando **markerCount.** Se un file non contiene marcatori, l'impostazione **di currentMarker** su un valore diverso da zero restituisce un errore. **L'impostazione di currentMarker** su un numero maggiore di **markerCount** comporta anche un errore.

La **proprietà currentMarker** restituisce sempre l'indicatore corrente o l'ultimo, il che significa che la posizione effettiva del file può essere in corrispondenza del marcatore corrente o prima del marcatore successivo. I marcatori sono numerati a partire da 1, quindi se un file contiene marcatori, è possibile impostare **currentMarker** su zero per modificare la posizione del file su zero.

Fino a quando non viene impostato l'elemento multimediale corrente (utilizzando *Player.***URL o** *Player*. **currentMedia**), **currentMarker** restituisce zero.

## <a name="examples"></a>Esempio

Nell'JScript seguente viene utilizzato **currentMarker** per avviare la riproduzione video dal marcatore che corrisponde alla proprietà **selectedIndex** di un elemento HTML SELECT. **L'oggetto Player** è stato creato con ID = "Player".


```JScript
<SELECT ID = "markers"  NAME = "markers"  LANGUAGE = "JScript"

    /* Seek to the marker number that corresponds to the SELECT element
       selectedIndex value when the list selection changes. */
    onChange = "Player.controls.currentMarker = markers.selectedIndex + 1;
">

    /* Fill the SELECT element with the marker identifiers. */
    <OPTION SELECTED>Sunrise
    <OPTION>Car chase 
    <OPTION>Happy ending
</SELECT>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> <dt>

[**Media.markerCount**](media-markercount.md)
</dt> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player.URL**](player-url.md)
</dt> </dl>

 

 





