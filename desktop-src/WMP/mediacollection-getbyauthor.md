---
title: Mediacollection. getByAuthor, metodo
description: Il metodo getByAuthor recupera una playlist degli elementi multimediali dall'autore specificato.
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- Metodo getByAuthor Windows Media Player
- Metodo getByAuthor Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getByAuthor
topic_type:
- apiref
api_name:
- MediaCollection.getByAuthor
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eae0928250e37e76bf3a39f38b43bef8a5691c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324534"
---
# <a name="mediacollectiongetbyauthor-method"></a>Mediacollection. getByAuthor, metodo

Il metodo **getByAuthor** recupera una playlist degli elementi multimediali dall'autore specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*autore* \[ in\]
</dt> <dd>

**Stringa** contenente il nome dell'autore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **playlist** .

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *mediacollection*. **getByAuthor** per recuperare una playlist di elementi multimediali. La playlist contiene elementi che corrispondono all'autore specificato dall'utente in un elemento input di testo HTML denominato GetAuthor. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play the media items. -->
<INPUT TYPE = "BUTTON"  NAME = "PlayAuthor"  
       ID = "PlayAuthor"  
       VALUE = "Play Author"

onClick = "
    /* Retrieve the author name text from the user. */
    var author = GetAuthor.value;

    /* Create the playlist by using getByAuthor. */
    var pl = Player.mediaCollection.getByAuthor(Author);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media items in the new playlist. */
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

 

 





