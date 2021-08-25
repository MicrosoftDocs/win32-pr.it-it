---
description: Rappresenta qualsiasi raccolta nel catalogo COM+. Usarlo per enumerare, aggiungere, rimuovere e recuperare elementi in una raccolta e per accedere alle raccolte correlate.
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: Classe COMAdminCatalogCollection (ComAdmin.h)
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
ms.openlocfilehash: 3656e65b89ae02b0cfe8ea3b1dbe9784d679c5eb40e11edbfe2951e08893e1aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029481"
---
# <a name="comadmincatalogcollection-class"></a>Classe COMAdminCatalogCollection

Rappresenta qualsiasi raccolta nel catalogo COM+. Usarlo per enumerare, aggiungere, rimuovere e recuperare elementi in una raccolta e per accedere alle raccolte correlate.

## <a name="when-to-implement"></a>Quando implementare

Questa classe viene implementata da COM+.



| Requisito | Valore |
|------------|--------------------------------------------------|
| Interfacce | [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a>Utilizzo

Usare gli oggetti creati dalla **classe COMAdminCatalogCollection** quando si vuole modificare a livello di codice una raccolta nel catalogo COM+. Queste raccolte corrispondono alle cartelle nello strumento di amministrazione Servizi componenti. Gli elementi all'interno delle cartelle corrispondono agli elementi nelle raccolte, che è possibile rappresentare usando gli oggetti creati dalla [**classe COMAdminCatalogObject.**](comadmincatalogobject.md)

Per informazioni sulle raccolte nel catalogo e sulle relative proprietà, vedere [Raccolte di amministrazione COM+.](com--administration-collections.md)

Per un'introduzione all'amministrazione a livello di codice di COM+, vedere [Automazione dell'amministrazione COM+.](automating-com--administration.md)

## <a name="remarks"></a>Commenti

Non è possibile creare direttamente **un oggetto COMAdminCatalogCollection.** Per usare i metodi di questo oggetto, è necessario creare un oggetto [**COMAdminCatalog,**](comadmincatalog.md) ottenere un riferimento a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)e quindi usare [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) per ottenere un riferimento a un'interfaccia [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) che rappresenta una raccolta di primo livello. Come illustrato nell'esempio seguente, in cui "TopCollection" deve essere sostituito dal nome di una delle raccolte di amministrazione COM+ di primo livello.


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



Per usare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di amministrazione COM+. È possibile creare un oggetto COMAdminCatalogCollection chiamando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) su un [**oggetto COMAdminCatalog.**](comadmincatalog.md) Come illustrato nell'esempio seguente, in cui "TopCollection" deve essere sostituito dal nome di una delle raccolte di amministrazione COM+ di primo livello.


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
| Intestazione<br/>                   | <dl> <dt>ComAdmin.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ComAdmin.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**COMAdminCatalog**](comadmincatalog.md)
</dt> <dt>

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




