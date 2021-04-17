---
description: Accede ai dati archiviati nel catalogo COM+.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: Classe COMAdminCatalog (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalog
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: fa6e71d13f5a3d157bd3ce1035d0616dc1e5a519
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483613"
---
# <a name="comadmincatalog-class"></a>Classe COMAdminCatalog

Accede ai dati archiviati nel catalogo COM+.

## <a name="when-to-implement"></a>Quando implementare

Questa classe è implementata da COM+.



| Requisito | Valore |
|------------|-------------------------------------------------------------------------------------------------------------------|
| CLSID      | \_COMADMINCATALOG CLSID                                                                                            |
| ProgID     | L "COMAdmin. COMAdminCatalog"                                                                                       |
| Interfacce | [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a>Utilizzo

Gli oggetti creati dalla classe **COMAdminCatalog** vengono utilizzati per avviare l'accesso a livello di codice ai dati di configurazione com+ archiviati nel catalogo com+. Queste informazioni si basano sulle cartelle e sugli elementi nell'albero della console dello strumento di amministrazione Servizi componenti. La classe **COMAdminCatalog** consente di accedere alle raccolte nel catalogo, installare componenti e applicazioni com+, avviare e arrestare i servizi e connettersi ai server remoti e gestirli.

Le cartelle dello strumento di amministrazione Servizi componenti corrispondono alle raccolte nel catalogo, che è possibile rappresentare usando gli oggetti creati dalla classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) . Gli elementi nelle cartelle corrispondono agli elementi delle raccolte, che è possibile rappresentare usando gli oggetti creati dalla classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

Non tutte le raccolte e gli elementi esposti tramite [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e [**COMAdminCatalogObject**](comadmincatalogobject.md) sono disponibili nello strumento di amministrazione Servizi componenti.

Per informazioni sulle raccolte specifiche e sulle relative proprietà, vedere la pagina relativa alle [raccolte di amministrazione com+](com--administration-collections.md).

Per un'introduzione all'amministrazione a livello di codice di COM+, vedere [automazione dell'amministrazione com+](automating-com--administration.md).

## <a name="remarks"></a>Commenti

Per creare questo oggetto, chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi amministratore COM+. Un oggetto COMAdminCatalog può essere dichiarato utilizzando "COMAdmin. COMAdminCatalog" come nome della classe.

In COM+ 1,5, rilasciato con Windows XP, la classe **COMAdminCatalog** implementa l'interfaccia [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) . Tuttavia, in COM+ 1,0, rilasciato con Windows 2000, la classe **COMAdminCatalog** implementa solo l'interfaccia [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>COMAdmin. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>COMAdmin. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)
</dt> <dt>

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

