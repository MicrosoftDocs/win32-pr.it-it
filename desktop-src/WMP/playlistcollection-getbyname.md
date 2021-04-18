---
title: PlaylistCollection. getByName (metodo)
description: Il metodo getByName recupera un oggetto PlaylistArray contenente playlist con il nome specificato, se esistente.
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- metodo getByName Media Player Windows
- metodo getByName Windows Media Player, Classe PlaylistCollection
- Classe PlaylistCollection Windows Media Player, metodo getByName
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7954df8e0ccc487df77ea31b3a26dce9eea6d2e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330455"
---
# <a name="playlistcollectiongetbyname-method"></a>PlaylistCollection. getByName (metodo)

Il metodo **GetByName** recupera un oggetto **PlaylistArray** contenente playlist con il nome specificato, se esistente.

## <a name="syntax"></a>Sintassi


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome* \[ in\]
</dt> <dd>

**Stringa** contenente il nome delle playlist da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **PlaylistArray** .

## <a name="remarks"></a>Commenti

Usare *PlaylistArray*. **conteggio** per determinare se esiste una playlist. Se **count** è zero, una playlist non esiste.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio di codice JScript seguente viene usato *PlaylistCollection*. **GetByName** per controllare l'oggetto **PlaylistCollection** per una playlist denominata "Three". Se è presente la playlist "Three-", **GetByName** imposta "Three" come playlist corrente. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**PlaylistArray. Count**](playlistarray-count.md)
</dt> <dt>

[**PlaylistCollection (oggetto)**](playlistcollection-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





