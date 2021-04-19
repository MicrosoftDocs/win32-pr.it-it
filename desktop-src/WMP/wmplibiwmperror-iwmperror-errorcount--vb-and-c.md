---
title: Proprietà errorCount di IWMPError
description: La proprietà errorCount ottiene il numero di errori nella coda degli errori.
ms.assetid: a30750c8-2025-4087-bd2b-f313ccbde38c
keywords:
- Finestra delle proprietà di errorCount Media Player
- Proprietà di errorCount Media Player Windows, interfaccia IWMPError
- Interfaccia IWMPError Windows Media Player, proprietà errorCount
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
ms.openlocfilehash: b62c16f07260847c91f1c9f18885587444a4ceb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332436"
---
# <a name="iwmperrorerrorcount-property"></a>Proprietà IWMPError:: errorCount

La proprietà **ErrorCount** ottiene il numero di errori nella coda degli errori.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 errorCount {get; set;}
```


```VB

Public ReadOnly Property errorCount As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta il numero di errori.

## <a name="remarks"></a>Commenti

È necessario impostare **IWMPSettings. enableErrorDialogs** su **false** se si sceglie di visualizzare i messaggi di errore personalizzati.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **ErrorCount** in un gestore eventi di errore per avvisare l'utente dell'errore più recente nella coda degli errori. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPError (VB e C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. enableErrorDialogs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





