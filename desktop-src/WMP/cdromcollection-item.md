---
title: Metodo cdromcollection. Item
description: Il metodo Item recupera l'oggetto CDROM in corrispondenza dell'indice specificato.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- Metodo Item Media Player Windows
- Metodo Item Media Player Windows, classe cdromcollection
- Classe cdromcollection Windows Media Player, metodo Item
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67dc58ae75819fa42940346b4f588b23a2f645a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333131"
---
# <a name="cdromcollectionitem-method"></a>Metodo cdromcollection. Item

Il metodo **Item** recupera l'oggetto **CDROM** in corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

**Numero** (**Long**) che contiene l'indice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **CDROM** .

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene usato *cdromcollection*. **elemento** per stampare il nome della playlist da ogni CD disponibile nel computer. Se l'unità contiene effettivamente contenuto DVD, è necessario Windows XP o versione successiva. È stato creato un elemento TextArea HTML con ID = "playlists". L'oggetto **Player** è stato creato con ID = "Player".


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Cdrom. driveSpecifier**](cdrom-drivespecifier.md)
</dt> <dt>

[**Oggetto cdromcollection**](cdromcollection-object.md)
</dt> <dt>

[**Cdromcollection. Count**](cdromcollection-count.md)
</dt> <dt>

[**Playlist.name**](playlist-name.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





