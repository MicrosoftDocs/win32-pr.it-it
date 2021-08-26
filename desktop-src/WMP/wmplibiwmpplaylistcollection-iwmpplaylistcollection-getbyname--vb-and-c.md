---
title: Metodo IWMPPlaylistCollection getByName
description: Il metodo getByName restituisce un'interfaccia IWMPPlaylistArray che fornisce l'accesso alle playlist con il nome specificato, se presente.
ms.assetid: d41afab1-4103-4f59-a432-21a502499444
keywords:
- Metodo getByName Windows Media Player
- Metodo getByName Windows Media Player, interfaccia IWMPPlaylistCollection
- Interfaccia IWMPPlaylistCollection Windows Media Player metodo , getByName
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fcee45af3ef55d53a05bab290fa92d3e6842fbb097358235b6720cbb1b54e0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999741"
---
# <a name="iwmpplaylistcollectiongetbyname-method"></a>Metodo IWMPPlaylistCollection::getByName

Il **metodo getByName** restituisce **un'interfaccia IWMPPlaylistArray** che fornisce l'accesso alle playlist con il nome specificato, se presente.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylistArray getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getByName
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrName* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il nome della playlist.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **WMPLib.IWMPPlaylistArray** per la matrice recuperata di playlist.

## <a name="remarks"></a>Commenti

Usare **IWMPPlaylistArray.count per** determinare se esiste una playlist. Se **count** è zero, la matrice è vuota.

Prima di chiamare questo metodo, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene utilizzato **getByName** per controllare la raccolta di playlist per una playlist denominata "Favorites -- 4 e 5 star rated". Se esiste una playlist con tale nome, **getByName** la imposta come playlist corrente. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// Get the count of the playlists named "Favorites -- 4 and 5 star rated".
int checkit = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").count;

// Since duplicate playlist names are allowed, the count returned
// will be either zero (no playlist) or greater than zero (playlist exists).
if (checkit > 0)
{
    // Retrieve a playlist array containing "Favorites -- 4 and 5 star rated".
    // Assume that there is only one playlist with that name, and assign it to the 
    // current playlist.
    player.currentPlaylist = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").Item(0);
}
```


```VB

'  Get the count of the playlists named &quot;Favorites -- 4 and 5 star rated&quot;.
Dim checkit As Integer = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).count

&#39;  Since duplicate playlist names are allowed, the count returned
&#39;  will be either zero (no playlist) or greater than zero (playlist exists).
If (checkit > 0) Then

    &#39;  Retrieve a playlist array object containing &quot;Favorites -- 4 and 5 star rated&quot;.
    &#39;  Assume that there is only one playlist with that name, and assign it to the 
    &#39;  current playlist.
    player.currentPlaylist = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).Item(0)

End If
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive.<br/>                                                                     |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPPlaylistArray (VB e C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray.count (VB e C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylistCollection (VB e C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





