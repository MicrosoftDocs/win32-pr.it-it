---
title: Metodo IWMPMediaCollection getByAuthor
description: Il metodo getByAuthor restituisce un'interfaccia IWMPPlaylist che fornisce l'accesso agli elementi multimediali dall'autore specificato.
ms.assetid: eb3793f6-bad1-4c80-991e-c6d0093ae57f
keywords:
- Metodo getByAuthor Windows Media Player
- Metodo getByAuthor Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player metodo , getByAuthor
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAuthor
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829232e6cd9fb64fec1d209991c3734ad435b4b69d0d7b66b135ab9cca1fe4a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053609"
---
# <a name="iwmpmediacollectiongetbyauthor-method"></a>Metodo IWMPMediaCollection::getByAuthor

Il `getByAuthor` metodo restituisce **un'interfaccia IWMPPlaylist** che fornisce l'accesso agli elementi multimediali dall'autore specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylist getByAuthor(
  System.String bstrAuthor
);
```


```VB

Public Function getByAuthor( _
  ByVal bstrAuthor As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAuthor
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrAuthor* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il nome dell'autore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **WMPLib.IWMPPlaylist** per gli elementi multimediali recuperati.

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

Esistono due modi per recuperare **un'interfaccia IWMPMediaCollection** e il comportamento del metodo dipende da quale di questi due modi `getByAuthor` si usa. Se si recupera l'interfaccia chiamando [AxWindowsMediaPlayer.mediaCollection,](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)il metodo restituisce tutti gli elementi `getByAuthor` multimediali nella libreria. Tuttavia, se si recupera l'interfaccia chiamando [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), il metodo restituisce solo gli elementi audio nella libreria con l'attributo e `getByAuthor` il valore specificati.

## <a name="examples"></a>Esempio

L'esempio seguente `getByAuthor` usa per creare una playlist di elementi multimediali quando l'utente fa clic su un pulsante. La playlist contiene elementi corrispondenti al nome dell'autore specificato dall'utente in una casella di testo. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void playAuthor_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the author's name from the text box. 
    string author = getAuthor.Text;

    // Create the playlist using getByAuthor. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAuthor(author);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAuthor_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAuthor.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the author&#39;s name from the text box. 
    Dim author As String = getAuthor.Text

    &#39; Create the playlist using getByAuthor. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAuthor(author)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





