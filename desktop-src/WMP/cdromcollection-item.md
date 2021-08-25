---
title: Metodo CdromCollection.item
description: Il metodo item recupera l'oggetto Cdrom in corrispondenza dell'indice specificato.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- Metodo item Windows Media Player
- Metodo item Windows Media Player , classe CdromCollection
- Classe CdromCollection Windows Media Player , metodo item
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
ms.openlocfilehash: a5f700a17c29c382e96a5601bd9bbfabf3c4ede1b253d9f271b1d37ab1106ee2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864081"
---
# <a name="cdromcollectionitem-method"></a>Metodo CdromCollection.item

Il **metodo item** recupera l'oggetto **Cdrom** in corrispondenza dell'indice specificato.

## <a name="syntax"></a>Sintassi


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

**Numero** (**long**) contenente l'indice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto Cdrom.**

## <a name="remarks"></a>Commenti

Per usare questo metodo, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

**Windows Media Player 10 Mobile:** Questo metodo non è supportato.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene *utilizzato CdromCollection*. **per** stampare il nome della playlist da ogni CD disponibile nel computer. Se l'unità contiene effettivamente contenuto DVD, è Windows XP o versione successiva. È stato creato un elemento TextArea HTML con ID = "playlists". **L'oggetto Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Cdrom.driveSpecifier**](cdrom-drivespecifier.md)
</dt> <dt>

[**Oggetto CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**CdromCollection.count**](cdromcollection-count.md)
</dt> <dt>

[**Playlist.name**](playlist-name.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





