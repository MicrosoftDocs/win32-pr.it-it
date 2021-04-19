---
title: Proprietà attributeCount di IWMPMedia
description: La proprietà attributeCount ottiene il numero di attributi che è possibile sottoporre a query e/o impostare per l'elemento multimediale.
ms.assetid: 527298ff-365d-41b0-90dd-e236d6adf6fa
keywords:
- Finestra delle proprietà di attributeCount Media Player
- Proprietà di attributeCount Media Player Windows, interfaccia IWMPMedia
- Interfaccia IWMPMedia Windows Media Player, proprietà attributeCount
topic_type:
- apiref
api_name:
- IWMPMedia.attributeCount
- IWMPMedia.get_attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5a56d06a54590afd315f04a90aa582f3a364db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332410"
---
# <a name="iwmpmediaattributecount-property"></a>Proprietà IWMPMedia:: attributeCount

La proprietà **attributeCount** ottiene il numero di attributi che è possibile sottoporre a query e/o impostare per l'elemento multimediale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```CSharp
public System.Int32 attributeCount {get;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a>Valore proprietà

**System. Int32** che rappresenta il conteggio.

## <a name="remarks"></a>Commenti

Prima di utilizzare questa proprietà, è necessario disporre dell'accesso in lettura alla libreria. Per altre informazioni, vedere [accesso alla libreria](library-access.md).

Per informazioni sugli attributi supportati da Windows Media Player, vedere il [riferimento all'attributo](attribute-reference.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene usato **attributeCount** per determinare il numero di attributi disponibili nell'elemento multimediale corrente. Il codice usa tale valore per visualizzare un elenco di nomi e valori di attributi in una casella di testo. L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.


```CSharp
// Store an IWMPMedia3 interface to the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Store the number of attributes in the current media item using attributeCount.
int numAttributes = cm.attributeCount;

// Create strings to hold each attribute name and value.
string atName;
string atValue;

// Create an array to hold the attribute list.
string [] atList = new string[numAttributes];

// Loop through the attribute list.   
for (int i = 0; i < numAttributes; i++)
{
    // Fill the strings with the attribute information.
    atName = cm.getAttributeName(i);
    atValue = cm.getItemInfo(atName);

    // Store the attribute information in an array.
    atList[i] = (atName + ": " + atValue);
}

// Display the attribute information in the text box.
attributeList.Lines = atList;
```


```VB

' Store an IWMPMedia3 interface to the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Store the number of attributes in the current media item using attributeCount.
Dim numAttributes As Integer = cm.attributeCount

&#39; Create strings to hold each attribute name and value.
Dim atName As String
Dim atValue As String

&#39; Create an array to hold the attribute list.
Dim atList(numAttributes) As String

&#39; Loop through the attribute list.   
For i As Integer = 0 To (numAttributes - 1)

    &#39; Fill the strings with the attribute information.
    atName = cm.getAttributeName(i)
    atValue = cm.getItemInfo(atName)

    &#39; Store the attribute information in an array.
    atList(i) = (atName + &quot;: &quot; + atValue)

Next i

&#39; Display the attribute information in the text box.
attributeList.Lines = atList
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

 

 





