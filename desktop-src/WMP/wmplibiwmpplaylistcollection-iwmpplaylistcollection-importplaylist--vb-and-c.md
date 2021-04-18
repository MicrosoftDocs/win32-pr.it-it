---
title: Metodo IWMPPlaylistCollection importPlaylist
description: Il metodo importPlaylist aggiunge una playlist statica alla libreria. | Metodo IWMPPlaylistCollection importPlaylist
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- Metodo importPlaylist Windows Media Player
- Metodo importPlaylist Windows Media Player, interfaccia IWMPPlaylistCollection
- Interfaccia IWMPPlaylistCollection Windows Media Player, metodo importPlaylist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.importPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ca727155d6ae859123d427812d93ebaa0b05c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324715"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a>Metodo IWMPPlaylistCollection:: importPlaylist

Il metodo **importPlaylist** aggiunge una playlist statica alla libreria.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylist importPlaylist(
  IWMPPlaylist pItem
);
```


```VB

Public Function importPlaylist( _
  ByVal pItem As IWMPPlaylist _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.importPlaylist
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*pItem* \[ in\]
</dt> <dd>

Interfaccia **wmplib. IWMPPlaylist** per la playlist che verrà aggiunta da questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **wmplib. IWMPPlaylist** per la playlist aggiunta.

## <a name="remarks"></a>Commenti

Le playlist che non contengono elementi multimediali non possono essere aggiunte alla libreria utilizzando questo metodo. Per creare una playlist vuota nella libreria, usare il metodo **nuova playlist** . È quindi possibile compilare la playlist risultante con elementi multimediali usando **IWMPPlaylist. appendItem** o **IWMPPlaylist. InsertItem**.

Se si passa questo metodo una playlist automatica, la query viene eseguita una volta e il risultato viene aggiunto alla libreria come playlist statica. Per aggiungere una playlist automatica alla libreria e mantenerne il comportamento automatico, usare **IWMPMediaCollection. Add**. Per altre informazioni, vedere [playlist statiche e automatiche](static-and-auto-playlists.md).

Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva.<br/>                                                                     |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMPMediaCollection. Add (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. appendItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylistCollection (VB e C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. nuova playlist (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





