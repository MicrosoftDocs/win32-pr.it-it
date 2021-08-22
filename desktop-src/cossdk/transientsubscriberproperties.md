---
description: Contiene un oggetto per ogni proprietà sottoscrittore per la raccolta TransientSubscriptions padre. Le sottoscrizioni temporanee possono essere create in tempo reale per l'esecuzione di istanze di oggetti e scompaiono quando l'oggetto viene eliminato.
ms.assetid: b4f003b0-db9d-45f1-a57d-3e4d321289ca
title: Raccolta TransientSubscriberProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriberProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: c29865978f65bb0f512e8b55ef9c5ad4bb1755d77bc322d5b0c34603702f3794
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372701"
---
# <a name="transientsubscriberproperties-collection"></a>Raccolta TransientSubscriberProperties

Contiene un oggetto per ogni proprietà sottoscrittore per la raccolta [**TransientSubscriptions**](transientsubscriptions.md) padre. Le sottoscrizioni temporanee possono essere create in tempo reale per l'esecuzione di istanze di oggetti e scompaiono quando l'oggetto viene eliminato.

Questa raccolta supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta TransientSubscriberProperties** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Errorinfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**TransientSubscriptions**](transientsubscriptions.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [Nome](#name)
-   [Valore](#value)

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome della proprietà. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono privati. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
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

 

 
