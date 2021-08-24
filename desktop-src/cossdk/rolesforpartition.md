---
description: La raccolta RolesForPartition è sempre correlata a un oggetto nella raccolta Partitions. Contiene un oggetto per ogni ruolo assegnato alla partizione a cui è correlato.
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: Raccolta RolesForPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForPartition
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6c1e64e314478793a5b421d1f0a6a76c2eb028708410a14ea426f52fbd41dfe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637041"
---
# <a name="rolesforpartition-collection"></a>Raccolta RolesForPartition

La **raccolta RolesForPartition** è sempre correlata a un oggetto nella [**raccolta Partitions.**](partitions.md) Contiene un oggetto per ogni ruolo assegnato alla partizione a cui è correlato.

Questa raccolta non supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta RolesForPartition** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Errorinfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**UsersInPartitionRole**](usersinpartitionrole.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Partizioni**](partitions.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [Descrizione](#description)
-   [Nome](#name)

### <a name="description"></a>Descrizione



| Voce | Valore |
|----------------|----------------------------|
| Descrizione    | Descrizione del ruolo. |
| Access         | ReadOnly                   |
| Type           | string                     |
| Predefinito        | ""                         |
| Sistema minimo | Windows Server 2003        |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome del ruolo. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono privati. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                                                                                                                    |
| Type           | string                                                                                                                                                                                                                                                      |
| Predefinito        | ""                                                                                                                                                                                                                                                          |
| Sistema minimo | Windows Server 2003                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
