---
title: Metodo MediaCollection.getByName
description: Il metodo getByName recupera una playlist degli elementi multimediali con il nome specificato.
ms.assetid: f9395a4f-06d6-438b-b7c5-7a063abdf59f
keywords:
- Metodo getByName Windows Media Player
- Metodo getByName Windows Media Player , classe MediaCollection
- Classe MediaCollection Windows Media Player , metodo getByName
topic_type:
- apiref
api_name:
- MediaCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15063a9d544f6ebe55e66513b79aeead7c94e8aeffed7571ccb2ac574e1cb876
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996291"
---
# <a name="mediacollectiongetbyname-method"></a>Metodo MediaCollection.getByName

Il **metodo getByName** recupera una playlist degli elementi multimediali con il nome specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.getByName(
  name
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*name* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto Playlist.**

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *MediaCollection*. **getByName** per recuperare tre elementi dalla libreria. Ogni elemento viene quindi aggiunto alla playlist corrente. **L'oggetto Player** è stato creato con ID="Player".


```JScript
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get a playlist object that contains an Internet URL.
var One = Player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");
 
// Get a playlist object that contains a file on a network server.
var Two = Player.mediaCollection.getByName("Jeanne");

// Get a playlist object that contains a file on a local drive.
var Three = Player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use Playlist.item with
// an index of zero to reference that item.
Player.currentPlaylist.appendItem(One.item(0));
Player.currentPlaylist.appendItem(Two.item(0));
Player.currentPlaylist.appendItem(Three.item(0));

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Oggetto Playlist**](playlist-object.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





