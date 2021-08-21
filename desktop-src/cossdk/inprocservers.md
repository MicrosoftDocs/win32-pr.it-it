---
description: Contiene un elenco dei server in-process registrati nel sistema. Contiene un oggetto per ogni componente registrato come server in-process.
ms.assetid: 10434de7-c5e3-4fb0-8472-2a581607fcc0
title: Raccolta InprocServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: b751f007082454832fe31172e35b834b66c36d13dbaf6a6687ba0036879b60c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047459"
---
# <a name="inprocservers-collection"></a>Raccolta InprocServers

Contiene un elenco dei server in-process registrati nel sistema. Contiene un oggetto per ogni componente registrato come server in-process.

Questa raccolta supporta il [**metodo Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection,**](comadmincatalogcollection.md) ma non il [**metodo Add.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) Per installare o importare componenti in un'applicazione, usare i metodi [**nell'oggetto COMAdminCatalog.**](comadmincatalog.md)

## <a name="members"></a>Membri

La **raccolta InprocServers** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

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
| Sistema minimo | Windows 2000                                                                                                                                              |



 

### <a name="inprocserver32"></a>InprocServer32



| Voce | Valore |
|----------------|----------------------------------|
| Descrizione    | Percorso del file per il componente. |
| Access         | ReadOnly                         |
| Type           | string                           |
| Predefinito        | N/A                              |
| Sistema minimo | Windows 2000                     |



 

### <a name="progid"></a>ProgID



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome che identifica il componente. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                            |
| Type           | string                                                                                                                                                              |
| Predefinito        | N/A                                                                                                                                                                 |
| Sistema minimo | Windows 2000                                                                                                                                                        |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
