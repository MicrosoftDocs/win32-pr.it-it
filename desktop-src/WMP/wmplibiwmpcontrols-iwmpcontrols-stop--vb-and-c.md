---
title: Metodo Stop IWMPControls
description: Il metodo Stop interrompe la riproduzione dell'elemento multimediale. | Metodo Stop IWMPControls
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- arresta il metodo Windows Media Player
- Metodo Stop Media Player Windows, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, metodo Stop
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
ms.openlocfilehash: a73271098340ea0cf0a645472b5ef6333ae0f4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332469"
---
# <a name="iwmpcontrolsstop-method"></a>Metodo IWMPControls:: Stop

Il metodo **Stop** interrompe la riproduzione dell'elemento multimediale.

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

Questo metodo fa in modo che Windows Media Player rilasciare tutte le risorse di sistema utilizzate, ad esempio il dispositivo audio. L'elemento multimediale corrente, tuttavia, non viene rilasciato.

Quando Windows Media Player viene arrestato, la posizione di riproduzione corrente nell'elemento multimediale viene reimpostata all'inizio dell'elemento. Successivamente, la chiamata a **IWMPControls. Play** avvierà la riproduzione dall'inizio dell'elemento multimediale. Per arrestare un'operazione di riproduzione senza modificare la posizione corrente, usare il metodo **IWMPControls. pause** .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **Stop** per arrestare l'elemento multimediale corrente in risposta all'evento Click di un pulsante. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Next (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[**IWMPControls. pause (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Previous (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





