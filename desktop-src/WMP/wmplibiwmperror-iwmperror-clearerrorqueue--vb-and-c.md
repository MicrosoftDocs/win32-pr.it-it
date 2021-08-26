---
title: Metodo IWMPError clearErrorQueue
description: Il metodo clearErrorQueue cancella gli errori dalla coda degli errori. | Metodo IWMPError clearErrorQueue
ms.assetid: a8e8e666-56e4-4e75-9ed5-2714d272ce7c
keywords:
- Metodo clearErrorQueue Windows Media Player
- Metodo clearErrorQueue Windows Media Player, interfaccia IWMPError
- Interfaccia IWMPError Windows Media Player, metodo clearErrorQueue
topic_type:
- apiref
api_name:
- IWMPError.clearErrorQueue
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f75b4e4d2a0e80a3f55a38744758497abc71f5899498fee95ee3b3db752631c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000451"
---
# <a name="iwmperrorclearerrorqueue-method"></a>Metodo IWMPError::clearErrorQueue

Il **metodo clearErrorQueue** cancella gli errori dalla coda degli errori.

## <a name="syntax"></a>Sintassi


```CSharp
public void clearErrorQueue();
```


```VB

Public Sub clearErrorQueue()
Implements IWMPError.clearErrorQueue
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Utilizzare questo metodo per cancellare la coda di errori dopo l'elaborazione di una serie di errori.

È consigliabile impostare **IWMPSettings.enableErrorDialogs** su **false** se si sceglie di visualizzare messaggi di errore personalizzati.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene **utilizzato clearErrorQueue** in un gestore dell'evento Error per svuotare la coda degli errori dopo la visualizzazione di tutte le descrizioni degli errori. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void player_ErrorEvent_clearErrorQueue(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Loop through the list of errors.
    for (int i = 0; i < max; i++)
    {
        // Get the description for this error.
        string errDesc = player.Error.get_Item(i).errorDescription;

        // Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc);
    }

    // Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue();
}
```


```VB

Public Sub player_ErrorEvent_clearErrorQueue(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Loop through the list of errors.
    For i As Integer = 0 To (max - 1)

        &#39; Get the description for this error.
        Dim errDesc As String = player.Error.Item(i).errorDescription

        &#39; Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc)

    Next i

    &#39; Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue()

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

[**Interfaccia IWMPError (VB e C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.enableErrorDialogs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





