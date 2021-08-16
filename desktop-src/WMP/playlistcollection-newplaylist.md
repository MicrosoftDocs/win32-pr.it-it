---
title: Metodo PlaylistCollection.newPlaylist
description: Il metodo newPlaylist crea una nuova playlist nella libreria.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- Metodo newPlaylist Windows Media Player
- Metodo newPlaylist Windows Media Player , classe PlaylistCollection
- Classe PlaylistCollection Windows Media Player , metodo newPlaylist
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
ms.openlocfilehash: af40d4de424997cb943711d84bf62805f2036afeb551c5d397ce82ae0975e812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334596"
---
# <a name="playlistcollectionnewplaylist-method"></a>Metodo PlaylistCollection.newPlaylist

Il **metodo newPlaylist** crea una nuova playlist nella libreria.

## <a name="syntax"></a>Sintassi


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*name* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome della playlist da creare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto Playlist.**

## <a name="remarks"></a>Commenti

Questo metodo crea una playlist vuota nella libreria. Per riempire la playlist con elementi multimediali, usare *Playlist*. **appendItem o** *Playlist.* **insertItem**.

Nella libreria sono consentite più playlist con lo stesso nome. Per evitare di creare un nome di playlist duplicato con questo metodo, usare **getByName** e *PlaylistArray*. **count** per determinare se esiste già una playlist con un nome specifico.

Gli spazi iniziali e finali non sono consentiti nei nomi delle playlist e vengono rimossi automaticamente dal valore specificato per il *parametro name.*

Per usare questo metodo, è necessario l'accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'JScript seguente viene creata una nuova playlist vuota denominata "ThreeList". **L'oggetto** Player è stato creato con ID="Player".


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Playlist.appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Playlist.insertItem**](playlist-insertitem.md)
</dt> <dt>

[**PlaylistArray.count**](playlistarray-count.md)
</dt> <dt>

[**Oggetto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**PlaylistCollection.remove**](playlistcollection-remove.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





