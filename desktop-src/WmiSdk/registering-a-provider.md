---
description: Prima di implementare il provider, è necessario innanzitutto registrare il provider con WMI. La registrazione del provider definisce il tipo di provider e le classi supportate dal provider. WMI può accedere solo a provider registrati.
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: Registrazione di un provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53592ecb452de1b6071cbb8f59cfaaef42b57f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314579"
---
# <a name="registering-a-provider"></a><span data-ttu-id="70f29-105">Registrazione di un provider</span><span class="sxs-lookup"><span data-stu-id="70f29-105">Registering a Provider</span></span>

<span data-ttu-id="70f29-106">Prima di implementare il provider, è necessario innanzitutto registrare il provider con WMI.</span><span class="sxs-lookup"><span data-stu-id="70f29-106">Before implementing your provider, you should first register your provider with WMI.</span></span> <span data-ttu-id="70f29-107">La registrazione del provider definisce il tipo di provider e le classi supportate dal provider.</span><span class="sxs-lookup"><span data-stu-id="70f29-107">Registering the provider defines the type of the provider and the classes that the provider supports.</span></span> <span data-ttu-id="70f29-108">WMI può accedere solo a provider registrati.</span><span class="sxs-lookup"><span data-stu-id="70f29-108">WMI can only access registered providers.</span></span>

> [!Note]  
> <span data-ttu-id="70f29-109">Per ulteriori informazioni sulla registrazione di un provider MI, vedere [procedura: registrare un provider mi](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).</span><span class="sxs-lookup"><span data-stu-id="70f29-109">For more information on registering an MI provider, see [How to: Register an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).</span></span>

 

<span data-ttu-id="70f29-110">Prima di registrare il provider, è possibile scrivere il codice del provider.</span><span class="sxs-lookup"><span data-stu-id="70f29-110">You can write your provider code before you register the provider.</span></span> <span data-ttu-id="70f29-111">Tuttavia, è molto difficile eseguire il debug di un provider non registrato con WMI.</span><span class="sxs-lookup"><span data-stu-id="70f29-111">However, it is very difficult to debug a provider that is not registered with WMI.</span></span> <span data-ttu-id="70f29-112">La determinazione delle interfacce per il provider consente inoltre di delineare lo scopo e la struttura di un provider.</span><span class="sxs-lookup"><span data-stu-id="70f29-112">Determining the interfaces for your provider also helps to outline the purpose and structure of a provider.</span></span> <span data-ttu-id="70f29-113">La registrazione del provider consente pertanto di progettare il provider.</span><span class="sxs-lookup"><span data-stu-id="70f29-113">Therefore, registering your provider helps you design your provider.</span></span>

<span data-ttu-id="70f29-114">Solo gli amministratori possono registrare o eliminare un provider.</span><span class="sxs-lookup"><span data-stu-id="70f29-114">Only administrators can register or delete a provider.</span></span>

<span data-ttu-id="70f29-115">Un provider deve essere registrato per tutti i diversi tipi di funzioni del provider che esegue.</span><span class="sxs-lookup"><span data-stu-id="70f29-115">A provider must be registered for all the different types of provider functions that it performs.</span></span> <span data-ttu-id="70f29-116">Quasi tutti i provider forniscono istanze delle classi che definiscono, ma possono anche fornire dati della proprietà, metodi, eventi o classi.</span><span class="sxs-lookup"><span data-stu-id="70f29-116">Nearly all providers supply instances of classes they define, but they may also provide property data, methods, events, or classes.</span></span> <span data-ttu-id="70f29-117">Il provider può inoltre essere registrato come provider di consumer di eventi o provider di contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="70f29-117">The provider may also be registered as an event consumer provider or a performance counter provider.</span></span> <span data-ttu-id="70f29-118">È consigliabile combinare tutte le funzionalità del provider in un provider anziché avere molti provider distinti per ogni tipo.</span><span class="sxs-lookup"><span data-stu-id="70f29-118">It is recommended that you combine all provider functionality in one provider rather than having many separate providers for each type.</span></span> <span data-ttu-id="70f29-119">Un esempio è il [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider), che fornisce metodi e istanze, e il [provider di quote disco](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), che fornisce istanze, metodi ed eventi.</span><span class="sxs-lookup"><span data-stu-id="70f29-119">An example is the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which provides methods and instances, and the [Disk Quota provider](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), which supplies instances, methods, and events.</span></span>

<span data-ttu-id="70f29-120">Un provider deve essere registrato per tutti i diversi tipi di funzioni del provider che esegue.</span><span class="sxs-lookup"><span data-stu-id="70f29-120">A provider must be registered for all the different types of provider functions that it performs.</span></span> <span data-ttu-id="70f29-121">Quasi tutti i provider forniscono istanze delle classi che definiscono, ma possono anche fornire dati della proprietà, metodi, eventi o classi.</span><span class="sxs-lookup"><span data-stu-id="70f29-121">Nearly all providers supply instances of classes they define, but they may also provide property data, methods, events, or classes.</span></span> <span data-ttu-id="70f29-122">Il provider può inoltre essere registrato come provider di consumer di eventi o provider di contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="70f29-122">The provider may also be registered as an event consumer provider or a performance counter provider.</span></span>

<span data-ttu-id="70f29-123">Per ogni tipo di registrazione viene utilizzata la stessa istanza di [**\_ \_ Win32Provider**](--win32provider.md) :</span><span class="sxs-lookup"><span data-stu-id="70f29-123">The same instance of [**\_\_Win32Provider**](--win32provider.md) is used for each type of registration:</span></span>

-   [<span data-ttu-id="70f29-124">Registrazione di un provider di istanze</span><span class="sxs-lookup"><span data-stu-id="70f29-124">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
-   [<span data-ttu-id="70f29-125">Registrazione di un provider di classi</span><span class="sxs-lookup"><span data-stu-id="70f29-125">Registering a Class Provider</span></span>](registering-a-class-provider.md)
-   [<span data-ttu-id="70f29-126">Registrazione di un provider di metodi</span><span class="sxs-lookup"><span data-stu-id="70f29-126">Registering a Method Provider</span></span>](registering-a-method-provider.md)
-   [<span data-ttu-id="70f29-127">Registrazione di un provider di eventi</span><span class="sxs-lookup"><span data-stu-id="70f29-127">Registering an Event Provider</span></span>](registering-an-event-provider.md)
-   [<span data-ttu-id="70f29-128">Registrazione di un provider di consumer di eventi</span><span class="sxs-lookup"><span data-stu-id="70f29-128">Registering an Event Consumer Provider</span></span>](registering-an-event-consumer-provider.md)
-   [<span data-ttu-id="70f29-129">Creazione di un provider di istanze in un provider di High-Performance</span><span class="sxs-lookup"><span data-stu-id="70f29-129">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a><span data-ttu-id="70f29-130">Esempio: creazione e registrazione di un'istanza di un provider</span><span class="sxs-lookup"><span data-stu-id="70f29-130">Example: Creating and Registering an Instance of a Provider</span></span>

<span data-ttu-id="70f29-131">Nell'esempio seguente viene illustrato un file MOF che crea e registra un'istanza del [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) nello \\ spazio dei nomi CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="70f29-131">The following example shows a MOF file that creates and registers an instance of the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider) in the root\\cimv2 namespace.</span></span> <span data-ttu-id="70f29-132">Assegna l'alias $Reg al provider per evitare il lungo percorso necessario nelle registrazioni di istanze e metodi.</span><span class="sxs-lookup"><span data-stu-id="70f29-132">It assigns the alias $Reg to the provider to avoid the long pathname required in the instance and method registrations.</span></span> <span data-ttu-id="70f29-133">Per ulteriori informazioni, vedere [creazione di un alias](creating-an-alias.md).</span><span class="sxs-lookup"><span data-stu-id="70f29-133">For more information, see [Creating an Alias](creating-an-alias.md).</span></span>

``` syntax
// Place the Registry provider in the root\cimv2 namespace
#pragma namespace("\\\\.\\ROOT\\cimv2")

// Create an instance of __Win32Provider
instance of __Win32Provider as $Reg
{
Name = "RegProv";        
CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
HostingModel = "NetworkServiceHost:LocalServiceHost";
};

// Register as an instance provider by
// creating an instance
// of __InstanceProviderRegistration
instance of __InstanceProviderRegistration
{
 provider = $Reg;
 SupportsDelete = FALSE;
 SupportsEnumeration = TRUE;
 SupportsGet = TRUE;
 SupportsPut = TRUE;
};

// Register as a method provider by
// creating an instance
// of __MethodProviderRegistration
instance of __MethodProviderRegistration
{
 provider = $Reg;
};

// Define the StdRegProv class
[dynamic: ToInstance, provider("RegProv")]
class StdRegProv
{
[implemented, static] uint32 CreateKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 DeleteKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 EnumKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[]);
[implemented, static] uint32 EnumValues(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[], 
 [OUT] sint32 Types[]);
[implemented, static] uint32 DeleteValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName);
 [implemented, static] uint32 SetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] uint32 uValue = 3);
[implemented, static] uint32 GetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint32 uValue);
[implemented, static] uint32 SetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "hello");
[implemented, static] uint32 GetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue[] = {"hello", "there"});
[implemented, static] uint32 GetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue[]);
[implemented, static] uint32 SetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "%path%");
[implemented, static] uint32 GetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetBinaryValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [in] uint8 uValue[] = {1, 2});
[implemented, static] uint32 GetBinaryValue(
 {IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint8 uValue[]);
[implemented, static] uint32 CheckAccess(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] uint32 uRequired = 3, 
 [OUT] boolean bGranted);
};
```

## <a name="example-registering-a-provider"></a><span data-ttu-id="70f29-134">Esempio: registrazione di un provider</span><span class="sxs-lookup"><span data-stu-id="70f29-134">Example: Registering a Provider</span></span>

<span data-ttu-id="70f29-135">Nella procedura riportata di seguito viene descritto come registrare un provider.</span><span class="sxs-lookup"><span data-stu-id="70f29-135">The following procedure describes how to register a provider.</span></span>

<span data-ttu-id="70f29-136">**Per registrare un provider**</span><span class="sxs-lookup"><span data-stu-id="70f29-136">**To register a provider**</span></span>

1.  <span data-ttu-id="70f29-137">Registrare il provider come server COM.</span><span class="sxs-lookup"><span data-stu-id="70f29-137">Register the provider as a COM server.</span></span>

    <span data-ttu-id="70f29-138">Se necessario, potrebbe essere necessario creare voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="70f29-138">If necessary, you may need to create registry entries.</span></span> <span data-ttu-id="70f29-139">Questo processo si applica a tutti i server COM e non è correlato a WMI.</span><span class="sxs-lookup"><span data-stu-id="70f29-139">This process applies to all COM servers and is unrelated to WMI.</span></span> <span data-ttu-id="70f29-140">Per ulteriori informazioni, vedere la sezione COM nella documentazione di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="70f29-140">For more information, see the COM section in the Microsoft Windows Software Development Kit (SDK) documentation.</span></span>

2.  <span data-ttu-id="70f29-141">Creare un file MOF che contiene istanze di [**\_ \_ Win32Provider**](--win32provider.md) e un'istanza di una classe derivata direttamente o indirettamente da [**\_ \_ ProviderRegistration**](--providerregistration.md), ad esempio [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="70f29-141">Create a MOF file that contains instances of [**\_\_Win32Provider**](--win32provider.md) and an instance of a class derived either directly or indirectly from [**\_\_ProviderRegistration**](--providerregistration.md), such as [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md).</span></span> <span data-ttu-id="70f29-142">Solo gli amministratori possono registrare o eliminare un provider creando istanze delle classi derivate da **\_ \_ Win32Provider** o [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="70f29-142">Only administrators can register or delete a provider by creating instances of classes derived from **\_\_Win32Provider** or [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>
3.  <span data-ttu-id="70f29-143">Impostare [**HostingModel**](--win32provider.md) nell'istanza di **\_ \_ Win32Provider** in base ai valori dei modelli di [hosting](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="70f29-143">Set the [**HostingModel**](--win32provider.md) in the instance of **\_\_Win32Provider** according to the values in [Hosting models](provider-hosting-and-security.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="70f29-144">A meno che il provider non richieda i privilegi elevati dell'account LocalSystem, la proprietà [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) deve essere impostata su "NetworkServiceHost".</span><span class="sxs-lookup"><span data-stu-id="70f29-144">Unless the provider requires the high privileges of the LocalSystem account, the [**\_\_Win32Provider.HostingModel**](--win32provider.md) property should be set to "NetworkServiceHost".</span></span> <span data-ttu-id="70f29-145">Per altre informazioni, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="70f29-145">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

     

    <span data-ttu-id="70f29-146">Nell'esempio MOF seguente dell'esempio completo viene illustrato il codice che crea un'istanza di [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="70f29-146">The following MOF example from the full example shows the code that creates an instance of [**\_\_Win32Provider**](--win32provider.md).</span></span>

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  <span data-ttu-id="70f29-147">Istanza di una classe derivata direttamente o indirettamente da [**\_ \_ ProviderRegistration**](--providerregistration.md)per descrivere l'implementazione logica del provider.</span><span class="sxs-lookup"><span data-stu-id="70f29-147">An instance of a class derived either directly or indirectly from [**\_\_ProviderRegistration**](--providerregistration.md), to describe the logical implementation of the provider.</span></span> <span data-ttu-id="70f29-148">Un provider può essere registrato per diversi tipi di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="70f29-148">A provider can be registered for several different types of functionality.</span></span> <span data-ttu-id="70f29-149">Nell'esempio precedente viene registrato RegProv come istanza e provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="70f29-149">The example above registers RegProv as an instance and method provider.</span></span> <span data-ttu-id="70f29-150">Tuttavia, se RegProv supporta la funzionalità, può essere registrato anche come proprietà o provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="70f29-150">But if RegProv supports the functionality, it could also be registered as a property or event provider.</span></span> <span data-ttu-id="70f29-151">Nella tabella seguente sono elencate le classi che registrano la funzionalità del provider.</span><span class="sxs-lookup"><span data-stu-id="70f29-151">The following table lists the classes that register provider functionality.</span></span>

    

    | <span data-ttu-id="70f29-152">Classi di registrazione del provider</span><span class="sxs-lookup"><span data-stu-id="70f29-152">Provider registration classes</span></span>                                                        | <span data-ttu-id="70f29-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70f29-153">Description</span></span>                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [<span data-ttu-id="70f29-154">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="70f29-154">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)           | <span data-ttu-id="70f29-155">Registra un [provider di istanze](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="70f29-155">Registers an [instance provider](registering-an-instance-provider.md).</span></span>             |
    | [<span data-ttu-id="70f29-156">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="70f29-156">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)                 | <span data-ttu-id="70f29-157">Registra un [provider di eventi](registering-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="70f29-157">Registers an [event provider](registering-an-event-provider.md).</span></span>                   |
    | [<span data-ttu-id="70f29-158">**\_\_EventConsumerProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="70f29-158">**\_\_EventConsumerProviderRegistration**</span></span>](--eventconsumerproviderregistration.md) | <span data-ttu-id="70f29-159">Registra un [provider di consumer di eventi](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="70f29-159">Registers an [event consumer provider](registering-an-event-consumer-provider.md).</span></span> |
    | [<span data-ttu-id="70f29-160">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="70f29-160">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)               | <span data-ttu-id="70f29-161">Registra un [provider di metodi](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="70f29-161">Registers a [method provider](registering-an-event-consumer-provider.md).</span></span>          |
    | [<span data-ttu-id="70f29-162">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="70f29-162">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)           | <span data-ttu-id="70f29-163">Registra un [provider di proprietà](registering-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="70f29-163">Registers a [property provider](registering-a-property-provider.md).</span></span>               |

    

     

5.  <span data-ttu-id="70f29-164">Inserire il file MOF in una directory permanente.</span><span class="sxs-lookup"><span data-stu-id="70f29-164">Place the MOF file into a permanent directory.</span></span>

    <span data-ttu-id="70f29-165">In genere, è necessario inserire il file nella directory di installazione del provider.</span><span class="sxs-lookup"><span data-stu-id="70f29-165">Typically, you should place the file in the installation directory of the provider.</span></span>

6.  <span data-ttu-id="70f29-166">Compilare il file MOF usando [mofcomp](mofcomp.md) o l'interfaccia [**IMOFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="70f29-166">Compile the MOF file using [mofcomp](mofcomp.md) or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="70f29-167">Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="70f29-167">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

    <span data-ttu-id="70f29-168">**Windows 8 e Windows Server 2012:** Quando si installano i provider, sia [**mofcomp**](mofcomp.md) che l'interfaccia [**IMOFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) considerano i \[ \] \[ qualificatori chiave e statici \] come true se sono presenti, indipendentemente dai valori effettivi.</span><span class="sxs-lookup"><span data-stu-id="70f29-168">**Windows 8 and Windows Server 2012:** When installing providers, both [**mofcomp**](mofcomp.md) and the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface treat the \[Key\] and \[Static\] qualifiers as true if they are present, regardless of their actual values.</span></span> <span data-ttu-id="70f29-169">Altri qualificatori vengono considerati false se sono presenti ma non sono impostati in modo esplicito su true.</span><span class="sxs-lookup"><span data-stu-id="70f29-169">Other qualifiers are treated as false if they are present but not explicitly set to true.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70f29-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70f29-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70f29-171">Sviluppo di un provider WMI</span><span class="sxs-lookup"><span data-stu-id="70f29-171">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="70f29-172">Impostazione di descrittori di sicurezza spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="70f29-172">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="70f29-173">Sicurezza del provider</span><span class="sxs-lookup"><span data-stu-id="70f29-173">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
