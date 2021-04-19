---
title: IWMPPlaylist. Item (VB e C)
description: La proprietà Item (il \_ metodo Get Item in C \) ottiene un'interfaccia per l'elemento multimediale in corrispondenza dell'indice specificato.
ms.assetid: 874663e2-0b89-4ef7-9d4a-3a334482b352
keywords:
- IWMPPlaylist. Item (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1318f37c3f590eec2c97252e2f484b0d1bc6d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324222"
---
# <a name="iwmpplaylistitem-vb-and-c"></a>IWMPPlaylist. Item (VB e C#)

La proprietà **Item** (il metodo **get \_ Item** in C#) ottiene un'interfaccia per l'elemento multimediale in corrispondenza dell'indice specificato.


```
[Visual Basic]
ReadOnly Property Item(
  lIndex As System.Int32
) As IWMPMedia
```




```
[C#]
IWMPMedia get_Item (
  System.Int32 lIndex 
);
```



## <a name="parameters"></a>Parametri

*lIndex*

**System. Int32** che rappresenta l'indice dell'elemento multimediale nella playlist.

## <a name="property-value"></a>Valore della proprietà

Interfaccia **wmplib. IWMPMedia** che fornisce l'accesso all'elemento multimediale in corrispondenza dell'indice specificato.

## <a name="remarks"></a>Commenti

**IWMPPlaylist. Item** è una proprietà di sola lettura in Visual Basic che accetta un parametro, mentre in C# viene chiamato il metodo **IWMPPlaylist. Get \_ Item** .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usata la proprietà **Item** (il metodo **get \_ Item** in C#) per recuperare un elemento multimediale da una playlist basata sulla selezione di un utente. Una casella di riepilogo è stata creata con il nome Weblist e riempita con i titoli dalla playlist denominata audioPlaylist. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
private void weblist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the selected item in the list box.
    int index = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Store the corresponding media item from the playlist.
    WMPLib.IWMPMedia listItem = audioPlaylist.get_Item(index);

    // Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL;
}
```


```VB

Public Sub weblist_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles weblist.SelectedIndexChanged

    &#39; Store the index of the selected item in the list box.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim index As Integer = lb.SelectedIndex

    &#39; Store the corresponding media item from the playlist.
    Dim listItem As WMPLib.IWMPMedia = audioPlaylist.Item(index)

    &#39; Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL

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

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. removeItem (VB e C#)**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





