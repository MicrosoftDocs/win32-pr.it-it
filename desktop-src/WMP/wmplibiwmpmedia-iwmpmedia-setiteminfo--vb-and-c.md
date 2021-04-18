---
title: Metodo IWMPMedia setItemInfo
description: Il metodo setItemInfo imposta il valore dell'attributo specificato per l'elemento multimediale.
ms.assetid: 247bbba5-7d9b-489d-8e41-ae8ec6e266fd
keywords:
- Metodo setItemInfo Windows Media Player
- Metodo setItemInfo Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, metodo setItemInfo
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
ms.openlocfilehash: 6702c80c13090a370e2922ccecade49bc06645de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328578"
---
# <a name="iwmpmediasetiteminfo-method"></a>Metodo IWMPMedia:: setItemInfo

Il metodo **setItemInfo** imposta il valore dell'attributo specificato per l'elemento multimediale.

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

*bstrItemName* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome dell'attributo.

</dd> <dt>

*bstrVal* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nuovo valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La proprietà **attributeCount** ottiene il numero di attributi disponibili per un determinato elemento multimediale. I numeri di indice possono quindi essere usati con il metodo **GetAttribute** per determinare i nomi degli attributi predefiniti che possono essere usati con questo metodo.

Prima di utilizzare questo metodo, utilizzare il metodo **isReadOnlyItem** per individuare se è possibile impostare un particolare attributo.

Prima di chiamare questo metodo, è necessario disporre dell'accesso completo alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Nota

Se si incorpora il controllo Windows Media Player nell'applicazione, gli attributi di file modificati non verranno scritti nel file multimediale digitale fino a quando l'utente non esegue Windows Media Player.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **setItemInfo** per modificare il valore dell'attributo genre per l'elemento multimediale corrente. Una casella di testo consente all'utente di immettere una stringa che viene quindi usata per modificare le informazioni sugli attributi in risposta all'evento Click di un pulsante. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


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
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB e C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. GetAttribute (VB e C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. isReadOnlyItem (VB e C#)**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)
</dt> </dl>

 

 





