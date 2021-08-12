---
title: IWMPError - proprietà errorCount
description: La proprietà errorCount ottiene il numero di errori nella coda degli errori.
ms.assetid: a30750c8-2025-4087-bd2b-f313ccbde38c
keywords:
- Proprietà errorCount Windows Media Player
- Proprietà errorCount Windows Media Player, interfaccia IWMPError
- Interfaccia IWMPError Windows Media Player proprietà , errorCount
topic_type:
- apiref
api_name:
- IWMPError.errorCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d288d1476318b1cace98d4b7549b7f5755b383da19d88ce04cbcf271326ac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568773"
---
# <a name="iwmperrorerrorcount-property"></a>Proprietà IWMPError::errorCount

La **proprietà errorCount** ottiene il numero di errori nella coda degli errori.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 errorCount {get; set;}
```


```VB

Public ReadOnly Property errorCount As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System.Int32** che rappresenta il numero di errori.

## <a name="remarks"></a>Commenti

È consigliabile impostare **IWMPSettings.enableErrorDialogs** su **false** se si sceglie di visualizzare messaggi di errore personalizzati.

## <a name="examples"></a>Esempio

L'esempio seguente usa **errorCount** in un gestore dell'evento Error per avvisare l'utente dell'errore più recente nella coda degli errori. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void player_ErrorEvent_errorCount(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Get the description of the last error. Error items start at zero,
    // so the item index will always be one less than the error count.
    string errDesc = player.Error.get_Item(max-1).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorCount(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Get the description of the last error. Error items start at zero,
    &#39; so the item index will always be one less than the error count.
    Dim errDesc As String = player.Error.Item(max - 1).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

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

 

 





