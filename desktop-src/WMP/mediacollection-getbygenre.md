---
title: Mediacollection. getByGenre, metodo
description: Il metodo getByGenre recupera una playlist degli elementi multimediali con il genere specificato.
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- Metodo getByGenre Windows Media Player
- Metodo getByGenre Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getByGenre
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
ms.openlocfilehash: 4b73cd7fe9bb3efa9115e2ba5d01b6d12c89898d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327168"
---
# <a name="mediacollectiongetbygenre-method"></a>Mediacollection. getByGenre, metodo

Il metodo **getByGenre** recupera una playlist degli elementi multimediali con il genere specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*genere* \[ in\]
</dt> <dd>

**Stringa** che contiene il nome del genere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **playlist** .

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *mediacollection*. **getByGenre** per recuperare una playlist di elementi multimediali. La playlist contiene elementi con il genere specificato dall'utente in un elemento input di testo HTML denominato getgenre. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Mediacollection (oggetto)**](mediacollection-object.md)
</dt> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





