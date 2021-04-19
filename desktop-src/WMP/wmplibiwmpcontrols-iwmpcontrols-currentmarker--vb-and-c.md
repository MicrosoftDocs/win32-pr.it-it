---
title: Proprietà currentMarker di IWMPControls
description: La proprietà currentMarker Ottiene o imposta il numero di marcatore corrente.
ms.assetid: faf8c32a-66de-47ce-aa3d-6699d9f9bdda
keywords:
- Finestra delle proprietà di currentMarker Media Player
- Proprietà di currentMarker Media Player Windows, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, proprietà currentMarker
topic_type:
- apiref
api_name:
- IWMPControls.currentMarker
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfbcea42594b15b8da08248d38b5d8f72a1de29d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332489"
---
# <a name="iwmpcontrolscurrentmarker-property"></a>Proprietà IWMPControls:: currentMarker

La proprietà **currentMarker** Ottiene o imposta il numero di marcatore corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 currentMarker {get; set;}
```


```VB

Public Property currentMarker As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta il numero del marcatore.

## <a name="remarks"></a>Commenti

L'impostazione di **currentMarker** fa sì che la riproduzione venga avviata dal marcatore specificato. Prima di provare a impostare **currentMarker**, determinare se un file contiene marcatori e il numero di marcatori utilizzando **IWMPMedia. markerCount**. Se un file non ha marcatori, l'impostazione di **currentMarker** su qualsiasi elemento, ma con zero, genera un errore. L'impostazione di **currentMarker** su un numero maggiore di **markerCount** genera anche un errore.

La proprietà **currentMarker** restituisce sempre il marcatore corrente o ultimo, il che significa che la posizione effettiva del file può essere in corrispondenza del marcatore corrente o prima del marcatore successivo. I marcatori sono numerati a partire da 1, pertanto se un file contiene marcatori, è possibile impostare **currentMarker** su zero per modificare la posizione del file su zero.

Fino a quando non viene impostato l'elemento multimediale corrente (usando **AxWindowsMediaPlayer. URL** o **AxWindowsMediaPlayer. CurrentMedia**), **currentMarker** restituisce zero.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **currentMarker** per avviare la riproduzione video dal marcatore che corrisponde alla proprietà SelectedIndex di una casella di riepilogo che è stata riempita con identificatori del marcatore. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
// Fill the list box with the marker identifiers of the current media item.
markers.Items.Add("Begining");
markers.Items.Add("Sunrise");
markers.Items.Add("Car chase");
markers.Items.Add("Happy ending");

// Set the currentMarker to the marker selected from the list box.
private void markers_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedMarker = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    player.Ctlcontrols.currentMarker = selectedMarker;
}
```


```VB

' Fill the list box with the marker identifiers of the current media item.
markers.Items.Add(&quot;Begining&quot;)
markers.Items.Add(&quot;Sunrise&quot;)
markers.Items.Add(&quot;Car chase&quot;)
markers.Items.Add(&quot;Happy ending&quot;)

&#39; Set the currentMarker to the marker selected from the list box.
Public Sub markers_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles markers.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedMarker As Integer = lb.SelectedIndex

    player.Ctlcontrols.currentMarker = selectedMarker

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

[**AxWindowsMediaPlayer. currentMedia (VB e C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB e C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. markerCount (VB e C#)**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





