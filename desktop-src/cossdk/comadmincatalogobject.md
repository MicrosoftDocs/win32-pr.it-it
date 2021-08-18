---
description: Rappresenta gli elementi nelle raccolte nel catalogo COM+. Usarlo per recuperare e modificare le proprietà esposte da un elemento in una raccolta.
ms.assetid: 1d7f248b-20ec-4b34-88ab-3c68bef72b5a
title: Classe COMAdminCatalogObject (ComAdmin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogObject
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: bce57021774b3abc2f69a1120862912452629c3e70d9c8fd0ebcc5d39ce5203d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548588"
---
# <a name="comadmincatalogobject-class"></a>Classe COMAdminCatalogObject

Rappresenta gli elementi nelle raccolte nel catalogo COM+. Usarlo per recuperare e modificare le proprietà esposte da un elemento in una raccolta.

## <a name="when-to-implement"></a>Quando implementare

Questa classe viene implementata da COM+.



| Requisito | Valore |
|------------|------------------------------------------|
| Interfacce | [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a>Utilizzo

Usare gli oggetti creati dalla **classe COMAdminCatalogObject** per modificare le proprietà degli elementi contenuti nelle raccolte nel catalogo COM+. Questi elementi corrispondono agli elementi visualizzati all'interno delle cartelle nell'albero della console dello strumento di amministrazione di Servizi componenti. Le cartelle nello strumento di amministrazione servizi componenti corrispondono alle raccolte nel catalogo, che è possibile rappresentare usando gli oggetti creati dalla [**classe COMAdminCatalogCollection.**](comadmincatalogcollection.md)

Non tutte le raccolte e gli elementi esposti tramite [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e **COMAdminCatalogObject** sono disponibili nello strumento di amministrazione servizi componenti.

Per informazioni su raccolte specifiche e sulle relative proprietà, vedere [Raccolte di amministrazione COM+.](com--administration-collections.md)

Per un'introduzione all'amministrazione a livello di codice di COM+, vedere [Automating COM+ Administration](automating-com--administration.md).

## <a name="remarks"></a>Commenti

Non è possibile creare direttamente un **oggetto COMAdminCatalogObject.** Per usare i metodi di questo oggetto, è necessario creare un oggetto [**COMAdminCatalog,**](comadmincatalog.md) ottenere un riferimento a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)e quindi [**usare ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) per ottenere un riferimento a un'interfaccia [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) che rappresenta una raccolta di primo livello o [**usare ICatalogCollection::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) per accedere a raccolte non di primo livello.

Dopo aver creato un riferimento all'interfaccia [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) della raccolta a cui si è interessati, chiamare [**ICatalogCollection::P opulate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) per popolare la raccolta con tutti i relativi elementi. Scorrere ognuno degli elementi nella raccolta chiamando [**ICatalogCollection::get \_ Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) per ottenere un riferimento a ogni [**interfaccia ICatalogObject.**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) Quando si trova l'elemento di interesse, è possibile modificare le proprietà dell'elemento e uscire dall'iterazione. Se si apportano modifiche a qualsiasi elemento di una raccolta, è necessario chiamare [**ICatalogCollection::SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) per salvare le modifiche nel catalogo COM+.

Questa operazione è illustrata nell'esempio seguente, in cui "TopCollection" deve essere sostituito dal nome di una delle raccolte di amministrazione COM+ di primo livello. "ItemName" deve essere sostituito dal nome dell'elemento a cui si è interessati. "PropertyName" deve essere sostituito dal nome della proprietà che si sta modificando nell'elemento. e varNewProp devono essere sostituiti da un elemento VARIANT che contiene il nuovo valore per la proprietà.


```C++
// Convert ItemName to a BSTR.
bstrItemName = SysAllocString(L"ItemName");
HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
  CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
  (void**)&pCatalog); 
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pCatalog->GetCollection(L"TopCollection", 
  (IDispatch**)&pTopColl);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Populate the TopCollection collection.
hr = pTopColl->Populate();
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Get the number of items in the collection.
hr = pTopColl->get_Count(&lCount);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
VARIANT varName;
VariantInit(&varName);
// Iterate through each item in the collection.
for (LONG lIdx = 0; lIdx < lCount; lIdx++) {
    hr = pTopColl->get_Item(lIdx, (IDispatch**)&pItem);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    hr = pItem->get_Name(&varName);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    // Compare the item name to bstrItemName.
    hr = VarBstrCmp(varName.bstrVal, bstrItemName, 1024L, NULL);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    if (VARCMP_EQ == hr) {  // The strings are equal.
        // Use the put_Value method to modify properties of the item.
        hr = pItem->put_Value(L"PropertyName", varNewProp);
        if (FAILED(hr)) exit(0);  // Replace with specific error handling.
        break;  // Exit the iteration.
    }
}
hr = pTopColl->SaveChanges(&lNum);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
SysFreeString(bstrItemName);


```



Per usare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di amministrazione COM+. È possibile creare un oggetto COMAdminCatalogCollection chiamando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) su un [**oggetto COMAdminCatalog**](comadmincatalog.md) o [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

Chiamare il [**metodo Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) per popolare la raccolta con tutti gli elementi. Scorrere ognuno degli elementi nella raccolta. Quando si trova l'elemento di interesse, è possibile modificare le proprietà dell'elemento e uscire dall'iterazione. Se si apportano modifiche a qualsiasi elemento di una raccolta, è necessario chiamare il metodo [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) dell'oggetto **COMAdminCatalogCollection** per salvare le modifiche nel catalogo COM+.

Questo è illustrato nell'esempio seguente, in cui "TopCollection" deve essere sostituito dal nome di una delle raccolte di amministrazione COM+ di primo livello. "ItemName" deve essere sostituito dal nome dell'elemento a cui si è interessati. "PropertyName" deve essere sostituito dal nome della proprietà che si sta modificando nell'elemento. e NewPropValue devono essere sostituiti dal nuovo valore per la proprietà .


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")
objTopCollection.Populate
Dim objItem As COMAdmin.COMAdminCatalogObject
For Each objItem in objTopCollection
    If objItem.Name = "ItemName" Then
        objItem.Value("PropertyName") = NewPropValue
        Exit For
    End If
Next
objAppCollection.SaveChanges

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>ComAdmin.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ComAdmin.Idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**COMAdminCatalog**](comadmincatalog.md)
</dt> <dt>

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)
</dt> <dt>

[**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




