---
title: IWMPError.Item (VB e C )
description: La proprietà Item (il metodo get \_ Item in C\) ottiene un'interfaccia IWMPErrorItem in corrispondenza dell'indice specificato nella coda degli errori.
ms.assetid: acfaaaa5-eb13-4ba0-8417-4229adc62c5d
keywords:
- IWMPError.Item (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPError.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be8d212eca9e9e54770e7e2751df345d80bbfb6bfc1b12714e811c7795990725
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575633"
---
# <a name="iwmperroritem-vb-and-c"></a>IWMPError.Item (VB e C#)

La **proprietà Item** (il metodo get **\_ Item** in C#) ottiene un'interfaccia **IWMPErrorItem** in corrispondenza dell'indice specificato nella coda degli errori.


```
[Visual Basic]
ReadOnly Property Item(
  dwIndex As System.Integer
) As IWMPErrorItem
```




```
[C#]
IWMPErrorItem get_Item (
  System.Int32 dwIndex
);
```



## <a name="parameters"></a>Parametri

*dwIndex*

**System.Int32 che rappresenta** l'indice in base zero di **un'interfaccia IWMPErrorItem** nella coda degli errori.

## <a name="property-value"></a>Valore della proprietà

Interfaccia **WMPLib.IWMPErrorItem.**

## <a name="remarks"></a>Commenti

Windows Media Player possibile generare una serie di errori in risposta a una condizione di errore. Questa proprietà ottiene un errore specifico nella coda usando un numero di indice. I numeri di indice per la coda degli errori iniziano con zero.

È consigliabile impostare **IWMPSettings.enableErrorDialogs** su **false** se si sceglie di visualizzare messaggi di errore personalizzati.

## <a name="examples"></a>Esempio

L'esempio seguente usa la proprietà **Item** (il metodo **get \_ Item** in C#) in un gestore eventi Error per recuperare e visualizzare informazioni sull'errore più recente nella coda degli errori. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void player_ErrorEvent_get_Item(object sender, System.EventArgs e)
{
    // Store the index of the most recent error.
    int max = (player.Error.errorCount - 1);

    // Get an interface for the most recent error item. Cast it to
    // a WMPLib.IWMPErrorItem2 interface to get all of the available functionality.
    WMPLib.IWMPErrorItem2 errItem = (WMPLib.IWMPErrorItem2)player.Error.get_Item(max);

    // Use the interface to access and store the error info.
    int errNum = errItem.errorCode;
    string errDesc = errItem.errorDescription;

    // Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + ":  " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_get_Item(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the index of the most recent error.
    Dim max As Integer = (player.Error.errorCount - 1)

    &#39; Get an interface for the most recent error item. 
    Dim errItem As WMPLib.IWMPErrorItem2 = player.Error.Item(max)

    &#39; Use the interface to access and store the error info.
    Dim errNum As Integer = errItem.errorCode
    Dim errDesc As String = errItem.errorDescription

    &#39; Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + &quot;:  &quot; + errDesc)

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

[**Interfaccia IWMPErrorItem (VB e C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.enableErrorDialogs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





