---
title: Proprietà durata IWMPMedia
description: La proprietà duration ottiene la durata in secondi dell'elemento multimediale corrente.
ms.assetid: f8a0bf3e-eeaf-46f5-90c8-d3b11ce4eb39
keywords:
- Proprietà duration Windows Media Player
- Proprietà duration Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player , proprietà duration
topic_type:
- apiref
api_name:
- IWMPMedia.duration
- IWMPMedia.get_duration
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38703c37e73ba6312970b8e5b929441c3c5c9ccd1f034ab244dc97c36c2d2162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506021"
---
# <a name="iwmpmediaduration-property"></a>Proprietà IWMPMedia::d uration

La **proprietà duration** ottiene la durata in secondi dell'elemento multimediale corrente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Double duration {get;}
```


```VB

Public ReadOnly Property duration As System.Double
```





## <a name="property-value"></a>Valore proprietà

**System.Double che** rappresenta la durata in secondi.

## <a name="remarks"></a>Commenti

Se questa proprietà viene usata con un elemento multimediale diverso da quello specificato in AxWindowsMediaPlayer.currentMedia, potrebbe non contenere un valore valido.

Per recuperare la durata dei file non presenti nella libreria dell'utente, è necessario attendere Windows Media Player aprire il file. ciò significa che **l'oggetto OpenState corrente** deve essere uguale a **MediaOpen.** È possibile verificarlo gestendo **AxWindowsMediaPlayer. \_ Evento \_ OpenStateChange WMPOCXEvents** o controllando periodicamente il valore di **AxWindowsMediaPlayer.openState.**

Per le playlist, la durata di ogni elemento multimediale può essere recuperata all'apertura del singolo elemento multimediale, anziché all'apertura della playlist.

Prima di usare questa proprietà, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria.](library-access.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene **utilizzata la durata** per visualizzare il tempo rimanente nell'elemento multimediale corrente in un'etichetta. Un timer aggiorna il testo nell'etichetta ogni secondo.


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 

private void TimerEventProcessor(object sender, System.EventArgs e)
{
    // Subtract the current position from the duration of the current media to get
    // the time remaining. Use the Math.floor method to round the result down to the
    // nearest whole number.
    double t = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition);

    // Display the time remaining in the current media.
    timeRemaining.Text = ("Seconds remaining: " + t.ToString());        
}
```


```VB

' Set the timer to fire an event every second and start the timer.
Timer.Interval = 1000
Timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a Select Case statement to
&#39; determine when to start and stop the timer. 

Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles Timer.Tick

    &#39; Subtract the current position from the duration of the current media to get
    &#39; the time remaining. Use the Math.Floor method to round the result down to the
    &#39; nearest whole number.
    Dim t As Double = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition)

    &#39; Display the time remaining in the current media.
    timeRemaining.Text = (&quot;Seconds remaining: &quot; + t.ToString())

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

[**AxWindowsMediaPlayer.currentMedia (VB e C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.openState (VB e C#)**](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer.OpenStateChange (VB e C#)**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.durationString (VB e C#)**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)
</dt> </dl>

 

 





