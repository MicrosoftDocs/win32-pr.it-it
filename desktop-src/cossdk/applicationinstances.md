---
description: Recupera informazioni relative all'esecuzione di applicazioni.
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: Raccolta ApplicationInstances
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationInstances
api_type:
- COM
api_location: ''
ms.openlocfilehash: 957fe3fa556a3e41e2484116ff2c9242fd63efa1469a4a6040f31aa04a3627e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129383"
---
# <a name="applicationinstances-collection"></a>Raccolta ApplicationInstances

Recupera informazioni relative all'esecuzione di applicazioni.

Questa raccolta supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta ApplicationInstances** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Errorinfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Applicazioni**](applications.md)
-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [Applicazione](#applicationinstances-collection)
-   [HasRecycled](#hasrecycled)
-   [InstanceID](#instanceid)
-   [IsPaused](#ispaused)
-   [Partitionid](#partitionid)
-   [ProcessID](#processid)

### <a name="application"></a>Applicazione



| Voce | Valore |
|----------------|-------------------------------------|
| Descrizione    | ID per l'applicazione in esecuzione. |
| Access         | ReadOnly                            |
| Type           | string                              |
| Predefinito        | N/A                                 |
| Sistema minimo | Windows XP                          |



 

### <a name="hasrecycled"></a>HasRecycled



| Voce | Valore |
|----------------|---------------------------------------------------------------|
| Descrizione    | Indica se l'istanza dell'applicazione è stata riciclata. |
| Access         | ReadOnly                                                      |
| Tipo           | Bool                                                          |
| Predefinito        | Falso                                                         |
| Sistema minimo | Windows XP                                                    |



 

### <a name="instanceid"></a>InstanceID



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Identificatore univoco globale per l'istanza dell'applicazione. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                                                                                            |
| Type           | string                                                                                                                                                                                                                              |
| Predefinito        | N/A                                                                                                                                                                                                                                 |
| Sistema minimo | Windows XP                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a>IsPaused



| Voce | Valore |
|----------------|-----------------------------------------------------------------|
| Descrizione    | Indica se l'istanza dell'applicazione è attualmente sospesa. |
| Access         | ReadOnly                                                        |
| Tipo           | Bool                                                            |
| Predefinito        | Falso                                                           |
| Sistema minimo | Windows XP                                                      |



 

### <a name="partitionid"></a>Partitionid



| Voce | Valore |
|----------------|-------------------------------------------------|
| Descrizione    | ID di partizione utilizzato dall'applicazione. |
| Access         | ReadOnly                                        |
| Type           | string                                          |
| Predefinito        | N/A                                             |
| Sistema minimo | Windows XP                                      |



 

### <a name="processid"></a>ProcessID



| Voce | Valore |
|----------------|---------------------------------------------|
| Descrizione    | ID processo dell'istanza dell'applicazione. |
| Access         | ReadOnly                                    |
| Type           | string                                      |
| Predefinito        | N/A                                         |
| Sistema minimo | Windows XP                                  |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
