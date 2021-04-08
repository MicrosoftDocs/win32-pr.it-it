---
description: Contiene un oggetto per ogni proprietà del Sottoscrittore per la raccolta SubscriptionsForComponent padre.
ms.assetid: 58c9edbd-1128-4b8c-bb5a-528c212aa6a7
title: Raccolta SubscriberProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7c7a563e3fd3e917812426e34debd87bfd534b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877614"
---
# <a name="subscriberproperties-collection"></a>Raccolta SubscriberProperties

Contiene un oggetto per ogni proprietà del Sottoscrittore per la raccolta [**SubscriptionsForComponent**](subscriptionsforcomponent.md) padre.

Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta **SubscriberProperties** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**SubscriptionsForComponent**](subscriptionsforcomponent.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [Nome](#name)
-   [Valore](#value)

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome della proprietà. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                                                                                                                              |
| Type           | string                                                                                                                                                                                                                                                                 |
| Predefinito        | "Nuova proprietà"                                                                                                                                                                                                                                                         |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="value"></a>Valore



| Voce | Valore |
|----------------|---------------------------|
| Descrizione    | Valore per la proprietà. |
| Access         | ReadWrite                 |
| Tipo           | Variant                   |
| Predefinito        | N/D                       |
| Sistema minimo | Windows 2000              |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
