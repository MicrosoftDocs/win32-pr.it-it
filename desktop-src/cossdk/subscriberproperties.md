---
description: Contiene un oggetto per ogni proprietà del sottoscrittore per la raccolta SubscriptionsForComponent padre.
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
ms.openlocfilehash: 7f4b1d46ecc0afd942a821a8ded3e6ad8c80106e6fe770bdce065ad41902cd1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915689"
---
# <a name="subscriberproperties-collection"></a>Raccolta SubscriberProperties

Contiene un oggetto per ogni proprietà del sottoscrittore per la [**raccolta SubscriptionsForComponent**](subscriptionsforcomponent.md) padre.

Questa raccolta supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta SubscriberProperties** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Errorinfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**SubscriptionsForComponent**](subscriptionsforcomponent.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [Nome](#name)
-   [Valore](#value)

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome della proprietà. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono spogliati. Questa proprietà viene restituita quando il [**metodo della**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) proprietà Key o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
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
| Predefinito        | N/A                       |
| Sistema minimo | Windows 2000              |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
