---
title: Metodo di riproduzione IWMPControls
description: Il metodo play avvia la riproduzione dell'elemento multimediale corrente o riprende la riproduzione di un elemento sospeso.
ms.assetid: 02e00df6-4dc1-44bb-9826-e69e8298ccaa
keywords:
- Metodo play Windows Media Player
- Metodo play Windows Media Player, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, metodo play
topic_type:
- apiref
api_name:
- IWMPControls.play
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2823c5f9846ec2569da0ede6629a4b7e8c04c7b61e14060451c8d0cf3a02f71d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761021"
---
# <a name="iwmpcontrolsplay-method"></a>Metodo IWMPControls::p lay

Il **metodo play** avvia la riproduzione dell'elemento multimediale corrente o riprende la riproduzione di un elemento sospeso.

## <a name="syntax"></a>Sintassi


```CSharp
public void play();
```


```VB

Public Sub play()
Implements IWMPControls.play
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se questo metodo viene chiamato durante l'inoltro rapido o il riavvolgimento, la velocità di riproduzione (il valore di **IWMPSettings.rate)** è impostata su 1.0.

## <a name="examples"></a>Esempio

L'esempio seguente usa **play** per riprodurre l'elemento multimediale corrente in risposta all'evento Click di un pulsante. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void playButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("play"))
    {
        controls.play();
    }
}
```


```VB

Public Sub playButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;play&quot;)) Then

        controls.play()

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

[**IWMPControls.playItem (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.rate (VB e C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





