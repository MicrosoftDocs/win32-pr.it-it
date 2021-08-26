---
title: Proprietà IWMPNetwork framesSkipped
description: La proprietà framesSkipped ottiene il numero totale di fotogrammi ignorati durante la riproduzione.
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- proprietà framesSkipped Windows Media Player
- proprietà framesSkipped Windows Media Player , interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player , proprietà framesSkipped
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
ms.openlocfilehash: 3640ff73eeadd1bf59eecc29045b0434f0885b7dc1eef319d6e6ee040442abdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999981"
---
# <a name="iwmpnetworkframesskipped-property"></a>Proprietà IWMPNetwork::framesSkipped

La **proprietà framesSkipped** ottiene il numero totale di fotogrammi ignorati durante la riproduzione.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.Int32** che rappresenta il numero di frame ignorati.

## <a name="examples"></a>Esempio

L'esempio di codice seguente **usa framesSkipped** per visualizzare il numero totale di fotogrammi ignorati durante la riproduzione. Le informazioni vengono visualizzate in un'etichetta quando l'utente fa clic su un pulsante. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


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
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





