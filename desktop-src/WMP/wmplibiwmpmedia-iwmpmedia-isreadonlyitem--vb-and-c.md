---
title: Metodo IWMPMedia isReadOnlyItem
description: Il metodo isReadOnlyItem restituisce un valore che indica se è possibile modificare gli attributi dell'elemento multimediale specificato.
ms.assetid: c810c5c1-8cb9-4ac7-ac49-1ebdc86f5d7f
keywords:
- Metodo isReadOnlyItem Windows Media Player
- Metodo isReadOnlyItem Windows Media Player, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, metodo isReadOnlyItem
topic_type:
- apiref
api_name:
- IWMPMedia.isReadOnlyItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21d3dfefc1222832783e62962298da8bcb02b25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332390"
---
# <a name="iwmpmediaisreadonlyitem-method"></a>Metodo IWMPMedia:: isReadOnlyItem

Il metodo **isReadOnlyItem** restituisce un valore che indica se è possibile modificare gli attributi dell'elemento multimediale specificato.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Boolean isReadOnlyItem(
  System.String bstrItemName
);
```


```VB

Public Function isReadOnlyItem( _
  ByVal bstrItemName As System.String _
) As System.Boolean
Implements IWMPMedia.isReadOnlyItem
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrItemName* \[ in\]
</dt> <dd>

**System. String** che rappresenta il nome dell'elemento multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore **System. Boolean** che indica se gli attributi sono di sola lettura.

## <a name="remarks"></a>Commenti

Se un attributo è di sola lettura, non può essere impostato con il metodo **setItemInfo** . Si noti che questo metodo può restituire valori diversi per un attributo specifico se usato con versioni diverse di Windows Media Player.

Prima di chiamare questo metodo, è necessario disporre dell'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **isReadOnlyItem** per inserire una casella di testo a più righe con informazioni sull'elemento multimediale corrente. Il codice Visualizza ogni attributo dell'elemento multimediale corrente, insieme al testo che indica se l'attributo è di sola lettura o in lettura/scrittura. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
// Store a WMPLib.IWMPMedia3 interface to the current media item.
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes in the current media item.
int attCount = player.currentMedia.attributeCount;

// Create an array to store the list of attribute information.
string[] atInfo = new string[attCount];

// Create a variable to hold each attribute name.
string atName;

// Loop through the attribute list.
for (int i = 0; i < cm.attributeCount; i++)
{
    // Get the attribute name.
    atName = cm.getAttributeName(i);

    // Test whether the attribute is read-only.
    string test = ((cm.isReadOnlyItem(atName)) ? "Read-Only" : "Read/Write");

    // Store the attribute information in the array.
    atInfo[i] = (atName + " is " + test);
}

// Display the attribute information in the text box.
rwText.Lines = atInfo;
```


```VB

' Store a WMPLib.IWMPMedia3 interface to the current media item.
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes in the current media item.
Dim attCount As Integer = player.currentMedia.attributeCount

&#39; Create an array to store the list of attribute information.
Dim atInfo(attCount) As String

&#39; Create a variable to hold each attribute name.
Dim atName As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (cm.attributeCount - 1)

    &#39; Get the attribute name.
    atName = cm.getAttributeName(i)

    &#39; Test whether the attribute is read-only.
    If (cm.isReadOnlyItem(atName)) Then

        atInfo(i) = (atName + &quot; is Read-Only&quot;)

    Else

        atInfo(i) = (atName + &quot; is Read/Write&quot;)

    End If

Next i

&#39; Display the attribute information in the text box.
rwText.Lines = atInfo
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

[**IWMPMedia. setItemInfo (VB e C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





