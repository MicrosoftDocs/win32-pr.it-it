---
description: Contiene un oggetto per ogni sottoscrizione per la raccolta di componenti padre.
ms.assetid: ec93d500-32bf-4e67-9eda-c1fe0349faa2
title: Raccolta SubscriptionsForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriptionsForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: c8334aa54b56a9dccaa7aa0787d8c997baf0445e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304728"
---
# <a name="subscriptionsforcomponent-collection"></a>Raccolta SubscriptionsForComponent

Contiene un oggetto per ogni sottoscrizione per la raccolta di [**componenti**](components.md) padre.

Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta **SubscriptionsForComponent** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**PublisherProperties**](publisherproperties.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**SubscriberProperties**](subscriberproperties.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Componenti**](components.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [Descrizione](#description)
-   [Enabled](#enabled)
-   [EventClassPartitionID](#eventclasspartitionid)
-   [EventCLSID](#eventclsid)
-   [FilterCriteria](#filtercriteria)
-   [ID](#subscriptionsforcomponent-collection)
-   [InterfaceID](#interfaceid)
-   [MachineName](#machinename)
-   [MethodName](#methodname)
-   [Nome](#machinename)
-   [PerUser](#peruser)
-   [PublisherID](#publisherid)
-   [Queued](#queued)
-   [SubscriberMoniker](#subscribermoniker)
-   [SubscriberPartitionID](#subscriberpartitionid)
-   [UserName](#username)

### <a name="description"></a>Descrizione



| Voce | Valore |
|----------------|-------------------------------------|
| Descrizione    | Descrizione della sottoscrizione. |
| Access         | ReadWrite                           |
| Type           | string                              |
| Predefinito        | ""                                  |
| Sistema minimo | Windows 2000                        |



 

### <a name="enabled"></a>Abilitato



| Voce | Valore |
|----------------|----------------------------------------------------------|
| Descrizione    | Indica se la sottoscrizione è attualmente abilitata. |
| Access         | ReadWrite                                                |
| Tipo           | Bool                                                     |
| Predefinito        | Vero                                                     |
| Sistema minimo | Windows 2000                                             |



 

### <a name="eventclasspartitionid"></a>EventClassPartitionID



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Quando si sottoscrive una classe di evento, viene utilizzato per rappresentare il GUID dell'ID di partizione che contiene la classe di evento. Quando si sottoscrive le classi di evento, il Sottoscrittore ha la possibilità di sottoscrivere una classe di evento nella stessa partizione o in una partizione diversa. |
| Access         | ReadWrite                                                                                                                                                                                                                                          |
| Type           | string                                                                                                                                                                                                                                             |
| Predefinito        | NULL                                                                                                                                                                                                                                               |
| Sistema minimo | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------|
| Descrizione    | CLSID per la classe di evento. È possibile indicare un EventCLSID o PublisherID, ma non entrambi. |
| Access         | WriteOnce                                                                                    |
| Type           | string                                                                                       |
| Predefinito        | N/D                                                                                          |
| Sistema minimo | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>FilterCriteria



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Stringa che indica i criteri di filtro. Può essere un CLSID per una classe [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) . |
| Access         | ReadWrite                                                                                                        |
| Type           | string                                                                                                           |
| Predefinito        | N/D                                                                                                              |
| Sistema minimo | Windows 2000                                                                                                     |



 

### <a name="id"></a>ID



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Identificatore della sottoscrizione. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                        |
| Type           | string                                                                                                                                                           |
| Predefinito        | <Generated>                                                                                                                                                |
| Sistema minimo | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>InterfaceID



| Voce | Valore |
|----------------|------------------------------------------|
| Descrizione    | IID per l'interfaccia sottoscritta. |
| Access         | ReadWrite                                |
| Type           | string                                   |
| Predefinito        | N/D                                      |
| Sistema minimo | Windows 2000                             |



 

### <a name="machinename"></a>MachineName



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------|
| Descrizione    | Nome di un computer remoto per le sottoscrizioni delle classi di evento in un computer remoto. |
| Access         | ReadWrite                                                                       |
| Type           | string                                                                          |
| Predefinito        | ""                                                                              |
| Sistema minimo | Windows 2000                                                                    |



 

### <a name="methodname"></a>MethodName



| Voce | Valore |
|----------------|----------------------------------------------|
| Descrizione    | Metodo sull'interfaccia sottoscritta. |
| Access         | ReadWrite                                    |
| Type           | string                                       |
| Predefinito        | N/D                                          |
| Sistema minimo | Windows 2000                                 |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome della sottoscrizione. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadWrite                                                                                                                                                                                                                          |
| Type           | string                                                                                                                                                                                                                             |
| Predefinito        | "Nuova sottoscrizione"                                                                                                                                                                                                                 |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="peruser"></a>PerUser



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------|
| Descrizione    | Indica se la sottoscrizione è valida solo per un determinato utente, nome utente. |
| Access         | ReadWrite                                                                   |
| Tipo           | Bool                                                                        |
| Predefinito        | Falso                                                                       |
| Sistema minimo | Windows 2000                                                                |



 

### <a name="publisherid"></a>PublisherID



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| Descrizione    | ID del server di pubblicazione. È possibile indicare un EventCLSID o PublisherID, ma non entrambi. |
| Access         | WriteOnce                                                                               |
| Type           | string                                                                                  |
| Predefinito        | ""                                                                                      |
| Sistema minimo | Windows 2000                                                                            |



 

### <a name="queued"></a>Queued



| Voce | Valore |
|----------------|-----------------------------------------------|
| Descrizione    | Indica se la sottoscrizione è in coda. |
| Access         | ReadWrite                                     |
| Tipo           | Bool                                          |
| Predefinito        | Falso                                         |
| Sistema minimo | Windows 2000                                  |



 

### <a name="subscribermoniker"></a>SubscriberMoniker



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------|
| Descrizione    | Moniker per un Sottoscrittore contrassegnato come accodato. Un valore predefinito viene generato quando la coda viene inizialmente impostata su true. |
| Access         | ReadWrite                                                                                                       |
| Type           | string                                                                                                          |
| Predefinito        | N/D                                                                                                             |
| Sistema minimo | Windows 2000                                                                                                    |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Quando si sottoscrive una classe di evento nella stessa partizione, utilizzata per rappresentare il GUID dell'ID di partizione del Sottoscrittore. Quando si sottoscrive le classi di evento, il Sottoscrittore ha la possibilità di sottoscrivere una classe di evento nella stessa partizione o in una partizione diversa. |
| Access         | WriteOnce                                                                                                                                                                                                                                                       |
| Type           | string                                                                                                                                                                                                                                                          |
| Predefinito        | <Generated>                                                                                                                                                                                                                                               |
| Sistema minimo | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>UserName



| Voce | Valore |
|----------------|--------------------------------------------------------------------------|
| Descrizione    | Nome dell'utente a cui si applica la sottoscrizione, quando l'oggetto di lettura è true. |
| Access         | ReadWrite                                                                |
| Type           | string                                                                   |
| Predefinito        | N/D                                                                      |
| Sistema minimo | Windows 2000                                                             |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
