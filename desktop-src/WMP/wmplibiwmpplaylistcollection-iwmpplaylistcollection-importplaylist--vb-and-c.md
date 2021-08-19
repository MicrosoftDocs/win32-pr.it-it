---
title: Metodo IWMPPlaylistCollection importPlaylist
description: Il metodo importPlaylist aggiunge una playlist statica alla libreria. | Metodo IWMPPlaylistCollection importPlaylist
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- Metodo importPlaylist Windows Media Player
- Metodo importPlaylist Windows Media Player, interfaccia IWMPPlaylistCollection
- Interfaccia IWMPPlaylistCollection Windows Media Player , metodo importPlaylist
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
ms.openlocfilehash: 3ee4c231a045b39454908753dc197c95e26d85c711968f07ab27dbd859c29c6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122531"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a>Metodo IWMPPlaylistCollection::importPlaylist

Il **metodo importPlaylist** aggiunge una playlist statica alla libreria.

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

*pItem* \[ Pollici\]
</dt> <dd>

Interfaccia **WMPLib.IWMPPlaylist** per la playlist che verrà aggiunta da questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **WMPLib.IWMPPlaylist** per la playlist aggiunta.

## <a name="remarks"></a>Commenti

Le playlist che non contengono elementi multimediali non possono essere aggiunte alla libreria usando questo metodo. Per creare una playlist vuota nella libreria, usare il **metodo newPlaylist.** È quindi possibile riempire la playlist risultante con elementi multimediali usando **IWMPPlaylist.appendItem** o **IWMPPlaylist.insertItem.**

Se si passa questo metodo a una playlist automatica, la query viene eseguita una sola volta e il risultato viene aggiunto alla libreria come playlist statica. Per aggiungere una playlist automatica alla libreria e mantenere il comportamento automatico, usare **IWMPMediaCollection.add**. Per altre informazioni, vedere [Playlist statiche e auto.](static-and-auto-playlists.md)

Prima di chiamare questo metodo, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successiva.<br/>                                                                     |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMPMediaCollection.add (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.appendItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.insertItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylistCollection (VB e C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.newPlaylist (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





