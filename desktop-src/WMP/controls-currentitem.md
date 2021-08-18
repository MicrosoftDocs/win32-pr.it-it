---
title: Controls.currentItem
description: La proprietà currentItem specifica o recupera l'elemento multimediale corrente.
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- Controls.currentItem Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentItem
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66dc0ad047213e0fbba7dbdd7336e67b8d015e39aba510ac37bd3701462413ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997551"
---
# <a name="controlscurrentitem"></a>Controls.currentItem

La **proprietà currentItem** specifica o recupera l'elemento multimediale corrente.

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un oggetto Media **di** lettura/scrittura.

## <a name="remarks"></a>Commenti

Questo metodo funziona solo con gli elementi in *Player*. **currentPlaylist**. La **chiamata di currentItem** con un riferimento a un elemento multimediale salvato non è supportata.

## <a name="examples"></a>Esempio

Nell'JScript seguente viene utilizzato **currentItem** per impostare l'elemento multimediale corrente del controllo lettore sul valore selezionato in un elemento HTML SELECT. La playlist corrente è stata specificata per la prima volta usando *PlaylistCollection*. **getByName**. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<SELECT ID = playItem  NAME = "playItem"  LANGUAGE = "JScript"

    /* Specify the current item when the selected list value changes. */
    onChange = "Player.controls.currentItem = Player.currentPlaylist.item(playItem.value);">

    /* Fill the SELECT element list with three items that match
       the songs in the playlist. */
    <OPTION VALUE = 0 >Laure
    <OPTION VALUE = 1 >Jeanne
    <OPTION VALUE = 2 >House
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

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





