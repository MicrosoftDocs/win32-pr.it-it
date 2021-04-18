---
title: Metodo IWMPMediaCollection getByAlbum
description: Il metodo getByAlbum restituisce un'interfaccia IWMPPlaylist che fornisce l'accesso agli elementi multimediali dall'album specificato.
ms.assetid: 26f004c0-de46-4792-8212-9d4ac749bb21
keywords:
- Metodo getByAlbum Windows Media Player
- Metodo getByAlbum Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player, metodo getByAlbum
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAlbum
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c455e9bd61038a4d72bb6537d7c62b30a5d0b733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333644"
---
# <a name="iwmpmediacollectiongetbyalbum-method"></a>Metodo IWMPMediaCollection:: getByAlbum

Il metodo **getByAlbum** restituisce un'interfaccia **IWMPPlaylist** che fornisce l'accesso agli elementi multimediali dall'album specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylist getByAlbum(
  System.String bstrAlbum
);
```


```VB

Public Function getByAlbum( _
  ByVal bstrAlbum As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAlbum
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrAlbum* \[ in\]
</dt> <dd>

**System. String** che rappresenta il titolo dell'album.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **wmplib. IWMPPlaylist** per gli elementi multimediali recuperati.

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Esistono due modi per recuperare un'interfaccia **IWMPMediaCollection** e il comportamento del metodo **getByAlbum** dipende da quali di questi due modi si usano. Se si recupera l'interfaccia chiamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), il metodo **getByAlbum** restituisce tutti gli elementi multimediali nella libreria. Tuttavia, se si recupera l'interfaccia chiamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), il metodo **getByAlbum** restituisce solo gli elementi audio della libreria che appartengono all'album specificato.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **getByAlbum** per creare una playlist di elementi multimediali quando l'utente fa clic su un pulsante. La playlist contiene elementi con l'album specificato dall'utente in una casella di testo. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
private void playAlbum_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the album title text that the user entered in the text box. 
    string album = getAlbum.Text;

    // Create the playlist using getByAlbum. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAlbum(album);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAlbum_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAlbum.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the album title text that the user entered in the text box. 
    Dim album As String = getAlbum.Text

    &#39; Create the playlist using getByAlbum. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAlbum(album)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





