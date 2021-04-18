---
title: Metodo IWMPMediaCollection getByAttribute
description: Il metodo getByAttribute restituisce un'interfaccia IWMPPlaylist che corrisponde all'attributo specificato con il valore specificato.
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- Metodo getByAttribute Windows Media Player
- Metodo getByAttribute Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player, metodo getByAttribute
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
ms.openlocfilehash: dd7adba98fbfa450cd938b56ec6d91598b918d0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333642"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a>Metodo IWMPMediaCollection:: getByAttribute

Il metodo **getByAttribute** restituisce un'interfaccia **IWMPPlaylist** che corrisponde all'attributo specificato con il valore specificato.

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

*bstrAttribute* \[ in\]
</dt> <dd>

**System. String** che rappresenta l'attributo specificato.

</dd> <dt>

*bstrValue* \[ in\]
</dt> <dd>

**System. String** che corrisponde al valore specificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **wmplib. IWMPPlaylist** per gli elementi multimediali recuperati.

## <a name="remarks"></a>Commenti

Questo metodo può essere utilizzato per creare una query generica per gli elementi multimediali che corrispondono a un valore per un attributo nella libreria. Questa operazione è utile nel caso di attributi definiti dall'utente. Se l'attributo non esiste, verrà generato un errore.

È possibile utilizzare questo metodo per recuperare tutti gli elementi multimediali di un tipo specifico. Usare il nome dell'attributo **mediaType** e uno dei valori seguenti.



| Valore    | Descrizione                                               |
|----------|-----------------------------------------------------------|
| Audio    | Musica e altri elementi solo audio                          |
| altro    | Altri elementi, ad esempio un file con estensione ASF o l'URL di un flusso. |
| Foto    | Elementi foto. Richiede Windows Media Player 10.            |
| playlist | Playlist rappresentate come elementi multimediali.                     |
| radio    | Elementi della stazione di radio. Non usato da Windows Media Player 10. |
| Video    | Elementi video.                                              |



 

Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Per informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).

Esistono due modi per recuperare un'interfaccia **IWMPMediaCollection** e il comportamento del metodo **getByAttribute** dipende da quali di questi due modi si usano. Se si recupera l'interfaccia chiamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), il metodo **getByAttribute** restituisce tutti gli elementi multimediali nella libreria. Tuttavia, se si recupera l'interfaccia chiamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), il metodo **getByAttribute** restituisce solo gli elementi audio della raccolta con l'attributo e il valore specificati.

## <a name="examples"></a>Esempio

L'esempio di codice seguente usa **getByAttribute** per riprodurre tutto il contenuto dalla libreria dall'artista denominato triodo 48. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getAll (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





