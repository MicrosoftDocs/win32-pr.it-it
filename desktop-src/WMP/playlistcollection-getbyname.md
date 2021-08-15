---
title: Metodo PlaylistCollection.getByName
description: Il metodo getByName recupera un oggetto PlaylistArray contenente playlist con il nome specificato, se presente.
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- Metodo getByName Windows Media Player
- Metodo getByName Windows Media Player , classe PlaylistCollection
- Classe PlaylistCollection Windows Media Player metodo , getByName
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
ms.openlocfilehash: 300307ff011abf8b28c645901422291ccab4cf7c66a7a3ba81121ffe1c22e573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334642"
---
# <a name="playlistcollectiongetbyname-method"></a>Metodo PlaylistCollection.getByName

Il **metodo getByName** recupera un oggetto **PlaylistArray** contenente playlist con il nome specificato, se presente.

## <a name="syntax"></a>Sintassi


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*name* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome delle playlist da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto PlaylistArray.**

## <a name="remarks"></a>Commenti

Usare *PlaylistArray.* **count per** determinare se esiste una playlist. Se **count** è zero, non esiste una playlist.

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *playlistCollection*. **getByName per** controllare **l'oggetto playlistCollection** per una playlist denominata "ThreeList". Se la playlist "Threelist" esiste, **getByName** imposta "ThreeList" come playlist corrente. **L'oggetto** Player è stato creato con l'ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**PlaylistArray.count**](playlistarray-count.md)
</dt> <dt>

[**Oggetto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





