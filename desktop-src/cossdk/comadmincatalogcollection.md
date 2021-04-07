---
description: Rappresenta qualsiasi raccolta nel catalogo COM+. Usarlo per enumerare, aggiungere, rimuovere e recuperare elementi in una raccolta e per accedere alle raccolte correlate.
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: Classe COMAdminCatalogCollection (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogCollection
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 985a6b947708542ec3ce1dc6ecc835c94259b315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748663"
---
# <a name="comadmincatalogcollection-class"></a>Classe COMAdminCatalogCollection

Rappresenta qualsiasi raccolta nel catalogo COM+. Usarlo per enumerare, aggiungere, rimuovere e recuperare elementi in una raccolta e per accedere alle raccolte correlate.

## <a name="when-to-implement"></a>Quando implementare

Questa classe è implementata da COM+.



| Requisito | Valore |
|------------|--------------------------------------------------|
| Interfacce | [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a>Utilizzo

Usare gli oggetti creati dalla classe **COMAdminCatalogCollection** quando si desidera modificare a livello di codice una raccolta nel catalogo com+. Queste raccolte corrispondono alle cartelle dello strumento di amministrazione Servizi componenti. Gli elementi all'interno delle cartelle corrispondono agli elementi delle raccolte, che è possibile rappresentare usando gli oggetti creati dalla classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

Per informazioni sulle raccolte nel catalogo e sulle relative proprietà, vedere la pagina relativa alle [raccolte di amministrazione com+](com--administration-collections.md).

Per un'introduzione all'amministrazione a livello di codice di COM+, vedere [automazione dell'amministrazione com+](automating-com--administration.md).

## <a name="remarks"></a>Commenti

Non è possibile creare direttamente un oggetto **COMAdminCatalogCollection** . Per usare i metodi di questo oggetto, è necessario creare un oggetto [**COMAdminCatalog**](comadmincatalog.md) , ottenere un riferimento a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)e quindi usare [**ICOMAdminCatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) per ottenere un riferimento a un'interfaccia [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) che rappresenta una raccolta di livello superiore. Questa operazione è illustrata nell'esempio seguente, in cui la "raccolta" deve essere sostituita dal nome di una delle raccolte di amministrazione COM+ di primo livello.


```C++
    HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pCatalog->GetCollection(L"TopCollection", 
      (IDispatch**)&pTopColl);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
```



Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi amministratore COM+. Un oggetto COMAdminCatalogCollection può essere creato chiamando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) su un oggetto [**COMAdminCatalog**](comadmincatalog.md) . Questa operazione è illustrata nell'esempio seguente, in cui la "raccolta" deve essere sostituita dal nome di una delle raccolte di amministrazione COM+ di primo livello.


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")

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

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




