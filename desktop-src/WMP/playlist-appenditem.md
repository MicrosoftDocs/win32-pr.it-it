---
title: Metodo Playlist.appendItem
description: Il metodo appendItem aggiunge un elemento multimediale alla fine della playlist.
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- Metodo appendItem Windows Media Player
- Metodo appendItem Windows Media Player , classe Playlist
- Classe Playlist Windows Media Player , metodo appendItem
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
ms.openlocfilehash: 79361ebcf2ea23b754a7bc86cb6fa4a0af465e4e6619ed692c027bc28eb7aa87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747120"
---
# <a name="playlistappenditem-method"></a>Metodo Playlist.appendItem

Il **metodo appendItem** aggiunge un elemento multimediale alla fine della playlist.

## <a name="syntax"></a>Sintassi


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*item* \[ Pollici\]
</dt> <dd>

**Oggetto** multimediale da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la playlist*. **appendItem** per aggiungere l'elemento multimediale corrente alla playlist denominata "ThreeList". **L'oggetto Player** è stato creato con ID="Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Playlist**](playlist-object.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





