---
title: Metodo di sospensione IWMPControls
description: Il metodo pause sospende la riproduzione dell'elemento multimediale. | Metodo di sospensione IWMPControls
ms.assetid: 1d9ebaf3-84b4-458d-a393-2b685cd0dbfb
keywords:
- sospendere il metodo Windows Media Player
- sospendere il metodo Windows Media Player, interfaccia IWMPControls
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
ms.openlocfilehash: 5cf89cfef66c84be76a529d9c0cef6ec3ae6ac40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332474"
---
# <a name="iwmpcontrolspause-method"></a>IWMPControls::p metodo ause

Il metodo **pause** sospende la riproduzione dell'elemento multimediale.

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

Quando un file viene sospeso, Windows Media Player non cede alcuna risorsa di sistema, ad esempio il dispositivo audio.

Per determinare se un particolare tipo di supporto può essere sospeso, passare il valore **System. String** "pause" alla proprietà **IWMPControls.** IsValid (il metodo **IWMPControls. Get \_ unavailable** in C#).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **pause** per sospendere la riproduzione dell'elemento multimediale corrente in risposta all'evento Click di un pulsante. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. disavailable (VB e C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> </dl>

 

 





