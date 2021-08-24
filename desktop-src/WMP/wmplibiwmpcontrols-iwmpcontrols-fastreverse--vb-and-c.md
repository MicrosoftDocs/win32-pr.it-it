---
title: Metodo fastReverse IWMPControls
description: Il metodo fastReverse avvia la riproduzione rapida dell'elemento multimediale nella direzione inversa.
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- Metodo fastReverse Windows Media Player
- Metodo fastReverse Windows Media Player, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, metodo fastReverse
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bbc1442ca223765b498560d078879c9a7033011117b7f663d4d40ff26bdd93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761081"
---
# <a name="iwmpcontrolsfastreverse-method"></a>Metodo IWMPControls::fastReverse

Il **metodo fastReverse** avvia la riproduzione rapida dell'elemento multimediale nella direzione inversa.

## <a name="syntax"></a>Sintassi


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il **metodo fastReverse** analizza il clip in ordine inverso a cinque volte la velocità normale, visualizzando solo i fotogrammi chiave se si tratta di un file video. Chiamare **fastReverse** equivale a specificare -5.0 per la frequenza impostando la **proprietà IWMPSettings.rate.** Se la frequenza viene modificata successivamente o se viene chiamato **IWMPControls.play** o **IWMPControls.stop,** Windows Media Player smetterà di invertire rapidamente.

Se l'elemento fa parte di una playlist, **fastReverse** si arresta all'inizio della traccia corrente. Ad esempio, se la traccia 3 si trova in **fastReverse,** quando viene raggiunto l'inizio della traccia 3, Windows Media Player non andrà a traccia 2. Il conteggio di riproduzione non viene incrementato quando si chiama **fastReverse.**

Se **chiami IWMPControls.fastForward** mentre **fastReverse** è in esecuzione, **fastReverse** verrà arrestato e **inizierà IWMPControls.fastForward.**

Questo metodo non funziona per le trasmissioni live e alcuni tipi di supporti digitali. Per determinare se è possibile usare l'inverso rapido in un clip, passare il valore **System.String** "FastReverse" alla proprietà **IWMPControls.isAvailable** (il metodo **IWMPControls.get \_ isAvailable** in C#).

## <a name="examples"></a>Esempio

L'esempio seguente usa **fastReverse** per invertire l'elemento multimediale corrente in risposta all'evento Click di un pulsante. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

    End If

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

[**Interfaccia IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.fastForward (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls.isAvailable (VB e C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls.stop (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.rate (VB e C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





