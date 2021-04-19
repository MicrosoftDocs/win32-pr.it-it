---
title: Proprietà currentItem di IWMPControls
description: La proprietà currentItem Ottiene o imposta l'elemento multimediale corrente in una playlist.
ms.assetid: 0a331b1f-95bd-48ea-b951-1ca35cc96865
keywords:
- Finestra delle proprietà di currentItem Media Player
- Proprietà di currentItem Media Player Windows, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, proprietà currentItem
topic_type:
- apiref
api_name:
- IWMPControls.currentItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae04eb333e2fd347fa6f88b33ec2482a4dd8fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332490"
---
# <a name="iwmpcontrolscurrentitem-property"></a>Proprietà IWMPControls:: currentItem

La proprietà **CurrentItem** Ottiene o imposta l'elemento multimediale corrente in una playlist.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPMedia currentItem {get; set;}
```


```VB

Public Property currentItem As IWMPMedia
```





## <a name="property-value"></a>Valore proprietà

Interfaccia **wmplib. IWMPMedia** che rappresenta l'elemento multimediale.

## <a name="remarks"></a>Commenti

Questa proprietà funziona solo con gli elementi nella playlist corrente. L'impostazione di **CurrentItem** sull'interfaccia di un elemento multimediale salvato non è supportata.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **CurrentItem** per impostare l'elemento multimediale corrente del lettore su un elemento selezionato da una casella di riepilogo. La casella di riepilogo è stata compilata con tutti gli elementi nella playlist corrente. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
private void playItem_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedItem = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop();

    // Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.get_Item(selectedItem);
    
    // Play the current item.
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playItem_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles playItem.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedItem As Integer = lb.SelectedIndex

    &#39; Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop()

    &#39; Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.Item(selectedItem)

    &#39; Play the current item.
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

[**IWMPControlsInterface (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPMediaInterface (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





