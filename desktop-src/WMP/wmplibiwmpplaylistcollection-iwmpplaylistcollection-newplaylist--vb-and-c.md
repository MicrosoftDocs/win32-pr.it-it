---
title: Metodo IWMPPlaylistCollection nuova playlist
description: Il metodo nuova playlist restituisce un'interfaccia IWMPPlaylist per una nuova playlist vuota nella libreria.
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- Metodo nuova playlist Windows Media Player
- Metodo nuova playlist Windows Media Player, interfaccia IWMPPlaylistCollection
- Interfaccia IWMPPlaylistCollection Windows Media Player, metodo nuova playlist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.newPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc455c5815cee1aaac139886bca1d847ddc62b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324713"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a>Metodo IWMPPlaylistCollection:: nuova playlist

Il metodo **nuova playlist** restituisce un'interfaccia **IWMPPlaylist** per una nuova playlist vuota nella libreria.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.newPlaylist
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrName* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome della nuova playlist.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **wmplib. IWMPPlaylist** per la nuova playlist.

## <a name="remarks"></a>Commenti

Questo metodo crea una playlist vuota nella libreria. Per riempire la playlist con elementi multimediali, usare **IWMPPlaylist. appendItem** o **IWMPPlaylist. InsertItem**.

Nella libreria sono consentite più playlist con lo stesso nome. Per evitare di creare un nome di playlist duplicato con questo metodo, usare il metodo **GetByName** e **IWMPPlaylistArray. Count** per individuare se una playlist con un determinato nome esiste già.

Gli spazi iniziali e finali non sono consentiti nei nomi delle playlist e vengono rimossi automaticamente dal valore specificato per il parametro *bstrName* .

Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creata una nuova playlist vuota denominata "Three", che viene aggiunta alla raccolta di playlist e viene restituita un'interfaccia. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva.<br/>                                                                     |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. appendItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray. Count (VB e C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylistCollection (VB e C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





