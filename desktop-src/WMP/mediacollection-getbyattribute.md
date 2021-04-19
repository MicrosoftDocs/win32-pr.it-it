---
title: Mediacollection. getByAttribute, metodo
description: Il metodo getByAttribute recupera una playlist di elementi multimediali che contengono un valore specificato per un attributo specificato.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- Metodo getByAttribute Windows Media Player
- Metodo getByAttribute Windows Media Player, classe Mediacollection
- Mediacollection (classe) Windows Media Player, metodo getByAttribute
topic_type:
- apiref
api_name:
- MediaCollection.getByAttribute
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533823127364416f8f4492c82381e682173c5c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330345"
---
# <a name="mediacollectiongetbyattribute-method"></a>Mediacollection. getByAttribute, metodo

Il metodo **getByAttribute** recupera una playlist di elementi multimediali che contengono un valore specificato per un attributo specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*attributo* \[ in\]
</dt> <dd>

**Stringa** che indica il nome dell'attributo da cercare. Per informazioni sugli attributi supportati da Windows Media Player, vedere la Guida di [riferimento](attribute-reference.md)agli attributi di Windows Media Player.

</dd> <dt>

*valore* \[ di in\]
</dt> <dd>

**Stringa** che indica il valore che l'attributo deve avere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **playlist** .

## <a name="remarks"></a>Commenti

Questo metodo può essere utilizzato per creare una query generica per gli elementi multimediali che corrispondono a un valore per un attributo nel database. Questa operazione è utile nel caso di attributi definiti dall'utente. Se l'attributo non esiste, verrà generato un errore.

È possibile utilizzare questo metodo per recuperare tutti gli elementi multimediali di un tipo specifico. Usare il nome di attributo "MediaType" e uno dei valori seguenti:



| Valore    | Descrizione                                                |
|----------|------------------------------------------------------------|
| Audio    | Musica e altri elementi solo audio.                          |
| playlist | Playlist rappresentate come oggetti **multimediali** .                |
| radio    | Elementi della stazione di radio. Non usato da Windows Media Player 10.  |
| Video    | Elementi video.                                               |
| Foto    | Elementi foto. Richiede Windows Media Player 10.             |
| altro    | Altri elementi, ad esempio file ASF o URL per flussi multimediali. |



 

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzato *mediacollection*. **getByAttribute** per riprodurre tutto il contenuto dalla libreria dall'artista denominato triodo 48. L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Get a playlist object filled with media items by a 
// particular artist.
var pl = Player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
Player.currentPlaylist = pl;

// Start Windows Media Player.
Player.controls.play();

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

 

 





