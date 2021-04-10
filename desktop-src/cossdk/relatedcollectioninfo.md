---
description: Recupera informazioni su altre raccolte correlate alla raccolta dalla quale viene chiamato.
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: Raccolta RelatedCollectionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RelatedCollectionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 21a9a1905d75c81d605f30a3f6cffced8837034d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225635"
---
# <a name="relatedcollectioninfo-collection"></a>Raccolta RelatedCollectionInfo

Recupera informazioni su altre raccolte correlate alla raccolta dalla quale viene chiamato. La raccolta **RelatedCollectionInfo** è accessibile da qualsiasi oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) tramite il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) . La raccolta **RelatedCollectionInfo** contiene un oggetto per ogni raccolta accessibile dalla raccolta originale. Le raccolte correlate seguono la gerarchia della raccolta di strumenti di amministrazione di Servizi componenti.

Questa raccolta non supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta **RelatedCollectionInfo** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**PropertyInfo**](propertyinfo.md)
-   **RelatedCollectionInfo**

È possibile passare a questa raccolta da ogni raccolta.

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [Nome](#name)

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome della raccolta correlata. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                                                                   |
| Type           | string                                                                                                                                                                                                     |
| Predefinito        | nessuno                                                                                                                                                                                                       |
| Sistema minimo | Windows 2000                                                                                                                                                                                               |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
