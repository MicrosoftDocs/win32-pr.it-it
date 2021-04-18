---
title: IWMPCdrom playlist (proprietà)
description: La proprietà playlist ottiene un'interfaccia IWMPPlaylist che rappresenta le tracce del CD attualmente presenti nell'unità CD o le voci del titolo a livello di radice per un DVD.
ms.assetid: 09c3db45-6586-4a5b-b72c-77c64473bdd0
keywords:
- Finestre delle proprietà della playlist Media Player
- Proprietà playlist Windows Media Player, interfaccia IWMPCdrom
- Interfaccia IWMPCdrom Windows Media Player, proprietà playlist
topic_type:
- apiref
api_name:
- IWMPCdrom.Playlist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a386881c8416f4ea1881f3ccd68ee4291aa3fa84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329673"
---
# <a name="iwmpcdromplaylist-property"></a>IWMPCdrom::P proprietà laylist

La proprietà **playlist** ottiene un'interfaccia **IWMPPlaylist** che rappresenta le tracce del CD attualmente presenti nell'unità CD o le voci del titolo a livello di radice per un DVD.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPPlaylist Playlist {get; set;}
```


```VB

Public ReadOnly Property Playlist As IWMPPlaylist
```





## <a name="property-value"></a>Valore proprietà

Interfaccia **wmplib. IWMPPlaylist** .

## <a name="remarks"></a>Commenti

In genere, il contenuto basato su DVD è organizzato in titoli. Ogni titolo contiene uno o più capitoli. Ogni DVD viene creato in modo diverso, quindi la modalità di utilizzo dei titoli e dei capitoli spetta all'autore del contenuto.

Per un DVD, questa proprietà ottiene una playlist che contiene come primo elemento un'interfaccia **IWMPMedia** denominata "DVD". Questa interfaccia rappresenta il supporto DVD. La riproduzione dell'elemento comporta la riproduzione del DVD dall'inizio se è la prima riproduzione dopo l'inserimento di un nuovo DVD o la ripresa della riproduzione se il DVD è uguale all'ultimo DVD visualizzato. Impostando questo elemento come elemento corrente durante la riproduzione, il DVD verrà riprodotto dall'inizio.

Gli elementi aggiuntivi, rappresentati dalle interfacce **IWMPMedia** , nella playlist sono titoli di DVD rappresentati da Playlist nidificate. Quando si imposta **IWMPControls. CurrentItem** in modo che corrisponda a uno di questi elementi nidificati della playlist, Windows Media Player imposta automaticamente la playlist nidificata come playlist corrente dopo l'inizio della riproduzione del capitolo. È quindi possibile usare le proprietà dell'interfaccia **IWMPPlaylist** , i metodi e gli eventi associati per lavorare con i capitoli DVD, che sono anche elementi della playlist.

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usata la **playlist** per inserire una casella di testo a più righe, denominata testo, con l'elenco di tracce del CD audio attualmente presente nella prima unità CD. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
// Get an interface that provides access to the CD playlist.
WMPLib.IWMPPlaylist playlist = player.cdromCollection.Item(0).Playlist;

// Create a string array to hold the track list.
String[] trackList = new String[playlist.count];

// Iterate through the CD playlist.
for (int i = 0; i < playlist.count; i++)
{
    trackList[i]= playlist.get_Item(i).name;
}

// Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList;
```


```VB

'  Get an interface that provides access to the CD playlist.
Dim playlist As WMPLib.IWMPPlaylist = player.cdromCollection.Item(0).Playlist

&#39;  Create a string array to hold the track list.
Dim trackList(playlist.count) As String

&#39;  Iterate through the CD playlist.
For i As Integer = 0 To (playlist.count - 1)

    trackList(i) = playlist.Item(i).name

Next i

&#39;  Display the list of CD tracks in a multi-line text box.
myText.Lines = trackList
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPCdrom (VB e C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPControls. currentItem (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





