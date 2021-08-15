---
title: Metodo IWMPMediaCollection getAttributeStringCollection
description: Il metodo getAttributeStringCollection restituisce un'interfaccia IWMPStringCollection che rappresenta il set di tutti i valori per un attributo specificato all'interno di un tipo di supporto.
ms.assetid: 5ac19c04-75db-4618-9c4e-b20e2f709024
keywords:
- Metodo getAttributeStringCollection Windows Media Player
- Metodo getAttributeStringCollection Windows Media Player, interfaccia IWMPMediaCollection
- Interfaccia IWMPMediaCollection Windows Media Player metodo , getAttributeStringCollection
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAttributeStringCollection
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508630ee8a377e1542f823c1afb21521206369aa3ce489c58afae47efa268880
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331943"
---
# <a name="iwmpmediacollectiongetattributestringcollection-method"></a>Metodo IWMPMediaCollection::getAttributeStringCollection

Il **metodo getAttributeStringCollection** restituisce **un'interfaccia IWMPStringCollection** che rappresenta il set di tutti i valori per un attributo specificato all'interno di un tipo di supporto.

## <a name="syntax"></a>Sintassi


```CSharp
public IWMPStringCollection getAttributeStringCollection(
  System.String bstrAttribute,
  System.String bstrMediaType
);
```


```VB

Public Function getAttributeStringCollection( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPStringCollection
Implements IWMPMediaCollection.getAttributeStringCollection
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrAttribute* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta l'attributo per cui vengono recuperati i valori.

</dd> <dt>

*bstrMediaType* \[ Pollici\]
</dt> <dd>

Oggetto **System.String** che rappresenta il tipo di supporto per il quale vengono recuperati i valori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Interfaccia **WMPLib.IWMPStringCollection** per i valori recuperati.

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, è necessario avere accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

Per informazioni sugli attributi supportati da Windows Media Player, vedere Informazioni di [riferimento sugli attributi](attribute-reference.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene **utilizzato getAttributeStringCollection** per visualizzare un elenco di valori che corrispondono a un attributo specifico per gli elementi audio nella raccolta di supporti. Una casella di riepilogo consente all'utente di selezionare un attributo, ad esempio Artista, Genere o Album, mentre una casella di testo su più righe visualizza il risultato. **L'oggetto AxWMPLib.AxWindowsMediaPlayer** è rappresentato dalla variabile denominata player.


```CSharp
private void audioAttributes_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Retrieve the attribute type from the ListBox
    string attributeType = (string)((System.Windows.Forms.ListBox)sender).SelectedItem;

    // Get an interface to the mediaCollection.  
    WMPLib.IWMPMediaCollection2 library = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

    // Get an interface to the string collection for the attribute type the user selects.
    WMPLib.IWMPStringCollection2 all = (WMPLib.IWMPStringCollection2)library.getAttributeStringCollection(attributeType, "Audio");

    // Clear the text box of previous results.
    attributeValues.Clear();

    // Create an array to hold the attribute values.
    string[] attributeArray = new string[all.count];
    
    // Loop through the string collection.
    for (int i = 0; i < all.count; i++)
    {
        // Store the items in the array.
        attributeArray[i] = all.Item(i);
    }

    // Display the items in the text box.
    attributeValues.Lines = attributeArray;
}
```


```VB

Public Sub audioAttributes_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles audioAttributes.SelectedIndexChanged

    &#39; Retrieve the attribute type from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim attributeType As String = lb.SelectedItem

    &#39; Get an interface to the mediaCollection.  
    Dim library As WMPLib.IWMPMediaCollection2 = player.mediaCollection

    &#39; Get an interface to the string collection for the attribute type the user selects.
    Dim all As WMPLib.IWMPStringCollection2 = library.getAttributeStringCollection(attributeType, &quot;Audio&quot;)

    &#39; Clear the text box of previous results.
    attributeValues.Clear()

    &#39; Create an array to hold the attribute values.
    Dim attributeArray(all.count) As String

    &#39; Loop through the string collection.
    For i As Integer = 0 To (all.count - 1)

        &#39; Store the items in the array.
        attributeArray(i) = all.Item(i)

    Next i

    &#39; Display the items in the text box.
    attributeValues.Lines = attributeArray

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

[**Interfaccia IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPStringCollection (VB e C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





