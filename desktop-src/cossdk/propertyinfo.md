---
description: Recupera le informazioni sulle proprietà supportate da una raccolta specificata.
ms.assetid: 5e3963c0-6769-4b5b-8636-2d8c98a8776b
title: Raccolta PropertyInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: bd9fdd2262d4499efd6a86fbc5b99bae786016f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127019"
---
# <a name="propertyinfo-collection"></a>Raccolta PropertyInfo

Recupera le informazioni sulle proprietà supportate da una raccolta specificata. La raccolta **PropertyInfo** è accessibile da qualsiasi oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) usando il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) . La raccolta **PropertyInfo** contiene un oggetto per ogni proprietà supportata dalla raccolta originale.

## <a name="members"></a>Membri

La raccolta **PropertyInfo** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   **PropertyInfo**
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta da ogni raccolta.

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [Nome](#name)

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome della proprietà. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                                                         |
| Type           | string                                                                                                                                                                                           |
| Predefinito        | nessuno                                                                                                                                                                                             |
| Sistema minimo | Windows 2000                                                                                                                                                                                     |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
