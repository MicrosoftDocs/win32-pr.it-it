---
title: URI risorse
description: Un URI di risorsa è un identificatore per un tipo distinto di operazione di gestione o di valore utilizzato dai servizi di gestione che implementano il protocollo WS-Management.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 665c73caf5cf636ab7f0a0162f488ff073917984
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516810"
---
# <a name="resource-uris"></a><span data-ttu-id="6574e-103">URI risorse</span><span class="sxs-lookup"><span data-stu-id="6574e-103">Resource URIs</span></span>

<span data-ttu-id="6574e-104">Un [*URI di risorsa*](windows-remote-management-glossary.md) è un identificatore per un tipo distinto di operazione di gestione o di valore utilizzato dai servizi di gestione che implementano il protocollo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="6574e-104">A [*resource URI*](windows-remote-management-glossary.md) is an identifier for a distinct type of management operation or value used by management services that implement the WS-Management protocol.</span></span> <span data-ttu-id="6574e-105">Un valore di gestione potrebbe essere la temperatura all'interno di un computer.</span><span class="sxs-lookup"><span data-stu-id="6574e-105">A management value could be the temperature inside a computer.</span></span> <span data-ttu-id="6574e-106">Un esempio di operazione di gestione è l'avvio di un servizio interrotto o l'impostazione di una quota utente del volume del disco.</span><span class="sxs-lookup"><span data-stu-id="6574e-106">An example of a management operation is starting a stopped service or setting a disk volume user quota.</span></span>

## <a name="resource-uri-format"></a><span data-ttu-id="6574e-107">Formato URI risorsa</span><span class="sxs-lookup"><span data-stu-id="6574e-107">Resource URI Format</span></span>

<span data-ttu-id="6574e-108">Un URI è costituito da un prefisso e da un percorso a una risorsa, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="6574e-108">A URI consists of a prefix and a path to a resource as is shown in the following example:</span></span>

<span data-ttu-id="6574e-109">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"</span><span class="sxs-lookup"><span data-stu-id="6574e-109">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"</span></span>

<span data-ttu-id="6574e-110">Questa specifica dello schema indica che l'URI è basato sulla versione 1 del protocollo WS-Management ufficiale e che la risorsa è una [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) nello \\ spazio dei nomi "root cimv2" del repository WMI.</span><span class="sxs-lookup"><span data-stu-id="6574e-110">This schema specification indicates that the URI is based on version 1 of the official WS-Management protocol and that the resource is a [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in the "root\\cimv2" namespace of the WMI repository.</span></span> <span data-ttu-id="6574e-111">I prefissi URI contengono una specifica dello schema, ad esempio "schemas.microsoft.com/wbem/wsman/1/wmi" e un tipo specifico di risorsa, ad esempio **\_ disco logico Win32**.</span><span class="sxs-lookup"><span data-stu-id="6574e-111">URI prefixes contain a schema specification, such as "schemas.microsoft.com/wbem/wsman/1/wmi" and a specific type of resource, such as **Win32\_LogicalDisk**.</span></span> <span data-ttu-id="6574e-112">Per ulteriori informazioni sull'identificazione di un'istanza specifica di una classe WMI, vedere [gestione remota Windows e WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6574e-112">For more information about identifying a specific instance of a WMI class, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="6574e-113">Per ulteriori informazioni, vedere [prefissi URI](uri-prefixes.md).</span><span class="sxs-lookup"><span data-stu-id="6574e-113">For more information, see [URI Prefixes](uri-prefixes.md).</span></span>

## <a name="types-of-resource-uris"></a><span data-ttu-id="6574e-114">Tipi di URI di risorsa</span><span class="sxs-lookup"><span data-stu-id="6574e-114">Types of Resource URIs</span></span>

<span data-ttu-id="6574e-115">Sebbene [*Strumentazione gestione Windows (WMI)*](windows-remote-management-glossary.md) sia l'origine principale dei dati di gestione per i sistemi operativi basati su Windows, esistono anche altre origini dello schema di gestione.</span><span class="sxs-lookup"><span data-stu-id="6574e-115">While [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md) is the primary source of management data for Windows-based operating systems, other sources of management schema also exist.</span></span>

<span data-ttu-id="6574e-116">L'elenco seguente descrive diversi tipi di URI di risorsa usati da Gestione remota Windows:</span><span class="sxs-lookup"><span data-stu-id="6574e-116">The following list describes several types of resource URIs used by Windows Remote Management:</span></span>

-   <span data-ttu-id="6574e-117">URI WMI</span><span class="sxs-lookup"><span data-stu-id="6574e-117">WMI URIs</span></span>

    <span data-ttu-id="6574e-118">Questo gruppo di URI rappresenta un percorso della classe [*Common Information Model*](/windows/desktop/WmiSdk/gloss-c) che include lo spazio dei nomi e la classe.</span><span class="sxs-lookup"><span data-stu-id="6574e-118">This group of URIs represent a [*Common Information Model*](/windows/desktop/WmiSdk/gloss-c) class path which includes namespace and class.</span></span>

    <span data-ttu-id="6574e-119">Gli URI WMI possono essere usati in:</span><span class="sxs-lookup"><span data-stu-id="6574e-119">WMI URIs can be used in:</span></span>

    -   <span data-ttu-id="6574e-120">Metodi di [**sessione**](session.md)</span><span class="sxs-lookup"><span data-stu-id="6574e-120">[**Session**](session.md) methods</span></span>
    -   <span data-ttu-id="6574e-121">Metodi [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span><span class="sxs-lookup"><span data-stu-id="6574e-121">[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) methods</span></span>
    -   <span data-ttu-id="6574e-122">Metodi [**WSMan. CreateResourceLocator**](wsman-createresourcelocator.md) o [**IWSMan. CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="6574e-122">[**WSMan.CreateResourceLocator**](wsman-createresourcelocator.md) or [**IWSMan.CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator) methods</span></span>
    -   <span data-ttu-id="6574e-123">Metodi [**resourceLocator**](resourcelocator.md) o [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="6574e-123">[**ResourceLocator**](resourcelocator.md) or [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) methods</span></span>

-   <span data-ttu-id="6574e-124">URI IPMI</span><span class="sxs-lookup"><span data-stu-id="6574e-124">IPMI URIs</span></span>

    <span data-ttu-id="6574e-125">Questo gruppo di URI rappresenta gli URI standard del settore basati sulla versione CIM 2,9.</span><span class="sxs-lookup"><span data-stu-id="6574e-125">This group of URIs represent industry standard URIs based upon CIM version 2.9.</span></span> <span data-ttu-id="6574e-126">Gli URI IPMI possono essere usati nei metodi di [**sessione**](session.md) [**Get**](session-get.md), [**put**](session-put.md), [**enumerate**](session-enumerate.md) e [**Invoke**](session-invoke.md).</span><span class="sxs-lookup"><span data-stu-id="6574e-126">IPMI URIs can be used in [**Session**](session.md) methods [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate**](session-enumerate.md) , and [**Invoke**](session-invoke.md).</span></span>

    <span data-ttu-id="6574e-127">Un esempio è https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd.</span><span class="sxs-lookup"><span data-stu-id="6574e-127">An example is https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd.</span></span> <span data-ttu-id="6574e-128">Questa risorsa viene definita in base allo schema CIM [DMTF.org](https://www.dmtf.org/home) .</span><span class="sxs-lookup"><span data-stu-id="6574e-128">This resource is defined according to the [DMTF.org](https://www.dmtf.org/home) CIM schema.</span></span>

-   <span data-ttu-id="6574e-129">URI di configurazione WinRM</span><span class="sxs-lookup"><span data-stu-id="6574e-129">WinRM configuration URIs</span></span>

    <span data-ttu-id="6574e-130">Questo gruppo di URI è costituito da operazioni di configurazione per la configurazione del [*listener*](windows-remote-management-glossary.md) WinRM.</span><span class="sxs-lookup"><span data-stu-id="6574e-130">This group of URIs are configuration operations for the WinRM [*listener*](windows-remote-management-glossary.md) configuration.</span></span>

    <span data-ttu-id="6574e-131"> https://schemas.microsoft.com/wbem/wsman/1/config/listener può essere usato nei metodi di [**sessione**](session.md) [**Get**](session-get.md), [**put**](session-put.md), [**create**](session-create.md), [**Delete**](session-delete.md)ed [**enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="6574e-131">https://schemas.microsoft.com/wbem/wsman/1/config/listener can be used in [**Session**](session.md) methods [**Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**Delete**](session-delete.md), and [**Enumerate**](session-enumerate.md).</span></span>

-   <span data-ttu-id="6574e-132">URI del [*registro eventi di sistema*](windows-remote-management-glossary.md) (SEL)</span><span class="sxs-lookup"><span data-stu-id="6574e-132">[*System Event Log*](windows-remote-management-glossary.md) (SEL) URIs</span></span>

    <span data-ttu-id="6574e-133">Questo gruppo di URI sottoscrive gli eventi dell'agente di raccolta eventi dal BMC.</span><span class="sxs-lookup"><span data-stu-id="6574e-133">This group of URIs subscribes to Event Collector events from the BMC.</span></span> <span data-ttu-id="6574e-134">È possibile sottoscrivere questi eventi usando lo strumento da riga di comando **wevtutil** .</span><span class="sxs-lookup"><span data-stu-id="6574e-134">You can subscribe to these events using the **Wevtutil** command-line tool.</span></span> <span data-ttu-id="6574e-135">Per altre informazioni, vedere https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.</span><span class="sxs-lookup"><span data-stu-id="6574e-135">For more information, see https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.</span></span>

## <a name="case-sensitivity"></a><span data-ttu-id="6574e-136">Maiuscole/minuscole</span><span class="sxs-lookup"><span data-stu-id="6574e-136">Case Sensitivity</span></span>

<span data-ttu-id="6574e-137">Il [*plug-in WMI*](windows-remote-management-glossary.md) conserva il caso dell'URI della risorsa ricevuto in una richiesta.</span><span class="sxs-lookup"><span data-stu-id="6574e-137">The [*WMI plug-in*](windows-remote-management-glossary.md) preserves the case of the resource URI received in a request.</span></span> <span data-ttu-id="6574e-138">Tuttavia, per garantire l'interoperabilità con altre implementazioni del protocollo WS-Management, usare il caso corretto per la risorsa richiesta nell'URI della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6574e-138">However, to ensure interoperability with other implementations of WS-Management protocol, use the correct case for the requested resource in resource URI.</span></span> <span data-ttu-id="6574e-139">Il caso corretto è l'ortografia definita dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="6574e-139">The correct case is the spelling defined by the resource provider.</span></span>

<span data-ttu-id="6574e-140">Sebbene gli URI delle risorse non richiedano la distinzione tra maiuscole e minuscole, il [*frammento*](windows-remote-management-glossary.md) XML</span><span class="sxs-lookup"><span data-stu-id="6574e-140">While resource URIs do not require case-sensitivity, [*fragment*](windows-remote-management-glossary.md) XML does.</span></span> <span data-ttu-id="6574e-141">Un frammento specifica una sola proprietà, anziché l'intero set di proprietà per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6574e-141">A fragment specifies just one property, rather than the entire set of properties for a resource.</span></span> <span data-ttu-id="6574e-142">Nel caso di risorse WMI, la sintassi del frammento ottiene una proprietà da un'istanza di risorsa.</span><span class="sxs-lookup"><span data-stu-id="6574e-142">In the case of WMI resources, fragment syntax gets one property from a resource instance.</span></span> <span data-ttu-id="6574e-143">Ad esempio, per ottenere solo la proprietà **Version** da [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) è necessario usare un frammento.</span><span class="sxs-lookup"><span data-stu-id="6574e-143">For example, getting only the **Version** property from [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requires using a fragment.</span></span> <span data-ttu-id="6574e-144">Per ulteriori informazioni sui frammenti, vedere "aggiunta di un selettore a un oggetto ResourceLocator o IWSManResourceLocator" in [gestione remota Windows e WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="6574e-144">For more information about fragments, see "Adding a selector to a ResourceLocator or IWSManResourceLocator object" in [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="6574e-145">Secondo gli standard XML e [*XPath*](windows-remote-management-glossary.md) , il [*plug-in WMI*](windows-remote-management-glossary.md) impone la distinzione tra maiuscole e minuscole per i frammenti e il codice XML che definisce i parametri di input per un metodo.</span><span class="sxs-lookup"><span data-stu-id="6574e-145">Following XML and [*XPath*](windows-remote-management-glossary.md) standards, the [*WMI plug-in*](windows-remote-management-glossary.md) enforces case-sensitivity for fragments and XML that defines the input parameters for a method.</span></span> <span data-ttu-id="6574e-146">La distinzione tra maiuscole e minuscole è necessaria per supportare lo standard XPath 1.0/livello 1.</span><span class="sxs-lookup"><span data-stu-id="6574e-146">Case-sensitivity is required to support the XPath 1.0/Level 1 standard.</span></span> <span data-ttu-id="6574e-147">Per ottenere i dati WMI tramite WinRM, la distinzione tra maiuscole e minuscole indica che i nomi delle classi, delle proprietà e dei metodi WMI devono corrispondere al caso del nome trovato nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="6574e-147">To get WMI data through WinRM, case-sensitivity means that the names of WMI classes, properties, and methods must match the case of the name found in the WMI repository.</span></span>

<span data-ttu-id="6574e-148">Per ulteriori informazioni, vedere [sintassi XPath](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="6574e-148">For more information, see [XPath Syntax](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).</span></span>

## <a name="case-sensitivity-examples"></a><span data-ttu-id="6574e-149">Esempi di distinzione maiuscole/minuscole</span><span class="sxs-lookup"><span data-stu-id="6574e-149">Case Sensitivity Examples</span></span>

<span data-ttu-id="6574e-150">Uno script che ottiene la proprietà del **\_ descrittore di sicurezza** da un'istanza della classe del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) WMI, ad esempio, non può utilizzare il maiuscolo per i nomi nel percorso del frammento, bensì solo l'URI.</span><span class="sxs-lookup"><span data-stu-id="6574e-150">For example, a script that obtains the **SECURITY\_DESCRIPTOR** property from an instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class cannot use upper-case for the names in the fragment path, only the URI.</span></span> <span data-ttu-id="6574e-151">Il [*plug-in WMI*](windows-remote-management-glossary.md) WinRM restituisce un errore per l'esempio VBScript seguente perché il codice XML XPath fornito per **FragmentPath** non usa la combinazione di maiuscole e minuscole corretta.</span><span class="sxs-lookup"><span data-stu-id="6574e-151">The WinRM [*WMI plug-in*](windows-remote-management-glossary.md) returns an error for the following VBScript example because the XPath XML supplied for the **FragmentPath** does not use the correct case.</span></span> <span data-ttu-id="6574e-152">Nel repository WMI la classe è digitata "servizio Win32 \_ ".</span><span class="sxs-lookup"><span data-stu-id="6574e-152">In the WMI repository, the class is spelled "Win32\_Service".</span></span>


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



<span data-ttu-id="6574e-153">Nella versione seguente dello stesso esempio viene illustrato l'utilizzo corretto del caso per la classe del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) e la proprietà del **\_ descrittore di sicurezza** .</span><span class="sxs-lookup"><span data-stu-id="6574e-153">The following version of the same example shows the correct use of case for the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class and **SECURITY\_DESCRIPTOR** property.</span></span>


```VB
ResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_Service/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



## <a name="related-topics"></a><span data-ttu-id="6574e-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6574e-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6574e-155">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="6574e-155">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="6574e-156">Gestione hardware remota</span><span class="sxs-lookup"><span data-stu-id="6574e-156">Remote Hardware Management</span></span>](remote-hardware-management.md)
</dt> <dt>

[<span data-ttu-id="6574e-157">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="6574e-157">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 