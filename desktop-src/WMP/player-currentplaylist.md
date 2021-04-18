---
title: Player. currentPlaylist
description: La proprietà currentPlaylist specifica o recupera l'oggetto playlist corrente.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- Player. currentPlaylist Windows Media Player
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
ms.openlocfilehash: ceae33a201086d268942e47496874678ec13f459
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331223"
---
# <a name="playercurrentplaylist"></a>Player. currentPlaylist

La proprietà currentPlaylist specifica o recupera l'oggetto **playlist** corrente.

## <a name="syntax"></a>Sintassi

*Player* . **currentPlaylist**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un oggetto **playlist** di lettura/scrittura.

## <a name="remarks"></a>Commenti

Se le *Impostazioni*. la proprietà **autostart** è true, la riproduzione viene avviata automaticamente quando si imposta **currentPlaylist**.

Questa proprietà accetta un oggetto playlist, che può essere acquisito in diversi modi, ad esempio chiamando *PlaylistArray*. **Item** o *PlaylistCollection*. **nuova playlist**. Per caricare un elemento della **playlist** usando un nome file, impostare la proprietà URL o usare *Player*. **nuova playlist**.

## <a name="examples"></a>Esempio

Nell'esempio JScript seguente viene recuperata la prima playlist nella libreria. USA quindi **currentPlaylist** per fare in modo che la playlist recuperata sia la playlist corrente e quindi per visualizzare il nome della playlist corrente. L'oggetto **Player** è stato creato con ID = "Player".


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
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**Player. nuova playlist**](player-newplaylist.md)
</dt> <dt>

[**Oggetto playlist**](playlist-object.md)
</dt> <dt>

[**PlaylistArray. Item**](playlistarray-item.md)
</dt> <dt>

[**PlaylistCollection. nuova playlist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Impostazioni. avvio automatico**](settings-autostart.md)
</dt> </dl>

 

 





