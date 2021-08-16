---
description: Specifica le applicazioni contenute in ogni partizione.
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
ms.openlocfilehash: 3badf52755a77557c200569c25610b5918cf8dd599d17a83bdebb5c4ddfa6801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305874"
---
# <a name="partitions-collection"></a>Raccolta partizioni

Specifica le applicazioni contenute in ogni partizione.

Questa raccolta supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta Partitions** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Applicazioni**](applications.md)
-   [**Errorinfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForPartition**](rolesforpartition.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [Variabile](#changeable)
-   [Eliminabile](#deleteable)
-   [Descrizione](#description)
-   [ID](#partitions-collection)
-   [Nome](#name)

### <a name="changeable"></a>Variabile



| Voce | Valore |
|----------------|--------------------------------------------------|
| Descrizione    | Determina se questa partizione è modificabile. |
| Access         | ReadWrite                                        |
| Tipo           | Bool                                             |
| Predefinito        | Vero                                             |
| Sistema minimo | Windows Server 2003                              |



 

### <a name="deleteable"></a>Eliminabile



| Voce | Valore |
|----------------|---------------------------------------------------|
| Descrizione    | Determina se questa partizione può essere eliminata. |
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
| Descrizione    | GUID che rappresenta la partizione. Questa proprietà viene restituita quando [**il metodo**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) della proprietà Key viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                          |
| Type           | string                                                                                                                                                             |
| Predefinito        | <Generated>                                                                                                                                                  |
| Sistema minimo | Windows Server 2003                                                                                                                                                |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Rappresenta il nome della partizione. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono privati. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadWrite                                                                                                                                                                                                                              |
| Type           | string                                                                                                                                                                                                                                 |
| Predefinito        | "Nuova partizione"                                                                                                                                                                                                                        |
| Sistema minimo | Windows Server 2003                                                                                                                                                                                                                    |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
