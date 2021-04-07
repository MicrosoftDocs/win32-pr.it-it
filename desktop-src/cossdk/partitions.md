---
description: Specifica le applicazioni contenute all'interno di ogni partizione.
ms.assetid: 264a35fd-ba71-4ae9-908a-24a72167c26b
title: Raccolta partizioni
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Partitions
api_type:
- COM
api_location: ''
ms.openlocfilehash: b1016ae932d6841a5db590f2d24496113d3cefc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749079"
---
# <a name="partitions-collection"></a>Raccolta partizioni

Specifica le applicazioni contenute all'interno di ogni partizione.

Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta di **partizioni** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Applicazioni**](applications.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForPartition**](rolesforpartition.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [Modificabili](#changeable)
-   [Cancellabile](#deleteable)
-   [Descrizione](#description)
-   [ID](#partitions-collection)
-   [Nome](#name)

### <a name="changeable"></a>Modificabili



| Voce | Valore |
|----------------|--------------------------------------------------|
| Descrizione    | Determina se la partizione può essere modificata. |
| Access         | ReadWrite                                        |
| Tipo           | Bool                                             |
| Predefinito        | Vero                                             |
| Sistema minimo | Windows Server 2003                              |



 

### <a name="deleteable"></a>Cancellabile



| Voce | Valore |
|----------------|---------------------------------------------------|
| Descrizione    | Determina se la partizione può essere eliminata. |
| Access         | ReadWrite                                         |
| Tipo           | Bool                                              |
| Predefinito        | Vero                                              |
| Sistema minimo | Windows Server 2003                               |



 

### <a name="description"></a>Descrizione



| Voce | Valore |
|----------------|---------------------------------------------------------------------|
| Descrizione    | Questa proprietà rappresenta la descrizione che identifica la partizione. |
| Access         | ReadWrite                                                           |
| Type           | string                                                              |
| Predefinito        | ""                                                                  |
| Sistema minimo | Windows Server 2003                                                 |



 

### <a name="id"></a>ID



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | GUID che rappresenta la partizione. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                          |
| Type           | string                                                                                                                                                             |
| Predefinito        | <Generated>                                                                                                                                                  |
| Sistema minimo | Windows Server 2003                                                                                                                                                |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Rappresenta il nome della partizione. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadWrite                                                                                                                                                                                                                              |
| Type           | string                                                                                                                                                                                                                                 |
| Predefinito        | "Nuova partizione"                                                                                                                                                                                                                        |
| Sistema minimo | Windows Server 2003                                                                                                                                                                                                                    |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
