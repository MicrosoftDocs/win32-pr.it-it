---
description: Contiene un oggetto per ogni applicazione COM+ installata nel computer locale. Le proprietà esposte da questi oggetti contengono tutte le impostazioni effettuate a livello di applicazione.
ms.assetid: c0c46592-5282-412d-8f54-67637be8218a
title: Raccolta di applicazioni
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Applications
api_type:
- COM
api_location: ''
ms.openlocfilehash: 54f286ae393e67d9732e21bc40cbb0f9c46d8c63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127171"
---
# <a name="applications-collection"></a>Raccolta di applicazioni

Contiene un oggetto per ogni applicazione COM+ installata nel computer locale. Le proprietà esposte da questi oggetti contengono tutte le impostazioni effettuate a livello di applicazione.

Per impostare le proprietà per i componenti all'interno di un'applicazione, utilizzare la raccolta [**componenti**](components.md) correlati. I ruoli vengono assegnati a un'applicazione tramite la raccolta di [**ruoli**](roles.md) correlati.

Per installare i componenti in un'applicazione, usare i metodi sull'oggetto [**COMAdminCatalog**](comadmincatalog.md) . Per installare un'applicazione da un file o per arrestare o esportare un'applicazione, usare anche i metodi sull'oggetto **COMAdminCatalog** . In caso contrario, per creare una nuova applicazione, è possibile aggiungere un oggetto alla raccolta di **applicazioni** .

Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta **Applications** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**ApplicationInstances**](applicationinstances.md)
-   [**Componenti**](components.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**LegacyComponents**](legacycomponents.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**Ruoli**](roles.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Partizioni**](partitions.md)
-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [3GigSupportEnabled](#3gigsupportenabled)
-   [AccessChecksLevel](#accesscheckslevel)
-   [Activation](#recycleactivationlimit)
-   [ApplicationAccessChecksEnabled](#applicationaccesschecksenabled)
-   [ApplicationDirectory](#applicationdirectory)
-   [ApplicationProxy](#applicationproxyservername)
-   [ApplicationProxyServerName](#applicationproxyservername)
-   [AppPartitionID](#apppartitionid)
-   [autenticazione](#authenticationcapability)
-   [AuthenticationCapability](#authenticationcapability)
-   [Modificabili](#changeable)
-   [CommandLine](#commandline)
-   [ConcurrentApps](#concurrentapps)
-   [CreatedBy](#createdby)
-   [CRMEnabled](#crmenabled)
-   [CRMLogFile](#crmlogfile)
-   [Cancellabile](#deleteable)
-   [Descrizione](#description)
-   [DumpEnabled](#dumpenabled)
-   [DumpOnException](#dumponexception)
-   [DumpOnFailfast](#dumponfailfast)
-   [DumpPath](#dumppath)
-   [EventsEnabled](#eventsenabled)
-   [ID](#applications-collection)
-   [Identità](#identity)
-   [ImpersonationLevel](#impersonationlevel)
-   [IsEnabled](#isenabled)
-   [IsSystem](#issystem)
-   [MaxDumpCount](#maxdumpcount)
-   [Nome](#applicationproxyservername)
-   [Password](#password)
-   [QCAuthenticateMsgs](#qcauthenticatemsgs)
-   [QCListenerMaxThreads](#qclistenermaxthreads)
-   [QueueListenerEnabled](#queuelistenerenabled)
-   [QueuingEnabled](#queuingenabled)
-   [RecycleActivationLimit](#recycleactivationlimit)
-   [RecycleCallLimit](#recyclecalllimit)
-   [RecycleExpirationTimeout](#recycleexpirationtimeout)
-   [RecycleLifetimeLimit](#recyclelifetimelimit)
-   [RecycleMemoryLimit](#recyclememorylimit)
-   [Replicabile](#replicable)
-   [RunForever](#runforever)
-   [ServiceName](#servicename)
-   [ShutdownAfter](#shutdownafter)
-   [SoapActivated](#soapactivated)
-   [SoapBaseUrl](#soapbaseurl)
-   [SoapMailTo](#soapmailto)
-   [SoapVRoot](#soapvroot)
-   [SRPEnabled](#srpenabled)
-   [SRPTrustLevel](#srptrustlevel)

### <a name="3gigsupportenabled"></a>3GigSupportEnabled



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica se l'applicazione può utilizzare 3 GB di memoria nel processo. Se questa funzionalità non è abilitata, l'applicazione può utilizzare solo 2 GB di memoria. |
| Access         | ReadWrite                                                                                                                                     |
| Tipo           | Bool                                                                                                                                          |
| Predefinito        | Falso                                                                                                                                         |
| Sistema minimo | Windows 2000                                                                                                                                  |



 

### <a name="accesscheckslevel"></a>AccessChecksLevel



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica se i controlli di accesso vengono eseguiti solo a livello di processo o a livello di processo e di componente. Si consiglia di usare le costanti nell'enumerazione e non i valori numerici. |
| Access         | ReadWrite                                                                                                                                                                                                       |
| Tipo           | Valori possibili lunghi: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                |
| Predefinito        | COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                                                                               |
| Sistema minimo | Windows 2000                                                                                                                                                                                                    |



 

### <a name="activation"></a>Activation



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | L'attivazione locale indica che gli oggetti all'interno dell'applicazione vengono eseguiti in un processo server locale dedicato (applicazione server). L'attivazione in-process indica che gli oggetti vengono eseguiti nel processo del creatore (applicazione libreria). |
| Access         | ReadWrite                                                                                                                                                                                                                           |
| Tipo           | Valori possibili lunghi: COMAdminActivationInproc (0) COMAdminActivationLocal (1)                                                                                                                                                        |
| Predefinito        | COMAdminActivationLocal (1)                                                                                                                                                                                                         |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a>ApplicationAccessChecksEnabled



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------|
| Descrizione    | Indica se vengono eseguiti controlli di accesso per l'applicazione quando i client effettuano chiamate al suo interno. |
| Access         | ReadWrite                                                                                          |
| Tipo           | Bool                                                                                               |
| Predefinito        | Vero                                                                                               |
| Sistema minimo | Windows 2000                                                                                       |



 

### <a name="applicationdirectory"></a>ApplicationDirectory



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Percorso completo dell'applicazione. Queste informazioni sono necessarie per la configurazione di assembly side-by-Side (SxS). Gli assembly side-by-Side (SxS) consentono alle applicazioni ASP di specificare quale versione di una DLL di sistema supportata da SxS usare, ad esempio MSVCRT, MSXML, COMCTL, GDIPLUS e così via. Se, ad esempio, l'applicazione ASP si basa su MSVCRT versione 2,0, è possibile assicurarsi che l'applicazione utilizzi ancora MSVCRT versione 2,0 anche dopo l'applicazione dei Service Pack al server. Qualsiasi nuova versione di MSVCRT è ancora installata nel computer, ma la versione 2,0 rimane e viene usata dall'applicazione. Le DLL supportate da SxS sono archiviate in% WINDIR% \\ WinSxS. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Type           | string                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Predefinito        | ""                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> È possibile utilizzare una sola versione di una DLL di sistema in qualsiasi pool di applicazioni, anche se questa funzionalità è configurabile a livello di applicazione. Se ad esempio l'applicazione App1 usa MSVCRT, la versione 2,5 e l'applicazione App2 usano MSVCRT, versione 2,4, App1 e App2 non devono trovarsi nello stesso pool di applicazioni. In caso affermativo, l'applicazione caricata per prima dispone della versione di MSVCRT caricata e l'altra applicazione viene forzata a utilizzarla finché le applicazioni non vengono scaricate.

 

Per ulteriori informazioni, vedere "assembly affiancati" nelle [modifiche apportate ai servizi com+ in IIS 6,0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).

### <a name="applicationproxy"></a>ApplicationProxy



| Voce | Valore |
|----------------|------------------------------------------------------------|
| Descrizione    | Indica se l'applicazione è un proxy di applicazione. |
| Access         | ReadOnly                                                   |
| Tipo           | Bool                                                       |
| Predefinito        | Falso                                                      |
| Sistema minimo | Windows 2000                                               |



 

### <a name="applicationproxyservername"></a>ApplicationProxyServerName



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome del server remoto utilizzato per l'esportazione del proxy di applicazione. Si tratta del nome del server a cui punta il proxy applicazione quando viene installato in un computer client. |
| Access         | ReadWrite                                                                                                                                                              |
| Type           | string                                                                                                                                                                 |
| Predefinito        | ""                                                                                                                                                                     |
| Sistema minimo | Windows 2000                                                                                                                                                           |



 

### <a name="apppartitionid"></a>AppPartitionID



| Voce | Valore |
|----------------|---------------------------------------------------|
| Descrizione    | GUID che rappresenta l'ID della partizione dell'applicazione. |
| Access         | ReadOnly                                          |
| Type           | string                                            |
| Predefinito        | <Generated>                                 |
| Sistema minimo | Windows Server 2003                               |



 

### <a name="authentication"></a>Authentication



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Imposta il livello di autenticazione per le chiamate, con i valori corrispondenti alle impostazioni di autenticazione RPC (Remote Procedure Call). Quando si sceglie COMAdminAuthenticationDefault, viene utilizzata l'impostazione nella proprietà DefaultAuthenticationLevel all'interno della raccolta [**LocalComputer**](localcomputer.md) . |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                             |
| Tipo           | Valori lunghi possibili: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)                                              |
| Predefinito        | COMAdminAuthenticationPacket (4)                                                                                                                                                                                                                                                                      |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> Per le applicazioni di libreria (in-process), le uniche impostazioni valide sono COMAdminAuthenticationDefault e COMAdminAuthenticationNone. Si consiglia di usare le costanti nell'enumerazione e non i valori numerici.

 

### <a name="authenticationcapability"></a>AuthenticationCapability



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina quale identità viene presentata quando vengono rappresentate le chiamate.                                                                                                                                                                      |
| Access         | ReadWrite                                                                                                                                                                                                                               |
| Tipo           | Valori lunghi possibili: COMAdminAuthenticationCapabilitiesNone (0x0) COMAdminAuthenticationCapabilitiesSecureReference (0x2) COMAdminAuthenticationCapabilitiesStaticCloaking (0x20) COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40) |
| Predefinito        | COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)                                                                                                                                                                                |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                            |



 

### <a name="changeable"></a>Modificabili



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina se le modifiche apportate alle impostazioni dell'applicazione o ai relativi componenti sono consentite, a livello di codice o tramite lo strumento di amministrazione Servizi componenti. |
| Access         | ReadWrite                                                                                                                                                                     |
| Tipo           | Bool                                                                                                                                                                          |
| Predefinito        | Vero                                                                                                                                                                          |
| Sistema minimo | Windows 2000                                                                                                                                                                  |



 

### <a name="commandline"></a>CommandLine



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Stringa della riga di comando da utilizzare per il debug. L'applicazione può essere avviata in un debugger con la riga di comando specificata. |
| Access         | ReadWrite                                                                                                                  |
| Type           | string                                                                                                                     |
| Predefinito        | ""                                                                                                                         |
| Sistema minimo | Windows 2000                                                                                                               |



 

### <a name="concurrentapps"></a>ConcurrentApps



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------|
| Descrizione    | Specifica il numero massimo di applicazioni in pool che possono essere eseguite simultaneamente. |
| Access         | ReadWrite                                                                        |
| Tipo           | Long (1-1048576)                                                                 |
| Predefinito        | 1                                                                                |
| Sistema minimo | Windows XP                                                                       |



 

### <a name="createdby"></a>CreatedBy



| Voce | Valore |
|----------------|---------------------------------------------------------------|
| Descrizione    | Stringa informativa per descrivere chi ha creato l'applicazione. |
| Access         | ReadWrite                                                     |
| Type           | string                                                        |
| Predefinito        | ""                                                            |
| Sistema minimo | Windows 2000                                                  |



 

### <a name="crmenabled"></a>CRMEnabled



| Voce | Valore |
|----------------|------------------------------------------------------------------|
| Descrizione    | Determina se il Gestione risorse di compensazione è abilitato. |
| Access         | ReadWrite                                                        |
| Tipo           | Bool                                                             |
| Predefinito        | Falso                                                            |
| Sistema minimo | Windows 2000                                                     |



 

### <a name="crmlogfile"></a>CRMLogFile



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------|
| Descrizione    | Nome e percorso del file per il mantenimento del log per il CRM (Compensating Resource Manager). |
| Access         | ReadWrite                                                                              |
| Type           | string                                                                                 |
| Predefinito        | ""                                                                                     |
| Sistema minimo | Windows 2000                                                                           |



 

### <a name="deleteable"></a>Cancellabile



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Consente di specificare se l'applicazione può essere eliminata, a livello di codice o tramite lo strumento di amministrazione Servizi componenti. |
| Access         | ReadWrite                                                                                                                   |
| Tipo           | Bool                                                                                                                        |
| Predefinito        | Vero                                                                                                                        |
| Sistema minimo | Windows 2000                                                                                                                |



 

### <a name="description"></a>Descrizione



| Voce | Valore |
|----------------|----------------------------|
| Descrizione    | Descrive l'applicazione. |
| Access         | ReadWrite                  |
| Type           | string                     |
| Predefinito        | ""                         |
| Sistema minimo | Windows 2000               |



 

### <a name="dumpenabled"></a>DumpEnabled



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------|
| Descrizione    | Consente di eseguire il dump dello stato di un'applicazione COM+ al momento dell'errore in una directory designata. |
| Access         | ReadWrite                                                                                             |
| Tipo           | Bool                                                                                                  |
| Predefinito        | Falso                                                                                                 |
| Sistema minimo | Windows XP                                                                                            |



 

> [!Note]  
> A partire da Windows Server 2003, solo gli amministratori dispongono di privilegi di accesso in lettura ai file di dump COM+.

 

### <a name="dumponexception"></a>DumpOnException



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Consente il dump dello stato di un'applicazione COM+ quando l'applicazione causa un'eccezione non gestita e viene terminata dal runtime COM+. |
| Access         | ReadWrite                                                                                                                                     |
| Tipo           | Bool                                                                                                                                          |
| Predefinito        | Falso                                                                                                                                         |
| Sistema minimo | Windows XP                                                                                                                                    |



 

### <a name="dumponfailfast"></a>DumpOnFailfast



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------|
| Descrizione    | Abilita il dump dello stato di un'applicazione COM+ in caso di errore dell'applicazione. |
| Access         | ReadWrite                                                                       |
| Tipo           | Bool                                                                            |
| Predefinito        | Falso                                                                           |
| Sistema minimo | Windows XP                                                                      |



 

### <a name="dumppath"></a>DumpPath



| Voce | Valore |
|----------------|--------------------------------------------------------------|
| Descrizione    | Percorso della directory in cui vengono salvati i file di dump. |
| Access         | ReadWrite                                                    |
| Type           | string                                                       |
| Predefinito        | "% SystemRoot% \\ system32 \\ com \\ "                           |
| Sistema minimo | Windows XP                                                   |



 

> [!Note]  
> A partire da Windows Server 2003, solo gli amministratori dispongono di privilegi di accesso in lettura ai file di dump COM+.

 

### <a name="eventsenabled"></a>EventsEnabled



| Voce | Valore |
|----------------|-----------------------------------------------------------|
| Descrizione    | Indica se gli eventi sono abilitati per l'applicazione. |
| Access         | ReadWrite                                                 |
| Tipo           | Bool                                                      |
| Predefinito        | Vero                                                      |
| Sistema minimo | Windows 2000                                              |



 

### <a name="id"></a>ID



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | GUID che rappresenta l'applicazione. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                            |
| Type           | string                                                                                                                                                               |
| Predefinito        | <Generated>                                                                                                                                                    |
| Sistema minimo | Windows 2000                                                                                                                                                         |



 

### <a name="identity"></a>Identità



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Imposta l'identità del processo server per l'applicazione. Specificare un account utente valido o "utente interattivo" per fare in modo che l'applicazione presupponga l'identità dell'utente che ha eseguito l'accesso corrente. È inoltre possibile specificare le stringhe "NT Authority \\ LocalService", "NT Authority \\ NetworkService" e "NT Authority \\ System". La password predefinita per questi tre account è "" (stringa vuota). |
| Access         |                                                                                                                                                                                                                                                                                                                                                                                    |
| Type           |                                                                                                                                                                                                                                                                                                                                                                                    |
| Predefinito        |                                                                                                                                                                                                                                                                                                                                                                                    |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                       |



 

La proprietà Identity non è abilitata per le applicazioni di libreria, che vengono eseguite nel processo client.

È necessario impostare la proprietà password contemporaneamente a Identity, prima di usare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), perché la password e l'identità vengono convalidate prima di essere salvate. Se la password e l'identità non vengono sincronizzate, l'applicazione non può essere avviata finché non vengono reimpostati da un amministratore.

### <a name="impersonationlevel"></a>ImpersonationLevel



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Imposta il livello di rappresentazione usato per le chiamate effettuate ad altre applicazioni.                                                                                           |
| Access         | ReadWrite                                                                                                                                                     |
| Tipo           | Valori lunghi possibili: COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4) |
| Predefinito        | COMAdminImpersonationImpersonate (3)                                                                                                                          |
| Sistema minimo | Windows 2000                                                                                                                                                  |



 

### <a name="isenabled"></a>IsEnabled



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Se l'applicazione o il componente COM+ è disabilitato, IsEnabled è false. Se l'applicazione o il componente COM+ è abilitato, IsEnabled è true. |
| Access         | ReadWrite                                                                                                                                 |
| Tipo           | Bool                                                                                                                                      |
| Predefinito        | Vero                                                                                                                                      |
| Sistema minimo | Windows XP                                                                                                                                |



 

### <a name="issystem"></a>IsSystem



| Voce | Valore |
|----------------|--------------------------------------|
| Descrizione    | Identifica le applicazioni di sistema COM+. |
| Access         | ReadOnly                             |
| Tipo           | Bool                                 |
| Predefinito        | Falso                                |
| Sistema minimo | Windows 2000                         |



 

### <a name="maxdumpcount"></a>MaxDumpCount



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------|
| Descrizione    | Indica il numero massimo di file da generare prima che si verifichi la sovrascrittura. |
| Access         | ReadWrite                                                                        |
| Tipo           | Long (1-200)                                                                     |
| Predefinito        | 5                                                                                |
| Sistema minimo | Windows XP                                                                       |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome dell'applicazione. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadWrite                                                                                                                                                                                                                            |
| Type           | string                                                                                                                                                                                                                               |
| Predefinito        | "Nuova applicazione"                                                                                                                                                                                                                    |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                         |



 

> [!Note]  
> I nomi univoci devono essere scelti per le applicazioni. Se vengono create più applicazioni con lo stesso nome, può interferire con il riferimento alle applicazioni in base al nome, causando un comportamento imprevedibile.

 

### <a name="password"></a>Password



| Voce | Valore |
|----------------|----------------------------------------------------------------------------|
| Descrizione    | Imposta la password utilizzata dal processo server per accedere con l'identità. |
| Access         | WriteOnly                                                                  |
| Type           | string                                                                     |
| Predefinito        | ""                                                                         |
| Sistema minimo | Windows 2000                                                               |



 

È necessario impostare la password nello stesso momento dell'identità, prima di usare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), perché la password e l'identità vengono convalidate prima di essere salvate. Se la password e l'identità non vengono sincronizzate, l'applicazione non può essere avviata finché non vengono reimpostati da un amministratore.

### <a name="qcauthenticatemsgs"></a>QCAuthenticateMsgs



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica in quali circostanze vengono autenticate le richieste accodate a un'applicazione.                                                 |
| Access         | ReadWrite                                                                                                                               |
| Tipo           | Valori lunghi possibili: COMAdminQCMessageAuthenticateSecureApps (0) COMAdminQCMessageAuthenticateOff (1) COMAdminQCMessageAuthenticateOn (2) |
| Predefinito        | COMAdminQCMessageAuthenticateSecureApps (0)                                                                                             |
| Sistema minimo | Windows XP                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a>QCListenerMaxThreads



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica il numero massimo di thread di listener simultanei. L'intervallo valido per questa proprietà è compreso tra 0 e 1000. Per un'applicazione appena creata, l'impostazione è derivata dall'algoritmo attualmente utilizzato per determinare il numero predefinito di thread del listener: 16 volte il numero di CPU nel server. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                 |
| Tipo           | Long (0-1000)                                                                                                                                                                                                                                                                                             |
| Predefinito        | 0                                                                                                                                                                                                                                                                                                         |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Questa proprietà è disponibile anche con funzionalità di lettura/scrittura dalla scheda **Accodamento** dello strumento di amministrazione Servizi componenti.

 

### <a name="queuelistenerenabled"></a>QueueListenerEnabled



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica se il listener dei componenti in coda è abilitato per l'applicazione. Se abilitata, il listener viene avviato all'avvio dell'applicazione. Questa proprietà ha effetto solo se QueuingEnabled è impostato su true. |
| Access         | ReadWrite                                                                                                                                                                                                            |
| Tipo           | Bool                                                                                                                                                                                                                 |
| Predefinito        | Falso                                                                                                                                                                                                                |
| Sistema minimo | Windows 2000                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a>QueuingEnabled



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------|
| Descrizione    | Indica se il servizio COM+ Queued Components è abilitato per l'applicazione. |
| Access         | ReadWrite                                                                            |
| Tipo           | Bool                                                                                 |
| Predefinito        | Falso                                                                                |
| Sistema minimo | Windows 2000                                                                         |



 

### <a name="recycleactivationlimit"></a>RecycleActivationLimit



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica il numero massimo di attivazioni di oggetti configurati nell'applicazione da accettare prima del riciclo del processo. Il numero predefinito di attivazioni è 0. |
| Access         | ReadWrite                                                                                                                                                            |
| Tipo           | Long (0-1048576)                                                                                                                                                     |
| Predefinito        | 0                                                                                                                                                                    |
| Sistema minimo | Windows XP                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a>RecycleCallLimit



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica il numero massimo di chiamate che consentono agli oggetti configurati nell'applicazione di accettare prima di riciclare il processo. Il numero predefinito di chiamate è 0. |
| Access         | ReadWrite                                                                                                                                                      |
| Tipo           | Long (0-1048576)                                                                                                                                               |
| Predefinito        | 0                                                                                                                                                              |
| Sistema minimo | Windows XP                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a>RecycleExpirationTimeout



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica la quantità di tempo (in minuti) per consentire l'esecuzione di un processo riciclato prima di arrestarlo. Il conto alla rovescia inizia subito dopo il riciclo del processo. Il timeout di scadenza massimo è di 1440 minuti (24 ore) e il valore predefinito è 15 minuti. |
| Access         | ReadWrite                                                                                                                                                                                                                                                        |
| Tipo           | Long (1-1440)                                                                                                                                                                                                                                                    |
| Predefinito        | 15                                                                                                                                                                                                                                                               |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a>RecycleLifetimeLimit



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica il numero massimo di minuti per consentire l'esecuzione di un processo prima del riciclo. Il limite massimo di durata è di 30240 minuti (21 giorni) e il valore predefinito è 0 minuti. |
| Access         | ReadWrite                                                                                                                                                                   |
| Tipo           | Long (0-30240)                                                                                                                                                              |
| Predefinito        | 0                                                                                                                                                                           |
| Sistema minimo | Windows XP                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a>RecycleMemoryLimit



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica la quantità massima di utilizzo di memoria (in kilobyte) consentita prima che venga riciclata. Se l'utilizzo della memoria del processo supera il numero specificato per un periodo più lungo di un minuto, il processo viene riciclato. La quantità predefinita di utilizzo della memoria è 0 KB. |
| Access         | ReadWrite                                                                                                                                                                                                                                                              |
| Tipo           | Long (0-1048576)                                                                                                                                                                                                                                                       |
| Predefinito        | 0                                                                                                                                                                                                                                                                      |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a>Replicabile



| Voce | Valore |
|----------------|------------------------------------------------------|
| Descrizione    | Indica se l'applicazione può essere replicata. |
| Access         | ReadWrite                                            |
| Tipo           | Bool                                                 |
| Predefinito        | Vero                                                 |
| Sistema minimo | Windows XP                                           |



 

### <a name="runforever"></a>RunForever



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Consente a un processo server di continuare se un'applicazione è inattiva. Se impostato su true, il processo server non viene arrestato quando viene lasciato inattivo. Se impostato su false, il processo viene arrestato in base al valore impostato dalla proprietà ShutdownAfter. RunForever non è abilitato per le applicazioni di libreria (in-process). |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                     |
| Predefinito        | Falso                                                                                                                                                                                                                                                                                                    |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a>ServiceName



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome del servizio corrispondente all'applicazione configurata per l'esecuzione come applicazione di servizio. Se questo valore è **null**, l'applicazione non è configurata per l'esecuzione come servizio. In caso contrario, è possibile trovare le informazioni di configurazione per il servizio utilizzando il nome del servizio. |
| Access         | ReadOnly                                                                                                                                                                                                                                                                         |
| Type           | string                                                                                                                                                                                                                                                                           |
| Predefinito        | ""                                                                                                                                                                                                                                                                               |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a>ShutdownAfter



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Imposta il ritardo prima di arrestare un processo server dopo che diventa inattivo. La latenza di arresto è compresa tra 0 e 1440 minuti (24 ore). Se RunForever è impostato su true, questa proprietà viene ignorata. ShutdownAfter non è abilitato per le applicazioni di libreria (in-process). |
| Access         | ReadWrite                                                                                                                                                                                                                                                          |
| Tipo           | Long (0-1440)                                                                                                                                                                                                                                                      |
| Predefinito        | 3                                                                                                                                                                                                                                                                  |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a>SoapActivated



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------|
| Descrizione    | Indica se l'applicazione viene esposta per l'utilizzo tramite il protocollo SOAP. |
| Access         | ReadWrite                                                                            |
| Tipo           | Bool                                                                                 |
| Predefinito        | Falso                                                                                |
| Sistema minimo | Windows Server 2003                                                                  |



 

### <a name="soapbaseurl"></a>SoapBaseUrl



| Voce | Valore |
|----------------|------------------------------------------------------------------------------|
| Descrizione    | Endpoint URL in corrispondenza del quale l'applicazione viene esposta tramite il protocollo SOAP. |
| Access         | ReadWrite                                                                    |
| Type           | string                                                                       |
| Predefinito        | ""                                                                           |
| Sistema minimo | Windows Server 2003                                                          |



 

### <a name="soapmailto"></a>SoapMailTo



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------|
| Descrizione    | Indirizzo di posta elettronica in cui l'applicazione viene esposta tramite il protocollo SOAP. |
| Access         | ReadWrite                                                                     |
| Type           | string                                                                        |
| Predefinito        | ""                                                                            |
| Sistema minimo | Windows Server 2003                                                           |



 

### <a name="soapvroot"></a>SoapVRoot



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Directory radice virtuale di IIS in cui risiedono gli script di accesso che espongono l'applicazione tramite il protocollo SOAP. |
| Access         | ReadWrite                                                                                                            |
| Type           | string                                                                                                               |
| Predefinito        | ""                                                                                                                   |
| Sistema minimo | Windows Server 2003                                                                                                  |



 

### <a name="srpenabled"></a>SRPEnabled



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina i criteri di restrizione software per l'applicazione. Se è impostato su true, viene usata la proprietà SRPTrustLevel per l'applicazione. Se è impostato su false, vengono usati i criteri di restrizione software dalle impostazioni di sicurezza locali. Le impostazioni di sicurezza locali vengono controllate tramite lo snap-in criteri di sicurezza locali di Microsoft Management Console. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                             |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                  |
| Predefinito        | Falso                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica il livello di attendibilità del criterio di restrizione software dell'applicazione. Questa proprietà viene utilizzata solo se la proprietà SRPEnabled è impostata su true. Il livello di attendibilità SRP si riferisce al livello di attendibilità che si è disposti a assegnare a un'applicazione. Un livello di attendibilità Unrestricted SRP corrisponde \_ al \_ valore di enumerazione LEVELID FULLYTRUSTED più sicuro, mentre un livello di ATTENDIBILità SRP non consentito corrisponde al \_ valore di enumerazione non consentito LEVELID più sicuro \_ . L'enumerazione per i livelli di attendibilità è definita in Winsafer. h. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Tipo           | Valori lunghi possibili: SAFER \_ LEVELID non \_ consentita (0x0) Safer \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Predefinito        | SAFER \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

Un'applicazione che si è disposti a considerare attendibile con accesso senza restrizioni deve avere la protezione più rigorosa collegata. Le applicazioni senza restrizioni possono caricare solo componenti senza restrizioni, mentre le applicazioni non consentite non potranno essere eseguite e pertanto non potranno caricare alcun componente.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
