---
description: Un provider di associazioni fornisce un meccanismo per registrare i profili e associarli ai profili implementati in spazi dei nomi diversi.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Scrittura di un provider di associazioni per l'interoperabilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f38f09a5c5771fe7fd04909f8247834b646ad1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323811"
---
# <a name="writing-an-association-provider-for-interop"></a>Scrittura di un provider di associazioni per l'interoperabilità

Un provider di associazioni fornisce un meccanismo per registrare i profili e associarli ai profili implementati in spazi dei nomi diversi.

I provider di associazioni vengono usati per esporre i profili standard, ad esempio un profilo di alimentazione. Questa operazione viene eseguita scrivendo un provider di associazioni nello spazio dei nomi radice/interoperabilità che espone le istanze di associazione implementando una classe, derivata da [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)). Il provider deve essere registrato sia nella radice/interoperabilità che nella radice/ <implemented> spazio dei nomi per supportare l'attraversamento dello spazio dei nomi incrociato.

Strumentazione gestione Windows (WMI) carica il provider di associazione ogni volta che viene eseguita una query di associazione nello spazio dei nomi radice/interoperabilità.

**Per implementare un provider di associazioni per l'interoperabilità**

1.  Derivare una classe da [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) e creare un'istanza statica di questa classe derivata nello \\ spazio dei nomi di interoperabilità radice. Come minimo, le proprietà seguenti devono essere propagate con valori validi:

    -   [**InstanceID**](/previous-versions//ee309375(v=vs.85))
    -   [**Registratore**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))

    Anche se [**InstanceID**](/previous-versions//ee309375(v=vs.85)) definisce in modo univoco l'istanza del **\_ RegisteredProfile CIM**, la combinazione di **registeredname**, **RegisteredOrganization** e **RegisteredVersion** deve identificare in modo univoco il profilo registrato nell'ambito dell'organizzazione. Per ulteriori informazioni sulle singole proprietà, vedere [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).

    Nell'esempio di codice seguente viene illustrata la sintassi per la derivazione della classe **ProcessProfile** da [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) e la compilazione dell'istanza statica.

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
    > Per i client Windows, la proprietà **RegisteredOrganization** deve essere impostata su 1 e la proprietà **OtherRegisteredOrganization** è impostata su "Microsoft".

     

2.  Creare un provider che restituisca istanze di associazione di [**\_ ElementConformsToProfile CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile). Si tratta di un processo in due passaggi.

    1.  Creare una classe derivata da [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in entrambi gli spazi dei nomi di interoperabilità e implementazione. Poiché lo stesso profilo può essere implementato da fornitori diversi, il nome della classe deve essere univoco. La convenzione di denominazione consigliata è " <Organization> \_ <ProductName> \_ <ClassName> \_ <Version> ". La proprietà **ConformantStandard** o **Managed** deve specificare il qualificatore **MSFT \_ targetNamespace** che contiene lo spazio dei nomi a cui appartiene questa classe.

        Nell'esempio di codice seguente viene descritta la sintassi per la derivazione della \_ classe Microsoft Process \_ ElementConformsToProfile \_ V1 da [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) nello \\ spazio dei nomi di interoperabilità radice. In questo esempio, l' \_ elemento gestito del processo Win32 fa riferimento allo \\ spazio dei nomi CIMV2 radice utilizzando il qualificatore **MSFT \_ targetNamespace** .

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        Nell'esempio di codice seguente viene descritta la sintassi per la derivazione della \_ classe Microsoft Process \_ ElementConformsToProfile \_ V1 da [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) nello \\ spazio dei nomi CIMV2 radice. In questo esempio, lo [**standard \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) conforme a CIM fa riferimento allo \\ spazio dei nomi di interoperabilità radice utilizzando il qualificatore **MSFT \_ targetNamespace** .

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        Se il qualificatore di **MSFT \_ targetNamespace** non è specificato nella proprietà che fa riferimento allo spazio dei nomi implementato, il filtro **ResultClass** dell'istruzione "ASSOCIATORS of" non funzionerà. Se, ad esempio, il qualificatore di **MSFT \_ targetNamespace** non è specificato, la seguente riga di comando di Windows PowerShell non restituirà un oggetto: **Get-WmiObject-Query "associatirs di {ProcessProfile. InstanceId =' Process '} dove ResultClass =' Win32 \_ Process '"**.

        Il qualificatore di **MSFT \_ targetNamespace** non può puntare a uno spazio dei nomi in un computer remoto. Lo spazio dei nomi seguente, ad esempio, non è supportato: MSFT \_ targetNamespace ( \\ \\ \\ \\ <RemoteMachine> \\ \\ \\ \\ interoperabilità radice).

    2.  Scrivere un provider che restituisce istanze della classe derivata creata. Per ulteriori informazioni, vedere [scrittura di un provider di istanze](writing-an-instance-provider.md). Quando si accede a istanze tra gli spazi dei nomi, potrebbe essere necessario accedere ai livelli di sicurezza per il client. Per ulteriori informazioni, vedere [rappresentazione di un client](impersonating-a-client.md).

        Il provider di associazioni deve implementare entrambi i metodi [**IWbemServices. CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) e [**IWbemServices. GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) . L'implementazione del metodo [**cQueryAsyncIWbemServices.Exe**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) è facoltativa. Poiché è possibile accedere a questo provider sia dall' \\ interoperabilità radice che dagli \\ <implemented> spazi dei nomi radice, non dovrebbe essere presente una dipendenza esplicita da uno spazio dei nomi all'interno del provider.

3.  Registrare il provider di associazioni nell' \\ interoperabilità radice e negli \\ <implemented> spazi dei nomi radice. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di istanze](registering-an-instance-provider.md).

    Nell'esempio di codice seguente viene illustrata la sintassi per registrare il provider di associazioni nello \\ spazio dei nomi di interoperabilità radice.

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

    Nell'esempio di codice seguente viene illustrata la sintassi per registrare il provider di associazioni nello \\ spazio dei nomi CIMV2 radice.

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

4.  Inserire lo schema per il [**\_ ElementConformsToProfile CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) nello spazio dei nomi implementato. Per i client Windows si tratta del file Interop. mof che si trova nella cartella% SystemRoot% \\ system32 \\ WBEM.
5.  Implementare l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.

    WMI utilizza [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per caricare e inizializzare un provider. Il [**IWbemProviderInit.Inimetodo tialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) deve essere implementato in modo da consentirne la chiamata per due spazi dei nomi diversi. Per ulteriori informazioni, vedere [inizializzazione di un provider](initializing-a-provider.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[Scrittura di un provider di istanze](writing-an-instance-provider.md)
</dt> <dt>

[Registrazione di un provider di istanze](registering-an-instance-provider.md)
</dt> </dl>

 

 
