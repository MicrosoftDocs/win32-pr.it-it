---
title: Metodo IWMPMedia setItemInfo
description: Il metodo setItemInfo imposta il valore dell'attributo specificato per l'elemento multimediale.
ms.assetid: 247bbba5-7d9b-489d-8e41-ae8ec6e266fd
keywords:
- Metodo setItemInfo Windows Media Player
- Metodo setItemInfo Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player metodo setItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24265e94880899df96aa954f2df30ca6e4f5ae1e5b4fc20c419085e3f9f0ab14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053639"
---
# <a name="iwmpmediasetiteminfo-method"></a>Metodo IWMPMedia::setItemInfo

Il **metodo setItemInfo** imposta il valore dell'attributo specificato per l'elemento multimediale.

## <a name="syntax"></a>Sintassi


```CSharp
public void setItemInfo(
  System.String bstrItemName,
  System.String bstrVal
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrItemName As System.String, _
  ByVal bstrVal As System.String _
)
Implements IWMPMedia.setItemInfo
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrItemName* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il nome dell'attributo.

</dd> <dt>

*bstrVal* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il nuovo valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La **proprietà attributeCount** ottiene il numero di attributi disponibili per un determinato elemento multimediale. I numeri di indice possono quindi essere usati con il **metodo getAttributeName** per determinare i nomi degli attributi predefiniti che possono essere usati con questo metodo.

Prima di usare questo metodo, usare il **metodo isReadOnlyItem** per individuare se è possibile impostare un attributo specifico.

Prima di chiamare questo metodo, è necessario avere accesso completo alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

Nota

Se si incorpora il controllo Windows Media Player nell'applicazione, gli attributi di file che si modificano non verranno scritti nel file multimediale digitale finché l'utente non esegue Windows Media Player.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene **utilizzato setItemInfo** per modificare il valore dell'attributo Genre per l'elemento multimediale corrente. Una casella di testo consente all'utente di immettere una stringa, che viene quindi usata per modificare le informazioni sull'attributo in risposta all'evento Click di un pulsante. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void setNewGenre_Click(object sender, System.EventArgs e)
{
    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Get the user input from the TextBox. 
    string atValue = genText.Text;

    // Test for read-only status of the attribute. 
    if( cm.isReadOnlyItem("Genre") == false )
    {
        // Change the attribute value. 
        cm.setItemInfo("Genre", atValue);
    } 
}
```


```VB

Public Sub setNewGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewGenre.Click

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Get the user input from the TextBox. 
    Dim atValue = genText.Text

    &#39; Test for read-only status of the attribute. 
    If (cm.isReadOnlyItem(&quot;Genre&quot;) = False) Then

        &#39; Change the attribute value. 
        cm.setItemInfo(&quot;Genre&quot;, atValue)

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

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.attributeCount (VB e C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.getAttributeName (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.isReadOnlyItem (VB e C#)**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)
</dt> </dl>

 

 





