---
title: Metodo MediaCollection.getByAttribute
description: Il metodo getByAttribute recupera una playlist di elementi multimediali che contengono un valore specificato per un attributo specificato.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- Metodo getByAttribute Windows Media Player
- Metodo getByAttribute Windows Media Player , classe MediaCollection
- Classe MediaCollection Windows Media Player metodo , getByAttribute
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
ms.openlocfilehash: f942f0718202d6c3e509b177c34c4c4be20c058b1e74991fa0ae89955d7711d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996310"
---
# <a name="mediacollectiongetbyattribute-method"></a>Metodo MediaCollection.getByAttribute

Il **metodo getByAttribute** recupera una playlist di elementi multimediali che contengono un valore specificato per un attributo specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*attributo* \[ Pollici\]
</dt> <dd>

**Stringa** che indica il nome dell'attributo da cercare. Per informazioni sugli attributi supportati da Windows Media Player, vedere le informazioni di Windows Media Player [sugli attributi](attribute-reference.md).

</dd> <dt>

*value* \[ Pollici\]
</dt> <dd>

**Stringa** che indica il valore che l'attributo deve avere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto Playlist.**

## <a name="remarks"></a>Commenti

Questo metodo può essere usato per creare una query generica per gli elementi multimediali che corrispondono a un valore per un attributo nel database. Ciò è utile nel caso di attributi definiti dall'utente. Se l'attributo non esiste, verrà restituito un errore.

È possibile usare questo metodo per recuperare tutti gli elementi multimediali di un tipo specifico. Usare il nome dell'attributo "MediaType" e uno dei valori seguenti:



| Valore    | Descrizione                                                |
|----------|------------------------------------------------------------|
| Audio    | Musica e altri elementi solo audio.                          |
| Playlist | Playlist rappresentate come **oggetti** multimediali.                |
| radio    | Elementi della stazione radio. Non usato da Windows Media Player 10.  |
| Video    | Elementi video.                                               |
| Foto    | Elementi foto. Richiede Windows Media Player 10.             |
| altro    | Altri elementi, ad esempio file ASF o URL ai supporti di streaming. |



 

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene *utilizzato MediaCollection*. **getByAttribute per** riprodurre tutto il contenuto della libreria dell'artista chiamato Triode 48. **L'oggetto** Player è stato creato con ID = "Player".


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

 

 





