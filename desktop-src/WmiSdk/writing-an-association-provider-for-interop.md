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
# <a name="writing-an-association-provider-for-interop"></a><span data-ttu-id="0af94-103">Scrittura di un provider di associazioni per l'interoperabilità</span><span class="sxs-lookup"><span data-stu-id="0af94-103">Writing an Association Provider for Interop</span></span>

<span data-ttu-id="0af94-104">Un provider di associazioni fornisce un meccanismo per registrare i profili e associarli ai profili implementati in spazi dei nomi diversi.</span><span class="sxs-lookup"><span data-stu-id="0af94-104">An association provider provides a mechanism to register profiles and associate them with profiles that are implemented in different namespaces.</span></span>

<span data-ttu-id="0af94-105">I provider di associazioni vengono usati per esporre i profili standard, ad esempio un profilo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="0af94-105">Association providers are used to expose standard profiles, like a power profile.</span></span> <span data-ttu-id="0af94-106">Questa operazione viene eseguita scrivendo un provider di associazioni nello spazio dei nomi radice/interoperabilità che espone le istanze di associazione implementando una classe, derivata da [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0af94-106">This is accomplished by writing an association provider in the root/interop namespace that exposes association instances by implementing a class, which is derived from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span> <span data-ttu-id="0af94-107">Il provider deve essere registrato sia nella radice/interoperabilità che nella radice/ <implemented> spazio dei nomi per supportare l'attraversamento dello spazio dei nomi incrociato.</span><span class="sxs-lookup"><span data-stu-id="0af94-107">The provider must be registered in both the root/interop and the root/<implemented> namespace to support cross namespace traversal.</span></span>

<span data-ttu-id="0af94-108">Strumentazione gestione Windows (WMI) carica il provider di associazione ogni volta che viene eseguita una query di associazione nello spazio dei nomi radice/interoperabilità.</span><span class="sxs-lookup"><span data-stu-id="0af94-108">Windows Management Instrumentation (WMI) loads the association provider whenever an association query is run in the root/interop namespace.</span></span>

<span data-ttu-id="0af94-109">**Per implementare un provider di associazioni per l'interoperabilità**</span><span class="sxs-lookup"><span data-stu-id="0af94-109">**To implement an association provider for interop**</span></span>

1.  <span data-ttu-id="0af94-110">Derivare una classe da [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) e creare un'istanza statica di questa classe derivata nello \\ spazio dei nomi di interoperabilità radice.</span><span class="sxs-lookup"><span data-stu-id="0af94-110">Derive a class from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) and create a static instance of this derived class in the root\\interop namespace.</span></span> <span data-ttu-id="0af94-111">Come minimo, le proprietà seguenti devono essere propagate con valori validi:</span><span class="sxs-lookup"><span data-stu-id="0af94-111">At a minimum, the following properties must be propagated with valid values:</span></span>

    -   <span data-ttu-id="0af94-112">[**InstanceID**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0af94-112">[**InstanceID**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="0af94-113">[**Registratore**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0af94-113">[**RegisteredName**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="0af94-114">[**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0af94-114">[**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))</span></span>
    -   <span data-ttu-id="0af94-115">[**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0af94-115">[**RegisteredVersion**](/previous-versions//ee309375(v=vs.85))</span></span>

    <span data-ttu-id="0af94-116">Anche se [**InstanceID**](/previous-versions//ee309375(v=vs.85)) definisce in modo univoco l'istanza del **\_ RegisteredProfile CIM**, la combinazione di **registeredname**, **RegisteredOrganization** e **RegisteredVersion** deve identificare in modo univoco il profilo registrato nell'ambito dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0af94-116">Even though [**InstanceID**](/previous-versions//ee309375(v=vs.85)) uniquely defines the instance of the **CIM\_RegisteredProfile**, the combination of **RegisteredName**, **RegisteredOrganization**, and **RegisteredVersion** must uniquely identify the registered profile within the scope of the organization.</span></span> <span data-ttu-id="0af94-117">Per ulteriori informazioni sulle singole proprietà, vedere [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0af94-117">For more information about the individual properties, see [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

    <span data-ttu-id="0af94-118">Nell'esempio di codice seguente viene illustrata la sintassi per la derivazione della classe **ProcessProfile** da [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) e la compilazione dell'istanza statica.</span><span class="sxs-lookup"><span data-stu-id="0af94-118">The following code example describes the syntax for deriving the **ProcessProfile** class from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) and populating the static instance.</span></span>

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
    > <span data-ttu-id="0af94-119">Per i client Windows, la proprietà **RegisteredOrganization** deve essere impostata su 1 e la proprietà **OtherRegisteredOrganization** è impostata su "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="0af94-119">For Windows clients, the **RegisteredOrganization** property must be set to 1 and the **OtherRegisteredOrganization** property set to "Microsoft".</span></span>

     

2.  <span data-ttu-id="0af94-120">Creare un provider che restituisca istanze di associazione di [**\_ ElementConformsToProfile CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile).</span><span class="sxs-lookup"><span data-stu-id="0af94-120">Create a provider that returns association instances of [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile).</span></span> <span data-ttu-id="0af94-121">Si tratta di un processo in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="0af94-121">This is a two-step process.</span></span>

    1.  <span data-ttu-id="0af94-122">Creare una classe derivata da [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in entrambi gli spazi dei nomi di interoperabilità e implementazione.</span><span class="sxs-lookup"><span data-stu-id="0af94-122">Create a class that is derived from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in both the interop and implementation namespaces.</span></span> <span data-ttu-id="0af94-123">Poiché lo stesso profilo può essere implementato da fornitori diversi, il nome della classe deve essere univoco.</span><span class="sxs-lookup"><span data-stu-id="0af94-123">Because the same profile can be implemented by different vendors, the name of the class should be unique.</span></span> <span data-ttu-id="0af94-124">La convenzione di denominazione consigliata è " <Organization> \_ <ProductName> \_ <ClassName> \_ <Version> ".</span><span class="sxs-lookup"><span data-stu-id="0af94-124">The recommended naming convention is "<Organization>\_<ProductName>\_<ClassName>\_<Version>".</span></span> <span data-ttu-id="0af94-125">La proprietà **ConformantStandard** o **Managed** deve specificare il qualificatore **MSFT \_ targetNamespace** che contiene lo spazio dei nomi a cui appartiene questa classe.</span><span class="sxs-lookup"><span data-stu-id="0af94-125">Either the **ConformantStandard** or the **ManagedElement** property must specify the **MSFT\_TargetNamespace** qualifier that contains the namespace to which this class belongs.</span></span>

        <span data-ttu-id="0af94-126">Nell'esempio di codice seguente viene descritta la sintassi per la derivazione della \_ classe Microsoft Process \_ ElementConformsToProfile \_ V1 da [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) nello \\ spazio dei nomi di interoperabilità radice.</span><span class="sxs-lookup"><span data-stu-id="0af94-126">The following code example describes the syntax for deriving the Microsoft\_Process\_ElementConformsToProfile\_v1 class from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in the root\\interop namespace.</span></span> <span data-ttu-id="0af94-127">In questo esempio, l' \_ elemento gestito del processo Win32 fa riferimento allo \\ spazio dei nomi CIMV2 radice utilizzando il qualificatore **MSFT \_ targetNamespace** .</span><span class="sxs-lookup"><span data-stu-id="0af94-127">In this example, the Win32\_Process managed element references the root\\cimv2 namespace by using the **MSFT\_TargetNamespace** qualifier.</span></span>

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        <span data-ttu-id="0af94-128">Nell'esempio di codice seguente viene descritta la sintassi per la derivazione della \_ classe Microsoft Process \_ ElementConformsToProfile \_ V1 da [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) nello \\ spazio dei nomi CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="0af94-128">The following code example describes the syntax for deriving the Microsoft\_Process\_ElementConformsToProfile\_v1 class from [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) in the root\\cimv2 namespace.</span></span> <span data-ttu-id="0af94-129">In questo esempio, lo [**standard \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) conforme a CIM fa riferimento allo \\ spazio dei nomi di interoperabilità radice utilizzando il qualificatore **MSFT \_ targetNamespace** .</span><span class="sxs-lookup"><span data-stu-id="0af94-129">In this example, the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) conformant standard references the root\\interop namespace by using the **MSFT\_TargetNamespace** qualifier.</span></span>

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        <span data-ttu-id="0af94-130">Se il qualificatore di **MSFT \_ targetNamespace** non è specificato nella proprietà che fa riferimento allo spazio dei nomi implementato, il filtro **ResultClass** dell'istruzione "ASSOCIATORS of" non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="0af94-130">If the **MSFT\_TargetNamespace** qualifier is not specified on the property that is referencing the implemented namespace, the **ResultClass** filter of "Associators of" statement will not work.</span></span> <span data-ttu-id="0af94-131">Se, ad esempio, il qualificatore di **MSFT \_ targetNamespace** non è specificato, la seguente riga di comando di Windows PowerShell non restituirà un oggetto: **Get-WmiObject-Query "associatirs di {ProcessProfile. InstanceId =' Process '} dove ResultClass =' Win32 \_ Process '"**.</span><span class="sxs-lookup"><span data-stu-id="0af94-131">For example, if the **MSFT\_TargetNamespace** qualifier is not specified, the following Windows PowerShell command-line will not return an object: **get-wmiobject -query "associators of {ProcessProfile.InstanceID='Process'} where resultclass='Win32\_Process'"**.</span></span>

        <span data-ttu-id="0af94-132">Il qualificatore di **MSFT \_ targetNamespace** non può puntare a uno spazio dei nomi in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="0af94-132">The **MSFT\_TargetNamespace** qualifier cannot point to a namespace on a remote computer.</span></span> <span data-ttu-id="0af94-133">Lo spazio dei nomi seguente, ad esempio, non è supportato: MSFT \_ targetNamespace ( \\ \\ \\ \\ <RemoteMachine> \\ \\ \\ \\ interoperabilità radice).</span><span class="sxs-lookup"><span data-stu-id="0af94-133">For example, the following namespace is not supported: MSFT\_TargetNamespace(\\\\\\\\<RemoteMachine>\\\\root\\\\interop).</span></span>

    2.  <span data-ttu-id="0af94-134">Scrivere un provider che restituisce istanze della classe derivata creata.</span><span class="sxs-lookup"><span data-stu-id="0af94-134">Write a provider that returns instances of the created derived class.</span></span> <span data-ttu-id="0af94-135">Per ulteriori informazioni, vedere [scrittura di un provider di istanze](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0af94-135">For more information, see [Writing an Instance Provider](writing-an-instance-provider.md).</span></span> <span data-ttu-id="0af94-136">Quando si accede a istanze tra gli spazi dei nomi, potrebbe essere necessario accedere ai livelli di sicurezza per il client.</span><span class="sxs-lookup"><span data-stu-id="0af94-136">When you access cross-namespace instances, you might have to access the security levels for the client.</span></span> <span data-ttu-id="0af94-137">Per ulteriori informazioni, vedere [rappresentazione di un client](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="0af94-137">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

        <span data-ttu-id="0af94-138">Il provider di associazioni deve implementare entrambi i metodi [**IWbemServices. CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) e [**IWbemServices. GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="0af94-138">The association provider should implement both the [**IWbemServices.CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) and [**IWbemServices.GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods.</span></span> <span data-ttu-id="0af94-139">L'implementazione del metodo [**cQueryAsyncIWbemServices.Exe**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="0af94-139">Implementing the [**IWbemServices.ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method is optional.</span></span> <span data-ttu-id="0af94-140">Poiché è possibile accedere a questo provider sia dall' \\ interoperabilità radice che dagli \\ <implemented> spazi dei nomi radice, non dovrebbe essere presente una dipendenza esplicita da uno spazio dei nomi all'interno del provider.</span><span class="sxs-lookup"><span data-stu-id="0af94-140">Because this provider can be accessed from both the root\\interop and the root\\<implemented> namespaces, there should not be an explicit dependency on a namespace inside the provider.</span></span>

3.  <span data-ttu-id="0af94-141">Registrare il provider di associazioni nell' \\ interoperabilità radice e negli \\ <implemented> spazi dei nomi radice.</span><span class="sxs-lookup"><span data-stu-id="0af94-141">Register the association provider in both the root\\interop and the root\\<implemented> namespaces.</span></span> <span data-ttu-id="0af94-142">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di istanze](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0af94-142">For more information, see [Registering an Instance Provider](registering-an-instance-provider.md).</span></span>

    <span data-ttu-id="0af94-143">Nell'esempio di codice seguente viene illustrata la sintassi per registrare il provider di associazioni nello \\ spazio dei nomi di interoperabilità radice.</span><span class="sxs-lookup"><span data-stu-id="0af94-143">The following code example describes the syntax to register the association provider in the root\\interop namespace.</span></span>

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

    <span data-ttu-id="0af94-144">Nell'esempio di codice seguente viene illustrata la sintassi per registrare il provider di associazioni nello \\ spazio dei nomi CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="0af94-144">The following code example describes the syntax to register the association provider in the root\\cimv2 namespace.</span></span>

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

4.  <span data-ttu-id="0af94-145">Inserire lo schema per il [**\_ ElementConformsToProfile CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) nello spazio dei nomi implementato.</span><span class="sxs-lookup"><span data-stu-id="0af94-145">Place the schema for the [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) into the implemented namespace.</span></span> <span data-ttu-id="0af94-146">Per i client Windows si tratta del file Interop. mof che si trova nella cartella% SystemRoot% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="0af94-146">For Windows clients this is the interop.mof file that is located in the %systemroot%\\system32\\wbem folder.</span></span>
5.  <span data-ttu-id="0af94-147">Implementare l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per il provider.</span><span class="sxs-lookup"><span data-stu-id="0af94-147">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="0af94-148">WMI utilizza [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per caricare e inizializzare un provider.</span><span class="sxs-lookup"><span data-stu-id="0af94-148">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="0af94-149">Il [**IWbemProviderInit.Inimetodo tialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) deve essere implementato in modo da consentirne la chiamata per due spazi dei nomi diversi.</span><span class="sxs-lookup"><span data-stu-id="0af94-149">The [**IWbemProviderInit.Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) method should be implemented in a way that allows it to be called for two different namespaces.</span></span> <span data-ttu-id="0af94-150">Per ulteriori informazioni, vedere [inizializzazione di un provider](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0af94-150">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0af94-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0af94-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0af94-152">**\_ELEMENTCONFORMSTOPROFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="0af94-152">**CIM\_ElementConformsToProfile**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

<span data-ttu-id="0af94-153">[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0af94-153">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0af94-154">Scrittura di un provider di istanze</span><span class="sxs-lookup"><span data-stu-id="0af94-154">Writing an Instance Provider</span></span>](writing-an-instance-provider.md)
</dt> <dt>

[<span data-ttu-id="0af94-155">Registrazione di un provider di istanze</span><span class="sxs-lookup"><span data-stu-id="0af94-155">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> </dl>

 

 
