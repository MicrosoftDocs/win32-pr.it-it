---
title: Metodo Playlist.item
description: Il metodo item recupera l'elemento multimediale in corrispondenza dell'indice specificato.
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- Metodo item Windows Media Player
- metodo item Windows Media Player , classe Playlist
- Classe Playlist Windows Media Player metodo , item
topic_type:
- apiref
api_name:
- Playlist.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72987feb8438edc50c28bb6349b44c4f43736549c92a293794a6bc728ed7853a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862231"
---
# <a name="playlistitem-method"></a>Metodo Playlist.item

Il **metodo item** recupera l'elemento multimediale in corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) contenente l'indice dell'elemento da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto Media.**

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata *la playlist*. **elemento** per recuperare un elemento multimediale dalla playlist corrente in base a una selezione dell'utente. È stato creato un elemento HTML SELECT con il nome "weblist" e riempito con i titoli della playlist corrente. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
// Store the value of the selected item in the list box
// using the selectedIndex property.
var index = weblist.selectedIndex;

// Store the corresponding digital media object from the current playlist.
var listItem = Player.currentPlaylist.item(index);

// Set the URL using the listItem variable.
Player.URL = listItem.sourceURL;

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Oggetto Playlist**](playlist-object.md)
</dt> <dt>

[**Playlist.insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Playlist.removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





