---
title: Controls. currentMarker
description: La proprietà currentMarker specifica o Recupera il numero di marcatore corrente.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Media Player di Windows Controls. currentMarker
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
ms.openlocfilehash: 8aae8af226b62550b3faae9389385d321bf10aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330119"
---
# <a name="controlscurrentmarker"></a>Controls. currentMarker

La proprietà **currentMarker** specifica o Recupera il numero di marcatore corrente.

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **numero** di lettura/scrittura (**Long**) il cui valore predefinito è zero.

## <a name="remarks"></a>Commenti

L'impostazione di **currentMarker** fa sì che la riproduzione venga avviata dal marcatore specificato. Prima di provare a impostare **currentMarker**, determinare se un file contiene marcatori e il numero di marcatori utilizzando **markerCount**. Se un file non ha marcatori, l'impostazione di **currentMarker** su qualsiasi elemento, ma con zero, genera un errore. L'impostazione di **currentMarker** su un numero maggiore di **markerCount** genera anche un errore.

La proprietà **currentMarker** restituisce sempre il marcatore corrente o ultimo, il che significa che la posizione effettiva del file può essere in corrispondenza del marcatore corrente o prima del marcatore successivo. I marcatori sono numerati a partire da 1, pertanto se un file contiene marcatori, è possibile impostare **currentMarker** su zero per modificare la posizione del file su zero.

Fino a quando non viene impostato l'elemento multimediale corrente (utilizzando *Player*.**URL** o *lettore*. **currentMedia**), **currentMarker** restituisce zero.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato **currentMarker** per avviare la riproduzione video dal marcatore che corrisponde alla proprietà **SelectedIndex** di un elemento HTML SELECT. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Controls**](controls-object.md)
</dt> <dt>

[**Media. markerCount**](media-markercount.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





