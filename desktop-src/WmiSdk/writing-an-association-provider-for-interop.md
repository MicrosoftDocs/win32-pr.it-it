---
description: Un provider di associazioni fornisce un meccanismo per registrare i profili e associarli ai profili implementati in spazi dei nomi diversi.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Scrittura di un provider di associazioni per l'interoperabilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d45ceebf9f3465bf9485f4105d9ea2e4438a25c9d169193a8b68c19669b51b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794271"
---
# <a name="writing-an-association-provider-for-interop"></a>Scrittura di un provider di associazioni per l'interoperabilità

Un provider di associazioni fornisce un meccanismo per registrare i profili e associarli ai profili implementati in spazi dei nomi diversi.

I provider di associazioni vengono usati per esporre i profili standard, ad esempio un profilo di alimentazione. Questa operazione viene eseguita scrivendo un provider di associazione nello spazio dei nomi root/interop che espone istanze di associazione implementando una classe derivata da [**CIM \_ RegisteredProfile.**](/previous-versions//ee309375(v=vs.85)) Il provider deve essere registrato sia nella radice/interoperabilità che nello spazio dei nomi <implemented> root/per supportare l'attraversamento tra spazi dei nomi.

Windows Strumentazione gestione (WMI) carica il provider di associazioni ogni volta che viene eseguita una query di associazione nello spazio dei nomi root/interop.

**Per implementare un provider di associazioni per l'interoperabilità**

1.  Derivare una classe [**da CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) e creare un'istanza statica di questa classe derivata nello spazio dei nomi di \\ interoperabilità radice. Come minimo, le proprietà seguenti devono essere propagate con valori validi:

    -   [**Instanceid**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredName**](/previous-versions//ee309375(v=vs.85))
    -   [**Registeredorganization**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))

    Anche se [**InstanceID**](/previous-versions//ee309375(v=vs.85)) definisce in modo univoco l'istanza di **CIM \_ RegisteredProfile,** la combinazione di **RegisteredName,** **RegisteredOrganization** e **RegisteredVersion** deve identificare in modo univoco il profilo registrato nell'ambito dell'organizzazione. Per altre informazioni sulle singole proprietà, vedere [**CIM \_ RegisteredProfile.**](/previous-versions//ee309375(v=vs.85))

    L'esempio di codice seguente descrive la sintassi per derivare la **classe ProcessProfile** da [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) e popolare l'istanza statica.

    ```syntax
    class ProcessProfile : CIM_RegisteredProfile
    {
    };

    instance of ProcessProfile as $PP
    {
         InstanceID = "Process";
         RegisteredName = "Process";
         RegisteredOrganization = "1"; // Set to "Other"
         OtherRegisteredOrganization = "Microsoft";
         RegisteredVersion = "1.0";
    };
    ```

    > [!Note]  
    > Per Windows client, la **proprietà RegisteredOrganization** deve essere impostata su 1 e la **proprietà OtherRegisteredOrganization** su "Microsoft".

     

2.  Creare un provider che restituisce istanze di associazione [**di \_ CiM ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile). Si tratta di un processo in due passaggi.

    1.  Creare una classe derivata da [**CiM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) negli spazi dei nomi di interoperabilità e implementazione. Poiché lo stesso profilo può essere implementato da fornitori diversi, il nome della classe deve essere univoco. La convenzione di denominazione consigliata è " <Organization> \_ <ProductName> \_ <ClassName> \_ <Version> ". La **proprietà ConformantStandard** o **ManagedElement** deve specificare il qualificatore **\_ TargetNamespace MSFT** che contiene lo spazio dei nomi a cui appartiene questa classe.

        L'esempio di codice seguente descrive la sintassi per la derivazione della classe \_ Microsoft Process \_ ElementConformsToProfile v1 da \_ [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) nello spazio dei nomi di \\ interoperabilità radice. In questo esempio l'elemento gestito Win32 Process fa riferimento allo spazio dei nomi cimv2 radice usando il qualificatore \_ \\ **MSFT \_ TargetNamespace.**

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        L'esempio di codice seguente descrive la sintassi per derivare la classe Microsoft \_ Process \_ ElementConformsToProfile v1 da \_ [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) nello spazio dei nomi \\ cimv2 radice. In questo esempio, lo standard [**conforme CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) fa riferimento allo spazio dei nomi di interoperabilità radice usando il qualificatore \\ **\_ TARGETNamespace MSFT.**

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        Se il qualificatore **\_ TargetNamespace MSFT** non viene specificato nella proprietà che fa riferimento allo spazio dei nomi implementato, il filtro **ResultClass** dell'istruzione "Associators of" non funzionerà. Se ad esempio il qualificatore **MSFT \_ TargetNamespace** non è specificato, la riga di comando Windows PowerShell seguente non restituirà un oggetto: **get-wmiobject -query "associators of {ProcessProfile.InstanceID='Process'} where resultclass='Win32 \_ Process'"**.

        Il **qualificatore \_ TargetNamespace MSFT** non può puntare a uno spazio dei nomi in un computer remoto. Ad esempio, lo spazio dei nomi seguente non è supportato: MSFT \_ TargetNamespace( \\ \\ \\ \\ <RemoteMachine> \\ \\ interoperabilità \\ \\ radice).

    2.  Scrivere un provider che restituisce istanze della classe derivata creata. Per altre informazioni, vedere [Scrittura di un provider di istanze](writing-an-instance-provider.md). Quando si accede a istanze tra spazi dei nomi, potrebbe essere necessario accedere ai livelli di sicurezza per il client. Per altre informazioni, vedere [Rappresentazione di un client](impersonating-a-client.md).

        Il provider di associazione deve implementare entrambi [**i metodi IWbemServices.CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) e [**IWbemServices.GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) L'implementazione [**IWbemServices.Exemetodo cQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) è facoltativa. Poiché è possibile accedere a questo provider sia dall'interoperabilità radice che dagli spazi dei nomi radice, non deve esserci una dipendenza esplicita da uno spazio dei nomi all'interno \\ \\ <implemented> del provider.

3.  Registrare il provider di associazione sia nell'interoperabilità \\ radice che negli spazi dei nomi \\ <implemented> radice. Per altre informazioni, vedere [Registrazione di un provider di istanze](registering-an-instance-provider.md).

    Nell'esempio di codice seguente viene descritta la sintassi per registrare il provider di associazione nello spazio dei nomi di \\ interoperabilità radice.

    ```syntax
    #pragma namespace("\\\\.\\root\\interop")
    instance of __Win32Provider as $P
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $P;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

    Nell'esempio di codice seguente viene descritta la sintassi per registrare il provider di associazioni nello spazio \\ dei nomi cimv2 radice.

    ```syntax
    #pragma namespace("\\\\.\\root\\cimv2")
    instance of __Win32Provider as $R
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $R;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

4.  Inserire lo schema per [**l'elemento \_ CIMConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) nello spazio dei nomi implementato. Per Windows client si tratta del file interop.mof che si trova nella cartella %systemroot% \\ system32 \\ wbem.
5.  Implementare [**l'interfaccia IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.

    WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per caricare e inizializzare un provider. Il [**IWbemProviderInit.Inimetodo tialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) deve essere implementato in modo da poter essere chiamato per due spazi dei nomi diversi. Per altre informazioni, vedere [Inizializzazione di un provider](initializing-a-provider.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Elemento \_ CIMConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[Scrittura di un provider di istanze](writing-an-instance-provider.md)
</dt> <dt>

[Registrazione di un provider di istanze](registering-an-instance-provider.md)
</dt> </dl>

 

 
