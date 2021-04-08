---
description: Contiene un singolo oggetto che corrisponde al computer di cui si desidera accedere al catalogo. Questo oggetto include informazioni sulle impostazioni a livello di computer.
ms.assetid: 75f14cad-9cd5-44a6-9afa-2c8ad1e87027
title: Raccolta LocalComputer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocalComputer
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4e1ce08f3bf1fef74af0d77ada15716abb4530a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748999"
---
# <a name="localcomputer-collection"></a>Raccolta LocalComputer

Contiene un singolo oggetto che corrisponde al computer di cui si desidera accedere al catalogo. Questo oggetto include informazioni sulle impostazioni a livello di computer. Se si chiama il metodo [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) su un oggetto creato dalla classe [**COMAdminCatalog**](comadmincatalog.md) , l'oggetto nella raccolta **LocalComputer** contiene informazioni sul computer remoto di cui si sta effettuando l'accesso.

Questa raccolta non supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta **LocalComputer** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [ApplicationProxyRSN](#applicationproxyrsn)
-   [CISEnabled](#cisenabled)
-   [DCOMEnabled](#dcomenabled)
-   [DefaultAuthenticationLevel](#defaultauthenticationlevel)
-   [DefaultImpersonationLevel](#defaultimpersonationlevel)
-   [DefaultToInternetPorts](#defaulttointernetports)
-   [Descrizione](#description)
-   [DSPartitionLookupEnabled](#dspartitionlookupenabled)
-   [InternetPortsListed](#internetportslisted)
-   [Routing](#isrouter)
-   [LoadBalancingCLSID](#loadbalancingclsid)
-   [LocalPartitionLookupEnabled](#localpartitionlookupenabled)
-   [Nome](#name)
-   [OperatingSystem](#operatingsystem)
-   [PartitionsEnabled](#partitionsenabled)
-   [Ports](#defaulttointernetports)
-   [ResourcePoolingEnabled](#resourcepoolingenabled)
-   [RPCProxyEnabled](#rpcproxyenabled)
-   [SecureReferencesEnabled](#securereferencesenabled)
-   [SecurityTrackingEnabled](#securitytrackingenabled)
-   [SRPActivateAsActivatorChecks](#srpactivateasactivatorchecks)
-   [SRPRunningObjectChecks](#srprunningobjectchecks)
-   [TransactionTimeout](#transactiontimeout)

### <a name="applicationproxyrsn"></a>ApplicationProxyRSN



| Voce | Valore |
|----------------|------------------------------------------------------------|
| Descrizione    | Nome del server remoto usato dai proxy di applicazione per impostazione predefinita. |
| Access         | ReadWrite                                                  |
| Type           | string                                                     |
| Predefinito        | ""                                                         |
| Sistema minimo | Windows 2000                                               |



 

### <a name="cisenabled"></a>CISEnabled



| Voce | Valore |
|----------------|-----------------------------------------------------|
| Descrizione    | Indica se i servizi Internet COM sono abilitati. |
| Access         | ReadWrite                                           |
| Tipo           | Bool                                                |
| Predefinito        | Falso                                               |
| Sistema minimo | Windows 2000                                        |



 

### <a name="dcomenabled"></a>DCOMEnabled



| Voce | Valore |
|----------------|---------------------------------------------|
| Descrizione    | Impostare su true per abilitare DCOM nel computer. |
| Access         | ReadWrite                                   |
| Tipo           | Bool                                        |
| Predefinito        | Vero                                        |
| Sistema minimo | Windows 2000                                |



 

### <a name="defaultauthenticationlevel"></a>DefaultAuthenticationLevel



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Livello di autenticazione utilizzato dalle applicazioni per le quali l'autenticazione è impostata su default. I valori corrispondono alle impostazioni di autenticazione RPC (Remote Procedure Call).                                                                                         |
| Access         | ReadWrite                                                                                                                                                                                                                                                |
| Tipo           | Valori lunghi possibili: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6) |
| Predefinito        | COMAdminAuthenticationConnect (2)                                                                                                                                                                                                                        |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                             |



 

> [!Note]  
> COMAdminAuthenticationDefault viene mappato a COMAdminAuthenticationConnect quando COM chiama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Si consiglia di usare le costanti nell'enumerazione e non i valori numerici.

 

### <a name="defaultimpersonationlevel"></a>DefaultImpersonationLevel



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Livello di rappresentazione per consentire se non ne è stato impostato uno.                                                                                                               |
| Access         | ReadWrite                                                                                                                                                     |
| Tipo           | Valori lunghi possibili: COMAdminImpersonationAnonymous (1) COMAdminImpersonationIdentify (2) COMAdminImpersonationImpersonate (3) COMAdminImpersonationDelegate (4) |
| Predefinito        | COMAdminImpersonationIdentify (2)                                                                                                                             |
| Sistema minimo | Windows 2000                                                                                                                                                  |



 

> [!Note]  
> Si consiglia di usare le costanti nell'enumerazione e non i valori numerici.

 

### <a name="defaulttointernetports"></a>DefaultToInternetPorts



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------|
| Descrizione    | Determina se il tipo predefinito di porta specificato deve essere Internet (true) o Intranet (false). |
| Access         | ReadWrite                                                                                           |
| Tipo           | Bool                                                                                                |
| Predefinito        | Falso                                                                                               |
| Sistema minimo | Windows 2000                                                                                        |



 

### <a name="description"></a>Descrizione



| Voce | Valore |
|----------------|--------------------------------|
| Descrizione    | Descrizione del computer. |
| Access         | ReadWrite                      |
| Type           | string                         |
| Predefinito        | ""                             |
| Sistema minimo | Windows 2000                   |



 

### <a name="dspartitionlookupenabled"></a>DSPartitionLookupEnabled



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------|
| Descrizione    | Indica se l'utente dei mapping della partizione viene archiviato nell'archivio di dominio. |
| Access         | ReadWrite                                                                              |
| Tipo           | Bool                                                                                   |
| Predefinito        | Vero                                                                                   |
| Sistema minimo | Windows Server 2003                                                                    |



 

### <a name="internetportslisted"></a>InternetPortsListed



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina se le porte elencate nella proprietà porte devono essere utilizzate per Internet (true) o per Intranet (false). |
| Access         | ReadWrite                                                                                                             |
| Tipo           | Bool                                                                                                                  |
| Predefinito        | Falso                                                                                                                 |
| Sistema minimo | Windows 2000                                                                                                          |



 

### <a name="isrouter"></a>Routing



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Impostare su true se il computer è un router per il servizio di bilanciamento del carico componente (CLB). Questa proprietà può essere impostata su true solo se il servizio di bilanciamento del carico componente è attualmente installato nel computer. in caso contrario, gli errori con COMAdmin \_ e \_ richiedono una \_ \_ piattaforma diversa. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                           |
| Tipo           | Bool                                                                                                                                                                                                                                                                                |
| Predefinito        | Falso                                                                                                                                                                                                                                                                               |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                        |



 

Se questa proprietà è impostata su true, il server CLB viene configurato e viene avviato all'avvio. Il server viene aggiunto alla raccolta ApplicationCluster se non è già presente.

### <a name="loadbalancingclsid"></a>LoadBalancingCLSID



| Voce | Valore |
|----------------|-------------------------------------|
| Descrizione    | CLSID dell'oggetto da bilanciare. |
| Access         | ReadWrite                           |
| Type           | string                              |
| Predefinito        | NULL                                |
| Sistema minimo | Windows XP                          |



 

### <a name="localpartitionlookupenabled"></a>LocalPartitionLookupEnabled



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------|
| Descrizione    | Indica se l'utente dei mapping della partizione viene archiviato nell'archivio locale. |
| Access         | ReadWrite                                                                             |
| Tipo           | Bool                                                                                  |
| Predefinito        | Vero                                                                                  |
| Sistema minimo | Windows Server 2003                                                                   |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome del computer. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                                                                                                                              |
| Type           | string                                                                                                                                                                                                                                                                 |
| Predefinito        | "Computer locale"                                                                                                                                                                                                                                                          |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a>OperatingSystem



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Sistema operativo installato nel computer locale.                                                                                                                                                                                                                                                                                                                                                                                                |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tipo           | Valori lunghi possibili: COMAdminOSNotInitialized (0) COMAdminOSWindows3 \_ 1 (1) COMAdminOSWindows9x (2) COMAdminOSWindows2000 (3) COMAdminOSWindows2000AdvancedServer (4) COMAdminOSWindows2000Unknown (5) COMAdminOSUnknown (6) COMAdminOSWindowsXPPersonal (11) COMAdminOSWindowsXPProfessional (12) COMAdminOSWindowsNETStandardServer (13) COMAdminOSWindowsNETEnterpriseServer (14) COMAdminOSWindowsNETDatacenterServer (15) COMAdminOSWindowsNETWebServer (16) |
| Predefinito        | COMAdminOSNotInitialized (0)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a>PartitionsEnabled



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica se le partizioni COM+ possono essere utilizzate nel computer locale. Se questa proprietà è false, qualsiasi tentativo di utilizzare le partizioni COM+ genera un errore. |
| Access         | ReadWrite                                                                                                                                               |
| Tipo           | Bool                                                                                                                                                    |
| Predefinito        | Falso                                                                                                                                                   |
| Sistema minimo | Windows Server 2003                                                                                                                                     |



 

### <a name="ports"></a>Porte



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Stringa che descrive le porte utilizzate per Internet o Intranet, a seconda della proprietà InternetPortsListed. ad esempio, "500-599:600-800". |
| Access         | ReadWrite                                                                                                                                               |
| Type           | string                                                                                                                                                  |
| Predefinito        | ""                                                                                                                                                      |
| Sistema minimo | Windows 2000                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a>ResourcePoolingEnabled



| Voce | Valore |
|----------------|-------------------------------------|
| Descrizione    | Consente l'uso dei distributori di risorse. |
| Access         | ReadWrite                           |
| Tipo           | Bool                                |
| Predefinito        | Vero                                |
| Sistema minimo | Windows 2000                        |



 

### <a name="rpcproxyenabled"></a>RPCProxyEnabled



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Controlla se il proxy IIS RPC è abilitato. Il proxy IIS RPC viene utilizzato in combinazione con IIS per l'inoltro delle chiamate al meccanismo RPC da IIS ed è uno dei componenti principali dei servizi Internet COM, che viene abilitato impostando CISEnabled su true. Per ulteriori informazioni su RPCProxyEnabled, vedere [http RPC Security](/windows/desktop/Rpc/rpc-over-http-security). |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                             |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                  |
| Predefinito        | Falso                                                                                                                                                                                                                                                                                                                                                 |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a>SecureReferencesEnabled



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Impone nei computer DCOM che le chiamate tra più processi ai metodi [**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) siano protette. |
| Access         | ReadWrite                                                                                                                                                                 |
| Tipo           | Bool                                                                                                                                                                      |
| Predefinito        | Falso                                                                                                                                                                     |
| Sistema minimo | Windows 2000                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a>SecurityTrackingEnabled



| Voce | Valore |
|----------------|---------------------------------------------------------|
| Descrizione    | Impostare su true se il rilevamento di sicurezza è abilitato per gli oggetti. |
| Access         | ReadWrite                                               |
| Tipo           | Bool                                                    |
| Predefinito        | Vero                                                    |
| Sistema minimo | Windows 2000                                            |



 

### <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina il modo in cui i criteri di restrizione software gestiscono le connessioni Activate-As-Activator. Se è impostato su true, il livello di attendibilità SRP configurato per l'oggetto server viene confrontato con il livello di attendibilità SRP dell'oggetto client e il livello di attendibilità superiore (più rigoroso) viene utilizzato per eseguire l'oggetto server. Se impostato su false, l'oggetto server viene eseguito con il livello di attendibilità SRP dell'oggetto client, indipendentemente dal livello di attendibilità SRP con cui è configurato il server. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Predefinito        | Vero                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina il modo in cui il criterio di restrizione software gestisce i tentativi di connessione ai processi esistenti. Se è impostato su false, i tentativi di connessione agli oggetti in esecuzione non vengono controllati per i livelli di attendibilità SRP appropriati. Se è impostato su true, l'oggetto in esecuzione deve disporre di un livello di attendibilità uguale o superiore (più rigoroso) SRP rispetto all'oggetto client. Ad esempio, un oggetto client con un livello di attendibilità non limitato non può connettersi a un oggetto in esecuzione con un livello di attendibilità non consentito. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Predefinito        | Vero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a>TransactionTimeout



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Deve essere impostato su un valore sufficiente in secondi se si eseguono numerose operazioni all'interno di una transazione. Il periodo di timeout predefinito è di 60 secondi e il periodo di timeout massimo è di 3600 secondi (1 ora). L'impostazione di questa proprietà su 0 Disabilita i timeout delle transazioni. Questa proprietà può essere sottoposta a override dai singoli componenti utilizzando la proprietà ComponentTransactionTimeout della raccolta [**Components**](components.md) . |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Tipo           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Predefinito        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a>Esempio

Nell'esempio di Visual Basic Microsoft riportato di seguito viene illustrato come connettersi a un computer remoto e ottenere la relativa proprietà SecurityTrackingEnabled tramite la raccolta **LocalComputer** del computer remoto. Per usare questo esempio, aggiungere la libreria dei tipi di amministrazione COM+ come riferimento al progetto Visual Basic.


```VB
Function RemoteComputerConnect(strComputer As String _
) As Boolean  ' Return False if any errors occur.
    
    RemoteComputerConnect = False   ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim boolSTE As Boolean
    Dim objCatalog As COMAdminCatalog
    Dim objRemoteRootColl As COMAdminCatalogCollection
    Dim objRemoteComputerColl As COMAdminCatalogCollection
    Dim objRemoteComputerItem As COMAdminCatalogObject
    
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objRemoteRootColl = objCatalog.Connect(strComputer)
    Set objRemoteComputerColl = objRemoteRootColl.GetCollection( _
      "LocalComputer", objRemoteRootColl.Name)
    objRemoteComputerColl.Populate
    Set objRemoteComputerItem = objRemoteComputerColl.Item(0)
    boolSTE = objRemoteComputerItem.Value("SecurityTrackingEnabled")
    If boolSTE Then
        MsgBox "Security Tracking is enabled on " & strComputer
    Else
        MsgBox "Security Tracking is NOT enabled on " & strComputer
    End If

    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
    RemoteComputerConnect = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
End Function


```



Per usare la funzione, fornire un valore stringa per il nome del computer remoto. Il codice di Visual Basic seguente illustra come connettersi al computer denominato "NomeComputerRemoto".


```VB
Sub Main()
    If Not RemoteComputerConnect("RemoteComputerName") Then
        MsgBox "RemoteComputerConnect failed."
    End If
End Sub

```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
