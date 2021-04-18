---
title: Gestione remota Windows e WMI
description: Gestione remota Windows può essere utilizzato per recuperare i dati esposti da Strumentazione gestione Windows.
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6942e89ea2e63ef809f3452e6ce55a493662c938
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321098"
---
# <a name="windows-remote-management-and-wmi"></a><span data-ttu-id="532a0-103">Gestione remota Windows e WMI</span><span class="sxs-lookup"><span data-stu-id="532a0-103">Windows Remote Management and WMI</span></span>

<span data-ttu-id="532a0-104">Gestione remota Windows può essere utilizzato per recuperare i dati esposti da Strumentazione gestione Windows ([WMI](/windows/desktop/WmiSdk/wmi-start-page) e [mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)).</span><span class="sxs-lookup"><span data-stu-id="532a0-104">Windows Remote Management can be used to retrieve data exposed by Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page) and [MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)).</span></span> <span data-ttu-id="532a0-105">È possibile ottenere dati WMI con script o applicazioni che utilizzano l' [API di scripting WinRM](winrm-scripting-api.md) o tramite lo strumento da riga di comando **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="532a0-105">You can obtain WMI data with scripts or applications that use the [WinRM Scripting API](winrm-scripting-api.md) or through the **Winrm** command-line tool.</span></span>

<span data-ttu-id="532a0-106">WinRM supporta la maggior parte delle classi e delle operazioni WMI note, inclusi gli oggetti incorporati.</span><span class="sxs-lookup"><span data-stu-id="532a0-106">WinRM supports most of the familiar WMI classes and operations, including embedded objects.</span></span> <span data-ttu-id="532a0-107">WinRM può utilizzare WMI per raccogliere dati sulle [*risorse*](windows-remote-management-glossary.md) o per gestire le risorse in un sistema operativo basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="532a0-107">WinRM can leverage WMI to collect data about [*resources*](windows-remote-management-glossary.md) or to manage resources on a Windows-based operating system.</span></span> <span data-ttu-id="532a0-108">Ciò significa che è possibile ottenere dati su oggetti quali dischi, schede di rete, servizi o processi nell'azienda tramite il set di [classi WMI](/windows/desktop/WmiSdk/wmi-classes)esistente.</span><span class="sxs-lookup"><span data-stu-id="532a0-108">That means that you can obtain data about objects such as disks, network adapters, services, or processes in your enterprise through the existing set of [WMI classes](/windows/desktop/WmiSdk/wmi-classes).</span></span> <span data-ttu-id="532a0-109">È inoltre possibile accedere ai dati hardware disponibili dal [provider standard IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)di WMI.</span><span class="sxs-lookup"><span data-stu-id="532a0-109">You can also access the hardware data that is available from the standard WMI [IPMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

## <a name="identifying-a-wmi-resource"></a><span data-ttu-id="532a0-110">Identificazione di una risorsa WMI</span><span class="sxs-lookup"><span data-stu-id="532a0-110">Identifying a WMI Resource</span></span>

<span data-ttu-id="532a0-111">È possibile fare riferimento a una classe WMI come [*risorsa*](windows-remote-management-glossary.md) in WinRM e nel protocollo WS-Management: un tipo di entità gestita, ad esempio un servizio o un disco.</span><span class="sxs-lookup"><span data-stu-id="532a0-111">You can reference a WMI class as a [*resource*](windows-remote-management-glossary.md) in WinRM and in the WS-Management protocol: a type of managed entity, like a service or a disk.</span></span>

<span data-ttu-id="532a0-112">Una classe o un metodo WMI viene identificato da un [*URI*](windows-remote-management-glossary.md), come qualsiasi altra risorsa quando si usa il protocollo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="532a0-112">A WMI class or method is identified by a [*URI*](windows-remote-management-glossary.md), just as any other resource is when using the WS-Management protocol.</span></span> <span data-ttu-id="532a0-113">L'URI può specificare una risorsa WMI (classe), un'azione WMI (metodo) o identificare un'istanza specifica di una classe nei [*messaggi*](windows-remote-management-glossary.md) inviati in rete.</span><span class="sxs-lookup"><span data-stu-id="532a0-113">The URI can specify a WMI resource (class), a WMI action (method), or identify a specific instance of a class in [*messages*](windows-remote-management-glossary.md) sent over a network.</span></span> <span data-ttu-id="532a0-114">Per altre informazioni, vedere [URI di risorsa](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="532a0-114">For more information, see [Resource URIs](resource-uris.md).</span></span>

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a><span data-ttu-id="532a0-115">Costruzione del prefisso URI per le classi WMI</span><span class="sxs-lookup"><span data-stu-id="532a0-115">Constructing the URI Prefix for WMI Classes</span></span>

<span data-ttu-id="532a0-116">Il prefisso URI contiene una parte fissa e lo spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="532a0-116">The URI prefix contains a fixed part and the WMI namespace.</span></span> <span data-ttu-id="532a0-117">Ad esempio, il prefisso URI in Windows Server che contiene la parte fissa del prefisso è: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` .</span><span class="sxs-lookup"><span data-stu-id="532a0-117">For example, the URI prefix in Windows Server that contains the fixed part of the prefix is: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>`.</span></span> <span data-ttu-id="532a0-118">Ciò consente di generare il prefisso URI per qualsiasi spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="532a0-118">This allows the URI prefix to be generated for any WMI namespace.</span></span> <span data-ttu-id="532a0-119">Ad esempio, per accedere allo spazio dei nomi WMI **\\ predefinito radice** , usare il prefisso URI seguente: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .</span><span class="sxs-lookup"><span data-stu-id="532a0-119">For example, to access the **root\\default** WMI namespace, use the following URI prefix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/`.</span></span>

<span data-ttu-id="532a0-120">La maggior parte delle classi WMI per la gestione si trova nello spazio dei nomi **\\ CIMV2 radice** .</span><span class="sxs-lookup"><span data-stu-id="532a0-120">The majority of the WMI classes for management are in the **root\\cimv2** namespace.</span></span> <span data-ttu-id="532a0-121">Per accedere alle classi e alle istanze nello spazio dei nomi **\\ CIMV2 radice** , usare il prefisso URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` .</span><span class="sxs-lookup"><span data-stu-id="532a0-121">To access classes and instances in **root\\cimv2** namespace, use the URI prefix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`.</span></span> <span data-ttu-id="532a0-122">Per altre informazioni, vedere [URI di risorsa](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="532a0-122">For more information, see [Resource URIs](resource-uris.md).</span></span>

## <a name="generating-a-complete-uri-for-wmi-classes"></a><span data-ttu-id="532a0-123">Generazione di un URI completo per le classi WMI</span><span class="sxs-lookup"><span data-stu-id="532a0-123">Generating a Complete URI for WMI Classes</span></span>

<span data-ttu-id="532a0-124">L'URI fornito, sia per lo strumento da riga di comando **WinRM** che per uno script, è costituito dal prefisso e dalla specifica della risorsa.</span><span class="sxs-lookup"><span data-stu-id="532a0-124">The URI that you supply, either to the **Winrm** command-line tool or to a script, consists of the prefix plus the resource specification.</span></span>

<span data-ttu-id="532a0-125">Nella procedura seguente viene descritto come generare un URI di risorsa per ottenere una classe WMI o per utilizzarla in un'operazione di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="532a0-125">The following procedure describes how to generate a resource URI either to get a WMI class or to use in an enumerate operation.</span></span>

<span data-ttu-id="532a0-126">**Per generare un URI di risorsa per una classe WMI**</span><span class="sxs-lookup"><span data-stu-id="532a0-126">**To generate a resource URI for a WMI class**</span></span>

1.  <span data-ttu-id="532a0-127">Iniziare con il prefisso che indica che è necessario utilizzare lo schema del protocollo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="532a0-127">Start with the prefix that indicates the WS-Management protocol schema should be used.</span></span>

    https://schemas.microsoft.com/wbem/wsman/1

    <span data-ttu-id="532a0-128">Il prefisso dell'URI della risorsa per le classi WMI è sempre lo stesso.</span><span class="sxs-lookup"><span data-stu-id="532a0-128">The resource URI prefix for WMI classes is always the same.</span></span> <span data-ttu-id="532a0-129">Per ulteriori informazioni, vedere [prefissi URI](uri-prefixes.md).</span><span class="sxs-lookup"><span data-stu-id="532a0-129">For more information, see [URI Prefixes](uri-prefixes.md).</span></span>

2.  <span data-ttu-id="532a0-130">Aggiungere lo spazio dei nomi WMI al prefisso.</span><span class="sxs-lookup"><span data-stu-id="532a0-130">Add the WMI namespace to the prefix.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  <span data-ttu-id="532a0-131">Aggiungere il nome della classe.</span><span class="sxs-lookup"><span data-stu-id="532a0-131">Add the class name.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  <span data-ttu-id="532a0-132">Per impostare il valore di una proprietà o per richiamare un metodo specifico, aggiungere il valore o i valori della chiave richiesti per la classe.</span><span class="sxs-lookup"><span data-stu-id="532a0-132">To set the value of a property, or to invoke a specific method, add the required key value or values for the class.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    <span data-ttu-id="532a0-133">Se si lascia vuoto il valore della chiave, non sarà possibile modificare il valore della proprietà originale.</span><span class="sxs-lookup"><span data-stu-id="532a0-133">If you leave the key value blank, you will not alter the original property value.</span></span>

    > [!Note]  
    > <span data-ttu-id="532a0-134">Se si lascia vuoto il valore della chiave, il valore della proprietà viene impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="532a0-134">Leaving the key value blank sets the property value to **NULL**.</span></span>

     

## <a name="locating-a-wmi-resource-with-winrm"></a><span data-ttu-id="532a0-135">Individuazione di una risorsa WMI con WinRM</span><span class="sxs-lookup"><span data-stu-id="532a0-135">Locating a WMI Resource with WinRM</span></span>

<span data-ttu-id="532a0-136">È possibile ottenere dati WMI tramite lo strumento da riga di comando, **WinRM** o tramite uno script Visual Basic che utilizza l' [API di scripting WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="532a0-136">You can obtain WMI data either through the command-line tool, **Winrm**, or through a Visual Basic script that uses the [WinRM Scripting API](winrm-scripting-api.md).</span></span> <span data-ttu-id="532a0-137">Non è possibile usare un [percorso WMI](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) per individuare una risorsa.</span><span class="sxs-lookup"><span data-stu-id="532a0-137">You do not use a [WMI path](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) to locate a resource.</span></span> <span data-ttu-id="532a0-138">Al contrario, è possibile convertire lo spazio dei nomi WMI e la gerarchia in un [*URI*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="532a0-138">Instead, you convert the WMI namespace and hierarchy to a [*URI*](windows-remote-management-glossary.md).</span></span>

<span data-ttu-id="532a0-139">L'URI WinRM per una classe WMI contiene due parti: il [prefisso URI](uri-prefixes.md) e la classe a cui si vuole accedere.</span><span class="sxs-lookup"><span data-stu-id="532a0-139">The WinRM URI for a WMI class contains two parts: the [URI prefix](uri-prefixes.md) and the class that you want to access.</span></span>

<span data-ttu-id="532a0-140">Ad esempio, è possibile fornire l'URI seguente al metodo [**Session. enumerate**](session-enumerate.md) per elencare tutti i servizi in un computer.</span><span class="sxs-lookup"><span data-stu-id="532a0-140">For example, the following URI can be supplied to the [**Session.Enumerate**](session-enumerate.md) method to list all the services on a computer.</span></span> <span data-ttu-id="532a0-141">Il prefisso dell'URI è `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` e la classe è [**il \_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="532a0-141">The URI prefix is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`, and the class is [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

<span data-ttu-id="532a0-142">In WMI elencare i dati per tutte le istanze di una risorsa o di una classe in diversi modi:</span><span class="sxs-lookup"><span data-stu-id="532a0-142">In WMI, list the data for all of the instances of a resource or class in several ways:</span></span>

-   <span data-ttu-id="532a0-143">Query per tutte le istanze di tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="532a0-143">A query for all the instances of that resource.</span></span>

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   <span data-ttu-id="532a0-144">Una chiamata a [**SWbemServices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) o [**SWbemObject. instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span><span class="sxs-lookup"><span data-stu-id="532a0-144">A call to [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) or [**SWbemObject.Instances\_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span></span>

    `Set colServices = InstancesOf("Win32_Service")`

<span data-ttu-id="532a0-145">In WinRM è possibile elencare tutte le istanze di una risorsa: [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="532a0-145">In WinRM, there is one way to list all of the instances of a resource: [**Session.Enumerate**](session-enumerate.md).</span></span>


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a><span data-ttu-id="532a0-146">Individuazione di un'istanza specifica di una risorsa WMI</span><span class="sxs-lookup"><span data-stu-id="532a0-146">Locating a Specific Instance of a WMI Resource</span></span>

<span data-ttu-id="532a0-147">In WMI è possibile designare una particolare istanza di una classe specificando i valori per le proprietà chiave o eseguendo una query per un'istanza che corrisponde a un elenco di valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="532a0-147">In WMI, you can designate a particular instance of a class either by specifying values for the key properties or by querying for an instance that matches a list of property values.</span></span> <span data-ttu-id="532a0-148">Le proprietà chiave hanno il [**qualificatore della chiave**](/windows/desktop/WmiSdk/key-qualifier)WMI.</span><span class="sxs-lookup"><span data-stu-id="532a0-148">Key properties have the WMI [**Key qualifier**](/windows/desktop/WmiSdk/key-qualifier).</span></span>

<span data-ttu-id="532a0-149">È possibile ottenere un'istanza specifica di una classe in diversi modi:</span><span class="sxs-lookup"><span data-stu-id="532a0-149">You can obtain a specific instance of a class in several ways:</span></span>

-   <span data-ttu-id="532a0-150">Una chiamata a [**Session. enumerate**](session-enumerate.md) con i parametri *Filter* e *dialetto* per creare una query.</span><span class="sxs-lookup"><span data-stu-id="532a0-150">A call to [**Session.Enumerate**](session-enumerate.md) with the *filter* and *dialect* parameters to create a query.</span></span>

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   <span data-ttu-id="532a0-151">Una chiamata a [**SWbemServices. Get**](/windows/desktop/WmiSdk/swbemservices-get).</span><span class="sxs-lookup"><span data-stu-id="532a0-151">A call to [**SWbemServices.Get**](/windows/desktop/WmiSdk/swbemservices-get).</span></span> <span data-ttu-id="532a0-152">Per [**Session. Get**](session-get.md), è necessario specificare uno o più valori di chiave specifici, preceduti da un punto interrogativo (?).</span><span class="sxs-lookup"><span data-stu-id="532a0-152">For [**Session.Get**](session-get.md), you must supply one or more specific key values, preceded by a question mark (?).</span></span>

    <span data-ttu-id="532a0-153">Il formato dell'URI per un'istanza specifica è `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .</span><span class="sxs-lookup"><span data-stu-id="532a0-153">The format of the URI for a specific instance is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    <span data-ttu-id="532a0-154">Una classe WMI può avere più di una chiave.</span><span class="sxs-lookup"><span data-stu-id="532a0-154">A WMI class may have more than one key.</span></span> <span data-ttu-id="532a0-155">Le coppie nome/valore chiave sono separate da un segno "+".</span><span class="sxs-lookup"><span data-stu-id="532a0-155">Key name-value pairs are separated by a "+" sign.</span></span> <span data-ttu-id="532a0-156">In tal caso, il formato è: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .</span><span class="sxs-lookup"><span data-stu-id="532a0-156">In that case, the format is: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2`.</span></span>

    <span data-ttu-id="532a0-157">La sintassi WinRM per ottenere un oggetto WMI singleton è diversa da WMI.</span><span class="sxs-lookup"><span data-stu-id="532a0-157">The WinRM syntax to obtain a singleton WMI object is different from WMI.</span></span> <span data-ttu-id="532a0-158">Un singleton è una classe WMI definita in modo che sia consentita una sola istanza.</span><span class="sxs-lookup"><span data-stu-id="532a0-158">A singleton is a WMI class defined so that only one instance is allowed.</span></span> <span data-ttu-id="532a0-159">[**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) o [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) sono esempi di una classe singleton WMI.</span><span class="sxs-lookup"><span data-stu-id="532a0-159">[**Win32\_CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) or [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) are examples of a WMI singleton class.</span></span>

    <span data-ttu-id="532a0-160">La sintassi WMI per i singleton è illustrata nell'esempio di codice VBScript seguente.</span><span class="sxs-lookup"><span data-stu-id="532a0-160">The WMI syntax for singletons is shown in the following VBScript code example.</span></span>

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    <span data-ttu-id="532a0-161">Nell'esempio seguente viene illustrata la sintassi singleton di WinRM che non utilizza "@".</span><span class="sxs-lookup"><span data-stu-id="532a0-161">The following example shows the WinRM singleton syntax which does not use "@".</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   <span data-ttu-id="532a0-162">Aggiunta di un [*selettore*](windows-remote-management-glossary.md) a un oggetto [**resourceLocator**](resourcelocator.md) o [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) .</span><span class="sxs-lookup"><span data-stu-id="532a0-162">Adding a [*selector*](windows-remote-management-glossary.md) to a [**ResourceLocator**](resourcelocator.md) or [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) object.</span></span>

    <span data-ttu-id="532a0-163">Nell'esempio di codice VBScript riportato di seguito viene illustrato come utilizzare un selettore per ottenere un'istanza specifica del [**\_ processore Win32**](/windows/desktop/CIMWin32Prov/win32-processor).</span><span class="sxs-lookup"><span data-stu-id="532a0-163">The following VBScript code example shows how to use a selector to get a specific instance of [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor).</span></span>

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a><span data-ttu-id="532a0-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="532a0-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="532a0-165">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="532a0-165">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="532a0-166">Prefissi URI</span><span class="sxs-lookup"><span data-stu-id="532a0-166">URI Prefixes</span></span>](uri-prefixes.md)
</dt> <dt>

[<span data-ttu-id="532a0-167">URI risorse</span><span class="sxs-lookup"><span data-stu-id="532a0-167">Resource URIs</span></span>](resource-uris.md)
</dt> <dt>

[<span data-ttu-id="532a0-168">Creazione di script in Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="532a0-168">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>
