---
description: Contiene un elenco dei server in-process registrati con il sistema per i componenti a 32 bit nei computer a 64 bit. Contiene un oggetto per ogni componente.
ms.assetid: 4dbcf059-b09b-4a65-95c9-3a4735c252c3
title: Raccolta WOWInprocServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWInprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: d85abf322d34d03c0f5e8863b5434343946b676e477e18077c82d83de78cafb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545572"
---
# <a name="wowinprocservers-collection"></a>Raccolta WOWInprocServers

Contiene un elenco dei server in-process registrati con il sistema per i componenti a 32 bit nei computer a 64 bit. Contiene un oggetto per ogni componente.

Questa raccolta supporta il [**metodo Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection,**](comadmincatalogcollection.md) ma non il [**metodo Add.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) Per installare o importare componenti in un'applicazione, usare i metodi [**nell'oggetto COMAdminCatalog.**](comadmincatalog.md)

## <a name="members"></a>Membri

La **raccolta WOWInprocServers** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [Clsid](#clsid)
-   [InprocServer32](#inprocserver32)
-   [ProgID](#progid)

### <a name="clsid"></a>CLSID



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | GUID per il componente. Questa proprietà viene restituita quando [**il metodo**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) della proprietà Key viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                  |
| Type           | string                                                                                                                                                    |
| Predefinito        | N/A                                                                                                                                                       |
| Sistema minimo | Windows XP                                                                                                                                                |



 

### <a name="inprocserver32"></a>InprocServer32



| Voce | Valore |
|----------------|----------------------------------|
| Descrizione    | Percorso del file per il componente. |
| Access         | ReadOnly                         |
| Type           | string                           |
| Predefinito        | N/A                              |
| Sistema minimo | Windows XP                       |



 

### <a name="progid"></a>ProgID



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome che identifica il componente. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                            |
| Type           | string                                                                                                                                                              |
| Predefinito        | N/A                                                                                                                                                                 |
| Sistema minimo | Windows XP                                                                                                                                                          |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
