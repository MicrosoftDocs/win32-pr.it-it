---
title: AxWindowsMediaPlayer.uiMode - proprietà
description: La proprietà uiMode ottiene o imposta un valore che indica quali controlli vengono visualizzati nell'interfaccia utente.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- Proprietà uiMode Windows Media Player
- Proprietà uiMode Windows Media Player , classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player proprietà uiMode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.uiMode
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f1d716d36aafbd3625ae1144e0adde1abf0898bee4cbe6831d627cea97bb9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618771"
---
# <a name="axwindowsmediaplayeruimode-property"></a>AxWindowsMediaPlayer.uiMode - proprietà

La proprietà uiMode ottiene o imposta un valore che indica quali controlli vengono visualizzati nell'interfaccia utente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a>Valore proprietà

Oggetto System.String che è uno dei valori seguenti.



| Valore     | Descrizione                                                                                                                                                                                                     | Esempio di audio                                                   | Esempio di video                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| invisibile | Windows Media Player è incorporato senza alcuna interfaccia utente visibile (controlli, video o finestra di visualizzazione).                                                                                                  | Non viene visualizzato nulla.                                         | Non viene visualizzato nulla.                                         |
| Nessuno      | Windows Media Player è incorporato senza controlli e con solo la finestra video o di visualizzazione visualizzata.                                                                                                   | ![uimode = 'none' con audio](images/uimode-none-audio-v11.png) | ![uimode = 'none' con video](images/uimode-none-video-v11.png) |
| Mini      | Windows Media Player incorporato con la finestra di stato, i controlli play/pause, stop, mute e volume visualizzati oltre alla finestra video o di visualizzazione.                                                    | ![uimode = 'mini' con audio](images/uimode-mini-audio-v11.png) | ![uimode = 'mini' con video](images/uimode-mini-video-v11.png) |
| completi      | Valore predefinito. Windows Media Player è incorporato con la finestra di stato, la barra di ricerca, la riproduzione/sospensione, l'arresto, l'disattivazione dell'audio, il successivo, il precedente, il avanzamento rapido, il riavvolgimento e i controlli del volume oltre alla finestra video o di visualizzazione. | ![uimode = 'full' con audio](images/uimode-full-audio-v11.png) | ![uimode = 'full' con video](images/uimode-full-video-v11.png) |
| custom    | Windows Media Player è incorporato con un'interfaccia utente personalizzata. Può essere usato solo nei programmi C++.                                                                                                                | Viene visualizzata l'interfaccia utente personalizzata.                           | Viene visualizzata l'interfaccia utente personalizzata.                           |



 

## <a name="remarks&quot;></a>Commenti

Questa proprietà specifica l'aspetto dell'oggetto Windows Media Player. Quando **uiMode è** impostato su &quot;none&quot;, &quot;mini&quot; o &quot;full&quot;, è presente una finestra per la visualizzazione di clip video e visualizzazioni audio. Questa finestra può essere nascosta in modalità mini o completa impostando l'attributo **height** del tag **OBJECT** su 40, misurato dal basso, e lasciando visibile la parte dei controlli dell'interfaccia utente. Se non si desidera alcuna interfaccia incorporata, impostare entrambi gli attributi **width** **e height** su zero.

Se **uiMode è** impostato su &quot;invisible&quot;, non viene visualizzata alcuna interfaccia utente, ma lo spazio è ancora riservato nella pagina come specificato da **width** e **height.** Ciò è utile per mantenere il layout di pagina quando **uiMode** può cambiare. Inoltre, lo spazio riservato è trasparente, quindi tutti gli elementi a livelli dietro il controllo saranno visibili.

Se **uiMode è** impostato su &quot;full&quot; o &quot;mini&quot;, Windows Media Player i controlli di trasporto in modalità schermo intero. Se **uiMode è** impostato su &quot;none&quot;, non vengono visualizzati controlli in modalità schermo intero.

Se la finestra è visibile e viene riprodotto il contenuto audio, la visualizzazione visualizzata sarà quella usata più di recente in Windows Media Player.

Se **uiMode** è impostato su &quot;custom&quot; in un programma C++ che implementa **IWMPRemoteMediaServices,** viene visualizzato il file di interfaccia indicato da **IWMPRemoteMediaServices.GetCustomUIMode.**

Durante la riproduzione a schermo intero, Windows Media Player il cursore del mouse quando **enableContextMenu** è uguale a false e **uiMode** è uguale a &quot;none&quot;.

## <a name=&quot;examples&quot;></a>Esempio

Nell'esempio seguente viene creata una casella di riepilogo che consente all'utente di modificare la modalità dell'interfaccia utente per un oggetto Windows Media Player incorporato. L'oggetto AxWMPLib.AxWindowsMediaPlayer è rappresentato dalla variabile denominata player.


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible");
uiModeOptions.Items.Add("none");
uiModeOptions.Items.Add("mini");
uiModeOptions.Items.Add("full");


private void uiModeOptions_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Get the selected UI mode in the list box as a string.
    string newMode = (string)(((System.Windows.Forms.ListBox)sender).SelectedItem);
     
    // Set the UI mode that the user selected.
    player.uiMode = newMode;            
}
```


```VB

' Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible&quot;)
uiModeOptions.Items.Add(&quot;none&quot;)
uiModeOptions.Items.Add(&quot;mini&quot;)
uiModeOptions.Items.Add(&quot;full&quot;)


Public Sub uiModeOptions_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles uiModeOptions.SelectedIndexChanged

    &#39; Get the selected UI mode in the list box as a string.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim newMode As String = lb.SelectedItem

    &#39; Set the UI mode that the user selected.
    player.uiMode = newMode

End Sub
```





## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player versione 7.0 o successiva. Windows Media Player serie 9 o successive per "invisibili" o "personalizzate"<br/>   |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.enableContextMenu (VB e C#)**](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





