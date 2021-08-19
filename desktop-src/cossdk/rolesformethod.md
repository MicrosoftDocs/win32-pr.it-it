---
description: Contiene un oggetto per ogni ruolo assegnato al metodo a cui è correlata la raccolta. I ruoli devono essere già assegnati a livello di applicazione.
ms.assetid: 3a086163-e367-4dd1-996b-821b3e1111b2
title: Raccolta RolesForMethod
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForMethod
api_type:
- COM
api_location: ''
ms.openlocfilehash: 01579f460ceb9a3099adefef48e9fc203e042956713478273ce654fce3a34022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047279"
---
# <a name="rolesformethod-collection"></a>Raccolta RolesForMethod

Contiene un oggetto per ogni ruolo assegnato al metodo a cui è correlata la raccolta. I ruoli devono essere già assegnati a livello di applicazione.

Questa raccolta supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta RolesForMethod** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Errorinfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**MetodiForInterface**](methodsforinterface.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [Nome](#name)

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome del ruolo. Deve essere già un ruolo assegnato all'applicazione (visualizzato nella raccolta Ruoli). Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono privati. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                                                                                                                                                                                                           |
| Type           | string                                                                                                                                                                                                                                                                                                                                              |
| Predefinito        | "Nuovo ruolo"                                                                                                                                                                                                                                                                                                                                          |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
