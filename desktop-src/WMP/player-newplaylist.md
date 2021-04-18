---
title: Player. nuova playlist, metodo
description: Il metodo nuova playlist crea un nuovo oggetto playlist.
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- Metodo nuova playlist Windows Media Player
- Metodo nuova playlist Windows Media Player, classe Player
- Classe Player Windows Media Player, metodo nuova playlist
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
ms.openlocfilehash: fa65ae4b453fe919116a33c5ee86b14ba353f681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324977"
---
# <a name="playernewplaylist-method"></a>Player. nuova playlist, metodo

Il metodo **nuova playlist** crea un nuovo oggetto **playlist** .

## <a name="syntax"></a>Sintassi


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome* \[ in\]
</dt> <dd>

**Stringa** contenente il nome della nuova playlist.

</dd> <dt>

*URL* \[ di in\]
</dt> <dd>

**Stringa** contenente l'URL della playlist Windows Media Metafile con la quale creare l'oggetto **playlist** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un oggetto **playlist** .

## <a name="remarks"></a>Commenti

Se il parametro *URL* è impostato su null o su "" (stringa vuota), verrà creato un oggetto **playlist** vuoto. Se il parametro *Name* è impostato su "", viene usato il nome del metafile.

La nuova playlist creata con questo metodo non viene aggiunta alla libreria. Per aggiungere una nuova playlist alla libreria, usare *PlaylistCollection*. **importPlaylist** o *PlaylistCollection*. **nuova playlist**. Eventuali spazi iniziali o finali nel nome della playlist vengono rimossi automaticamente quando vengono aggiunti alla libreria.

Poiché la libreria consente più playlist con lo stesso nome, è consigliabile verificare la presenza di una playlist con un nome specificato prima di aggiungerne una nuova.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Player**](player-object.md)
</dt> <dt>

[**PlaylistCollection. importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**PlaylistCollection. nuova playlist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Metafile di Windows Media**](windows-media-metafiles.md)
</dt> </dl>

 

 





