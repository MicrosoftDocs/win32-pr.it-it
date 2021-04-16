---
description: Contiene un oggetto per ogni componente nell'applicazione correlata.
ms.assetid: f502ba60-b2b1-4556-8f91-22a474e60e0d
title: Raccolta componenti
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Components
api_type:
- COM
api_location: ''
ms.openlocfilehash: f68013985beff427b5681c5b78c2c00df9e69263
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524217"
---
# <a name="components-collection"></a>Raccolta componenti

Contiene un oggetto per ogni componente nell'applicazione correlata. La raccolta **Components** è sempre correlata a un oggetto nella raccolta [**Applications**](applications.md) . Le proprietà esposte da questi oggetti contengono impostazioni effettuate a livello di componente.

Questa raccolta supporta il metodo [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , ma non il metodo [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) . Per installare o importare componenti in un'applicazione, usare i metodi sull'oggetto [**COMAdminCatalog**](comadmincatalog.md) .

## <a name="members"></a>Membri

La raccolta **Components** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**ErrorInfo**](errorinfo.md)
-   [**InterfacesForComponent**](interfacesforcomponent.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForComponent**](rolesforcomponent.md)
-   [**SubscriptionsForComponent**](subscriptionsforcomponent.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Applicazioni**](applications.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [AllowInprocSubscribers](#allowinprocsubscribers)
-   [ApplicationID](#applicationid)
-   [Numero di bit](#bitness)
-   [CLSID](#multiinterfacepublisherfilterclsid)
-   [ComponentAccessChecksEnabled](#componentaccesschecksenabled)
-   [ComponentTransactionTimeout](#componenttransactiontimeoutenabled)
-   [ComponentTransactionTimeoutEnabled](#componenttransactiontimeoutenabled)
-   [COMTIIntrinsics](#comtiintrinsics)
-   [ConstructionEnabled](#constructionenabled)
-   [ConstructorString](#constructorstring)
-   [CreationTimeout](#creationtimeout)
-   [Descrizione](#description)
-   [DLL](#dll)
-   [EventTrackingEnabled](#eventtrackingenabled)
-   [P:System.EnterpriseServices.ExceptionClassAttribute.Value](#exceptionclass)
-   [FireInParallel](#fireinparallel)
-   [IISIntrinsics](#iisintrinsics)
-   [InitializeServerApplication](#initializeserverapplication)
-   [IsEnabled](#isenabled)
-   [IsEventClass](#iseventclass)
-   [IsInstalled](#isinstalled)
-   [IsPrivateComponent](#isprivatecomponent)
-   [JustInTimeActivation](#justintimeactivation)
-   [LoadBalancingSupported](#loadbalancingsupported)
-   [MaxPoolSize](#maxpoolsize)
-   [MinPoolSize](#minpoolsize)
-   [MultiInterfacePublisherFilterCLSID](#multiinterfacepublisherfilterclsid)
-   [MustRunInClientContext](#mustruninclientcontext)
-   [MustRunInDefaultContext](#mustrunindefaultcontext)
-   [ObjectPoolingEnabled](#objectpoolingenabled)
-   [ProgID](#progid)
-   [PublisherID](#publisherid)
-   [SoapAssemblyName](#soapassemblyname)
-   [SoapTypeName](#soaptypename)
-   [Sincronizzazione](#synchronization)
-   [ThreadingModel](#threadingmodel)
-   [Transazione](#componenttransactiontimeout)
-   [Proprietà TxIsolationLevel](#txisolationlevel)
-   [VersionBuild](#versionbuild)
-   [VersionMajor](#versionmajor)
-   [VersionMinor](#versionminor)
-   [VersionSubBuild](#versionsubbuild)

### <a name="allowinprocsubscribers"></a>AllowInprocSubscribers



| Voce | Valore |
|----------------|--------------------------------------------------------------------|
| Descrizione    | Abilita nei Sottoscrittori di processo se il componente è una classe di evento. |
| Access         | ReadWrite                                                          |
| Tipo           | Bool                                                               |
| Predefinito        | Vero                                                               |
| Sistema minimo | Windows 2000                                                       |



 

### <a name="applicationid"></a>ApplicationID



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | GUID per l'applicazione contenente il componente. Deve essere un GUID di un'applicazione valida, che viene verificato prima che venga chiamato [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) . Se questo valore viene modificato in modo da essere un GUID per un'altra applicazione, il componente si sposta sull'applicazione. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                        |
| Type           | string                                                                                                                                                                                                                                                                                           |
| Predefinito        | N/D                                                                                                                                                                                                                                                                                              |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                     |



 

### <a name="bitness"></a>Numero di bit



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Rappresenta il tipo di bit binario di un componente. Nei sistemi che utilizzano Windows a 64 bit, questa proprietà distingue tra i componenti a 64 bit e i componenti a 32 bit. |
| Access         | ReadOnly                                                                                                                                                            |
| Tipo           | Valori lunghi possibili: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)                                                                                       |
| Predefinito        | N/D                                                                                                                                                                 |
| Sistema minimo | Windows XP                                                                                                                                                          |



 

### <a name="clsid"></a>CLSID



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | GUID per il componente. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                  |
| Type           | string                                                                                                                                                    |
| Predefinito        | N/D                                                                                                                                                       |
| Sistema minimo | Windows 2000                                                                                                                                              |



 

### <a name="componentaccesschecksenabled"></a>ComponentAccessChecksEnabled



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica se i controlli degli accessi in base al ruolo vengono eseguiti sulle chiamate al componente e funzionano insieme alle proprietà AccessChecksLevel e ApplicationAccessChecksEnabled nell'applicazione. |
| Access         | ReadWrite                                                                                                                                                                                                  |
| Tipo           | Bool                                                                                                                                                                                                       |
| Predefinito        | Falso                                                                                                                                                                                                      |
| Sistema minimo | Windows 2000                                                                                                                                                                                               |



 

### <a name="componenttransactiontimeout"></a>ComponentTransactionTimeout



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Se utilizzata in una transazione, specifica il periodo di tempo in cui il componente causa il timeout della transazione. Il valore predefinito è 60 secondi e non può essere più lungo di 3600 secondi (1 ora). Il valore di timeout può essere impostato su 0, specificando un periodo di timeout delle transazioni infinito. Per usare questa proprietà, ComponentTransactionTimeoutEnabled deve essere true. Il valore di questa proprietà esegue l'override del timeout della transazione globale specificato dalla proprietà TransactionTimeout della raccolta [**LocalComputer**](localcomputer.md) . |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Tipo           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Predefinito        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="componenttransactiontimeoutenabled"></a>ComponentTransactionTimeoutEnabled



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Specifica se il periodo di timeout della transazione è abilitato per questo componente. Per impostazione predefinita, la funzionalità di timeout della transazione è disabilitata. Quando questa proprietà è true, viene usato il timeout specificato da ComponentTransactionTimeout. Quando questa proprietà è false, viene usato il timeout specificato dalla proprietà TransactionTimeout della raccolta [**LocalComputer**](localcomputer.md) . |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                      |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                           |
| Predefinito        | Falso                                                                                                                                                                                                                                                                                                                                                                                          |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="comtiintrinsics"></a>COMTIIntrinsics



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Consente il passaggio delle proprietà di contesto dal COM Transaction Integrator (COMTI) nel contesto per questa classe. COMTI semplifica l'attività di wrapping delle transazioni mainframe e della logica di business come componenti COM. |
| Access         | ReadWrite                                                                                                                                                                                                            |
| Tipo           | Bool                                                                                                                                                                                                                 |
| Predefinito        | Falso                                                                                                                                                                                                                |
| Sistema minimo | Windows 2000                                                                                                                                                                                                         |



 

### <a name="constructionenabled"></a>ConstructionEnabled



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------|
| Descrizione    | Determina se ConstructorString viene passato all'oggetto quando viene costruito. |
| Access         | ReadWrite                                                                                |
| Tipo           | Bool                                                                                     |
| Predefinito        | Falso                                                                                    |
| Sistema minimo | Windows 2000                                                                             |



 

### <a name="constructorstring"></a>ConstructorString



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Stringa di inizializzazione per la costruzione di componenti. È possibile creare oggetti diversi dallo stesso componente generico usando stringhe del costruttore di oggetti. Se ConstructionEnabled è false, questa proprietà viene ignorata. |
| Access         | ReadWrite                                                                                                                                                                                                          |
| Type           | string                                                                                                                                                                                                             |
| Predefinito        | ""                                                                                                                                                                                                                 |
| Sistema minimo | Windows 2000                                                                                                                                                                                                       |



 

### <a name="creationtimeout"></a>CreationTimeout



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Quando si crea l'oggetto, numero di millisecondi prima che venga restituito un errore di timeout. Il timeout massimo è pari a 2147483647 millisecondi (circa 25 giorni). |
| Access         | ReadWrite                                                                                                                                              |
| Tipo           | Long (0-2147483647)                                                                                                                                    |
| Predefinito        | 0                                                                                                                                                      |
| Sistema minimo | Windows 2000                                                                                                                                           |



 

### <a name="description"></a>Descrizione



| Voce | Valore |
|----------------|--------------------------|
| Descrizione    | Descrive il componente. |
| Access         | ReadWrite                |
| Type           | string                   |
| Predefinito        | ""                       |
| Sistema minimo | Windows 2000             |



 

### <a name="dll"></a>DLL



| Voce | Valore |
|----------------|---------------------------------------------------------|
| Descrizione    | Nome e percorso del file contenente il componente. |
| Access         | ReadOnly                                                |
| Type           | string                                                  |
| Predefinito        | N/D                                                     |
| Sistema minimo | Windows 2000                                            |



 

### <a name="eventtrackingenabled"></a>EventTrackingEnabled



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina se gli eventi vengono rilevati. Gli eventi includono azioni come l'arresto dell'applicazione. creazione e rilascio di oggetti; riferimenti a oggetti, coerenza, attivazione e disattivazione; chiamate al metodo, restituzione ed eccezioni; avvio della transazione, preparazione al commit e interruzione; connessione, allocazione e riciclo del dispenser di risorse; allocazione e riciclo di thread. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                     |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                          |
| Predefinito        | Vero                                                                                                                                                                                                                                                                                                                                                                          |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="exceptionclass"></a>P:System.EnterpriseServices.ExceptionClassAttribute.Value



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Il CLSID, che può essere un GUID o una stringa del moniker, per attivare un programma alternativo durante il processo di gestione di un programma di componenti in coda con errori ripetuti. |
| Access         | ReadWrite                                                                                                                                                                 |
| Type           | string                                                                                                                                                                    |
| Predefinito        | ""                                                                                                                                                                        |
| Sistema minimo | Windows 2000                                                                                                                                                              |



 

### <a name="fireinparallel"></a>FireInParallel



| Voce | Valore |
|----------------|----------------------------------------------------------------------------|
| Descrizione    | Consente di attivare gli eventi in parallelo se il componente è una classe di evento. |
| Access         | ReadWrite                                                                  |
| Tipo           | Bool                                                                       |
| Predefinito        | Falso                                                                      |
| Sistema minimo | Windows 2000                                                               |



 

### <a name="iisintrinsics"></a>IISIntrinsics



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Consente il passaggio di proprietà di contesto IIS, ad esempio un oggetto sessione dell'applicazione o un oggetto sessione utente, nel contesto di questa classe. |
| Access         | ReadWrite                                                                                                                                   |
| Tipo           | Bool                                                                                                                                        |
| Predefinito        | Falso                                                                                                                                       |
| Sistema minimo | Windows 2000                                                                                                                                |



 

### <a name="initializeserverapplication"></a>InitializeServerApplication



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------|
| Descrizione    | Indica se il componente viene utilizzato per inizializzare un'applicazione server. |
| Access         | ReadWrite                                                                   |
| Tipo           | Bool                                                                        |
| Predefinito        | Falso                                                                       |
| Sistema minimo | Windows Server 2003                                                         |



 

### <a name="isenabled"></a>IsEnabled



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | False se l'applicazione o il componente COM+ è disabilitato. Se l'applicazione o il componente COM+ è abilitato, IsEnabled è true. |
| Access         | ReadWrite                                                                                                                   |
| Tipo           | Bool                                                                                                                        |
| Predefinito        | Vero                                                                                                                        |
| Sistema minimo | Windows XP                                                                                                                  |



 

### <a name="iseventclass"></a>IsEventClass



| Voce | Valore |
|----------------|----------------------------------------------------|
| Descrizione    | Indica se il componente è una classe di evento. |
| Access         | ReadOnly                                           |
| Tipo           | Bool                                               |
| Predefinito        | Falso                                              |
| Sistema minimo | Windows 2000                                       |



 

### <a name="isinstalled"></a>IsInstalled



| Voce | Valore |
|----------------|-----------------------------------------------------------------|
| Descrizione    | Indica se il componente è installato in un'applicazione. |
| Access         | ReadOnly                                                        |
| Tipo           | Bool                                                            |
| Predefinito        | Falso                                                           |
| Sistema minimo | Windows Server 2003                                             |



 

### <a name="isprivatecomponent"></a>IsPrivateComponent



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina se un'applicazione server è un componente privato. Un componente privato in un'applicazione server può essere attivato solo dall'interno dell'applicazione. Se, ad esempio, si chiama [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) su un componente privato, l'operazione non riesce da out-of-process ma ha esito positivo in-process. Al contrario, se si chiama **CoCreateInstance** su un componente pubblico, l'operazione ha esito positivo sia in-process che out-of-process. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Predefinito        | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="justintimeactivation"></a>JustInTimeActivation



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina se l' [attivazione JIT](enabling-jit-activation-for-a-component.md) è abilitata per il componente. Questa proprietà è impostata su true quando il [supporto delle transazioni](setting-the-transaction-attribute.md) è impostato su Required, richiede New o supported. Quando JustInTimeActivation è impostato su true, il [supporto della sincronizzazione](setting-the-synchronization-attribute.md) deve essere impostato su Required (impostazione predefinita) o richiede New. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Predefinito        | Falso                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="loadbalancingsupported"></a>LoadBalancingSupported



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Se il servizio di bilanciamento del carico dei componenti è installato e abilitato nel server, determina se il componente partecipa al bilanciamento del carico. |
| Access         | ReadWrite                                                                                                                                        |
| Tipo           | Bool                                                                                                                                             |
| Predefinito        | Falso                                                                                                                                            |
| Sistema minimo | Windows 2000                                                                                                                                     |



 

### <a name="maxpoolsize"></a>MaxPoolSize



| Voce | Valore |
|----------------|-----------------------------------|
| Descrizione    | Numero massimo di oggetti in pool. |
| Access         | ReadWrite                         |
| Tipo           | Long (1-1048576)                  |
| Predefinito        | 1048576                           |
| Sistema minimo | Windows 2000                      |



 

### <a name="minpoolsize"></a>MinPoolSize



| Voce | Valore |
|----------------|-----------------------------------|
| Descrizione    | Numero minimo di oggetti in pool. |
| Access         | ReadWrite                         |
| Tipo           | Long (0-1048576)                  |
| Predefinito        | 0                                 |
| Sistema minimo | Windows 2000                      |



 

### <a name="multiinterfacepublisherfilterclsid"></a>MultiInterfacePublisherFilterCLSID



| Voce | Valore |
|----------------|-------------------------------------------------------------------------|
| Descrizione    | CLSID per il filtro del server di pubblicazione utilizzato se il componente è una classe di evento. |
| Access         | ReadWrite                                                               |
| Type           | string                                                                  |
| Predefinito        | N/D                                                                     |
| Sistema minimo | Windows 2000                                                            |



 

### <a name="mustruninclientcontext"></a>MustRunInClientContext



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica che il componente deve essere attivato nel contesto del chiamante originale. In caso contrario, l'attivazione non riesce. |
| Access         | ReadWrite                                                                                                 |
| Tipo           | Bool                                                                                                      |
| Predefinito        | Falso                                                                                                     |
| Sistema minimo | Windows XP                                                                                                |



 

### <a name="mustrunindefaultcontext"></a>MustRunInDefaultContext



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica che il componente deve essere attivato nel contesto del chiamante predefinito. In caso contrario, l'attivazione non riesce. |
| Access         | ReadWrite                                                                                                    |
| Tipo           | Bool                                                                                                         |
| Predefinito        | Falso                                                                                                        |
| Sistema minimo | Windows 2000                                                                                                 |



 

### <a name="objectpoolingenabled"></a>ObjectPoolingEnabled



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------|
| Descrizione    | Determina se il [pool di oggetti com+](com--object-pooling.md) è abilitato per il componente. |
| Access         | ReadWrite                                                                                       |
| Tipo           | Bool                                                                                            |
| Predefinito        | Falso                                                                                           |
| Sistema minimo | Windows 2000                                                                                    |



 

### <a name="progid"></a>ProgID



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome descrittivo usato per identificare il componente. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                                              |
| Type           | string                                                                                                                                                                                |
| Predefinito        | N/D                                                                                                                                                                                   |
| Sistema minimo | Windows 2000                                                                                                                                                                          |



 

### <a name="publisherid"></a>PublisherID



| Voce | Valore |
|----------------|------------------------------------------------------------------------|
| Descrizione    | Identificatore per l'autore di eventi se il componente è una classe di evento. |
| Access         | ReadWrite                                                              |
| Type           | string                                                                 |
| Predefinito        | ""                                                                     |
| Sistema minimo | Windows 2000                                                           |



 

### <a name="soapassemblyname"></a>SoapAssemblyName



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------|
| Descrizione    | GUID che identifica l'assembly GAC eseguito quando il componente viene richiamato come servizio SOAP. |
| Access         | ReadWrite                                                                                        |
| Type           | string                                                                                           |
| Predefinito        | NULL                                                                                             |
| Sistema minimo | Windows Server 2003                                                                              |



 

### <a name="soaptypename"></a>SoapTypeName



| Voce | Valore |
|----------------|------------------------------------------------------------------------------|
| Descrizione    | Nome del tipo gestito per un componente che può essere richiamato come servizio SOAP. |
| Access         | ReadWrite                                                                    |
| Type           | string                                                                       |
| Predefinito        | NULL                                                                         |
| Sistema minimo | Windows Server 2003                                                          |



 

### <a name="synchronization"></a>Sincronizzazione



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina la [sincronizzazione](setting-the-synchronization-attribute.md) delle chiamate per il componente.                                                                                                     |
| Access         | ReadWrite                                                                                                                                                                                           |
| Tipo           | Valori lunghi possibili: COMAdminSynchronizationIgnored (0) COMAdminSynchronizationNone (1) COMAdminSynchronizationSupported (2) COMAdminSynchronizationRequired (3) COMAdminSynchronizationRequiresNew (4) |
| Predefinito        | COMAdminSynchronizationIgnored (0)                                                                                                                                                                  |
| Sistema minimo | Windows 2000                                                                                                                                                                                        |



 

### <a name="threadingmodel"></a>ThreadingModel



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina il modo in cui le istanze del componente vengono assegnate ai thread per l'esecuzione del metodo. I valori corrispondono ai modelli di threading COM.                                                                                        |
| Access         | ReadOnly                                                                                                                                                                                                                  |
| Tipo           | Valori lunghi possibili: COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) COMAdminThreadingModelNotSpecified (5) |
| Predefinito        | N/D                                                                                                                                                                                                                       |
| Sistema minimo | Windows 2000                                                                                                                                                                                                              |



 

### <a name="transaction"></a>Transazione



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina il modo in cui un componente supporta [le transazioni](setting-the-transaction-attribute.md). Si consiglia di usare le costanti nell'enumerazione e non i valori numerici. |
| Access         | ReadWrite                                                                                                                                                                              |
| Tipo           | Valori lunghi possibili: COMAdminTransactionIgnored (0) COMAdminTransactionNone (1) COMAdminTransactionSupported (2) COMAdminTransactionRequired (3) COMAdminTransactionRequiresNew (4)        |
| Predefinito        | COMAdminTransactionNone (1)                                                                                                                                                            |
| Sistema minimo | Windows 2000                                                                                                                                                                           |



 

### <a name="txisolationlevel"></a>Proprietà TxIsolationLevel



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica i livelli di isolamento delle transazioni. Sono disponibili cinque livelli di isolamento: nessuno, Read uncommitted, Read Committed, Repeatable Read e serialized. Il livello di isolamento predefinito viene serializzato.                           |
| Access         | ReadWrite                                                                                                                                                                                                                  |
| Tipo           | Valori lunghi possibili: COMAdminTxIsolationLevelAny (0) COMAdminTxIsolationLevelReadUnCommitted (1) COMAdminTxIsolationLevelReadCommitted (2) COMAdminTxIsolationLevelRepeatableRead (3) COMAdminTxIsolationLevelSerializable (4) |
| Predefinito        | COMAdminTxIsolationLevelSerializable (4)                                                                                                                                                                                   |
| Sistema minimo | Windows XP                                                                                                                                                                                                                 |



 

### <a name="versionbuild"></a>VersionBuild



| Voce | Valore |
|----------------|---------------------------|
| Descrizione    | Identificatore di compilazione della versione. |
| Access         | ReadOnly                  |
| Type           | string                    |
| Predefinito        | ""                        |
| Sistema minimo | Windows 2000              |



 

### <a name="versionmajor"></a>VersionMajor



| Voce | Valore |
|----------------|---------------------|
| Descrizione    | Identificatore di versione. |
| Access         | ReadOnly            |
| Type           | string              |
| Predefinito        | ""                  |
| Sistema minimo | Windows 2000        |



 

### <a name="versionminor"></a>VersionMinor



| Voce | Valore |
|----------------|-------------------------|
| Descrizione    | Identificatore secondario della versione. |
| Access         | ReadOnly                |
| Type           | string                  |
| Predefinito        | ""                      |
| Sistema minimo | Windows 2000            |



 

### <a name="versionsubbuild"></a>VersionSubBuild



| Voce | Valore |
|----------------|-------------------------------|
| Descrizione    | Identificatore della sottocompilazione della versione. |
| Access         | ReadOnly                      |
| Type           | string                        |
| Predefinito        | ""                            |
| Sistema minimo | Windows 2000                  |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
