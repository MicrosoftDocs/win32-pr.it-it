---
title: Proprietà errorCode IWMPErrorItem
description: La proprietà errorCode ottiene il codice di errore corrente.
ms.assetid: 00719067-685d-4ef2-9eec-72c7892fcdb9
keywords:
- proprietà errorCode Windows Media Player
- proprietà errorCode Windows Media Player, interfaccia IWMPErrorItem
- Interfaccia IWMPErrorItem Windows Media Player , proprietà errorCode
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorCode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d7179684fb0332e25716282adfd47a5f769493f646f73c82d0391bbce4e6a91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031211"
---
# <a name="iwmperroritemerrorcode-property"></a>Proprietà IWMPErrorItem::errorCode

La **proprietà errorCode** ottiene il codice di errore corrente.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 errorCode {get; set;}
```


```VB

Public ReadOnly Property errorCode As System.Int32
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.Int32** che rappresenta il codice di errore.

## <a name="remarks"></a>Commenti

È necessario impostare **IWMPSettings.enableErrorDialogs** su **false** se si sceglie di visualizzare messaggi di errore personalizzati.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene **utilizzato errorCode** in un gestore eventi Error per visualizzare il codice di errore all'utente. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void player_ErrorEvent_errorCode(object sender, System.EventArgs e)
{
    // Get the error code for the first error item.
    int errCode = player.Error.get_Item(0).errorCode;

    // Display the error code.
    System.Windows.Forms.MessageBox.Show("Error number: " + errCode.ToString());
}
```


```VB

Public Sub player_ErrorEvent_errorCode(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error code for the first error item.
    Dim errCode As Integer = player.Error.Item(0).errorCode

    &#39; Display the error code.
    System.Windows.Forms.MessageBox.Show(&quot;Error number: &quot; + errCode.ToString())

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

[**Interfaccia IWMPErrorItem (VB e C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.enableErrorDialogs (VB e C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





