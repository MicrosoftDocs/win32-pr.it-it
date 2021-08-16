---
description: Recupera informazioni sulle proprietà supportate da una raccolta specificata.
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
ms.openlocfilehash: cf5c354711ec9ca34af1809707a7a869d39a3026ca5cb7ca11d2245c02be049b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547588"
---
# <a name="propertyinfo-collection"></a>Raccolta PropertyInfo

Recupera informazioni sulle proprietà supportate da una raccolta specificata. La **raccolta PropertyInfo** è accessibile da qualsiasi [**oggetto COMAdminCatalogCollection**](comadmincatalogcollection.md) usando il [**metodo GetCollection.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) La **raccolta PropertyInfo** contiene un oggetto per ogni proprietà supportata dalla raccolta originale.

## <a name="members"></a>Membri

La **raccolta PropertyInfo** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   **Propertyinfo**
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta da ogni raccolta.

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [Nome](#name)

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome della proprietà. Questa proprietà viene restituita quando il [**metodo della**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) proprietà Key o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                                                         |
| Type           | string                                                                                                                                                                                           |
| Predefinito        | nessuno                                                                                                                                                                                             |
| Sistema minimo | Windows 2000                                                                                                                                                                                     |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
