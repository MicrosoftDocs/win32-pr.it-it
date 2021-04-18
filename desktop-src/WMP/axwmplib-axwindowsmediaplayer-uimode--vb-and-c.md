---
title: Proprietà AxWindowsMediaPlayer. uiMode
description: La proprietà uiMode Ottiene o imposta un valore che indica quali controlli vengono visualizzati nell'interfaccia utente.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- Finestra delle proprietà di uiMode Media Player
- Proprietà uiMode Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà uiMode
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
ms.openlocfilehash: 33edcf6bdff9e1587269df9eb49c3729099d091e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330899"
---
# <a name="axwindowsmediaplayeruimode-property"></a>Proprietà AxWindowsMediaPlayer. uiMode

La proprietà uiMode Ottiene o imposta un valore che indica quali controlli vengono visualizzati nell'interfaccia utente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a>Valore proprietà

System. String che corrisponde a uno dei valori seguenti.



| Valore     | Descrizione                                                                                                                                                                                                     | Esempio di audio                                                   | Esempio video                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| invisibile | Windows Media Player è incorporato senza alcuna interfaccia utente visibile (controlli, video o finestra di visualizzazione).                                                                                                  | Non viene visualizzato alcun elemento.                                         | Non viene visualizzato alcun elemento.                                         |
| Nessuno      | Windows Media Player viene incorporato senza controlli e con solo la finestra video o visualizzazione visualizzata.                                                                                                   | ![uiMode =' none ' con audio](images/uimode-none-audio-v11.png) | ![uiMode =' none ' con video](images/uimode-none-video-v11.png) |
| minima      | Windows Media Player è incorporato con la finestra di stato, i controlli di riproduzione, sospensione, arresto, silenziamento e volume visualizzati oltre alla finestra video o visualizzazione.                                                    | ![uiMode =' mini ' con audio](images/uimode-mini-audio-v11.png) | ![uiMode =' mini ' con video](images/uimode-mini-video-v11.png) |
| completi      | Valore predefinito. Windows Media Player viene incorporato con la finestra di stato, la barra di ricerca, i controlli di riproduzione, pausa, arresto, silenziamento, avanti, precedente, avanzamento rapido, Rewind e volume oltre alla finestra video o visualizzazione. | ![uiMode =' Full ' con audio](images/uimode-full-audio-v11.png) | ![uiMode =' Full ' con video](images/uimode-full-video-v11.png) |
| custom    | Windows Media Player è incorporato con un'interfaccia utente personalizzata. Può essere usato solo nei programmi C++.                                                                                                                | Viene visualizzata l'interfaccia utente personalizzata.                           | Viene visualizzata l'interfaccia utente personalizzata.                           |



 

## <a name="remarks&quot;></a>Commenti

Questa proprietà specifica l'aspetto della Media Player Windows incorporata. Quando **uiMode** è impostato su &quot;None&quot;, &quot;mini&quot; o &quot;full&quot;, per la visualizzazione di clip video e visualizzazioni audio è presente una finestra. Questa finestra può essere nascosta in modalità mini o full impostando l'attributo **Height** del tag **Object** su 40, che viene misurato dalla parte inferiore e lascia visibile la parte Controls dell'interfaccia utente. Se non si desidera alcuna interfaccia incorporata, impostare gli attributi **Width** e **Height** su zero.

Se **uiMode** è impostato su &quot;invisibile&quot;, non viene visualizzata alcuna interfaccia utente, ma lo spazio è ancora riservato nella pagina come specificato in **larghezza** e **altezza**. Questa operazione è utile per mantenere il layout di pagina quando è possibile modificare **uiMode** . Inoltre, lo spazio riservato è trasparente, quindi tutti gli elementi a livelli dietro il controllo saranno visibili.

Se **uiMode** è impostato su &quot;full&quot; o &quot;mini&quot;, Windows Media Player Visualizza i controlli di trasporto in modalità schermo intero. Se **uiMode** è impostato su &quot;None&quot;, non viene visualizzato alcun controllo in modalità schermo intero.

Se la finestra è visibile e il contenuto audio viene riprodotto, la visualizzazione visualizzata sarà quella usata più di recente in Windows Media Player.

Se **uiMode** è impostato su &quot;Custom&quot; in un programma C++ che implementa **IWMPRemoteMediaServices**, viene visualizzato il file dell'interfaccia indicato da **IWMPRemoteMediaServices. GetCustomUIMode** .

Durante la riproduzione a schermo intero, Windows Media Player nasconde il cursore del mouse quando **enableContextMenu** è uguale a false e **uiMode** è uguale a &quot;None&quot;.

## <a name=&quot;examples&quot;></a>Esempio

Nell'esempio seguente viene creata una casella di riepilogo che consente all'utente di modificare la modalità di interfaccia utente per un oggetto Windows Media Player incorporato. L'oggetto AxWMPLib. AxWindowsMediaPlayer è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player versione 7,0 o successiva. Windows Media Player 9 Series o versione successiva per "invisibile" o "personalizzato"<br/>   |
| Spazio dei nomi<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. enableContextMenu (VB e C#)**](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





