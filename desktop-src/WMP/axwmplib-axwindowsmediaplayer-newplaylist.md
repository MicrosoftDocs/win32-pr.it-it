---
title: AxWindowsMediaPlayer. nuova playlist, metodo
description: Il metodo nuova playlist restituisce un'interfaccia IWMPPlaylist per una nuova playlist.
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- Metodo nuova playlist Windows Media Player
- Metodo nuova playlist Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, metodo nuova playlist
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc82be7aae37b4c1334b79f84e9d607b4f73cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330008"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a>AxWindowsMediaPlayer. nuova playlist, metodo

Il metodo nuova playlist restituisce un'interfaccia IWMPPlaylist per una nuova playlist.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName,
  System.String bstrURL
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String, _
  ByVal bstrURL As System.String _
) As IWMPPlaylist
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrName* 
</dt> <dd>

**System. String** che rappresenta il nome della nuova playlist.

</dd> <dt>

*bstrURL* 
</dt> <dd>

**System. String** che rappresenta l'URL della playlist Windows Media Metafile utilizzata per inizializzare la nuova playlist.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia WMPLib. IWMPPlaylist che rappresenta la playlist appena creata.

## <a name="remarks"></a>Commenti

Se il parametro *bstrURL* è una stringa di lunghezza zero o null (""), questo metodo crea una **playlist** vuota. Se il parametro *bstrName* è una stringa di lunghezza zero (""), questo metodo applica il nome del metafile corrente.

La nuova playlist creata con questo metodo non viene aggiunta alla libreria. Per aggiungere una nuova playlist alla libreria, usare IWMPPlaylistCollection. **importPlaylist** o IWMPPlaylistCollection. **nuova playlist**. Eventuali spazi iniziali o finali nel nome della playlist vengono rimossi automaticamente quando vengono aggiunti alla libreria.

Poiché la libreria consente più playlist con lo stesso nome, è consigliabile verificare la presenza di una playlist con un nome specificato prima di aggiungerne una nuova.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                          |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. importPlaylist (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. nuova playlist (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





