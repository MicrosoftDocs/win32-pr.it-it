---
title: Metodo Player.newPlaylist
description: Il metodo newPlaylist crea un nuovo oggetto Playlist.
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- Metodo newPlaylist Windows Media Player
- Metodo newPlaylist Windows Media Player , classe Player
- Classe Player Windows Media Player , metodo newPlaylist
topic_type:
- apiref
api_name:
- Player.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380d1f2751487f5c648b154852be625a5c93103851541dea7e2488ba75080ca0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572831"
---
# <a name="playernewplaylist-method"></a>Metodo Player.newPlaylist

Il **metodo newPlaylist** crea un nuovo **oggetto Playlist.**

## <a name="syntax"></a>Sintassi


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*name* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome della nuova playlist.

</dd> <dt>

*URL* \[ Pollici\]
</dt> <dd>

**Stringa** contenente l'URL della playlist Windows metafile multimediale con cui creare l'oggetto **Playlist.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **oggetto Playlist.**

## <a name="remarks"></a>Commenti

Se il *parametro URL* è impostato su Null o "" (stringa vuota), verrà creato un oggetto **Playlist** vuoto. Se il *parametro name* è impostato su "", viene usato il nome nel metafile.

La nuova playlist creata con questo metodo non viene aggiunta alla libreria. Per aggiungere una nuova playlist alla libreria, usare *PlaylistCollection*. **importPlaylist** o *PlaylistCollection*. **newPlaylist**. Gli spazi iniziali o finali nel nome della playlist vengono rimossi automaticamente quando vengono aggiunti alla libreria.

Poiché la libreria consente più playlist con lo stesso nome, è possibile verificare la presenza di una playlist con un nome specificato prima di aggiungerne una nuova.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**PlaylistCollection.newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Windows Metafile multimediali**](windows-media-metafiles.md)
</dt> </dl>

 

 





