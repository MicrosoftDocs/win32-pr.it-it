---
title: Playlist. Item (metodo)
description: Il metodo Item recupera l'elemento multimediale in corrispondenza dell'indice specificato.
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- Metodo Item Media Player Windows
- Metodo Item Media Player Windows, classe playlist
- Classe playlist Windows Media Player, metodo Item
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
ms.openlocfilehash: 79c69386871aeec33dbc36a066ce3f75e80d7514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332541"
---
# <a name="playlistitem-method"></a>Playlist. Item (metodo)

Il metodo **Item** recupera l'elemento multimediale in corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

**Numero** (**Long**) che contiene l'indice dell'elemento da recuperare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **multimediale** .

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene utilizzata la *playlist*. **elemento** per recuperare un elemento multimediale dalla playlist corrente in base a una selezione dell'utente. È stato creato un elemento HTML SELECT denominato "Weblist", che è stato compilato con i titoli della playlist corrente. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> <dt>

[**Playlist. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Playlist. removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





