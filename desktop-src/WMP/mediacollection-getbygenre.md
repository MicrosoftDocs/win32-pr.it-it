---
title: Metodo MediaCollection.getByGenre
description: Il metodo getByGenre recupera una playlist degli elementi multimediali con il genere specificato.
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- Metodo getByGenre Windows Media Player
- Metodo getByGenre Windows Media Player , classe MediaCollection
- Classe MediaCollection Windows Media Player metodo , getByGenre
topic_type:
- apiref
api_name:
- MediaCollection.getByGenre
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df514e7ed399e73f6778912df32a4ed0be57a90039fe867c75cf31a3eec807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135014"
---
# <a name="mediacollectiongetbygenre-method"></a>Metodo MediaCollection.getByGenre

Il **metodo getByGenre** recupera una playlist degli elementi multimediali con il genere specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*genre* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome del genere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto Playlist.**

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'JScript seguente viene utilizzato *MediaCollection*. **getByGenre per** recuperare una playlist di elementi multimediali. La playlist contiene elementi con il genere specificato dall'utente in un elemento di input HTML TEXT denominato GetGenre. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play 
the media items. -->
<INPUT TYPE = "BUTTON"  
       NAME = "PlayGenre"  
       ID = "PlayGenre"  
       VALUE = "Play Genre"

onClick = "
    /* Retrieve the genre text from the user. */
    var genre = GetGenre.value;

    /* Create the playlist using getByGenre. */
    var pl = Player.mediaCollection.getByGenre(genre);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the digital media item in the new playlist. */
    Player.controls.play();
">

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

 

 





