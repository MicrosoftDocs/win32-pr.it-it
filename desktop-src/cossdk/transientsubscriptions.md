---
description: Contiene un oggetto per ogni sottoscrizione temporanea. Le sottoscrizioni temporanee possono essere create in tempo reale per le istanze di oggetti in esecuzione e scompaiono quando l'oggetto viene eliminato.
ms.assetid: beee291c-e03f-4ee0-b1f2-99dcf113c46e
title: Raccolta TransientSubscriptions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriptions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 68ccdd222f4fe205e58adf5195df694ec1256804
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879931"
---
# <a name="transientsubscriptions-collection"></a>Raccolta TransientSubscriptions

Contiene un oggetto per ogni sottoscrizione temporanea. Le sottoscrizioni temporanee possono essere create in tempo reale per le istanze di oggetti in esecuzione e scompaiono quando l'oggetto viene eliminato.

Questa raccolta supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta TransientSubscriptions** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Errorinfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**Proprietà del server di pubblicazione temporaneo**](transientpublisherproperties.md)
-   [**TransientSubscriberProperties**](transientsubscriberproperties.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [Descrizione](#description)
-   [Enabled](#enabled)
-   [EventClassPartitionID](#eventclasspartitionid)
-   [EventCLSID](#eventclsid)
-   [Filtercriteria](#filtercriteria)
-   [ID](#transientsubscriptions-collection)
-   [Interfaceid](#interfaceid)
-   [MethodName](#methodname)
-   [Nome](#methodname)
-   [PerUser](#peruser)
-   [PUBLISHERID](#publisherid)
-   [Interfaccia del sottoscrittore](#subscriberinterface)
-   [SubscriberPartitionID](#subscriberpartitionid)
-   [UserName](#username)

### <a name="description"></a>Descrizione



| Voce | Valore |
|----------------|-------------------------------------|
| Descrizione    | Descrizione della sottoscrizione. |
| Access         | ReadWrite                           |
| Type           | Stringa                              |
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
| Descrizione    | Quando si sottoscrive una classe di evento, utilizzata per rappresentare il GUID dell'ID di partizione contenente la classe di evento. Quando si sottoscrive una classe di evento, il sottoscrittore ha la possibilità di sottoscrivere una classe di evento nella stessa partizione o in una partizione diversa. |
| Access         | ReadWrite                                                                                                                                                                                                                                          |
| Type           | Stringa                                                                                                                                                                                                                                             |
| Predefinito        | NULL                                                                                                                                                                                                                                               |
| Sistema minimo | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------|
| Descrizione    | CLSID per la classe di evento. È possibile indicare un EventCLSID o un PublisherID, ma non entrambi. |
| Access         | WriteOnce                                                                                    |
| Type           | Stringa                                                                                       |
| Predefinito        | N/A                                                                                          |
| Sistema minimo | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>Filtercriteria



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Stringa che indica i criteri di filtro. Può essere un CLSID per una [**classe PublisherFilter.**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) |
| Access         | ReadWrite                                                                                                            |
| Type           | Stringa                                                                                                               |
| Predefinito        | N/A                                                                                                                  |
| Sistema minimo | Windows 2000                                                                                                         |



 

### <a name="id"></a>ID



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Identificatore per la sottoscrizione. Questa proprietà viene restituita quando [**il metodo**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) della proprietà Key viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                        |
| Type           | Stringa                                                                                                                                                           |
| Predefinito        | &lt;Generato&gt;                                                                                                                                                |
| Sistema minimo | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>Interfaceid



| Voce | Valore |
|----------------|----------------------------------|
| Descrizione    | IID per l'interfaccia sottoscritta. |
| Access         | WriteOnce                        |
| Type           | Stringa                           |
| Predefinito        | N/A                              |
| Sistema minimo | Windows 2000                     |



 

### <a name="methodname"></a>MethodName



| Voce | Valore |
|----------------|----------------------------------------------|
| Descrizione    | Metodo nell'interfaccia a cui viene effettuata la sottoscrizione. |
| Access         | ReadWrite                                    |
| Type           | Stringa                                       |
| Predefinito        | N/A                                          |
| Sistema minimo | Windows 2000                                 |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome della sottoscrizione. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono privati. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadWrite                                                                                                                                                                                                                              |
| Type           | Stringa                                                                                                                                                                                                                                 |
| Predefinito        | "Nuova sottoscrizione"                                                                                                                                                                                                                     |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                           |



 

### <a name="peruser"></a>PerUser



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica se la sottoscrizione si applica solo a un determinato utente, rappresentato dalla proprietà UserName. |
| Access         | ReadWrite                                                                                               |
| Tipo           | Bool                                                                                                    |
| Predefinito        | Falso                                                                                                   |
| Sistema minimo | Windows 2000                                                                                            |



 

### <a name="publisherid"></a>PublisherID



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------|
| Descrizione    | ID per il server di pubblicazione. È possibile indicare un EventCLSID o un PublisherID, ma non entrambi. |
| Access         | WriteOnce                                                                           |
| Type           | Stringa                                                                              |
| Predefinito        | ""                                                                                  |
| Sistema minimo | Windows 2000                                                                        |



 

### <a name="subscriberinterface"></a>SubscriberInterface



| Voce | Valore |
|----------------|------------------------------------------|
| Descrizione    | Puntatore all'interfaccia del sottoscrittore. |
| Access         | ReadWrite                                |
| Tipo           | Variant                                  |
| Predefinito        | N/A                                      |
| Sistema minimo | Windows 2000                             |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Quando si esegue la sottoscrizione a una classe di evento nella stessa partizione, usata per rappresentare il GUID dell'ID di partizione del sottoscrittore. Quando si esegue la sottoscrizione alle classi di evento, il sottoscrittore ha la possibilità di sottoscrivere una classe di evento nella stessa partizione o in una partizione diversa. |
| Access         | WriteOnce                                                                                                                                                                                                                                                       |
| Type           | Stringa                                                                                                                                                                                                                                                          |
| Predefinito        | &lt;Generato&gt;                                                                                                                                                                                                                                               |
| Sistema minimo | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>Nome utente



| Voce | Valore |
|----------------|-------------------------------------------------------------------------|
| Descrizione    | Nome dell'utente a cui si applica la sottoscrizione quando PerUser è True. |
| Access         | ReadWrite                                                               |
| Type           | Stringa                                                                  |
| Predefinito        | N/A                                                                     |
| Sistema minimo | Windows 2000                                                            |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
