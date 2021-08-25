---
title: Metodo pause IWMPControls
description: Il metodo pause sospende la riproduzione dell'elemento multimediale. | Metodo pause IWMPControls
ms.assetid: 1d9ebaf3-84b4-458d-a393-2b685cd0dbfb
keywords:
- Metodo pause Windows Media Player
- Metodo pause Windows Media Player, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, metodo pause
topic_type:
- apiref
api_name:
- IWMPControls.pause
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49950b5d2c5588e27755f3845e65f0a79ce0aae6ccc4a05dd4e5af3186b879de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861881"
---
# <a name="iwmpcontrolspause-method"></a>Metodo IWMPControls::p ause

Il **metodo pause** sospende la riproduzione dell'elemento multimediale.

## <a name="syntax"></a>Sintassi


```CSharp
public void pause();
```


```VB

Public Sub pause()
Implements IWMPControls.pause
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando un file viene sospeso, Windows Media Player non c'è alcuna risorsa di sistema, ad esempio il dispositivo audio.

Per determinare se un particolare tipo di supporto può essere sospeso, passare il valore **System.String** "pause" alla proprietà **IWMPControls.isAvailable** (il **metodo IWMPControls.get \_ isAvailable** in C#).

## <a name="examples"></a>Esempio

L'esempio seguente usa **pause** per sospendere la riproduzione dell'elemento multimediale corrente in risposta all'evento Click di un pulsante. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void pauseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("pause"))
    {
        controls.pause();
    }
}
```


```VB

Public Sub pauseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles pauseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;pause&quot;)) Then

        controls.pause()

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

[**IWMPControls.isAvailable (VB e C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> </dl>

 

 





