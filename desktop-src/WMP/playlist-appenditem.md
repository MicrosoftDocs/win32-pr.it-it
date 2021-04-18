---
title: Playlist. appendItem, metodo
description: Il metodo appendItem aggiunge un elemento multimediale alla fine della playlist.
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- Metodo appendItem Windows Media Player
- Metodo appendItem Media Player Windows, classe playlist
- Classe playlist Windows Media Player, metodo appendItem
topic_type:
- apiref
api_name:
- Playlist.appendItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 828799d5b6e71e7ff0e7be4c1e55714f6343be51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327145"
---
# <a name="playlistappenditem-method"></a>Playlist. appendItem, metodo

Il metodo **appendItem** aggiunge un elemento multimediale alla fine della playlist.

## <a name="syntax"></a>Sintassi


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*elemento* \[ di in\]
</dt> <dd>

Oggetto **multimediale** da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *playlist*. **appendItem** aggiungere l'elemento multimediale corrente alla playlist denominata "Three". L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Get the current media item.
var currMedia = Player.currentMedia;

// Get the playlist object by name.
var plThreeList = Player.playlistCollection.getByName("ThreeList").item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





