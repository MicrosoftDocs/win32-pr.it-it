---
description: È possibile visualizzare o modificare le informazioni rese disponibili tramite WMI tramite script.
ms.assetid: 90e71e17-c2e7-42ad-a72e-2b475e6163fe
ms.tgt_platform: multiple
title: Creazione di uno script WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ef13a5f9269dbc24566e95ce37101d10afa6c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968646"
---
# <a name="creating-a-wmi-script"></a><span data-ttu-id="788be-103">Creazione di uno script WMI</span><span class="sxs-lookup"><span data-stu-id="788be-103">Creating a WMI Script</span></span>

<span data-ttu-id="788be-104">È possibile visualizzare o modificare le informazioni rese disponibili tramite WMI tramite script.</span><span class="sxs-lookup"><span data-stu-id="788be-104">You can view or manipulate any information made available through WMI using scripts.</span></span> <span data-ttu-id="788be-105">Gli script possono essere scritti in qualsiasi linguaggio di scripting che supporta l'hosting di script Microsoft ActiveX, tra cui Visual Basic Scripting Edition (VBScript), PowerShell e Perl.</span><span class="sxs-lookup"><span data-stu-id="788be-105">Scripts can be written in any scripting language that supports Microsoft ActiveX script hosting, including Visual Basic Scripting Edition (VBScript), PowerShell, and Perl.</span></span> <span data-ttu-id="788be-106">Windows script host (WSH), Active Server Pages e Internet Explorer possono ospitare tutti gli script WMI.</span><span class="sxs-lookup"><span data-stu-id="788be-106">Windows Script Host (WSH), Active Server Pages, and Internet Explorer can all host WMI scripts.</span></span>

> [!Note]
>
> <span data-ttu-id="788be-107">Il linguaggio di scripting primario attualmente supportato da WMI è PowerShell.</span><span class="sxs-lookup"><span data-stu-id="788be-107">The primary scripting language currently supported by WMI is PowerShell.</span></span> <span data-ttu-id="788be-108">Tuttavia, WMI contiene anche un solido corpo di supporto per lo scripting per VBScript e altri linguaggi che accedono all' [API di scripting per WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="788be-108">However, WMI also contains a robust body of scripting support for VBScript and other languages that access the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

 

## <a name="wmi-scripting-languages"></a><span data-ttu-id="788be-109">Linguaggi di scripting WMI</span><span class="sxs-lookup"><span data-stu-id="788be-109">WMI Scripting Languages</span></span>

<span data-ttu-id="788be-110">I due linguaggi principali supportati da WMI sono PowerShell e VBScript (tramite Windows script host o WSH).</span><span class="sxs-lookup"><span data-stu-id="788be-110">The two main languages supported by WMI are PowerShell and VBScript (through the Windows Script Host, or WSH).</span></span>

-   <span data-ttu-id="788be-111">**PowerShell** è stato progettato con una stretta integrazione con WMI.</span><span class="sxs-lookup"><span data-stu-id="788be-111">**PowerShell** was designed with tight integration with WMI in mind.</span></span> <span data-ttu-id="788be-112">Di conseguenza, molti degli elementi sottostanti di WMI sono incorporati nei cmdlet WMI: [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)e [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1).</span><span class="sxs-lookup"><span data-stu-id="788be-112">As such, much of the underlying elements of WMI are built into the WMI cmdlets: [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1), and [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1).</span></span> <span data-ttu-id="788be-113">Nella tabella seguente vengono descritti i processi generali utilizzati per l'accesso alle informazioni di WMI.</span><span class="sxs-lookup"><span data-stu-id="788be-113">The following table describes the general processes used for accessing WMI information.</span></span> <span data-ttu-id="788be-114">Si noti che, mentre la maggior parte di questi esempi USA Get-WMIObject, molti dei cmdlet WMI di PowerShell hanno gli stessi parametri, ad esempio *-Class* o *-Credentials*.</span><span class="sxs-lookup"><span data-stu-id="788be-114">Note that while most of these examples use Get-WMIObject, many of the PowerShell WMI cmdlets have the same parameters, such as *-Class* or *-Credentials*.</span></span> <span data-ttu-id="788be-115">Pertanto, molti di questi processi funzionano anche per altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="788be-115">Therefore, many of these processes also work for other objects.</span></span> <span data-ttu-id="788be-116">Per una discussione più approfondita su PowerShell e WMI, vedere [uso del Cmdlet Get-WMiObject](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) e [Windows PowerShell-la connessione WMI](/previous-versions/technet-magazine/cc162365(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="788be-116">For a more in-depth discussion of PowerShell and WMI, see [Using the Get-WMiObject Cmdlet](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) and [Windows PowerShell - the WMI Connection](/previous-versions/technet-magazine/cc162365(v=msdn.10)).</span></span>

-   <span data-ttu-id="788be-117">**VBScript**, al contrario, effettua chiamate in modo esplicito all' [API di scripting per WMI](scripting-api-for-wmi.md), come indicato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="788be-117">**VBScript**, in contrast, explicitly makes calls to the [Scripting API for WMI](scripting-api-for-wmi.md), as mentioned above.</span></span> <span data-ttu-id="788be-118">Altri linguaggi, ad esempio Perl, possono anche usare l'API di scripting per WMI.</span><span class="sxs-lookup"><span data-stu-id="788be-118">Other languages, such as Perl, can also use the scripting API for WMI.</span></span> <span data-ttu-id="788be-119">Tuttavia, ai fini di questa documentazione, la maggior parte degli esempi che illustrano l'API di scripting per WMI utilizzerà VBScript.</span><span class="sxs-lookup"><span data-stu-id="788be-119">However, for the purposes of this documentation, most samples that demonstrate the scripting API for WMI will use VBScript.</span></span> <span data-ttu-id="788be-120">Quando una tecnica di programmazione è specifica di VBScript, tuttavia, verrà chiamata.</span><span class="sxs-lookup"><span data-stu-id="788be-120">When a programming technique is specific to VBScript, however, it will be called out.</span></span>

    <span data-ttu-id="788be-121">VBScript presenta essenzialmente due modi distinti per accedere a WMI.</span><span class="sxs-lookup"><span data-stu-id="788be-121">VBScript has essentially two separate ways of accessing WMI.</span></span> <span data-ttu-id="788be-122">Il primo consiste nell'utilizzare un oggetto [**SWbemLocator**](swbemlocator.md) per la connessione a WMI.</span><span class="sxs-lookup"><span data-stu-id="788be-122">The first is using an [**SWbemLocator**](swbemlocator.md) object to connect to WMI.</span></span> <span data-ttu-id="788be-123">In alternativa, è possibile utilizzare [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) e un moniker.</span><span class="sxs-lookup"><span data-stu-id="788be-123">Alternately, you can use [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) and a moniker.</span></span> <span data-ttu-id="788be-124">Un moniker è una stringa che può descrivere un numero di elementi: le credenziali, le impostazioni di rappresentazione, il computer a cui ci si vuole connettere, lo [*spazio dei nomi*](gloss-n.md) WMI (ad esempio, il percorso generale in cui WMI archivia gruppi di oggetti) e l'oggetto WMI che si vuole recuperare.</span><span class="sxs-lookup"><span data-stu-id="788be-124">A moniker is a string that can describe a number of elements: your credentials, impersonation settings, what computer you want to connect to, the WMI [*namespace*](gloss-n.md) (ie, the general location where WMI stores groups of objects), and what WMI object you want to retrieve.</span></span> <span data-ttu-id="788be-125">Molti degli esempi seguenti descrivono entrambe le tecniche.</span><span class="sxs-lookup"><span data-stu-id="788be-125">Many of the examples below describe both techniques.</span></span> <span data-ttu-id="788be-126">Per ulteriori informazioni, vedere [creazione di una stringa di moniker](constructing-a-moniker-string.md) e [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="788be-126">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md) and [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

    <span data-ttu-id="788be-127">Indipendentemente dalla tecnica utilizzata per connettersi a WMI, è probabile che vengano recuperati uno o più oggetti dall'API di scripting.</span><span class="sxs-lookup"><span data-stu-id="788be-127">Regardless of what technique you use to connect to WMI, you will likely retrieve one or more objects from the Scripting API.</span></span> <span data-ttu-id="788be-128">Il più comune è [**SWbemObject**](swbemobject.md), che WMI USA per descrivere un oggetto WMI.</span><span class="sxs-lookup"><span data-stu-id="788be-128">The most common is [**SWbemObject**](swbemobject.md), which WMI uses to describe a WMI object.</span></span> <span data-ttu-id="788be-129">In alternativa, è possibile utilizzare un oggetto [**SWbemServices**](swbemservices.md) per descrivere il servizio WMI stesso oppure un oggetto [**SWbemObjectPath**](swbemobjectpath.md) per descrivere la posizione di un oggetto WMI.</span><span class="sxs-lookup"><span data-stu-id="788be-129">Alternately, you may use an [**SWbemServices**](swbemservices.md) object to describe the WMI service itself, or an [**SWbemObjectPath**](swbemobjectpath.md) object to describe the location of a WMI object.</span></span> <span data-ttu-id="788be-130">Per ulteriori informazioni, vedere Creazione di [script con SWbemObject](scripting-with-swbemobject.md) e [oggetti helper di scripting](scripting-helper-objects.md).</span><span class="sxs-lookup"><span data-stu-id="788be-130">For more information, see [Scripting with SWbemObject](scripting-with-swbemobject.md) and [Scripting Helper Objects](scripting-helper-objects.md).</span></span>

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a><span data-ttu-id="788be-131">Uso di WMI e di un linguaggio di scripting...</span><span class="sxs-lookup"><span data-stu-id="788be-131">Using WMI and a Scripting Language, How Do I...</span></span>

<dl> <dt>

<span data-ttu-id="788be-132"><span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>... connettersi a WMI?</span><span class="sxs-lookup"><span data-stu-id="788be-132"><span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>...connect to WMI?</span></span>
</dt> <dd>

<span data-ttu-id="788be-133">Per VBScript e l'API di scripting per WMI, recuperare un oggetto [**SWbemServices**](swbemservices.md) con un moniker e una chiamata a [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)).</span><span class="sxs-lookup"><span data-stu-id="788be-133">For VBScript and the Scripting API for WMI, retrieve an [**SWbemServices**](swbemservices.md) object with a moniker and a call to [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)).</span></span> <span data-ttu-id="788be-134">In alternativa, è possibile connettersi al server con una chiamata a [**SWbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="788be-134">Alternately, you can connect to the server with a call to [**SWbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="788be-135">È quindi possibile utilizzare l'oggetto per accedere a uno spazio dei nomi WMI o a un'istanza di classe WMI specifica.</span><span class="sxs-lookup"><span data-stu-id="788be-135">You can then use the object to access a specific WMI namespace or WMI class instance.</span></span>

<span data-ttu-id="788be-136">Per PowerShell, la connessione a WMI viene in genere eseguita direttamente nella chiamata al cmdlet. di conseguenza, non sono necessari passaggi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="788be-136">For PowerShell, connecting to WMI is generally done directly in the cmdlet call; as such, no additional steps are necessary.</span></span>

<span data-ttu-id="788be-137">Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md), creazione di [una stringa del moniker](constructing-a-moniker-string.md)e [connessione a WMI con VBScript](connecting-to-wmi-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="788be-137">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md), [Constructing a Moniker String](constructing-a-moniker-string.md), and [Connecting to WMI with VBScript](connecting-to-wmi-with-vbscript.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example: implicitly uses the local compuer (.) and default namespace ("root\cimv2")
Set objWMIService = GetObject("winmgmts:")
```


```PowerShell

#Already has all the defaults set
get-WmiObject Win32_LogicalDisk

#Or, to be explicit,
get-WmiObject -class Win32_LogicalDisk -Computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Impersonation Impersonate
```





</dd> <dt>

<span data-ttu-id="788be-138"><span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>... recuperare informazioni da WMI?</span><span class="sxs-lookup"><span data-stu-id="788be-138"><span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>...retrieve information from WMI?</span></span>
</dt> <dd>

<span data-ttu-id="788be-139">Per VBScript e l'API di scripting per WMI, usare una funzione di recupero, ad esempio [**wbemServices. Get**](swbemservices-get.md) o [**wbemServices. InstancesOf**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="788be-139">For VBScript and the Scripting API for WMI, use a retrieval function, such as [**WbemServices.Get**](swbemservices-get.md) or [**WbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span> <span data-ttu-id="788be-140">È anche possibile inserire il nome della classe dell'oggetto da recuperare in un moniker, che può essere più efficiente.</span><span class="sxs-lookup"><span data-stu-id="788be-140">You may also place the class name of the object to retrieve in a moniker, which may be more efficient.</span></span>

<span data-ttu-id="788be-141">Per PowerShell, usare il parametro *-Class* .</span><span class="sxs-lookup"><span data-stu-id="788be-141">For PowerShell, use the *-Class* parameter.</span></span> <span data-ttu-id="788be-142">Si noti che-Class è il parametro predefinito; di conseguenza, non è necessario specificarlo in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="788be-142">Note that -Class is the default parameter; as such, you don't need to explicitly state it.</span></span>

<span data-ttu-id="788be-143">Per ulteriori informazioni, vedere [recupero di dati di istanze o classi WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="788be-143">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")
Set colScheduledJobs = objService.InstancesOf("Win32_ScheduledJob")

' Second example
SSet Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")
```


```PowerShell

#default - you don't actually need to use the -Class parameter
Get-WMIObject Win32_WmiSetting

#but you can if you want to
Get-WMIObject -Class Win32_WmiSetting
```





</dd> <dt>

<span data-ttu-id="788be-144"><span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>... creazione di una query WMI</span><span class="sxs-lookup"><span data-stu-id="788be-144"><span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>...create a WMI query?</span></span>
</dt> <dd>

<span data-ttu-id="788be-145">Per VBScript e l'API di scripting per WMI, usare il metodo [**SWbemServices.ExecQuery**](swbemservices-execquery.md) .</span><span class="sxs-lookup"><span data-stu-id="788be-145">For VBScript and the Scripting API for WMI, use the [**SWbemServices.ExecQuery**](swbemservices-execquery.md) method.</span></span>

<span data-ttu-id="788be-146">Per PowerShell, usare il parametro *-query* .</span><span class="sxs-lookup"><span data-stu-id="788be-146">For PowerShell, use the *-Query* parameter.</span></span> <span data-ttu-id="788be-147">È anche possibile filtrare utilizzando il parametro *-Filter* .</span><span class="sxs-lookup"><span data-stu-id="788be-147">You can also filter using the *-Filter* parameter.</span></span>

<span data-ttu-id="788be-148">Per ulteriori informazioni, vedere [esecuzione di query su WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="788be-148">For more information, see [Querying WMI](querying-wmi.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

Get-WmiObject -query &quot;SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'&quot;

#or

get-wmiObject -Class Win32_LogicalDisk -Filter &quot;DeviceID = &#39;C:&#39;&quot;
```





</dd> <dt>

<span data-ttu-id="788be-149"><span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>... enumerare un elenco di oggetti WMI</span><span class="sxs-lookup"><span data-stu-id="788be-149"><span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>...enumerate through a list of WMI objects?</span></span>
</dt> <dd>

<span data-ttu-id="788be-150">Per VBScript e l'API di scripting per WMI, usare l'oggetto contenitore [**SWbemObjectSet**](swbemobjectset.md) , che viene trattato nello script come raccolta che può essere enumerata.</span><span class="sxs-lookup"><span data-stu-id="788be-150">For VBScript and the Scripting API for WMI, use the [**SWbemObjectSet**](swbemobjectset.md) container object, which is treated in script as a collection that can be enumerated.</span></span> <span data-ttu-id="788be-151">È possibile recuperare un **SWbemObjectSet** da una chiamata da [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) o [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="788be-151">You can retrieve an **SWbemObjectSet** from a call from [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) or [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="788be-152">PowerShell è in grado di recuperare e gestire le enumerazioni come per qualsiasi altro oggetto. non esiste alcun elemento particolarmente univoco in WMI.</span><span class="sxs-lookup"><span data-stu-id="788be-152">PowerShell is able to retrieve and handle enumerations as it would any other object; there is nothing particularly unique to WMI.</span></span>

<span data-ttu-id="788be-153">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="788be-153">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDevice")
```


```PowerShell

$logicalDevices = Get-WmiObject CIM_LogicalDevice
foreach ($device in $logicalDevices)
{
    $device.name
}

#or, to be more compact

Get-WmiObject cim_logicalDevice | ForEach-Object { $_.name }

```





</dd> <dt>

<span data-ttu-id="788be-154"><span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>... accedere a uno spazio dei nomi WMI diverso</span><span class="sxs-lookup"><span data-stu-id="788be-154"><span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>...access a different WMI namespace?</span></span>
</dt> <dd>

<span data-ttu-id="788be-155">Per VBScript e l'API di scripting per WMI, indicare lo spazio dei nomi nel moniker, altrimenti è possibile dichiarare in modo esplicito lo spazio dei nomi nella chiamata a [**SwbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="788be-155">For VBScript and the Scripting API for WMI, state the namespace in the moniker, or else you can explicitly state the namespace in the call to [**SwbemLocator.ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

<span data-ttu-id="788be-156">Per PowerShell, usare il parametro *-namespace* .</span><span class="sxs-lookup"><span data-stu-id="788be-156">For PowerShell, use the *-Namespace* parameter.</span></span> <span data-ttu-id="788be-157">Lo spazio dei nomi predefinito è "root \\ cimV2". Tuttavia, molte classi meno recenti vengono archiviate in "root \\ default".</span><span class="sxs-lookup"><span data-stu-id="788be-157">The default namespace is "root\\cimV2"; however, many older classes are stored in "root\\default".</span></span>

<span data-ttu-id="788be-158">Per trovare il percorso di una classe WMI specificata, vedere la pagina di riferimento.</span><span class="sxs-lookup"><span data-stu-id="788be-158">To find the location of a given WMI class, look at the reference page.</span></span> <span data-ttu-id="788be-159">In alternativa, è possibile esplorare manualmente uno spazio dei nomi usando Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="788be-159">Alternately, you can manually explore a namespace using get-WmiObject.</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & "." & "\root\cimv2")
```


```PowerShell

Get-WmiObject -list * -Namespace root\default

#or, to retrieve all namespaces,
Get-WmiObject -Namespace root -Class __Namespace
```





</dd> <dt>

<span data-ttu-id="788be-160"><span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>... recuperare tutte le istanze figlio di una classe?</span><span class="sxs-lookup"><span data-stu-id="788be-160"><span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>...retrieve all child instances of a class?</span></span>
</dt> <dd>

<span data-ttu-id="788be-161">Per i linguaggi che usano direttamente l'API di scripting per WMI e PowerShell, WMI supporta il recupero delle classi figlio di una classe base.</span><span class="sxs-lookup"><span data-stu-id="788be-161">For languages that directly use the Scripting API for WMI and PowerShell, WMI supports retrieving the child classes of a base class.</span></span> <span data-ttu-id="788be-162">Di conseguenza, per recuperare le istanze figlio, è necessario cercare solo la classe padre.</span><span class="sxs-lookup"><span data-stu-id="788be-162">As such, in order to retrieve the child instances, you need to only search for the parent class.</span></span> <span data-ttu-id="788be-163">Nell'esempio seguente viene eseguita la ricerca di [**CIM \_ disco logico**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), una classe WMI preinstallata che rappresenta dischi logici in un computer basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="788be-163">The following example searches for [**CIM\_LogicalDisk**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), which is a preinstalled WMI class that represents logical disks on a Windows-based computer system.</span></span> <span data-ttu-id="788be-164">Di conseguenza, la ricerca di questa classe padre restituisce anche le istanze di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), che viene usato da Windows per descrivere i dischi rigidi.</span><span class="sxs-lookup"><span data-stu-id="788be-164">As such, searching for this parent class also returns instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), which is what Windows uses to describe hard drives.</span></span> <span data-ttu-id="788be-165">Per ulteriori informazioni, vedere [Common Information Model](common-information-model.md).</span><span class="sxs-lookup"><span data-stu-id="788be-165">For more information, see [Common Information Model](common-information-model.md).</span></span> <span data-ttu-id="788be-166">WMI fornisce un intero schema di classi preinstallate che consentono di accedere agli oggetti gestiti e di controllarli.</span><span class="sxs-lookup"><span data-stu-id="788be-166">WMI supplies an entire schema of such preinstalled classes that allow you to access and control managed objects.</span></span> <span data-ttu-id="788be-167">Per ulteriori informazioni, vedere [classi Win32](/windows/desktop/CIMWin32Prov/win32-provider) e [classi WMI](wmi-classes.md).</span><span class="sxs-lookup"><span data-stu-id="788be-167">For more information, see [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider) and [WMI Classes](wmi-classes.md)..</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span data-ttu-id="788be-168"><span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>... individuare un oggetto WMI.</span><span class="sxs-lookup"><span data-stu-id="788be-168"><span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>...locate a WMI object?</span></span>
</dt> <dd>

<span data-ttu-id="788be-169">Per l'API di scripting per WMI e PowerShell, WMI utilizza una combinazione di spazio dei nomi, nome classe e proprietà chiave per identificare in modo univoco un'istanza WMI specificata.</span><span class="sxs-lookup"><span data-stu-id="788be-169">For both the Scripting API for WMI and PowerShell, WMI uses a combination of namespace, class name, and key properties to uniquely identify a given WMI instance.</span></span> <span data-ttu-id="788be-170">Insieme, questo è noto come percorso dell'oggetto WMI.</span><span class="sxs-lookup"><span data-stu-id="788be-170">Together, this is known as the WMI object path.</span></span> <span data-ttu-id="788be-171">Per VBScript, la proprietà [**SWbemObject. \_ path**](swbemobject-path-.md) descrive il percorso di un determinato oggetto restituito dall'API di scripting.</span><span class="sxs-lookup"><span data-stu-id="788be-171">For VBScript, the [**SWbemObject.Path\_**](swbemobject-path-.md) property describes the path for any given object returned by the scripting API.</span></span> <span data-ttu-id="788be-172">Per PowerShell, ogni oggetto WMI avrà una \_ \_ proprietà Path.</span><span class="sxs-lookup"><span data-stu-id="788be-172">For PowerShell, every WMI object will have a \_\_PATH property.</span></span> <span data-ttu-id="788be-173">Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md) .</span><span class="sxs-lookup"><span data-stu-id="788be-173">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md)</span></span>

<span data-ttu-id="788be-174">Oltre allo spazio dei nomi e al nome della classe, un oggetto WMI avrà anche una proprietà chiave che identifica in modo univoco tale istanza rispetto ad altre istanze nel computer.</span><span class="sxs-lookup"><span data-stu-id="788be-174">In addition to namespace and class name, a WMI object will also have a key property, which uniquely identifies that instance compared to other instances on your machine.</span></span> <span data-ttu-id="788be-175">Ad esempio, la proprietà **DeviceID** è la proprietà chiave per la [**classe \_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="788be-175">For example, the **DeviceID** property is the key property for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span> <span data-ttu-id="788be-176">Per ulteriori informazioni, vedere [Managed Object Format (MOF)](managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="788be-176">For more information, see [Managed Object Format (MOF)](managed-object-format--mof-.md).</span></span>

<span data-ttu-id="788be-177">Infine, il percorso relativo è semplicemente una forma abbreviata del percorso e include il nome della classe e il valore della chiave.</span><span class="sxs-lookup"><span data-stu-id="788be-177">Finally, the Relative path is simply a shortened form of the path, and includes the class name and key value.</span></span> <span data-ttu-id="788be-178">Negli esempi seguenti il percorso può essere " \\ \\ ComputerName \\ root \\ CIMV2: Win32 \_ disco logico. DeviceID =" D: "", mentre il percorso relativo sarà "" Win32LogicalDisk. DeviceID = "D" "".</span><span class="sxs-lookup"><span data-stu-id="788be-178">In the examples below, the path may be "\\\\computerName\\root\\cimv2:Win32\_LogicalDisk.DeviceID="D:"", while the relative path would be ""Win32LogicalDisk.DeviceID="D""".</span></span>


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_.Relpath

'or to get the path
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_
```




```PowerShell
#retrieving the path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__PATH  }

#retrieving the relative path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__RELPATH  }
```



</dd> <dt>

<span data-ttu-id="788be-179"><span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>... impostare le informazioni in WMI?</span><span class="sxs-lookup"><span data-stu-id="788be-179"><span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>...set information in WMI?</span></span>
</dt> <dd>

<span data-ttu-id="788be-180">Per VBScript e l'API di scripting per WMI, usare il metodo [**SWbemObject \_ . Put**](swbemobject-put-.md) .</span><span class="sxs-lookup"><span data-stu-id="788be-180">For VBScript and the Scripting API for WMI, use the [**SWbemObject.Put\_**](swbemobject-put-.md) method.</span></span>

<span data-ttu-id="788be-181">Per PowerShell, è possibile usare il metodo Put oppure else [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="788be-181">For PowerShell, you can either use the Put method, or else [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span></span>

<span data-ttu-id="788be-182">Per ulteriori informazioni, vedere [modifica di una proprietà dell'istanza](modifying-an-instance-property.md).</span><span class="sxs-lookup"><span data-stu-id="788be-182">For more information, see [Modifying an Instance Property](modifying-an-instance-property.md).</span></span>


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject("Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path
```


```PowerShell

$mySettings = get-WMIObject Win32_WmiSetting
$mySettings.LoggingLevel = 1
$mySettings.Put()

#or

Set-WMIInstance -class Win32_WMISetting -argument @{LoggingLevel=1}
```





</dd> <dt>

<span data-ttu-id="788be-183"><span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>... usare credenziali diverse?</span><span class="sxs-lookup"><span data-stu-id="788be-183"><span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>...use different credentials?</span></span>
</dt> <dd>

<span data-ttu-id="788be-184">Per VBScript e l'API di scripting per WMI, usare i parametri *username* e *password* nel metodo [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="788be-184">For VBScript and the Scripting API for WMI, use the *UserName* and *Password* parameters in the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

<span data-ttu-id="788be-185">Per PowerShell, usare il parametro *-Credential* .</span><span class="sxs-lookup"><span data-stu-id="788be-185">For PowerShell, use the *-Credential* parameter.</span></span>

<span data-ttu-id="788be-186">Si noti che è possibile utilizzare credenziali alternative solo in un sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="788be-186">Note that you can only use alternate credentials on a remote system.</span></span> <span data-ttu-id="788be-187">Per ulteriori informazioni, vedere [protezione dei client di scripting](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="788be-187">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>


```VB
strComputer = "remoteComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Credential FABRIKAM\administrator  `
-ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="788be-188"><span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>... accedere a un computer remoto?</span><span class="sxs-lookup"><span data-stu-id="788be-188"><span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>...access a remote computer?</span></span>
</dt> <dd>

<span data-ttu-id="788be-189">Per VBScript e l'API di scripting per WMI, indicare in modo esplicito il nome del computer nel moniker, altrimenti nella chiamata a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="788be-189">For VBScript and the Scripting API for WMI, explicitly state the name of the computer in either the moniker, or else in the call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="788be-190">Per ulteriori informazioni, vedere [connessione a WMI in modalità remota con VBScript](connecting-to-wmi-remotely-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="788be-190">For more information, see [Connecting to WMI Remotely with VBScript](connecting-to-wmi-remotely-with-vbscript.md).</span></span>

<span data-ttu-id="788be-191">Per PowerShell, usare il parametro *-ComputerName* .</span><span class="sxs-lookup"><span data-stu-id="788be-191">For PowerShell, use the *-ComputerName* parameter.</span></span> <span data-ttu-id="788be-192">Per altre informazioni, vedere [connessione a WMI in modalità remota con PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="788be-192">For more information, see [Connecting to WMI Remotely with PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span></span>


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer("myRemoteServerName", "root\cimv2")
Set colScheduledJobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine

'example 2

strComputer = "myRemoteServerName"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_logicalDisk -ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="788be-193"><span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>... impostare i livelli di autenticazione e di rappresentazione?</span><span class="sxs-lookup"><span data-stu-id="788be-193"><span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>...set the Authentication and Impersonation levels?</span></span>
</dt> <dd>

<span data-ttu-id="788be-194">Per VBScript e l'API di scripting per WMI, utilizzare la proprietà [**SWbemServices \_ . Security**](swbemlocator-security-.md) nell'oggetto server restituito, altrimenti impostare i valori rilevanti nel moniker.</span><span class="sxs-lookup"><span data-stu-id="788be-194">For VBScript and the Scripting API for WMI, use the [**SWbemServices.Security\_**](swbemlocator-security-.md) property on the returned server object, or else set the relevant values in the moniker.</span></span>

<span data-ttu-id="788be-195">Per PowerShell, usare rispettivamente i parametri *-Authentication* e *-Impersonation* .</span><span class="sxs-lookup"><span data-stu-id="788be-195">For PowerShell, use the *-Authentication* and *-Impersonation* parameters, respectively.</span></span> <span data-ttu-id="788be-196">Per ulteriori informazioni, vedere [protezione dei client di scripting](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="788be-196">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

<span data-ttu-id="788be-197">Per ulteriori informazioni, vedere [protezione dei client di scripting](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="788be-197">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>


```VB
' First example
Set Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")

' Second example
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set Service = Locator.ConnectServer       
service.Security_.ImpersonationLevel = wbemImpersonationLevelImpersonate  
Set objinstance = Service.Get("Win32_Service=""ALERTER""")
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Impersonation Impersonate `
 -Authentication PacketIntegrity -Credential FABRIKAM\administrator -ComputerName $Computer
```





</dd> <dt>

<span data-ttu-id="788be-198"><span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>... gestione degli errori in WMI</span><span class="sxs-lookup"><span data-stu-id="788be-198"><span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>...handle errors in WMI?</span></span>
</dt> <dd>

<span data-ttu-id="788be-199">Per l'API di scripting per WMI, il provider può fornire un oggetto [**SWbemLastError**](swbemlasterror.md) per fornire ulteriori informazioni su un errore.</span><span class="sxs-lookup"><span data-stu-id="788be-199">For the Scripting API for WMI, the provider may supply an [**SWbemLastError**](swbemlasterror.md) object to give further information on an error.</span></span>

<span data-ttu-id="788be-200">In VBScript, in particolare, la gestione degli errori è supportata anche tramite l'oggetto **Err** nativo.</span><span class="sxs-lookup"><span data-stu-id="788be-200">In VBScript in particular, error handling is also supported using the native **Err** object.</span></span> <span data-ttu-id="788be-201">È anche possibile accedere all'oggetto [**SWbemLastError**](swbemlasterror.md), come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="788be-201">You may also access the [**SWbemLastError**](swbemlasterror.md)object, as described above.</span></span> <span data-ttu-id="788be-202">Per ulteriori informazioni, vedere [recupero di un codice di errore](retrieving-an-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="788be-202">For more information, see [Retrieving an Error Code](retrieving-an-error-code.md).</span></span>

<span data-ttu-id="788be-203">Per PowerShell, è possibile usare le tecniche standard di gestione degli errori di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="788be-203">For PowerShell, you can use the standard PowerShell error handling techniques.</span></span> <span data-ttu-id="788be-204">Per altre informazioni, vedere [Introduzione alla gestione degli errori in PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).</span><span class="sxs-lookup"><span data-stu-id="788be-204">For more information, see [An Introduction to Error Handling in PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).</span></span>


```VB
'using Err
On Error Resume Next
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number

'using SWbemLastError

On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



</dd> </dl>

 

 
