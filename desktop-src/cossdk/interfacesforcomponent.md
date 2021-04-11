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
ms.openlocfilehash: 9450c898e694e5459dbb126d7f7bf11b853e33d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127026"
---
# <a name="interfacesforcomponent-collection"></a>Raccolta InterfacesForComponent

Contiene un oggetto per ogni interfaccia esposta dal componente a cui è correlata la raccolta.

Questa raccolta non supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta **InterfacesForComponent** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**ErrorInfo**](errorinfo.md)
-   [**MethodsForInterface**](methodsforinterface.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForInterface**](rolesforinterface.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Componenti**](components.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [CLSID](#clsid)
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
| Predefinito        | N/D                       |
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
| Descrizione    | GUID per l'interfaccia. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                  |
| Type           | string                                                                                                                                                    |
| Predefinito        | N/D                                                                                                                                                       |
| Sistema minimo | Windows 2000                                                                                                                                              |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome dell'interfaccia. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                    |
| Type           | string                                                                                                                                                      |
| Predefinito        | N/D                                                                                                                                                         |
| Sistema minimo | Windows 2000                                                                                                                                                |



 

### <a name="queuingenabled"></a>QueuingEnabled



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Contrassegna l'interfaccia come accodabile e può essere impostata tramite l'SDK di amministrazione o lo strumento di amministrazione Servizi componenti. Tuttavia, è possibile impostare il flag di **Accodamento abilitato** solo per un'interfaccia con il flag di **Accodamento supportato** impostato. |
| Access         | ReadWrite                                                                                                                                                                                                                          |
| Tipo           | Bool                                                                                                                                                                                                                               |
| Predefinito        | Falso                                                                                                                                                                                                                              |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a>QueueingSupported



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | L'interfaccia supporta l'accodamento. Affinché un'interfaccia supporti l'accodamento, tutti i metodi devono avere solo parametri in. L' **Accodamento supportato** viene esposto come proprietà di sola lettura. |
| Access         | ReadOnly                                                                                                                                                               |
| Tipo           | Bool                                                                                                                                                                   |
| Predefinito        | Falso                                                                                                                                                                  |
| Sistema minimo | Windows 2000                                                                                                                                                           |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
