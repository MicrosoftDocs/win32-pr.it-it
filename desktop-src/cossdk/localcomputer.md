---
description: Contiene un singolo oggetto che corrisponde al computer a cui si accede al catalogo. Questo oggetto contiene informazioni sulle impostazioni a livello di computer.
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
ms.openlocfilehash: b832da702942e8f84baee4303b7fa74a7fd74d683d62534cca619e8c7270e88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813465"
---
# <a name="localcomputer-collection"></a>Raccolta LocalComputer

Contiene un singolo oggetto che corrisponde al computer a cui si accede al catalogo. Questo oggetto contiene informazioni sulle impostazioni a livello di computer. Se si chiama il [**metodo Connessione**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) su un oggetto creato dalla [**classe COMAdminCatalog,**](comadmincatalog.md) l'oggetto nella raccolta **LocalComputer** contiene informazioni sul computer remoto di cui si accede al catalogo.

Questa raccolta non supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta LocalComputer** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Errorinfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [ApplicationProxyRSN](#applicationproxyrsn)
-   [CISEnabled](#cisenabled)
-   [DCOMEnabled](#dcomenabled)
-   [DefaultAuthenticationLevel](#defaultauthenticationlevel)
-   [DefaultImpersonationLevel](#defaultimpersonationlevel)
-   [DefaultToInternetPorts](#defaulttointernetports)
-   [Descrizione](#description)
-   [DSPartitionLookupEnabled](#dspartitionlookupenabled)
-   [InternetPortsListed](#internetportslisted)
-   [IsRouter](#isrouter)
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
| Descrizione    | Nome del server remoto utilizzato dai proxy di applicazione per impostazione predefinita. |
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
| Descrizione    | Impostare su True per abilitare DCOM nel computer. |
| Access         | ReadWrite                                   |
| Tipo           | Bool                                        |
| Predefinito        | Vero                                        |
| Sistema minimo | Windows 2000                                |



 

### <a name="defaultauthenticationlevel"></a>DefaultAuthenticationLevel



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Livello di autenticazione usato dalle applicazioni con Autenticazione impostata su Predefinito. I valori corrispondono alle impostazioni di autenticazione RPC (Remote Procedure Call).                                                                                         |
| Access         | ReadWrite                                                                                                                                                                                                                                                |
| Tipo           | Valori possibili lunghi:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6) |
| Predefinito        | COMAdminAuthenticationConnect (2)                                                                                                                                                                                                                        |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                             |



 

> [!Note]  
> COMAdminAuthenticationDefault viene mappato a COMAdminAuthenticationConnect quando COM chiama [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). È consigliabile usare le costanti nell'enumerazione e non i valori numerici.

 

### <a name="defaultimpersonationlevel"></a>DefaultImpersonationLevel



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Livello di rappresentazione da consentire se non ne è impostato uno.                                                                                                               |
| Access         | ReadWrite                                                                                                                                                     |
| Tipo           | Valori possibili lunghi:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4) |
| Predefinito        | COMAdminImpersonationIdentify (2)                                                                                                                             |
| Sistema minimo | Windows 2000                                                                                                                                                  |



 

> [!Note]  
> È consigliabile usare le costanti nell'enumerazione e non i valori numerici.

 

### <a name="defaulttointernetports"></a>DefaultToInternetPorts



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------|
| Descrizione    | Determina se il tipo predefinito di porta fornito deve essere Internet (True) o Intranet (False). |
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
| Descrizione    | Indica se l'utente dei mapping delle partizioni viene archiviato nell'archivio di dominio. |
| Access         | ReadWrite                                                                              |
| Tipo           | Bool                                                                                   |
| Predefinito        | Vero                                                                                   |
| Sistema minimo | Windows Server 2003                                                                    |



 

### <a name="internetportslisted"></a>InternetPortsListed



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina se le porte elencate nella proprietà Porte devono essere usate per Internet (True) o per intranet (False). |
| Access         | ReadWrite                                                                                                             |
| Tipo           | Bool                                                                                                                  |
| Predefinito        | Falso                                                                                                                 |
| Sistema minimo | Windows 2000                                                                                                          |



 

### <a name="isrouter"></a>IsRouter



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Impostare su True se il computer è un router per il servizio di bilanciamento del carico dei componenti. Questa proprietà può essere impostata su True solo se il servizio di bilanciamento del carico del componente è attualmente installato nel computer. In caso contrario, si verifica un errore con COMADMIN \_ E \_ REQUIRES DIFFERENT \_ \_ PLATFORM. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                           |
| Tipo           | Bool                                                                                                                                                                                                                                                                                |
| Predefinito        | Falso                                                                                                                                                                                                                                                                               |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                        |



 

Se questa proprietà è impostata su True, il server CLB viene configurato e avviato all'avvio. Il server viene aggiunto alla raccolta ApplicationCluster, se non è già presente.

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
| Descrizione    | Indica se l'utente dei mapping delle partizioni viene archiviato nell'archivio locale. |
| Access         | ReadWrite                                                                             |
| Tipo           | Bool                                                                                  |
| Predefinito        | Vero                                                                                  |
| Sistema minimo | Windows Server 2003                                                                   |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome del computer. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono privati. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                                                                                                                              |
| Type           | string                                                                                                                                                                                                                                                                 |
| Predefinito        | "Computer locale"                                                                                                                                                                                                                                                          |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a>OperatingSystem



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Sistema operativo installato nel computer locale.                                                                                                                                                                                                                                                                                                                                                                                                |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tipo           | Valori possibili long:COMAdminOSNotInitialized (0)COMAdminOSWindows3 \_ 1(1)COMAdminOSWindows9x (2)COMAdminOSWindows2000 (3)COMAdminOSWindows2000AdvancedServer (4)COMAdminOSWindows2000Unknown (5)COMAdminOSUnknown (5)COMAdminOSUnknown (4)6)COMAdminOSWindowsXPPersonal (11)COMAdminOSWindowsXPProfessional (12)COMAdminOSWindowsNETStandardServer (13)COMAdminOSWindowsNETEnterpriseServer (14)COMAdminOSWindowsNETDatacenterServer (15)COMAdminOSWindowsNETWebServer (16) |
| Predefinito        | COMAdminOSNotInitialized (0)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a>PartitionsEnabled



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Indica se è possibile usare partizioni COM+ nel computer locale. Se questa proprietà è False, qualsiasi tentativo di usare partizioni COM+ restituisce un errore. |
| Access         | ReadWrite                                                                                                                                               |
| Tipo           | Bool                                                                                                                                                    |
| Predefinito        | Falso                                                                                                                                                   |
| Sistema minimo | Windows Server 2003                                                                                                                                     |



 

### <a name="ports"></a>Porte



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Stringa che descrive le porte per l'uso su Internet o Intranet, a seconda della proprietà InternetPortsListed. ad esempio "500-599: 600-800". |
| Access         | ReadWrite                                                                                                                                               |
| Type           | string                                                                                                                                                  |
| Predefinito        | ""                                                                                                                                                      |
| Sistema minimo | Windows 2000                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a>ResourcePoolingEnabled



| Voce | Valore |
|----------------|-------------------------------------|
| Descrizione    | Abilita l'uso di distributori di risorse. |
| Access         | ReadWrite                           |
| Tipo           | Bool                                |
| Predefinito        | Vero                                |
| Sistema minimo | Windows 2000                        |



 

### <a name="rpcproxyenabled"></a>RPCProxyEnabled



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Controlla se il proxy IIS RPC è abilitato. Il proxy IIS RPC viene usato insieme a IIS per inoltrare le chiamate al meccanismo RPC da IIS ed è una delle parti principali dei servizi Internet COM, che viene abilitata impostando CISEnabled su True. Per altre informazioni su RPCProxyEnabled, vedere [Sicurezza RPC HTTP](/windows/desktop/Rpc/rpc-over-http-security). |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                             |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                  |
| Predefinito        | Falso                                                                                                                                                                                                                                                                                                                                                 |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a>SecureReferencesEnabled



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Impone nei computer DCOM che le chiamate tra processi ai metodi [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sono protette. |
| Access         | ReadWrite                                                                                                                                                                 |
| Tipo           | Bool                                                                                                                                                                      |
| Predefinito        | Falso                                                                                                                                                                     |
| Sistema minimo | Windows 2000                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a>SecurityTrackingEnabled



| Voce | Valore |
|----------------|---------------------------------------------------------|
| Descrizione    | Impostare su True se il rilevamento della sicurezza è abilitato per gli oggetti. |
| Access         | ReadWrite                                               |
| Tipo           | Bool                                                    |
| Predefinito        | Vero                                                    |
| Sistema minimo | Windows 2000                                            |



 

### <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina il modo in cui i criteri di restrizione software (SRP) gestisce le connessioni di attivazione come attivatore. Se impostato su True, il livello di attendibilità SRP configurato per l'oggetto server viene confrontato con il livello di attendibilità SRP dell'oggetto client e il livello di attendibilità più alto (più stringente) viene usato per eseguire l'oggetto server. Se impostato su False, l'oggetto server viene eseguito con il livello di attendibilità SRP dell'oggetto client, indipendentemente dal livello di attendibilità SRP con cui è configurato il server. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Predefinito        | Vero                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Determina il modo in cui i criteri di restrizione software (SRP) gestisce i tentativi di connessione ai processi esistenti. Se impostato su False, i tentativi di connessione agli oggetti in esecuzione non vengono verificati per i livelli di attendibilità SRP appropriati. Se impostato su True, l'oggetto in esecuzione deve avere un livello di attendibilità SRP uguale o superiore (più stringente) rispetto all'oggetto client. Ad esempio, un oggetto client con un livello di attendibilità SRP senza restrizioni non può connettersi a un oggetto in esecuzione con un livello di attendibilità SRP non consentito. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Predefinito        | Vero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema minimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a>TransactionTimeout



| Voce | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Deve essere impostato su un valore sufficiente in secondi se si esezionano numerose operazioni all'interno di una transazione. Il periodo di timeout predefinito è 60 secondi e il periodo di timeout massimo è 3600 secondi (1 ora). L'impostazione di questa proprietà su 0 disabilita i timeout delle transazioni. Questa proprietà può essere sottoposta a override da singoli componenti usando la proprietà ComponentTransactionTimeout della [**raccolta Components.**](components.md) |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Tipo           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Predefinito        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a>Esempio

L'esempio di Microsoft Visual Basic seguente illustra come connettersi a un computer remoto e ottenere la relativa proprietà SecurityTrackingEnabled usando la raccolta **LocalComputer** del computer remoto. Per usare questo esempio, aggiungere la libreria dei tipi di amministrazione COM+ come riferimento al Visual Basic progetto.


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



Per usare la funzione , specificare un valore stringa per il nome del computer remoto. Il codice Visual Basic seguente illustra come connettersi al computer denominato "RemoteComputerName".


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

 

 
