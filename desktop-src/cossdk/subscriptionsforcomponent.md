---
description: Contiene un oggetto per ogni sottoscrizione per la raccolta Components padre.
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
ms.openlocfilehash: be18f77c4946a5d8a79adc09e97bc9ab35782fdb837f15b82794cbf5f624d59d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546163"
---
# <a name="subscriptionsforcomponent-collection"></a>Raccolta SubscriptionsForComponent

Contiene un oggetto per ogni sottoscrizione per la raccolta [**Components**](components.md) padre.

Questa raccolta supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta SubscriptionsForComponent** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Errorinfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**Proprietà publisher**](publisherproperties.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**Proprietà Sottoscrittore**](subscriberproperties.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Componenti**](components.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [Descrizione](#description)
-   [Enabled](#enabled)
-   [EventClassPartitionID](#eventclasspartitionid)
-   [EventCLSID](#eventclsid)
-   [Filtercriteria](#filtercriteria)
-   [ID](#subscriptionsforcomponent-collection)
-   [Interfaceid](#interfaceid)
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
| Descrizione    | Descrizione per la sottoscrizione. |
| Access         | ReadWrite                           |
| Type           | string                              |
| Predefinito        | ""                                  |
| Sistema minimo | Windows 2000                        |



 

### <a name="enabled"></a>Attivato



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
| Descrizione    | Quando si esegue la sottoscrizione a una classe di evento, usata per rappresentare il GUID dell'ID di partizione contenente la classe di evento. Quando si esegue la sottoscrizione alle classi di evento, il sottoscrittore ha la possibilità di sottoscrivere una classe di evento nella stessa partizione o in una partizione diversa. |
| Access         | ReadWrite                                                                                                                                                                                                                                          |
| Type           | string                                                                                                                                                                                                                                             |
| Predefinito        | NULL                                                                                                                                                                                                                                               |
| Sistema minimo | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------|
| Descrizione    | CLSID per la classe di evento. È possibile indicare un EventCLSID o un PublisherID, ma non entrambi. |
| Access         | WriteOnce                                                                                    |
| Type           | string                                                                                       |
| Predefinito        | N/A                                                                                          |
| Sistema minimo | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>Filtercriteria



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Stringa che indica i criteri di filtro. Può essere un CLSID per una [**classe PublisherFilter.**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) |
| Access         | ReadWrite                                                                                                        |
| Type           | string                                                                                                           |
| Predefinito        | N/A                                                                                                              |
| Sistema minimo | Windows 2000                                                                                                     |



 

### <a name="id"></a>ID



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Identificatore per la sottoscrizione. Questa proprietà viene restituita quando [**il metodo**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) della proprietà Key viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                        |
| Type           | string                                                                                                                                                           |
| Predefinito        | <Generated>                                                                                                                                                |
| Sistema minimo | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>Interfaceid



| Voce | Valore |
|----------------|------------------------------------------|
| Descrizione    | IID per l'interfaccia sottoscritta. |
| Access         | ReadWrite                                |
| Type           | string                                   |
| Predefinito        | N/A                                      |
| Sistema minimo | Windows 2000                             |



 

### <a name="machinename"></a>MachineName



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------|
| Descrizione    | Nome di computer remoto per le sottoscrizioni alle classi di eventi in un computer remoto. |
| Access         | ReadWrite                                                                       |
| Type           | string                                                                          |
| Predefinito        | ""                                                                              |
| Sistema minimo | Windows 2000                                                                    |



 

### <a name="methodname"></a>MethodName



| Voce | Valore |
|----------------|----------------------------------------------|
| Descrizione    | Metodo nell'interfaccia a cui viene effettuata la sottoscrizione. |
| Access         | ReadWrite                                    |
| Type           | string                                       |
| Predefinito        | N/A                                          |
| Sistema minimo | Windows 2000                                 |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome per la sottoscrizione. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono privati. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadWrite                                                                                                                                                                                                                          |
| Type           | string                                                                                                                                                                                                                             |
| Predefinito        | "Nuova sottoscrizione"                                                                                                                                                                                                                 |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="peruser"></a>PerUser



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------|
| Descrizione    | Indica se la sottoscrizione si applica solo a un determinato utente, UserName. |
| Access         | ReadWrite                                                                   |
| Tipo           | Bool                                                                        |
| Predefinito        | Falso                                                                       |
| Sistema minimo | Windows 2000                                                                |



 

### <a name="publisherid"></a>PublisherID



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| Descrizione    | ID per il server di pubblicazione. È possibile indicare un EventCLSID o un PublisherID, ma non entrambi. |
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
| Descrizione    | Moniker per un sottoscrittore contrassegnato come In coda. Un valore predefinito viene generato quando Queued è inizialmente impostato su True. |
| Access         | ReadWrite                                                                                                       |
| Type           | string                                                                                                          |
| Predefinito        | N/A                                                                                                             |
| Sistema minimo | Windows 2000                                                                                                    |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Quando si esegue la sottoscrizione a una classe di evento nella stessa partizione, usata per rappresentare il GUID dell'ID di partizione del sottoscrittore. Quando si esegue la sottoscrizione alle classi di evento, il sottoscrittore ha la possibilità di sottoscrivere una classe di evento nella stessa partizione o in una partizione diversa. |
| Access         | WriteOnce                                                                                                                                                                                                                                                       |
| Type           | string                                                                                                                                                                                                                                                          |
| Predefinito        | <Generated>                                                                                                                                                                                                                                               |
| Sistema minimo | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>Nome utente



| Voce | Valore |
|----------------|--------------------------------------------------------------------------|
| Descrizione    | Nome dell'utente a cui si applica la sottoscrizione, quando PerUser è True. |
| Access         | ReadWrite                                                                |
| Type           | string                                                                   |
| Predefinito        | N/A                                                                      |
| Sistema minimo | Windows 2000                                                             |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
