---
description: Rappresenta gli elementi nelle raccolte nel catalogo COM+. Usarlo per recuperare e modificare le proprietà esposte da un elemento in una raccolta.
ms.assetid: 1d7f248b-20ec-4b34-88ab-3c68bef72b5a
title: Classe COMAdminCatalogObject (COMAdmin. h)
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
ms.openlocfilehash: 19fb873e29ad235b11dfe6e7a95b2ad47a8405b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126717"
---
# <a name="comadmincatalogobject-class"></a>Classe COMAdminCatalogObject

Rappresenta gli elementi nelle raccolte nel catalogo COM+. Usarlo per recuperare e modificare le proprietà esposte da un elemento in una raccolta.

## <a name="when-to-implement"></a>Quando implementare

Questa classe è implementata da COM+.



| Requisito | Valore |
|------------|------------------------------------------|
| Interfacce | [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a>Utilizzo

Usare gli oggetti creati dalla classe **COMAdminCatalogObject** per modificare le proprietà degli elementi contenuti nelle raccolte nel catalogo com+. Questi elementi corrispondono agli elementi visualizzati all'interno delle cartelle nell'albero della console dello strumento di amministrazione Servizi componenti. Le cartelle dello strumento di amministrazione Servizi componenti corrispondono alle raccolte nel catalogo, che è possibile rappresentare usando gli oggetti creati dalla classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

Non tutte le raccolte e gli elementi esposti tramite [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e **COMAdminCatalogObject** sono disponibili nello strumento di amministrazione Servizi componenti.

Per informazioni sulle raccolte specifiche e sulle relative proprietà, vedere la pagina relativa alle [raccolte di amministrazione com+](com--administration-collections.md).

Per un'introduzione all'amministrazione a livello di codice di COM+, vedere [automazione dell'amministrazione com+](automating-com--administration.md).

## <a name="remarks"></a>Commenti

Non è possibile creare direttamente un oggetto **COMAdminCatalogObject** . Per usare i metodi di questo oggetto, è necessario creare un oggetto [**COMAdminCatalog**](comadmincatalog.md) , ottenere un riferimento a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)e quindi usare [**ICOMAdminCatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) per ottenere un riferimento a un'interfaccia [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) che rappresenta una raccolta di livello superiore o usare [**ICatalogCollection:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) per accedere a raccolte che non sono di primo livello.

Quando si dispone di un riferimento all'interfaccia [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) della raccolta a cui si è interessati, chiamare [**ICatalogCollection::P ripopolamento**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) per popolare la raccolta con tutti i relativi elementi. Scorrere ogni elemento della raccolta chiamando [**ICatalogCollection:: Get \_ Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) per ottenere un riferimento a ogni interfaccia [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) . Quando si trova l'elemento di interesse, è possibile modificare le proprietà dell'elemento e uscire dall'iterazione. Se si apportano modifiche a tutti gli elementi di una raccolta, è necessario chiamare [**ICatalogCollection:: SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) per salvare le modifiche apportate al catalogo com+.

Questa operazione è illustrata nell'esempio seguente, in cui la "raccolta" deve essere sostituita dal nome di una delle raccolte di amministrazione COM+ di primo livello. "ItemName" deve essere sostituito con il nome dell'elemento a cui si è interessati. "PropertyName" deve essere sostituito dal nome della proprietà che si sta modificando nell'elemento. e varNewProp devono essere sostituiti da una variante che contiene il nuovo valore per la proprietà.


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



Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi amministratore COM+. Un oggetto COMAdminCatalogCollection può essere creato chiamando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) su un oggetto [**COMAdminCatalog**](comadmincatalog.md) o [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

Chiamare il metodo [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) per popolare la raccolta con tutti i relativi elementi. Scorre ogni elemento della raccolta. Quando si trova l'elemento di interesse, è possibile modificare le proprietà dell'elemento e uscire dall'iterazione. Se si apportano modifiche a elementi di una raccolta, è necessario chiamare il metodo [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) dell'oggetto **COMAdminCatalogCollection** per salvare le modifiche apportate al catalogo com+.

Questa operazione è illustrata nell'esempio seguente, in cui la "raccolta" deve essere sostituita dal nome di una delle raccolte di amministrazione COM+ di primo livello. "ItemName" deve essere sostituito con il nome dell'elemento a cui si è interessati. "PropertyName" deve essere sostituito dal nome della proprietà che si sta modificando nell'elemento. e NewPropValue devono essere sostituiti dal nuovo valore per la proprietà.


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
| Intestazione<br/>                   | <dl> <dt>COMAdmin. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>COMAdmin. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**COMAdminCatalog**](comadmincatalog.md)
</dt> <dt>

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)
</dt> <dt>

[**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




