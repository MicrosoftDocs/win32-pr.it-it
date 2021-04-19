---
title: Proprietà currentPosition di IWMPControls
description: La proprietà currentPosition Ottiene o imposta la posizione corrente nell'elemento multimediale in secondi dall'inizio.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- Finestra delle proprietà di currentPosition Media Player
- Proprietà di currentPosition Media Player Windows, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player, proprietà currentPosition
topic_type:
- apiref
api_name:
- IWMPControls.currentPosition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee8c2c8244d6034069f21033978ce2883ff852d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332487"
---
# <a name="iwmpcontrolscurrentposition-property"></a>Proprietà IWMPControls:: currentPosition

La proprietà **currentPosition** Ottiene o imposta la posizione corrente nell'elemento multimediale in secondi dall'inizio.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a>Valore proprietà

**System. Double** che rappresenta la posizione corrente.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **currentPosition** per cercare una posizione fornita dall'utente. In risposta a un clic del pulsante, **currentPosition** è impostato sul valore immesso in una casella di testo denominata NewPosition. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
private void setPosition_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text);
}
```


```VB

Public Sub setPosition_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setPosition.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text)

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

[**IWMPControls. currentPositionString (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





