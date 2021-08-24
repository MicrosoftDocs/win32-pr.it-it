---
description: Accede ai dati archiviati nel catalogo COM+.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: Classe COMAdminCatalog (ComAdmin.h)
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
ms.openlocfilehash: 8be3f0f3f9aa59c2199c50b73b8a4d4488b0c9a65d3e0679b65350d6b8b07fd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128993"
---
# <a name="comadmincatalog-class"></a>Classe COMAdminCatalog

Accede ai dati archiviati nel catalogo COM+.

## <a name="when-to-implement"></a>Quando implementare

Questa classe viene implementata da COM+.



| Requisito | Valore |
|------------|-------------------------------------------------------------------------------------------------------------------|
| CLSID      | CLSID \_ COMAdminCatalog                                                                                            |
| ProgID     | L"COMAdmin.COMAdminCatalog"                                                                                       |
| Interfacce | [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a>Utilizzo

Gli oggetti creati dalla classe **COMAdminCatalog** vengono utilizzati per iniziare l'accesso a livello di codice ai dati di configurazione COM+ archiviati nel catalogo COM+. Queste informazioni sono alla base delle cartelle e degli elementi dell'albero della console dello strumento di amministrazione Servizi componenti. La **classe COMAdminCatalog** consente di accedere alle raccolte nel catalogo, installare applicazioni e componenti COM+, avviare e arrestare servizi, connettersi ai server remoti e amministrarlo.

Le cartelle nello strumento di amministrazione Servizi componenti corrispondono alle raccolte nel catalogo, che è possibile rappresentare usando gli oggetti creati dalla [**classe COMAdminCatalogCollection.**](comadmincatalogcollection.md) Gli elementi nelle cartelle corrispondono agli elementi delle raccolte, che è possibile rappresentare usando oggetti creati dalla [**classe COMAdminCatalogObject.**](comadmincatalogobject.md)

Non tutte le raccolte e gli elementi esposti tramite [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e [**COMAdminCatalogObject**](comadmincatalogobject.md) sono disponibili nello strumento di amministrazione Servizi componenti.

Per informazioni su raccolte specifiche e sulle relative proprietà, vedere [Raccolte di amministrazione COM+.](com--administration-collections.md)

Per un'introduzione all'amministrazione a livello di codice di COM+, vedere [Automazione dell'amministrazione COM+.](automating-com--administration.md)

## <a name="remarks"></a>Commenti

Per creare questo oggetto, chiamare [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

Per usare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di amministrazione COM+. Un oggetto COMAdminCatalog può essere dichiarato usando "COMAdmin.COMAdminCatalog" come nome della classe.

In COM+ 1.5, rilasciato con Windows XP, la classe **COMAdminCatalog** implementa [**l'interfaccia ICOMAdminCatalog2.**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) Tuttavia, in COM+ 1.0, rilasciato con Windows 2000, la classe **COMAdminCatalog** implementa solo [**l'interfaccia ICOMAdminCatalog.**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>ComAdmin.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ComAdmin.idl</dt> </dl> |



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

 

