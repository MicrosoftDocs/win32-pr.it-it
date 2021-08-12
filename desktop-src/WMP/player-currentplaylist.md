---
title: Player.currentPlaylist
description: La proprietà currentPlaylist specifica o recupera l'oggetto Playlist corrente.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- Player.currentPlaylist Windows Media Player
topic_type:
- apiref
api_name:
- Player.currentPlaylist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7139c567eab5fbb3c324916dec260d34f57429cb50bb99d199f35be8aee7a1c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573216"
---
# <a name="playercurrentplaylist"></a>Player.currentPlaylist

La proprietà currentPlaylist specifica o recupera l'oggetto **Playlist** corrente.

## <a name="syntax"></a>Sintassi

*lettore* . **currentPlaylist**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un oggetto Playlist **di** lettura/scrittura.

## <a name="remarks"></a>Commenti

Se *l'Impostazioni*. **la proprietà autoStart** è true, la riproduzione inizia automaticamente ogni volta che si imposta **currentPlaylist**.

Questa proprietà accetta un oggetto Playlist, che può essere acquisito in diversi modi, ad esempio chiamando *PlaylistArray*. **elemento** o *PlaylistCollection*. **newPlaylist**. Per caricare un elemento **playlist** usando un nome file, impostare la proprietà URL o usare *Player*. **newPlaylist**.

## <a name="examples"></a>Esempio

Nell'JScript seguente viene recuperata la prima playlist nella libreria. Usa quindi **currentPlaylist** per impostare la playlist recuperata come playlist corrente e quindi per visualizzare il nome della playlist corrente. **L'oggetto** Player è stato creato con ID = "Player".


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player.newPlaylist**](player-newplaylist.md)
</dt> <dt>

[**Oggetto Playlist**](playlist-object.md)
</dt> <dt>

[**PlaylistArray.item**](playlistarray-item.md)
</dt> <dt>

[**PlaylistCollection.newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Impostazioni.autoStart**](settings-autostart.md)
</dt> </dl>

 

 





