---
title: Proprietà Name di IWMPMedia
description: La proprietà Name ottiene o imposta il nome dell'elemento multimediale.
ms.assetid: d1057871-bccf-4f84-9b1d-74c41a8f7f7c
keywords:
- Proprietà nome Windows Media Player
- Proprietà nome Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, proprietà Name
topic_type:
- apiref
api_name:
- IWMPMedia.name
- IWMPMedia.get_name
- IWMPMedia.put_name
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c526fc9847b06d0f7b6f4ebadf71761fd29a9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332388"
---
# <a name="iwmpmedianame-property"></a>Proprietà IWMPMedia:: Name

La proprietà **Name** Ottiene o imposta il nome dell'elemento multimediale.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String name {get; set;}
```


```VB

Public Property name As System.String
```





## <a name="property-value"></a>Valore proprietà

**System. String** che rappresenta il nome dell'elemento multimediale.

## <a name="remarks"></a>Commenti

Prima di utilizzare questa proprietà, è necessario disporre dell'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene utilizzato **Name** per modificare il nome dell'elemento multimediale corrente. Una casella di testo consente all'utente di immettere un nuovo nome e il nome viene modificato in risposta all'evento Click di un pulsante. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
private void setNewName_Click(object sender, System.EventArgs e)
{
    // ...Add code to ensure that the TextBox contains a valid value.

    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Change the name. 
    cm.name = nameText.Text;
}
```


```VB

Public Sub setNewName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewName.Click

    &#39; ...Add code to ensure that the TextBox contains a valid value.

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Change the name. 
    cm.name = nameText.Text

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

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





