---
description: Gli script WMI possono condensare molti dei passaggi necessari in un programma C++.
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: Connessione a WMI con VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6952c42a024ebedd10d9ec8ced0bc4946d808c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883541"
---
# <a name="connecting-to-wmi-with-vbscript"></a><span data-ttu-id="a085d-103">Connessione a WMI con VBScript</span><span class="sxs-lookup"><span data-stu-id="a085d-103">Connecting to WMI with VBScript</span></span>

<span data-ttu-id="a085d-104">Gli script WMI possono condensare molti dei passaggi necessari in un programma C++.</span><span class="sxs-lookup"><span data-stu-id="a085d-104">WMI scripts can condense many of the steps required in a C++ program.</span></span> <span data-ttu-id="a085d-105">Possono connettersi a WMI, non solo tramite un oggetto [**SWbemLocator**](swbemlocator.md) , ma anche tramite il moniker "winmgmts:".</span><span class="sxs-lookup"><span data-stu-id="a085d-105">They can connect to WMI, not only through an [**SWbemLocator**](swbemlocator.md) object, but also through the moniker "winmgmts:".</span></span> <span data-ttu-id="a085d-106">Un moniker è un nome breve che individua uno spazio dei nomi, una classe o un'istanza in WMI.</span><span class="sxs-lookup"><span data-stu-id="a085d-106">A moniker is a short name that locates a namespace, class, or instance in WMI.</span></span> <span data-ttu-id="a085d-107">Il nome "winmgmts:" è il moniker WMI che indica a Windows script host di utilizzare gli oggetti WMI, si connette allo spazio dei nomi predefinito e ottiene un oggetto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="a085d-107">The name "winmgmts:" is the WMI moniker that tells the Windows Script Host to use the WMI objects, connects to the default namespace, and obtains an [**SWbemServices**](swbemservices.md) object.</span></span> <span data-ttu-id="a085d-108">Altre informazioni di connessione, ad esempio un livello di rappresentazione o una classe o un'istanza specifica, vengono visualizzate nella stringa che segue il nome del moniker.</span><span class="sxs-lookup"><span data-stu-id="a085d-108">Other connection information, such as an impersonation level or a specific class or instance, appears in the string following the moniker name.</span></span> <span data-ttu-id="a085d-109">È possibile utilizzare i moniker nelle chiamate che consentono di creare o ottenere oggetti WMI.</span><span class="sxs-lookup"><span data-stu-id="a085d-109">You can use monikers in calls that either create or get WMI objects.</span></span> <span data-ttu-id="a085d-110">Per ulteriori informazioni, vedere [creazione di una stringa di moniker](constructing-a-moniker-string.md).</span><span class="sxs-lookup"><span data-stu-id="a085d-110">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>

<span data-ttu-id="a085d-111">Nella procedura seguente viene descritto come connettersi a WMI utilizzando **SWbemLocator**.</span><span class="sxs-lookup"><span data-stu-id="a085d-111">The following procedure describes how to connect to WMI using **SWbemLocator**.</span></span>

<span data-ttu-id="a085d-112">**Per connettersi a WMI mediante SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="a085d-112">**To connect to WMI using SWbemLocator**</span></span>

1.  <span data-ttu-id="a085d-113">Recuperare un oggetto Locator con una chiamata a [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a085d-113">Retrieve a locator object with a call to [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span>

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  <span data-ttu-id="a085d-114">Accedere allo spazio dei nomi utilizzando una chiamata al metodo [**ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="a085d-114">Log on to the namespace using a call to the [**ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    <span data-ttu-id="a085d-115">Se non si specifica un computer nella chiamata a [**ConnectServer**](swbemlocator-connectserver.md), WMI si connette al computer locale.</span><span class="sxs-lookup"><span data-stu-id="a085d-115">If you do not specify a computer in the call to [**ConnectServer**](swbemlocator-connectserver.md), then WMI connects to the local computer.</span></span> <span data-ttu-id="a085d-116">Se non si specifica uno spazio dei nomi, WMI si connette allo spazio dei nomi specificato nella chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a085d-116">If you do not specify a namespace, then WMI connects to the namespace specified in the registry key.</span></span>

    <span data-ttu-id="a085d-117">**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **default namespace**</span><span class="sxs-lookup"><span data-stu-id="a085d-117">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Namespace**</span></span>

    <span data-ttu-id="a085d-118">Lo spazio dei nomi predefinito è \\ \\ CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="a085d-118">The default namespace is \\root\\cimv2.</span></span> <span data-ttu-id="a085d-119">Per ulteriori informazioni sugli spazi dei nomi, vedere [creazione di gerarchie all'interno di WMI](creating-hierarchies-within-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a085d-119">For more information about namespaces, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

3.  <span data-ttu-id="a085d-120">Impostare il livello di rappresentazione con una chiamata al metodo [**SWbemServices. Security \_**](swbemservices-security-.md) .</span><span class="sxs-lookup"><span data-stu-id="a085d-120">Set the impersonation level with a call to the [**SWbemServices.Security\_**](swbemservices-security-.md) method.</span></span>

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    <span data-ttu-id="a085d-121">Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="a085d-121">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

4.  <span data-ttu-id="a085d-122">Implementare lo scopo dello script.</span><span class="sxs-lookup"><span data-stu-id="a085d-122">Implement the purpose of your script.</span></span>

    <span data-ttu-id="a085d-123">WMI espone un'ampia gamma di oggetti di scripting che usano per accedere ai dati e modificarli attraverso la rete.</span><span class="sxs-lookup"><span data-stu-id="a085d-123">WMI exposes a variety of scripting objects that use to access and manipulate data across your network.</span></span> <span data-ttu-id="a085d-124">Per ulteriori informazioni, vedere la pagina relativa alla [modifica delle informazioni sulle classi e sulle istanze e sull'](manipulating-class-and-instance-information.md) [API di scripting per WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a085d-124">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    objService.Security_.ImpersonationLevel = 3
    Set Jobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
    i=0
    For each Job in Jobs
        i = i+1   
        WScript.Echo Job.JobId & "  " & Job.Command & VBNewLine
    Next
    If i = 0 Then
        WScript.Echo "No Jobs Scheduled with the AT command were found"
    End If
    ```

    

<span data-ttu-id="a085d-125">Nella procedura seguente viene descritto come connettersi a WMI e recuperare un oggetto utilizzando un moniker.</span><span class="sxs-lookup"><span data-stu-id="a085d-125">The following procedure describes how to connect to WMI and retrieve an object using a moniker.</span></span>

<span data-ttu-id="a085d-126">**Per connettersi a WMI e recuperare un oggetto utilizzando un moniker**</span><span class="sxs-lookup"><span data-stu-id="a085d-126">**To connect to WMI and retrieve an object using a moniker**</span></span>

1.  <span data-ttu-id="a085d-127">Chiamare [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) con un moniker nel parametro di input.</span><span class="sxs-lookup"><span data-stu-id="a085d-127">Call [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) with a moniker in the input parameter.</span></span>

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    <span data-ttu-id="a085d-128">Moiniker contiene un numero di elementi che è possibile utilizzare per connettersi a WMI:</span><span class="sxs-lookup"><span data-stu-id="a085d-128">The moiniker contains a number of elements that you can use to connect to WMI:</span></span>

    -   <span data-ttu-id="a085d-129">"Winmgmts:" indica a WSH di usare [oggetti API di scripting](scripting-api-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a085d-129">The "winmgmts:" tells WSH to use [Scripting API objects](scripting-api-objects.md).</span></span> <span data-ttu-id="a085d-130">In questo particolare esempio, WSH saprà che deve restituire un SWbemObject che descrive il primo \_ ScheduledJob Win32 nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a085d-130">In this particular example, the WSH will know that it should return an SWbemObject that describes the first Win32\_scheduledJob on the system.</span></span> <span data-ttu-id="a085d-131">Altri oggetti possibili da restituire sarebbero un oggetto SWbemCollection o [**SWbemServices**](swbemservices.md) , a seconda del moniker descritto.</span><span class="sxs-lookup"><span data-stu-id="a085d-131">Other possible objects to return would be an SWbemCollection or an [**SWbemServices**](swbemservices.md) object, depending on what the moniker described.</span></span>

    -   <span data-ttu-id="a085d-132">Facoltativamente, è possibile impostare i livelli di sicurezza per la connessione.</span><span class="sxs-lookup"><span data-stu-id="a085d-132">You can optionally set the security levels for the connection.</span></span> <span data-ttu-id="a085d-133">Si noti che, tuttavia, non è possibile impostare le informazioni sul nome e sulla password in un moniker.</span><span class="sxs-lookup"><span data-stu-id="a085d-133">Note that you cannot set name and password information in a moniker, however.</span></span> <span data-ttu-id="a085d-134">Per ulteriori informazioni, vedere [protezione dei client di scripting](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="a085d-134">For more information, see [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

    -   <span data-ttu-id="a085d-135">Facoltativamente, è possibile definire il percorso dell'oggetto WMI.</span><span class="sxs-lookup"><span data-stu-id="a085d-135">You can optionally define the path to the WMI object.</span></span> <span data-ttu-id="a085d-136">Sono inclusi il computer locale o remoto, lo spazio dei nomi, nonché il nome della classe.</span><span class="sxs-lookup"><span data-stu-id="a085d-136">This includes either the local or remote computer, the namespace, as well as the name of the class.</span></span> <span data-ttu-id="a085d-137">Per ulteriori informazioni sull'utilizzo di VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) negli script WMI, vedere [creazione di un'istanza](creating-an-instance.md) e [recupero di un'istanza di WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="a085d-137">For more information about using the VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) in WMI scripts, see [Creating an Instance](creating-an-instance.md) and [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="a085d-138">Invece di recuperare un singolo elemento o raccolta, è anche possibile scegliere di recuperare l'oggetto [**SWbemServices**](swbemservices.md) (come descritto nell'esempio precedente).</span><span class="sxs-lookup"><span data-stu-id="a085d-138">Instead of retrieving a single item or collection, you can also choose to retrieve the [**SWbemServices**](swbemservices.md) object (as described in the previous example).</span></span> <span data-ttu-id="a085d-139">Successivamente, è possibile chiamare query aggiuntive sull'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="a085d-139">Afterwards, you can then call additional queries on the returned object.</span></span>

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    <span data-ttu-id="a085d-140">Nell'esempio precedente, Impersonate, o impersonationLevel = 3, è il livello di sicurezza del processo predefinito.</span><span class="sxs-lookup"><span data-stu-id="a085d-140">In the previous example, impersonate, or impersonationLevel=3, is the default process security level.</span></span> <span data-ttu-id="a085d-141">Nell'esempio seguente non è necessario specificare questo livello di sicurezza del processo a meno che non sia necessario modificare la sicurezza del processo per **delegare**.</span><span class="sxs-lookup"><span data-stu-id="a085d-141">In the following example, it is not necessary to specify this process security level unless you need to change the process security to **delegate**.</span></span> <span data-ttu-id="a085d-142">Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="a085d-142">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a085d-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a085d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a085d-144">Creazione di script in WMI</span><span class="sxs-lookup"><span data-stu-id="a085d-144">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
