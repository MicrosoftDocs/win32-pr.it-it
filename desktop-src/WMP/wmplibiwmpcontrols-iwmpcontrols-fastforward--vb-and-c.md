---
title: Metodo IWMPControls fastForward
description: Il metodo fastForward avvia la riproduzione rapida dell'elemento multimediale nella direzione in avanti. | Metodo IWMPControls fastForward
ms.assetid: 44609d63-1d1a-489c-ac17-60b6d3ddc588
keywords:
- Metodo fastForward Windows Media Player
- Metodo fastForward Windows Media Player, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, metodo fastForward
topic_type:
- apiref
api_name:
- IWMPControls.fastForward
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d99307a7b188b238157af62833273b8c724eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332486"
---
# <a name="iwmpcontrolsfastforward-method"></a>Metodo IWMPControls:: fastForward

Il metodo **fastForward** avvia la riproduzione rapida dell'elemento multimediale nella direzione in avanti.

## <a name="syntax"></a>Sintassi


```CSharp
public void fastForward();
```


```VB

Public Sub fastForward()
Implements IWMPControls.fastForward
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo **fastForward** riproduce il clip in cinque volte la velocità normale. La chiamata di **fastForward** equivale a specificare 5,0 per la frequenza impostando la proprietà **IWMPSettings. rate** . Se la frequenza viene modificata in seguito o se viene chiamato **IWMPControls. Play** o **IWMPControls. stop** , Windows Media Player interromperà l'invio rapido.

Il metodo **fastForward** non funziona per le trasmissioni live e per determinati tipi di supporti. Per determinare se è possibile eseguire rapidamente l'avanzamento in un clip, passare il valore **System. String** "fastforward" alla proprietà **IWMPControls.** IsValid (il metodo **IWMPControls. \_ Get** in C#).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **fastForward** per eseguire rapidamente l'avanzamento dell'elemento multimediale corrente in risposta all'evento Click di un pulsante. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
private void fastForwardButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastForward"))
    {
        controls.fastForward();
    }
}
```


```VB

Public Sub fastForwardButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastForwardButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface. 
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastForward&quot;)) Then

        controls.fastForward()

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

[**IWMPControls. disavailable (VB e C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Stop (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. rate (VB e C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





