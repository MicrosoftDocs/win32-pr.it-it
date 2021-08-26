---
description: La raccolta Roles è sempre correlata a un oggetto nella raccolta Applications. Contiene un oggetto per ogni ruolo assegnato all'applicazione a cui è correlato.
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: Raccolta di ruoli
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Roles
api_type:
- COM
api_location: ''
ms.openlocfilehash: 133477d82f718b992a628bde8af58f22d8d50a9e4974816c7c8f56be7ba8e33f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029471"
---
# <a name="roles-collection"></a>Raccolta di ruoli

La **raccolta** Roles è sempre correlata a un oggetto nella [**raccolta Applications.**](applications.md) Contiene un oggetto per ogni ruolo assegnato all'applicazione a cui è correlato.

Questa raccolta supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta Roles** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Errorinfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**UsersInRole**](usersinrole.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Applicazioni**](applications.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [Descrizione](#description)
-   [Nome](#name)

### <a name="description"></a>Descrizione



| Voce | Valore |
|----------------|----------------------------|
| Descrizione    | Descrizione del ruolo. |
| Access         | ReadWrite                  |
| Type           | string                     |
| Predefinito        | ""                         |
| Sistema minimo | Windows 2000               |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome del ruolo. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono spogliati. Questa proprietà viene restituita quando il [**metodo della**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) proprietà Key o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                                                                                                                   |
| Type           | string                                                                                                                                                                                                                                                      |
| Predefinito        | "Nuovo ruolo"                                                                                                                                                                                                                                                  |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
