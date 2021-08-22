---
description: 'Raccolta UsersInPartitionRole: contiene un oggetto per ogni utente nel ruolo a cui è correlata la raccolta.'
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: Raccolta UsersInPartitionRole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInPartitionRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: d07c62fc6c6cc871f803b1f752201bd500e2705c3cfca272ff350ffd018f6018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499647"
---
# <a name="usersinpartitionrole-collection"></a>Raccolta UsersInPartitionRole

Contiene un oggetto per ogni utente nel ruolo a cui è correlata la raccolta.

Questa raccolta supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta UsersInPartitionRole** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Errorinfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**RolesForPartition**](rolesforpartition.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [Utente](#usersinpartitionrole-collection)

### <a name="user"></a>Utente



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome utente. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                                             |
| Type           | string                                                                                                                                                                                |
| Predefinito        | "Nuovo utente"                                                                                                                                                                            |
| Sistema minimo | Windows Server 2003                                                                                                                                                                   |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
