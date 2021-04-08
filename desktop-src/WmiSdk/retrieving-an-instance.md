---
description: Il recupero di un'istanza di è una delle procedure di recupero più comuni che è probabile eseguire in WMI.
ms.assetid: c3258783-ffcd-4c40-aaf2-7c65617cf9f8
ms.tgt_platform: multiple
title: Recupero di un'istanza WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdacf5fe5c86618eb84d70a5505897a94a7ace2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058266"
---
# <a name="retrieving-a-wmi-instance"></a><span data-ttu-id="2f3ca-103">Recupero di un'istanza WMI</span><span class="sxs-lookup"><span data-stu-id="2f3ca-103">Retrieving a WMI Instance</span></span>

<span data-ttu-id="2f3ca-104">Il recupero di un'istanza di è una delle procedure di recupero più comuni che è probabile eseguire in WMI.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-104">Retrieving an instance is one of the most common retrieval procedures you are likely to perform in WMI.</span></span> <span data-ttu-id="2f3ca-105">È possibile recuperare un'istanza esistente o creare una nuova istanza senza nome.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-105">You can retrieve an existing instance or create a new unnamed instance.</span></span> <span data-ttu-id="2f3ca-106">Il percorso WMI per l'istanza esistente è un parametro obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-106">The WMI path to the existing instance is a required parameter.</span></span> <span data-ttu-id="2f3ca-107">Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="2f3ca-107">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

> [!Note]  
> <span data-ttu-id="2f3ca-108">Quando si specifica un'istanza, un provider potrebbe non essere in grado di fornire un valore per determinate proprietà.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-108">When providing an instance, a provider may be unable to provide a value for certain properties.</span></span> <span data-ttu-id="2f3ca-109">Se non diversamente specificato nella descrizione della proprietà, non è possibile dedurre alcun significato da un valore vuoto.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-109">Unless otherwise stated in the property description, you cannot infer any meaning from an empty value.</span></span> <span data-ttu-id="2f3ca-110">Questo non deve essere confuso con una stringa con un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="2f3ca-110">This is not to be confused with a string which has a **NULL** value.</span></span> <span data-ttu-id="2f3ca-111">In questo caso, il valore viene popolato.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-111">In this case, the value is populated.</span></span> <span data-ttu-id="2f3ca-112">È vuoto ma ha un valore: **null**.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-112">It is empty but has a value: **NULL**.</span></span>

 

<span data-ttu-id="2f3ca-113">Recuperare una copia locale dell'istanza con una chiamata al cmdlet [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-113">Retrieve a local copy of the instance with a call to the PowerShell [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet.</span></span>

<span data-ttu-id="2f3ca-114">**Per recuperare un'istanza di una classe WMI mediante PowerShell**</span><span class="sxs-lookup"><span data-stu-id="2f3ca-114">**To retrieve an instance of a WMI class using PowerShell**</span></span>

-   <span data-ttu-id="2f3ca-115">È possibile recuperare istanze specifiche usando i parametri *-Class* e *-Filter* .</span><span class="sxs-lookup"><span data-stu-id="2f3ca-115">You can retrieve specific instances using the *-class* and *-filter* parameters.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

<span data-ttu-id="2f3ca-116">È possibile recuperare un'istanza WMI usando C# creando un oggetto di ricerca usando [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)), quindi inserendo i valori di chiave rilevanti, quindi cercando tale oggetto con una chiamata a [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2f3ca-116">You can retrieve a WMI instance using C# by creating a search object using [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)), and then filling it with the relevant key values, and then searching for that object with a [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) call.</span></span>

<span data-ttu-id="2f3ca-117">**Per recuperare un'istanza di una classe WMI utilizzando C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="2f3ca-117">**To retrieve an instance of a WMI class using C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="2f3ca-118">Utilizzando lo spazio dei nomi [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , creare un nuovo oggetto [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) con il nome e lo spazio dei nomi della classe pertinenti.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-118">Using the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace, create a new [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) object with the relevant class name and namespace.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance myDrive = new CimInstance(className, Namespace);
    ```

    

2.  <span data-ttu-id="2f3ca-119">Creare un [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) contenente il nome e il valore della proprietà chiave dell'istanza che si desidera cercare e aggiungere tale proprietà all'oggetto classe.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-119">Create a [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) that contains the name and value of the key property of the instance you wish to search for, and add that property to your class object.</span></span>

    ```CSharp
    myDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    ```

    

3.  <span data-ttu-id="2f3ca-120">Recuperare l'oggetto da WMI con una chiamata [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2f3ca-120">Retrieve the object from WMI with a [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) call.</span></span>

    ```CSharp
    CimSession mySession = CimSession.Create("localhost");
    CimInstance searchInstance = mySession.GetInstance(Namespace, myDrive);
    ```

    

<span data-ttu-id="2f3ca-121">È possibile recuperare un'istanza della classe WMI specifica o una raccolta di istanze di classi WMI usando le classi nello spazio dei nomi [System. Management](/dotnet/api/system.management) .</span><span class="sxs-lookup"><span data-stu-id="2f3ca-121">You can retrieve either a specific WMI class instance, or a collection of WMI class instances, using classes in the [System.Management](/dotnet/api/system.management) namespace.</span></span>

> [!Note]  
> <span data-ttu-id="2f3ca-122">**System. Management** era lo spazio dei nomi .NET originale utilizzato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate rispetto alle controparti **Microsoft. Management. Infrastructure** più moderne.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-122">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="2f3ca-123">**Per recuperare un'istanza di una classe WMI utilizzando C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="2f3ca-123">**To retrieve an instance of a WMI class using C# (System.Management)**</span></span>

1.  <span data-ttu-id="2f3ca-124">Recuperare una copia locale di un'istanza specifica creando un nuovo [ManagementObject](/dotnet/api/system.management.managementobject), con il nome e il valore dell'istanza specifico passati tramite il parametro *ManagementPath* .</span><span class="sxs-lookup"><span data-stu-id="2f3ca-124">Retrieve a local copy of a specific instance by creating a new [ManagementObject](/dotnet/api/system.management.managementobject), with the name and specific instance value passed in though the *ManagementPath* parameter.</span></span> <span data-ttu-id="2f3ca-125">È quindi possibile recuperare i dati dell'istanza chiamando in modo esplicito [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span><span class="sxs-lookup"><span data-stu-id="2f3ca-125">You can then retrieve the instance data by explicitly calling [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject objInst = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    objInst.Get();
    ```

    

2.  <span data-ttu-id="2f3ca-126">In alternativa, è possibile recuperare tutte le istanze di una classe WMI eseguendone la ricerca con un [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher)e quindi enumerando i [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection)restituiti.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-126">Alternately, you can retrieve all instances of a WMI class by searching for them with a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher), and then enumerating through the returned [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

    foreach (ManagementObject objDisk in colDisks)
    {
       Console.WriteLine("Device ID : {0}", objDisk["DeviceID"]);
    }

    Console.ReadLine();
    ```

    

    <span data-ttu-id="2f3ca-127">È possibile chiamare in modo implicito il metodo **Get** accedendo all'istanza.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-127">You can implicitly call the **Get** method by accessing the instance.</span></span> <span data-ttu-id="2f3ca-128">Per ulteriori informazioni, vedere [recupero di parte di un'istanza di WMI](retrieving-part-of-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="2f3ca-128">For more information, see [Retrieving Part of a WMI Instance](retrieving-part-of-an-instance.md).</span></span>

<span data-ttu-id="2f3ca-129">Recuperare una copia locale dell'istanza con una chiamata al metodo VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) .</span><span class="sxs-lookup"><span data-stu-id="2f3ca-129">Retrieve a local copy of the instance with a call to the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) method.</span></span>

<span data-ttu-id="2f3ca-130">**Per recuperare un'istanza di una classe WMI utilizzando VBScript**</span><span class="sxs-lookup"><span data-stu-id="2f3ca-130">**To retrieve an instance of a WMI class using VBScript**</span></span>

-   <span data-ttu-id="2f3ca-131">Chiamare [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) con il percorso dell'oggetto dell'istanza, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-131">Call [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) with the object path of the instance as shown in the following example.</span></span>

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk='C:'")
    ```

    

    <span data-ttu-id="2f3ca-132">Per recuperare un'istanza specifica, è necessario assegnare un nome come parte del percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-132">Retrieving a specific instance requires giving a name as part of the object path.</span></span>

<span data-ttu-id="2f3ca-133">In C++, chiamare [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="2f3ca-133">In C++, call [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="2f3ca-134">**Per recuperare un'istanza di una classe WMI mediante C++**</span><span class="sxs-lookup"><span data-stu-id="2f3ca-134">**To retrieve an instance of a WMI class using C++**</span></span>

-   <span data-ttu-id="2f3ca-135">Recuperare una copia locale dell'istanza con una chiamata a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="2f3ca-135">Retrieve a local copy of the instance with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span> <span data-ttu-id="2f3ca-136">È necessario includere il percorso WMI dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-136">The WMI path to the object must be included.</span></span>

    <span data-ttu-id="2f3ca-137">Come suggerisce il nome, [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) recupera l'istanza in modo asincrono, mentre [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) recupera l'istanza in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-137">As the name implies, [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) retrieves the instance asynchronously, while [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) retrieves the instance synchronously.</span></span> <span data-ttu-id="2f3ca-138">Se si desidera utilizzare il recupero asincrono, è necessario implementare l'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="2f3ca-138">If you want to use asynchronous retrieval, you must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="2f3ca-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="2f3ca-139">Examples</span></span>

<span data-ttu-id="2f3ca-140">Per un esempio di VBScript da utilizzare come modello per recuperare informazioni sulla classe e sull'istanza, vedere l'esempio di [script del modello WMI](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) nella raccolta TechNet.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-140">For a VBScript example to use as a template to retrieve class and instance information, see the [WMI Template Script](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) example on TechNet Gallery.</span></span> <span data-ttu-id="2f3ca-141">In questo particolare esempio viene utilizzato GetObject per recuperare il servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="2f3ca-141">This particular example uses GetObject to retrieve the WMI Service.</span></span>

 

 
