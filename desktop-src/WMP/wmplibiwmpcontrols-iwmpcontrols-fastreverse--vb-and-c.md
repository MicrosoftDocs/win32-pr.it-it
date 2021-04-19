---
title: Metodo IWMPControls fastReverse
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
ms.openlocfilehash: 7061481aea13b0ed83c3a3d0eb47ca24b940358b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332483"
---
# <a name="iwmpcontrolsfastreverse-method"></a>Metodo IWMPControls:: fastReverse

Il metodo **fastReverse** avvia la riproduzione rapida dell'elemento multimediale nella direzione inversa.

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

Il metodo **fastReverse** analizza il clip in senso inverso cinque volte la velocità normale, visualizzando solo i fotogrammi chiave se si tratta di un file video. La chiamata di **fastReverse** equivale a specificare-5,0 per la frequenza impostando la proprietà **IWMPSettings. rate** . Se la frequenza viene modificata in seguito o se viene chiamato **IWMPControls. Play** o **IWMPControls. stop** , Windows Media Player interromperà velocemente.

Se l'elemento fa parte di una playlist, **fastReverse** si interrompe all'inizio della traccia corrente. Ad esempio, se Track 3 si trova in **fastReverse**, quando si raggiunge l'inizio di Track 3, Windows Media Player non passerà a Track 2. Il numero di Play non viene incrementato quando si chiama **fastReverse**.

Se si chiama **IWMPControls. fastForward** mentre **fastReverse** è in esecuzione, **fastReverse** verrà arrestato e **IWMPControls. fastForward** inizierà.

Questo metodo non funziona per trasmissioni live e determinati tipi di supporti digitali. Per determinare se è possibile utilizzare l'inversione veloce in un clip, passare il valore **System. String** "FastReverse" alla proprietà **IWMPControls.** IsValid (il metodo **IWMPControls. \_ Get** in C#).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **fastReverse** per invertire l'elemento multimediale corrente in risposta all'evento Click di un pulsante. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. fastForward (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls. disavailable (VB e C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Stop (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. rate (VB e C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





