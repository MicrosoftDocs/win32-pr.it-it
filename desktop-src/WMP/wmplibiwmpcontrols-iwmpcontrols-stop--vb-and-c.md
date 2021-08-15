---
title: Metodo stop IWMPControls
description: Il metodo stop arresta la riproduzione dell'elemento multimediale. | Metodo stop IWMPControls
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- Metodo stop Windows Media Player
- Metodo stop Windows Media Player, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player , metodo stop
topic_type:
- apiref
api_name:
- IWMPControls.stop
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f941ac90fa86cdd16dedf5349c0a6d614c57f49bc91009f5d62c56bb83144bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332076"
---
# <a name="iwmpcontrolsstop-method"></a>Metodo IWMPControls::stop

Il **metodo stop** arresta la riproduzione dell'elemento multimediale.

## <a name="syntax"></a>Sintassi


```CSharp
public void stop();
```


```VB

Public Sub stop()
Implements IWMPControls.stop
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo Windows Media Player rilasciare tutte le risorse di sistema in uso, ad esempio il dispositivo audio. L'elemento multimediale corrente, tuttavia, non viene rilasciato.

Quando Windows Media Player viene arrestata, la posizione di riproduzione corrente nell'elemento multimediale viene reimpostata all'inizio dell'elemento. Successivamente, **la chiamata a IWMPControls.play** inizierà la riproduzione dall'inizio dell'elemento multimediale. Per interrompere un'operazione di riproduzione senza modificare la posizione corrente, usa il **metodo IWMPControls.pause.**

## <a name="examples"></a>Esempio

L'esempio seguente usa **stop** per arrestare l'elemento multimediale corrente in risposta all'evento Click di un pulsante. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void stopButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("stop"))
    {
        controls.stop();
    }
}
```


```VB

Public Sub stopButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles stopButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;stop&quot;)) Then

        controls.stop()

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

[**IWMPControls.next (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[**IWMPControls.pause (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls.previous (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





