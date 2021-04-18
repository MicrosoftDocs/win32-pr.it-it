---
title: PlaylistCollection. nuova playlist, metodo
description: Il metodo nuova playlist crea una nuova playlist nella libreria.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- Metodo nuova playlist Windows Media Player
- Metodo nuova playlist Windows Media Player, Classe PlaylistCollection
- Classe PlaylistCollection Windows Media Player, metodo nuova playlist
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d94c25a8dfe6f1eb7c4dac40dd644433a5f0d7e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331370"
---
# <a name="playlistcollectionnewplaylist-method"></a>PlaylistCollection. nuova playlist, metodo

Il metodo **nuova playlist** crea una nuova playlist nella libreria.

## <a name="syntax"></a>Sintassi


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome* \[ in\]
</dt> <dd>

**Stringa** contenente il nome della playlist da creare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **playlist** .

## <a name="remarks"></a>Commenti

Questo metodo crea una playlist vuota nella libreria. Per riempire la playlist con elementi multimediali, usare *playlist*. **appendItem** o *playlist*. **InsertItem**.

Nella libreria sono consentite più playlist con lo stesso nome. Per evitare di creare un nome di playlist duplicato con questo metodo, usare **GetByName** e *PlaylistArray*. **conteggio** per determinare se una playlist con un determinato nome esiste già.

Gli spazi iniziali e finali non sono consentiti nei nomi delle playlist e vengono rimossi automaticamente dal valore specificato per il parametro *Name* .

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene creata una nuova playlist vuota denominata "Three". L'oggetto **Player** è stato creato con ID = "Player".


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mediacollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Playlist. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Playlist. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**PlaylistArray. Count**](playlistarray-count.md)
</dt> <dt>

[**PlaylistCollection (oggetto)**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection. getByName**](playlistcollection-getbyname.md)
</dt> <dt>

[**PlaylistCollection. importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**PlaylistCollection. Remove**](playlistcollection-remove.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





