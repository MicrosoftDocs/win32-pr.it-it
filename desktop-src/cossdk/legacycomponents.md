---
description: Contiene un oggetto per ogni componente non configurato nella raccolta di applicazioni. I componenti non configurati non possono utilizzare i servizi COM+. Le proprietà esposte da questi oggetti contengono impostazioni effettuate a livello di componente.
ms.assetid: 87f3b93f-71aa-4187-88d2-889c13d8bd06
title: Raccolta LegacyComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyComponents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5761950dcb0ceb5c857daf37ba2236733ec30c22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748175"
---
# <a name="legacycomponents-collection"></a>Raccolta LegacyComponents

Contiene un oggetto per ogni componente non configurato nella raccolta di applicazioni. I componenti non configurati non possono utilizzare i servizi COM+. Le proprietà esposte da questi oggetti contengono impostazioni effettuate a livello di componente.

Questa raccolta supporta il metodo [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , ma non il metodo [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) . Per installare o importare componenti in un'applicazione, usare i metodi sull'oggetto [**COMAdminCatalog**](comadmincatalog.md) .

## <a name="members"></a>Membri

La raccolta **LegacyComponents** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Applicazioni**](applications.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [AccessPermissions](#accesspermissions)
-   [ActivateAtStorage](#activateatstorage)
-   [AppID](#appid)
-   [AppName](#appname)
-   [AuthenticationLevel](#authenticationlevel)
-   [Numero di bit](#bitness)
-   [ClassName](#classname)
-   [CLSID](#clsid)
-   [DllSurrogate](#dllsurrogate)
-   [InprocHandler32](#inprochandler32)
-   [InprocServer32](#inprocserver32)
-   [IsEnabled](#isenabled)
-   [LaunchPermissions](#launchpermissions)
-   [LocalServer32](#localserver32)
-   [LocalService](#localservice)
-   [Password](#password)
-   [ProgID](#progid)
-   [RemoteServer](#remoteserver)
-   [RunAs](#runas)
-   [ServiceParameter](#serviceparameter)
-   [SRPTrustLevel](#srptrustlevel)
-   [ThreadingModel](#threadingmodel)

### <a name="accesspermissions"></a>AccessPermissions



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------|
| Descrizione    | Specifica gli account utente a cui è consentito o negato l'accesso al componente. |
| Access         | ReadWrite                                                                       |
| Type           | string                                                                          |
| Predefinito        | N/D                                                                             |
| Sistema minimo | Windows XP                                                                      |



 

### <a name="activateatstorage"></a>ActivateAtStorage



| Voce | Valore |
|----------------|------------------------------------------------------------------|
| Descrizione    | Specifica se eseguire il server nel computer di archiviazione dati. |
| Access         | ReadWrite                                                        |
| Tipo           | Stringa valori possibili: "N" "Y"                                    |
| Predefinito        | "N"                                                              |
| Sistema minimo | Windows XP                                                       |



 

### <a name="appid"></a>AppID



| Voce | Valore |
|----------------|---------------------|
| Descrizione    | ID applicazione. |
| Access         | ReadOnly            |
| Type           | string              |
| Predefinito        | N/D                 |
| Sistema minimo | Windows XP          |



 

### <a name="appname"></a>AppName



| Voce | Valore |
|----------------|------------------------------|
| Descrizione    | Nome dell'applicazione. |
| Access         | ReadOnly                     |
| Type           | string                       |
| Predefinito        | N/D                          |
| Sistema minimo | Windows XP                   |



 

### <a name="authenticationlevel"></a>AuthenticationLevel



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Imposta il livello di autenticazione per le chiamate, con i valori corrispondenti alle impostazioni di autenticazione RPC (Remote Procedure Call). Quando si sceglie COMAdminAuthenticationDefault, viene utilizzata l'impostazione nella proprietà DefaultAuthenticationLevel all'interno della raccolta [**LocalComputer**](localcomputer.md) . |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                             |
| Tipo           | Valori lunghi possibili: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)                                              |
| Predefinito        | COMAdminAuthenticationDefault (0)                                                                                                                                                                                                                                                                     |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> Si consiglia di usare le costanti nell'enumerazione e non i valori numerici.

 

### <a name="bitness"></a>Numero di bit



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Rappresenta il tipo binario bit del componente. Nei sistemi che utilizzano Windows a 64 bit, questa proprietà distingue tra i componenti a 64 bit e i componenti a 32 bit. |
| Access         | ReadOnly                                                                                                                                                              |
| Tipo           | Valori lunghi possibili: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)                                                                                         |
| Predefinito        | N/D                                                                                                                                                                   |
| Sistema minimo | Windows XP                                                                                                                                                            |



 

### <a name="classname"></a>ClassName



| Voce | Valore |
|----------------|------------------------|
| Descrizione    | Nome della classe. |
| Access         | ReadOnly               |
| Type           | string                 |
| Predefinito        | N/D                    |
| Sistema minimo | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | GUID per il componente. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                  |
| Type           | string                                                                                                                                                    |
| Predefinito        | N/D                                                                                                                                                       |
| Sistema minimo | Windows XP                                                                                                                                                |



 

### <a name="dllsurrogate"></a>DllSurrogate



| Voce | Valore |
|----------------|------------------------------------------------------------|
| Descrizione    | Specifica il percorso completo di un'applicazione server surragate. |
| Access         | ReadWrite                                                  |
| Type           | string                                                     |
| Predefinito        | N/D                                                        |
| Sistema minimo | Windows XP                                                 |



 

### <a name="inprochandler32"></a>InprocHandler32



| Voce | Valore |
|----------------|--------------------------------------------------------------------|
| Descrizione    | Specifica il percorso completo di una DLL del gestore personalizzato in-process a 32 bit. |
| Access         | ReadWrite                                                          |
| Type           | string                                                             |
| Predefinito        | N/D                                                                |
| Sistema minimo | Windows XP                                                         |



 

### <a name="inprocserver32"></a>InprocServer32



| Voce | Valore |
|----------------|------------------------------------------------------------|
| Descrizione    | Specifica il percorso completo di una DLL del server in-process a 32 bit. |
| Access         | ReadWrite                                                  |
| Type           | string                                                     |
| Predefinito        | N/D                                                        |
| Sistema minimo | Windows XP                                                 |



 

### <a name="isenabled"></a>IsEnabled



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Se l'applicazione o il componente COM+ è disabilitato, IsEnabled è false. Se l'applicazione o il componente COM+ è abilitato, IsEnabled è true. |
| Access         | ReadWrite                                                                                                                                 |
| Tipo           | Bool                                                                                                                                      |
| Predefinito        | Vero                                                                                                                                      |
| Sistema minimo | Windows XP                                                                                                                                |



 

### <a name="launchpermissions"></a>LaunchPermissions



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------|
| Descrizione    | Specifica gli account utente per i quali è consentita o negata l'autorizzazione per avviare il componente. |
| Access         | ReadWrite                                                                              |
| Type           | string                                                                                 |
| Predefinito        | N/D                                                                                    |
| Sistema minimo | Windows XP                                                                             |



 

### <a name="localserver32"></a>LocalServer32



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Specifica il percorso completo di un'applicazione server locale a 32 bit. Per proteggere la sicurezza del sistema, usare stringhe tra virgolette nel percorso per indicare dove termina il nome file eseguibile e gli argomenti iniziano. Ad esempio, " \\ " C: \\ programmi \\ aziendali file \\Application.exe\\ "param1 param2". |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                   |
| Type           | string                                                                                                                                                                                                                                                                                      |
| Predefinito        | N/D                                                                                                                                                                                                                                                                                         |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a>LocalService



| Voce | Valore |
|----------------|-----------------------------------------------------|
| Descrizione    | Specifica il percorso completo dell'applicazione di servizio. |
| Access         | ReadWrite                                           |
| Type           | string                                              |
| Predefinito        | N/D                                                 |
| Sistema minimo | Windows XP                                          |



 

### <a name="password"></a>Password



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Imposta la password utilizzata dal processo server per accedere con l'identità RunAs specificata. È necessario impostare la password contemporaneamente all'identità RunAs, prima di usare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), perché la password e l'identità vengono convalidate prima di essere salvate. Se la password e l'identità non vengono sincronizzate, il componente non può essere avviato finché non viene reimpostato da un amministratore. |
| Access         | WriteOnly                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Type           | string                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Predefinito        | NULL                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a>ProgID



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome che identifica il componente. Questa proprietà viene restituita quando il metodo della proprietà Name viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                             |
| Type           | string                                                                                                                               |
| Predefinito        | N/D                                                                                                                                  |
| Sistema minimo | Windows XP                                                                                                                           |



 

### <a name="remoteserver"></a>RemoteServer



| Voce | Valore |
|----------------|---------------------------------------|
| Descrizione    | Specifica il computer server remoto. |
| Access         | ReadWrite                             |
| Type           | string                                |
| Predefinito        | N/D                                   |
| Sistema minimo | Windows XP                            |



 

### <a name="runas"></a>RunAs



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Specifica l'utente con la cui identità viene eseguito il componente. È necessario impostare la password contemporaneamente all'identità RunAs, prima di usare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), perché la password e l'identità vengono convalidate prima di essere salvate. Se la password e l'identità non vengono sincronizzate, il componente non può essere avviato finché non viene reimpostato da un amministratore. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                         |
| Type           | string                                                                                                                                                                                                                                                                                                                                                                                            |
| Predefinito        | N/D                                                                                                                                                                                                                                                                                                                                                                                               |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a>ServiceParameter



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------|
| Descrizione    | Specifica i parametri passati all'applicazione quando vengono richiamati come applicazione di servizio. |
| Access         | ReadWrite                                                                                 |
| Type           | string                                                                                    |
| Predefinito        | N/D                                                                                       |
| Sistema minimo | Windows XP                                                                                |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica il livello di attendibilità del componente per i criteri di restrizione software. Il livello di attendibilità SRP si riferisce al livello di attendibilità che si è disposti a assegnare a un componente. Un livello di attendibilità Unrestricted SRP corrisponde \_ al \_ valore di enumerazione LEVELID FULLYTRUSTED più sicuro, mentre un livello di ATTENDIBILità SRP non consentito corrisponde al \_ valore di enumerazione non consentito LEVELID più sicuro \_ . L'enumerazione per i livelli di attendibilità è definita in Winsafer. h. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipo           | Valori lunghi possibili: SAFER \_ LEVELID non \_ consentita (0x0) Safer \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                         |
| Predefinito        | \_FULLYTRUSTED LEVELID più sicuro \_                                                                                                                                                                                                                                                                                                                                                                                                        |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

Un componente di cui si è disposti a considerare attendibile l'accesso senza restrizioni deve disporre della sicurezza più rigorosa collegata. Le applicazioni senza restrizioni possono caricare solo componenti senza restrizioni, mentre le applicazioni non consentite non potranno essere eseguite e pertanto non potranno caricare alcun componente.

### <a name="threadingmodel"></a>ThreadingModel



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina il modo in cui le istanze del componente vengono assegnate ai thread per l'esecuzione del metodo. I valori corrispondono ai modelli di threading COM.                                                  |
| Access         | ReadOnly                                                                                                                                                                            |
| Tipo           | Valori lunghi possibili: COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) |
| Predefinito        | N/D                                                                                                                                                                                 |
| Sistema minimo | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
