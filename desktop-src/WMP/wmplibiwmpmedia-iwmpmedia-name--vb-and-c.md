---
title: Proprietà name di IWMPMedia
description: La proprietà name ottiene o imposta il nome dell'elemento multimediale.
ms.assetid: d1057871-bccf-4f84-9b1d-74c41a8f7f7c
keywords:
- proprietà name Windows Media Player
- proprietà name Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player , proprietà name
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
ms.openlocfilehash: 46f4e99aaa7a05530a555cb51a6b1b10d511a342143f2be2bc7e029cc813cfba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568736"
---
# <a name="iwmpmedianame-property"></a>Proprietà IWMPMedia::name

La **proprietà name** ottiene o imposta il nome dell'elemento multimediale.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String name {get; set;}
```


```VB

Public Property name As System.String
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.String** che rappresenta il nome dell'elemento multimediale.

## <a name="remarks"></a>Commenti

Prima di usare questa proprietà, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene **utilizzato name** per modificare il nome dell'elemento multimediale corrente. Una casella di testo consente all'utente di immettere un nuovo nome e il nome viene modificato in risposta all'evento Click di un pulsante. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


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
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





