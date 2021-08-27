---
description: Contiene un oggetto per ogni interfaccia esposta dal componente a cui è correlata la raccolta.
ms.assetid: ee755693-e3ff-4bb1-9fde-a2bfee9c3d29
title: Raccolta InterfacesForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InterfacesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 13c0ed22b6d4ee8ffb4a0d6c4d3f6475341192f656c48553ab901206be833b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047449"
---
# <a name="interfacesforcomponent-collection"></a>Raccolta InterfacesForComponent

Contiene un oggetto per ogni interfaccia esposta dal componente a cui è correlata la raccolta.

Questa raccolta non supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta InterfacesForComponent** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Errorinfo**](errorinfo.md)
-   [**MetodiForInterface**](methodsforinterface.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForInterface**](rolesforinterface.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Componenti**](components.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [Clsid](#clsid)
-   [Descrizione](#description)
-   [IID](#iid)
-   [Nome](#name)
-   [QueuingEnabled](#queuingenabled)
-   [QueueingSupported](#queueingsupported)

### <a name="clsid"></a>CLSID



| Voce | Valore |
|----------------|---------------------------|
| Descrizione    | GUID per il componente. |
| Access         | ReadOnly                  |
| Type           | string                    |
| Predefinito        | N/A                       |
| Sistema minimo | Windows 2000              |



 

### <a name="description"></a>Descrizione



| Voce | Valore |
|----------------|----------------------------------|
| Descrizione    | Descrizione dell'interfaccia. |
| Access         | ReadWrite                        |
| Type           | string                           |
| Predefinito        | ""                               |
| Sistema minimo | Windows 2000                     |



 

### <a name="iid"></a>IID



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | GUID per l'interfaccia. Questa proprietà viene restituita quando [**il metodo**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) della proprietà Key viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                  |
| Type           | string                                                                                                                                                    |
| Predefinito        | N/A                                                                                                                                                       |
| Sistema minimo | Windows 2000                                                                                                                                              |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome dell'interfaccia. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                    |
| Type           | string                                                                                                                                                      |
| Predefinito        | N/A                                                                                                                                                         |
| Sistema minimo | Windows 2000                                                                                                                                                |



 

### <a name="queuingenabled"></a>QueuingEnabled



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Contrassegna l'interfaccia come accodamentabile e può essere impostata usando l'SDK di amministrazione o lo strumento amministrativo Servizi componenti. Tuttavia, solo un'interfaccia con il flag **Accodamento** supportato impostato può avere il flag **Abilitato per** l'accodamento impostato. |
| Access         | ReadWrite                                                                                                                                                                                                                          |
| Tipo           | Bool                                                                                                                                                                                                                               |
| Predefinito        | Falso                                                                                                                                                                                                                              |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a>QueueingSupported



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | L'interfaccia supporta l'accodamento. Perché un'interfaccia supporti l'accodamento, tutti i metodi devono avere solo nei parametri. **L'accodamento supportato** viene esposto come proprietà di sola lettura. |
| Access         | ReadOnly                                                                                                                                                               |
| Tipo           | Bool                                                                                                                                                                   |
| Predefinito        | Falso                                                                                                                                                                  |
| Sistema minimo | Windows 2000                                                                                                                                                           |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
