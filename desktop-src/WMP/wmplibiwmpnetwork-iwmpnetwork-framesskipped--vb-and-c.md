---
title: Proprietà framesSkipped di IWMPNetwork
description: La proprietà framesSkipped ottiene il numero totale di frame ignorati durante la riproduzione.
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- Finestra delle proprietà di framesSkipped Media Player
- Proprietà di framesSkipped Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, proprietà framesSkipped
topic_type:
- apiref
api_name:
- IWMPNetwork.framesSkipped
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8409cec50089111184f96e4463f57cc9c4fbae07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328282"
---
# <a name="iwmpnetworkframesskipped-property"></a>Proprietà IWMPNetwork:: framesSkipped

La proprietà **framesSkipped** ottiene il numero totale di frame ignorati durante la riproduzione.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta il numero di frame ignorati.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene usato **framesSkipped** per visualizzare il numero totale di frame ignorati durante la riproduzione. Le informazioni vengono visualizzate in un'etichetta quando l'utente fa clic su un pulsante. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
private void showFramesSkipped_Click(object sender, System.EventArgs e)
{
    framesSkippedLabel.Text = ("Frames skipped: " + player.network.framesSkipped.ToString());
}
```


```VB

Public Sub showFramesSkipped_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showFramesSkipped.Click

    framesSkippedLabel.Text = (&quot;Frames skipped: &quot; + player.network.framesSkipped.ToString())

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

[**Interfaccia IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





