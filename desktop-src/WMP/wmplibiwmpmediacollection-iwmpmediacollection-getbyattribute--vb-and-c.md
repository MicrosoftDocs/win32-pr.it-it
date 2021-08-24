---
title: Metodo getByAttribute IWMPMediaCollection
description: Il metodo getByAttribute restituisce un'interfaccia IWMPPlaylist che corrisponde all'attributo specificato con il valore specificato.
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- Metodo getByAttribute Windows Media Player
- Metodo getByAttribute Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player metodo , getByAttribute
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fb8dab44cd1f26c080d438c15f545c882d2e4427af7fa04049b539ce8b3cf13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735021"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a>Metodo IWMPMediaCollection::getByAttribute

Il **metodo getByAttribute** restituisce **un'interfaccia IWMPPlaylist** che corrisponde all'attributo specificato con il valore specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrAttribute* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta l'attributo specificato.

</dd> <dt>

*bstrValue* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il valore specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **WMPLib.IWMPPlaylist** per gli elementi multimediali recuperati.

## <a name="remarks"></a>Commenti

Questo metodo può essere usato per creare una query generica per gli elementi multimediali che corrispondono a un valore per un attributo nella libreria. Ciò è utile nel caso di attributi definiti dall'utente. Se l'attributo non esiste, verrà restituito un errore.

È possibile usare questo metodo per recuperare tutti gli elementi multimediali di un tipo specifico. Usare il nome **dell'attributo MediaType** e uno dei valori seguenti.



| Valore    | Descrizione                                               |
|----------|-----------------------------------------------------------|
| Audio    | Musica e altri elementi solo audio                          |
| altro    | Altri elementi, ad esempio un file asf o l'URL di un flusso. |
| Foto    | Elementi foto. Richiede Windows Media Player 10.            |
| Playlist | Playlist rappresentate come elementi multimediali.                     |
| radio    | Elementi della stazione radio. Non usato da Windows Media Player 10. |
| Video    | Elementi video.                                              |



 

Prima di chiamare questo metodo, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

Per informazioni sugli attributi supportati da Windows Media Player, vedere Informazioni di [riferimento sugli attributi](attribute-reference.md).

Esistono due modi per recuperare **un'interfaccia IWMPMediaCollection** e il comportamento del metodo **getByAttribute** dipende da quale di questi due modi si usa. Se si recupera l'interfaccia chiamando [AxWindowsMediaPlayer.mediaCollection,](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)il **metodo getByAttribute** restituisce tutti gli elementi multimediali nella libreria. Tuttavia, se si recupera l'interfaccia chiamando [IWMPLibrary.mediaCollection,](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)il **metodo getByAttribute** restituisce solo gli elementi audio nella libreria con l'attributo e il valore specificati.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene utilizzato **getByAttribute** per riprodurre tutto il contenuto della libreria dell'artista denominato Triode 48. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
player.Ctlcontrols.play()
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
</dt> <dt>

[**IWMPPlaylistCollection.getAll (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





