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
ms.openlocfilehash: 23ce8d7dc343e9cbca9aab642aee99424c5fffdde8ef0f15a52d2959bf492095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549426"
---
# <a name="applications-collection"></a>Raccolta di applicazioni

Contiene un oggetto per ogni applicazione COM+ installata nel computer locale. Le proprietà esposte da questi oggetti contengono tutte le impostazioni effettuate a livello di applicazione.

È possibile impostare le proprietà per i componenti all'interno di un'applicazione usando la raccolta [**Components**](components.md) correlata. Per assegnare ruoli a un'applicazione, usare la raccolta [**Ruoli**](roles.md) correlata.

Per installare i componenti in un'applicazione, usare i metodi [**nell'oggetto COMAdminCatalog.**](comadmincatalog.md) Per installare un'applicazione da un file o arrestare o esportare un'applicazione, usare anche i metodi **nell'oggetto COMAdminCatalog.** In caso contrario, per creare una nuova applicazione, è possibile aggiungere un oggetto alla **raccolta Applications.**

Questa raccolta supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta Applications** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**ApplicationInstances**](applicationinstances.md)
-   [**Componenti**](components.md)
-   [**Errorinfo**](errorinfo.md)
-   [**LegacyComponents**](legacycomponents.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**Ruoli**](roles.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Partizioni**](partitions.md)
-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [3GigSupportEnabled](#3gigsupportenabled)
-   [AccessChecksLevel](#accesscheckslevel)
-   [Activation](#recycleactivationlimit)
-   [ApplicationAccessChecksEnabled](#applicationaccesschecksenabled)
-   [Applicationdirectory](#applicationdirectory)
-   [ApplicationProxy](#applicationproxyservername)
-   [ApplicationProxyServerName](#applicationproxyservername)
-   [AppPartitionID](#apppartitionid)
-   [autenticazione](#authenticationcapability)
-   [AuthenticationCapability](#authenticationcapability)
-   [Variabile](#changeable)
-   [CommandLine](#commandline)
-   [ConcurrentApps](#concurrentapps)
-   [CreatedBy](#createdby)
-   [CRMEnabled](#crmenabled)
-   [CRMLogFile](#crmlogfile)
-   [Eliminabile](#deleteable)
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
-   [Servicename](#servicename)
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
| Descrizione    | Indica se l'applicazione può usare 3 GB di memoria nel processo. Se questa opzione non è abilitata, l'applicazione può usare solo 2 GB di memoria. |
| Access         | ReadWrite                                                                                                                                     |
| Tipo           | Bool                                                                                                                                          |
| Predefinito        | Falso                                                                                                                                         |
| Sistema minimo | Windows 2000                                                                                                                                  |



 

### <a name="accesscheckslevel"></a>AccessChecksLevel



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica se i controlli di accesso vengono eseguiti solo a livello di processo o a livello di processo e di componente. È consigliabile usare le costanti nell'enumerazione e non i valori numerici. |
| Access         | ReadWrite                                                                                                                                                                                                       |
| Tipo           | Valori possibili lunghi: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                |
| Predefinito        | COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                                                                               |
| Sistema minimo | Windows 2000                                                                                                                                                                                                    |



 

### <a name="activation"></a>Activation



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | L'attivazione locale indica che gli oggetti all'interno dell'applicazione vengono eseguiti all'interno di un processo server locale dedicato (applicazione server). L'attivazione in-process indica che gli oggetti vengono eseguiti nel processo dell'autore (applicazione libreria). |
| Access         | ReadWrite                                                                                                                                                                                                                           |
| Tipo           | Valori possibili long:COMAdminActivationInproc (0)COMAdminActivationLocal (1)                                                                                                                                                        |
| Predefinito        | COMAdminActivationLocal (1)                                                                                                                                                                                                         |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a>ApplicationAccessChecksEnabled



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------|
| Descrizione    | Indica se vengono eseguiti controlli di accesso per l'applicazione quando i client effettuano chiamate all'applicazione. |
| Access         | ReadWrite                                                                                          |
| Tipo           | Bool                                                                                               |
| Predefinito        | Vero                                                                                               |
| Sistema minimo | Windows 2000                                                                                       |



 

### <a name="applicationdirectory"></a>Applicationdirectory



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Percorso completo dell'applicazione. Queste informazioni sono necessarie quando si configurano assembly side-by-side (SxS). Gli assembly side-by-side (SxS) consentono alle applicazioni ASP di specificare la versione di una DLL di sistema supportata da SxS da usare, ad esempio MSVCRT, MSXML, COMCTL, GDIPLUS e così via. Ad esempio, se l'applicazione ASP si basa su MSVCRT versione 2.0, è possibile assicurarsi che l'applicazione usi ancora MSVCRT versione 2.0 anche dopo l'applicazione dei Service Pack al server. Qualsiasi nuova versione di MSVCRT è ancora installata nel computer, ma la versione 2.0 rimane e viene usata dall'applicazione. Le DLL supportate da SxS vengono archiviate in %WINDIR% \\ WinSxS. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Type           | string                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Predefinito        | ""                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> È possibile usare una sola versione di una DLL di sistema in qualsiasi pool di applicazioni, anche se questa funzionalità è configurabile a livello di applicazione. Ad esempio, se l'applicazione App1 usa MSVCRT, la versione 2.5 e l'applicazione App2 usa MSVCRT, versione 2.4, App1 e App2 non devono essere nello stesso pool di applicazioni. In caso contrario, l'applicazione caricata per prima ha la versione di MSVCRT caricata e l'altra applicazione viene forzata a usarla fino a quando le applicazioni non vengono scaricate.

 

Per altre informazioni, vedere "Assembly side-by-side" in Modifiche ai servizi [COM+ in IIS 6.0.](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90))

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
| Descrizione    | Nome del server remoto utilizzato durante l'esportazione del proxy dell'applicazione. È il nome del server a cui punta il proxy dell'applicazione quando viene installato in un computer client. |
| Access         | ReadWrite                                                                                                                                                              |
| Type           | string                                                                                                                                                                 |
| Predefinito        | ""                                                                                                                                                                     |
| Sistema minimo | Windows 2000                                                                                                                                                           |



 

### <a name="apppartitionid"></a>AppPartitionID



| Voce | Valore |
|----------------|---------------------------------------------------|
| Descrizione    | GUID che rappresenta l'ID partizione applicazione. |
| Access         | ReadOnly                                          |
| Type           | string                                            |
| Predefinito        | <Generated>                                 |
| Sistema minimo | Windows Server 2003                               |



 

### <a name="authentication"></a>Autenticazione



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Imposta il livello di autenticazione per le chiamate, con valori corrispondenti alle impostazioni di autenticazione RPC (Remote Procedure Call). Quando si sceglie COMAdminAuthenticationDefault, viene usata l'impostazione nella proprietà DefaultAuthenticationLevel all'interno [**della raccolta LocalComputer.**](localcomputer.md) |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                             |
| Tipo           | Valori possibili long:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)                                              |
| Predefinito        | COMAdminAuthenticationPacket (4)                                                                                                                                                                                                                                                                      |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> Per le applicazioni libreria (in-process), le uniche impostazioni valide sono COMAdminAuthenticationDefault e COMAdminAuthenticationNone . È consigliabile usare le costanti nell'enumerazione e non i valori numerici.

 

### <a name="authenticationcapability"></a>AuthenticationCapability



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina l'identità presentata quando vengono rappresentate le chiamate.                                                                                                                                                                      |
| Access         | ReadWrite                                                                                                                                                                                                                               |
| Tipo           | Valori possibili long:COMAdminAuthenticationCapabilitiesNone (0x0)COMAdminAuthenticationCapabilitiesSecureReference (0x2)COMAdminAuthenticationCapabilitiesStaticCloaking (0x20)COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40) |
| Predefinito        | COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)                                                                                                                                                                                |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                            |



 

### <a name="changeable"></a>Variabile



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina se sono consentite modifiche alle impostazioni dell'applicazione o a quelle dei relativi componenti, a livello di codice o tramite lo strumento di amministrazione di Servizi componenti. |
| Access         | ReadWrite                                                                                                                                                                     |
| Tipo           | Bool                                                                                                                                                                          |
| Predefinito        | Vero                                                                                                                                                                          |
| Sistema minimo | Windows 2000                                                                                                                                                                  |



 

### <a name="commandline"></a>CommandLine



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Stringa della riga di comando da utilizzare nel debug. L'applicazione può essere avviata in un debugger con la riga di comando specificata. |
| Access         | ReadWrite                                                                                                                  |
| Type           | string                                                                                                                     |
| Predefinito        | ""                                                                                                                         |
| Sistema minimo | Windows 2000                                                                                                               |



 

### <a name="concurrentapps"></a>ConcurrentApps



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------|
| Descrizione    | Specifica il numero massimo di applicazioni in pool che possono essere eseguite contemporaneamente. |
| Access         | ReadWrite                                                                        |
| Tipo           | Long (1-1048576)                                                                 |
| Predefinito        | 1                                                                                |
| Sistema minimo | Windows XP                                                                       |



 

### <a name="createdby"></a>CreatedBy



| Voce | Valore |
|----------------|---------------------------------------------------------------|
| Descrizione    | Stringa informativo per descrivere chi ha creato l'applicazione. |
| Access         | ReadWrite                                                     |
| Type           | string                                                        |
| Predefinito        | ""                                                            |
| Sistema minimo | Windows 2000                                                  |



 

### <a name="crmenabled"></a>CRMEnabled



| Voce | Valore |
|----------------|------------------------------------------------------------------|
| Descrizione    | Determina se l'Resource Manager di compensazione è abilitata. |
| Access         | ReadWrite                                                        |
| Tipo           | Bool                                                             |
| Predefinito        | Falso                                                            |
| Sistema minimo | Windows 2000                                                     |



 

### <a name="crmlogfile"></a>CRMLogFile



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------|
| Descrizione    | Nome e percorso del file per mantenere il log per il gestore delle risorse di compensazione (CRM). |
| Access         | ReadWrite                                                                              |
| Type           | string                                                                                 |
| Predefinito        | ""                                                                                     |
| Sistema minimo | Windows 2000                                                                           |



 

### <a name="deleteable"></a>Eliminabile



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Imposta se l'applicazione può essere eliminata, a livello di codice o tramite lo strumento di amministrazione di Servizi componenti. |
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
| Descrizione    | Abilita il dump dello stato di un'applicazione COM+ al momento dell'errore in una directory designata. |
| Access         | ReadWrite                                                                                             |
| Tipo           | Bool                                                                                                  |
| Predefinito        | Falso                                                                                                 |
| Sistema minimo | Windows XP                                                                                            |



 

> [!Note]  
> A Windows Server 2003, solo gli amministratori hanno privilegi di accesso in lettura ai file di dump COM+.

 

### <a name="dumponexception"></a>DumpOnException



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Abilita il dump dello stato di un'applicazione COM+ quando l'applicazione causa un'eccezione non gestita e viene terminata dal runtime COM+. |
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
| Predefinito        | "%systemroot% \\ system32 \\ com \\ dmp"                           |
| Sistema minimo | Windows XP                                                   |



 

> [!Note]  
> A Windows Server 2003, solo gli amministratori hanno privilegi di accesso in lettura ai file di dump COM+.

 

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
| Descrizione    | GUID che rappresenta l'applicazione. Questa proprietà viene restituita quando [**il metodo**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) della proprietà Key viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                            |
| Type           | string                                                                                                                                                               |
| Predefinito        | <Generated>                                                                                                                                                    |
| Sistema minimo | Windows 2000                                                                                                                                                         |



 

### <a name="identity"></a>Identità



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Imposta l'identità del processo server per l'applicazione. Specificare un account utente valido o "Utente interattivo" per fare in modo che l'applicazione presupponga l'identità dell'utente attualmente connesso. È anche possibile specificare le stringhe "nt authority \\ localservice", "nt authority \\ networkservice" e "nt authority \\ system". La password predefinita per questi tre account è "" (stringa vuota). |
| Access         |                                                                                                                                                                                                                                                                                                                                                                                    |
| Type           |                                                                                                                                                                                                                                                                                                                                                                                    |
| Predefinito        |                                                                                                                                                                                                                                                                                                                                                                                    |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                       |



 

La proprietà Identity non è abilitata per le applicazioni di libreria eseguite nel processo client.

La proprietà Password deve essere impostata contemporaneamente a Identity, prima di usare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), perché la password e l'identità vengono convalidate prima del salvataggio. Se la password e l'identità non vengono sincronizzate, l'applicazione non può essere avviata fino a quando non viene reimpostata da un amministratore.

### <a name="impersonationlevel"></a>ImpersonationLevel



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Imposta il livello di rappresentazione utilizzato per le chiamate effettuate ad altre applicazioni.                                                                                           |
| Access         | ReadWrite                                                                                                                                                     |
| Tipo           | Valori possibili lunghi:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4) |
| Predefinito        | COMAdminImpersonationImpersonate (3)                                                                                                                          |
| Sistema minimo | Windows 2000                                                                                                                                                  |



 

### <a name="isenabled"></a>IsEnabled



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Se l'applicazione o il componente COM+ è disabilitato, IsEnabled è False. Se l'applicazione o il componente COM+ è abilitato, IsEnabled è True. |
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
| Descrizione    | Nome dell'applicazione. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono spogliati. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadWrite                                                                                                                                                                                                                            |
| Type           | string                                                                                                                                                                                                                               |
| Predefinito        | "Nuova applicazione"                                                                                                                                                                                                                    |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                         |



 

> [!Note]  
> È consigliabile scegliere nomi univoci per le applicazioni. Se vengono create più applicazioni con lo stesso nome, può interferire con il riferimento alle applicazioni in base al nome, determinando un comportamento imprevedibile.

 

### <a name="password"></a>Password



| Voce | Valore |
|----------------|----------------------------------------------------------------------------|
| Descrizione    | Imposta la password utilizzata dal processo server per accedere con l'identità . |
| Access         | WriteOnly                                                                  |
| Type           | string                                                                     |
| Predefinito        | ""                                                                         |
| Sistema minimo | Windows 2000                                                               |



 

La password deve essere impostata contemporaneamente a Identity, prima di usare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), perché la password e l'identità vengono convalidate prima del salvataggio. Se la password e l'identità non vengono sincronizzate, l'applicazione non può essere avviata fino a quando non viene reimpostata da un amministratore.

### <a name="qcauthenticatemsgs"></a>QCAuthenticateMsgs



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica in quali circostanze vengono autenticate le richieste in coda a un'applicazione.                                                 |
| Access         | ReadWrite                                                                                                                               |
| Tipo           | Valori long possibili:COMAdminQCMessageAuthenticateSecureApps (0)COMAdminQCMessageAuthenticateOff (1)COMAdminQCMessageAuthenticateOn (2) |
| Predefinito        | COMAdminQCMessageAuthenticateSecureApps (0)                                                                                             |
| Sistema minimo | Windows XP                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a>QCListenerMaxThreads



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica il numero massimo di thread del listener simultanei. L'intervallo valido per questa proprietà è compreso tra 0 e 1000. Per un'applicazione appena creata, l'impostazione è derivata dall'algoritmo attualmente usato per determinare il numero predefinito di thread del listener: 16 volte il numero di CPU nel server. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                 |
| Tipo           | Long (0-1000)                                                                                                                                                                                                                                                                                             |
| Predefinito        | 0                                                                                                                                                                                                                                                                                                         |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Questa proprietà è disponibile anche con funzionalità di lettura/scrittura dalla scheda **Accodamento** dello strumento di amministrazione Servizi componenti.

 

### <a name="queuelistenerenabled"></a>QueueListenerEnabled



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica se il listener dei componenti in coda è abilitato per l'applicazione. Se abilitata, il listener viene avviato all'avvio dell'applicazione. Questa proprietà ha effetto solo se QueuingEnabled è impostato su True. |
| Access         | ReadWrite                                                                                                                                                                                                            |
| Tipo           | Bool                                                                                                                                                                                                                 |
| Predefinito        | Falso                                                                                                                                                                                                                |
| Sistema minimo | Windows 2000                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a>QueuingEnabled



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------|
| Descrizione    | Indica se il servizio Componenti in coda COM+ è abilitato per l'applicazione. |
| Access         | ReadWrite                                                                            |
| Tipo           | Bool                                                                                 |
| Predefinito        | Falso                                                                                |
| Sistema minimo | Windows 2000                                                                         |



 

### <a name="recycleactivationlimit"></a>RecycleActivationLimit



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica il numero massimo di attivazioni di oggetti configurati nell'applicazione da accettare prima di riciclare il processo. Il numero predefinito di attivazioni è 0. |
| Access         | ReadWrite                                                                                                                                                            |
| Tipo           | Long (0-1048576)                                                                                                                                                     |
| Predefinito        | 0                                                                                                                                                                    |
| Sistema minimo | Windows XP                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a>RecycleCallLimit



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica il numero massimo di chiamate per consentire agli oggetti configurati nell'applicazione di accettare prima di riciclare il processo. Il numero predefinito di chiamate è 0. |
| Access         | ReadWrite                                                                                                                                                      |
| Tipo           | Long (0-1048576)                                                                                                                                               |
| Predefinito        | 0                                                                                                                                                              |
| Sistema minimo | Windows XP                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a>RecycleExpirationTimeout



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica la quantità di tempo (in minuti) per consentire l'esecuzione di un processo riciclato prima di arrestarlo. Il conto alla rovescia inizia immediatamente dopo il riciclo del processo. Il timeout di scadenza massimo è 1440 minuti (24 ore) e il valore predefinito è 15 minuti. |
| Access         | ReadWrite                                                                                                                                                                                                                                                        |
| Tipo           | Long (1-1440)                                                                                                                                                                                                                                                    |
| Predefinito        | 15                                                                                                                                                                                                                                                               |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a>RecycleLifetimeLimit



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica il numero massimo di minuti per consentire l'esecuzione di un processo prima di riciclarlo. Il limite di durata massimo è 30240 minuti (21 giorni) e il valore predefinito è 0 minuti. |
| Access         | ReadWrite                                                                                                                                                                   |
| Tipo           | Long (0-30240)                                                                                                                                                              |
| Predefinito        | 0                                                                                                                                                                           |
| Sistema minimo | Windows XP                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a>RecycleMemoryLimit



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica la quantità massima di utilizzo della memoria (in kilobyte) consentita per un processo prima che venga riciclato. Se l'utilizzo della memoria del processo supera il numero specificato per un periodo superiore a un minuto, il processo viene riciclato. La quantità predefinita di utilizzo della memoria è 0 KB. |
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
| Descrizione    | Consente a un processo server di continuare se un'applicazione è inattiva. Se impostato su True, il processo del server non si arresta quando viene lasciato inattivo. Se impostato su False, il processo viene arrestato in base al valore impostato dalla proprietà ShutdownAfter. RunForever non è abilitato per le applicazioni di libreria (in-process). |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                     |
| Predefinito        | Falso                                                                                                                                                                                                                                                                                                    |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a>ServiceName



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome del servizio corrispondente all'applicazione configurata per l'esecuzione come applicazione di servizio. Se questo valore è **NULL,** l'applicazione non è configurata per l'esecuzione come servizio. In caso contrario, è possibile trovare le informazioni di configurazione per il servizio usando il nome del servizio. |
| Access         | ReadOnly                                                                                                                                                                                                                                                                         |
| Type           | string                                                                                                                                                                                                                                                                           |
| Predefinito        | ""                                                                                                                                                                                                                                                                               |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a>ShutdownAfter



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Imposta il ritardo prima di arrestare un processo server dopo che diventa inattivo. La latenza di arresto va da 0 a 1440 minuti (24 ore). Se RunForever è impostato su True, questa proprietà viene ignorata. ShutdownAfter non è abilitato per le applicazioni di libreria (in-process). |
| Access         | ReadWrite                                                                                                                                                                                                                                                          |
| Tipo           | Long (0-1440)                                                                                                                                                                                                                                                      |
| Predefinito        | 3                                                                                                                                                                                                                                                                  |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a>SoapActivated



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------|
| Descrizione    | Indica se l'applicazione è esposta per l'utilizzo tramite il protocollo SOAP. |
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
| Descrizione    | Directory radice virtuale IIS in cui si trovano gli script di accesso che espongono l'applicazione tramite il protocollo SOAP. |
| Access         | ReadWrite                                                                                                            |
| Type           | string                                                                                                               |
| Predefinito        | ""                                                                                                                   |
| Sistema minimo | Windows Server 2003                                                                                                  |



 

### <a name="srpenabled"></a>SRPEnabled



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina i criteri di restrizione software (SRP) per l'applicazione. Se impostato su True, viene usata la proprietà SRPTrustLevel per l'applicazione. Se impostato su False, vengono usati i criteri di restrizione software delle impostazioni di sicurezza locali. Le impostazioni di sicurezza locali vengono controllate tramite lo snap-in Criteri di sicurezza locali del Microsoft Management Console. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                             |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                  |
| Predefinito        | Falso                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica il livello di attendibilità dei criteri di restrizione software (SRP) dell'applicazione. Questa proprietà viene usata solo se la proprietà SRPEnabled è impostata su True. Il livello di attendibilità SRP si riferisce al livello di attendibilità che si è disposti a concedere a un'applicazione. Un livello di attendibilità SRP senza restrizioni corrisponde al valore dell'enumerazione SAFER LEVELID FULLYTRUSTED, mentre un livello di attendibilità SRP non consentito corrisponde al valore dell'enumerazione \_ \_ SAFER \_ LEVELID \_ DISALLOWED. L'enumerazione per i livelli di attendibilità è definita in Winsafer.h. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Tipo           | Valori possibili lunghi:SAFER \_ LEVELID \_ DISALLOWED (0x0)SAFER \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Predefinito        | SAFER \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

A un'applicazione di cui si è disposti a considerare attendibile l'accesso senza restrizioni deve essere associata la sicurezza più severa. Le applicazioni senza restrizioni possono caricare solo componenti senza restrizioni, mentre le applicazioni non consentite non potranno essere eseguite e pertanto non potranno caricare alcun componente.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
