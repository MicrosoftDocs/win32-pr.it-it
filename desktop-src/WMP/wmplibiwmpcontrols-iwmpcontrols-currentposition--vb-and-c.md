---
title: Proprietà currentPosition IWMPControls
description: La proprietà currentPosition ottiene o imposta la posizione corrente nell'elemento multimediale in secondi dall'inizio.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- Proprietà currentPosition Windows Media Player
- Proprietà currentPosition Windows Media Player, interfaccia IWMPControls
- Interfaccia IWMPControls Windows Media Player proprietà , currentPosition
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
ms.openlocfilehash: ac8eca861240256899fa19513fc1fb64cd540d47acb213f718674ebbda2d5f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053669"
---
# <a name="iwmpcontrolscurrentposition-property"></a>Proprietà IWMPControls::currentPosition

La **proprietà currentPosition** ottiene o imposta la posizione corrente nell'elemento multimediale in secondi dall'inizio.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a>Valore proprietà

**System.Double** che rappresenta la posizione corrente.

## <a name="examples"></a>Esempio

L'esempio seguente **usa currentPosition** per cercare una posizione fornita dall'utente. In risposta al clic di un pulsante, **currentPosition** viene impostato sul valore immesso in una casella di testo denominata newPosition. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


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
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentPositionString (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





