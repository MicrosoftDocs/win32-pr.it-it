---
title: Proprietà bufferingTime di IWMPNetwork
description: La proprietà bufferingTime ottiene o imposta la quantità di tempo in millisecondi allocata per il buffering dei dati in ingresso prima dell'inizio della riproduzione.
ms.assetid: b5936b21-a17b-4801-a5fc-c6d6521e05aa
keywords:
- BufferingTime - proprietà Windows Media Player
- Proprietà bufferingTime Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player proprietà , bufferingTime
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d224e35dd9c87dad627e71f2ae07d3d0b9e24ee1b094cfa5dea549e86c69a65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999991"
---
# <a name="iwmpnetworkbufferingtime-property"></a>Proprietà IWMPNetwork::bufferingTime

La **proprietà bufferingTime** ottiene o imposta la quantità di tempo in millisecondi allocata per il buffering dei dati in ingresso prima dell'inizio della riproduzione.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 bufferingTime {get; set;}
```


```VB

Public Property bufferingTime As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System.Int32** che rappresenta il tempo di memorizzazione nel buffer in millisecondi, compreso tra zero e 60.000 con un valore predefinito di 5.000.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene **utilizzato bufferingTime per** specificare il numero di secondi allocati per il buffering dei dati in ingresso. Una casella di testo consente all'utente di immettere un nuovo valore per **bufferingTime** e la proprietà viene aggiornata in risposta all'evento Click di un pulsante. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void setBufTime_Click(object sender, System.EventArgs e)
{
    // Retrieve input from the user and convert it to an integer.
    int newTime = System.Convert.ToInt32(bufText.Text);

    // Test whether the integer is within the valid range. 
    if (newTime >= 0 & newTime <= 60) 
    {
        // Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000);
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("Buffering time must be between 0 and 60.");
    }
}
```


```VB

Public Sub setBufTime_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setBufTime.Click

    &#39; Retrieve input from the user and convert it to an integer.
    Dim newTime As Integer = System.Convert.ToInt32(bufText.Text)

    &#39; Test whether the integer is within the valid range. 
    If (newTime >= 0 And newTime <= 60) Then

        &#39; Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000)

    Else

        System.Windows.Forms.MessageBox.Show(&quot;Buffering time must be between 0 and 60.&quot;)

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

[**Interfaccia IWMPNetwork (VB e C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





