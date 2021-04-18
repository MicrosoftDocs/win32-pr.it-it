---
description: Una query sincrona è una query che mantiene il controllo sul processo dell'applicazione per la durata della query.
ms.assetid: 628e9a31-7b0d-4099-bfa5-56330bb4eb6b
ms.tgt_platform: multiple
title: Richiamo di una query sincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d4bb2ff61a1c94bf7390a65d51e773ad943a45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318871"
---
# <a name="invoking-a-synchronous-query"></a><span data-ttu-id="91e8d-103">Richiamo di una query sincrona</span><span class="sxs-lookup"><span data-stu-id="91e8d-103">Invoking a Synchronous Query</span></span>

<span data-ttu-id="91e8d-104">Una query sincrona è una query che mantiene il controllo sul processo dell'applicazione per la durata della query.</span><span class="sxs-lookup"><span data-stu-id="91e8d-104">A synchronous query is a query that maintains control over the process of your application for the duration of the query.</span></span> <span data-ttu-id="91e8d-105">Una query sincrona richiede una singola chiamata di interfaccia ed è quindi più semplice di una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="91e8d-105">A synchronous query requires a single interface call, and is therefore more simple than an asynchronous call.</span></span> <span data-ttu-id="91e8d-106">Tuttavia, una query sincrona può causare il blocco dell'applicazione per query o query di grandi dimensioni in una rete.</span><span class="sxs-lookup"><span data-stu-id="91e8d-106">However, a synchronous query has the potential of locking up your application for large queries or queries over a network.</span></span>

<span data-ttu-id="91e8d-107">Nella procedura riportata di seguito viene descritto come eseguire una query di dati sincrona utilizzando PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91e8d-107">The following procedure describes how to issue a synchronous data query using PowerShell.</span></span>

<span data-ttu-id="91e8d-108">**Per eseguire una query di dati sincrona in PowerShell**</span><span class="sxs-lookup"><span data-stu-id="91e8d-108">**To issue a synchronous data query in PowerShell**</span></span>

-   <span data-ttu-id="91e8d-109">Descrivere la query a WMI utilizzando il cmdlet [Get-WMIOBJECT](https://technet.microsoft.com/library/dd315379.aspx) WMI e il parametro *-query* .</span><span class="sxs-lookup"><span data-stu-id="91e8d-109">Describe your query to WMI using the WMI [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet and the *-query* parameter.</span></span> <span data-ttu-id="91e8d-110">Tramite il cmdlet viene restituito un singolo oggetto o una raccolta di oggetti, a seconda del numero di oggetti che si adattano alla query.</span><span class="sxs-lookup"><span data-stu-id="91e8d-110">The cmdlet returns either a single object, or a collection of objects, depending on how many objects fit the query.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

<span data-ttu-id="91e8d-111">Nella procedura riportata di seguito viene descritto come eseguire una query di dati sincrona utilizzando C#.</span><span class="sxs-lookup"><span data-stu-id="91e8d-111">The following procedure describes how to issue a synchronous data query using C#.</span></span>

<span data-ttu-id="91e8d-112">**Per eseguire una query di dati sincrona in C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="91e8d-112">**To issue a synchronous data query in C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="91e8d-113">Descrivere la query a WMI usando CimSession. QueryInstances.</span><span class="sxs-lookup"><span data-stu-id="91e8d-113">Describe your query to WMI using CimSession.QueryInstances.</span></span> <span data-ttu-id="91e8d-114">Questo metodo restituisce una raccolta di oggetti CimInstance.</span><span class="sxs-lookup"><span data-stu-id="91e8d-114">This method returns a collection of CimInstance objects.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  <span data-ttu-id="91e8d-115">Usare le tecniche standard di raccolta del linguaggio C# per accedere a ogni oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="91e8d-115">Use standard C# language collection techniques to access each returned object.</span></span>

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

<span data-ttu-id="91e8d-116">Nella procedura riportata di seguito viene descritto come eseguire una query di dati sincrona utilizzando C#.</span><span class="sxs-lookup"><span data-stu-id="91e8d-116">The following procedure describes how to issue a synchronous data query using C#.</span></span>

<span data-ttu-id="91e8d-117">**Per eseguire una query di dati sincrona in C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="91e8d-117">**To issue a synchronous data query in C# (System.Management)**</span></span>

1.  <span data-ttu-id="91e8d-118">Creare la query con un oggetto [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) e recuperare le informazioni con una chiamata a [ManagementObjectSearcher. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).</span><span class="sxs-lookup"><span data-stu-id="91e8d-118">Create the query with a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) object, and retrieve the information with a call to [ManagementObjectSearcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).</span></span>

    <span data-ttu-id="91e8d-119">Questo metodo restituisce un oggetto [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) .</span><span class="sxs-lookup"><span data-stu-id="91e8d-119">This method returns a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) object.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  <span data-ttu-id="91e8d-120">Usare le tecniche standard di raccolta del linguaggio C# per accedere a ogni oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="91e8d-120">Use standard C# language collection techniques to access each returned object.</span></span>

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

<span data-ttu-id="91e8d-121">Nella procedura riportata di seguito viene descritto come eseguire una query di dati sincrona utilizzando VBScript.</span><span class="sxs-lookup"><span data-stu-id="91e8d-121">The following procedure describes how to issue a synchronous data query using VBScript.</span></span>

<span data-ttu-id="91e8d-122">**Per eseguire una query di dati sincrona in VBScript**</span><span class="sxs-lookup"><span data-stu-id="91e8d-122">**To issue a synchronous data query in VBScript**</span></span>

1.  <span data-ttu-id="91e8d-123">Descrivere la query in WMI con [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="91e8d-123">Describe your query to WMI using [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span> <span data-ttu-id="91e8d-124">Questo metodo restituisce un [**SWbemObjectSet**](swbemobjectset.md).</span><span class="sxs-lookup"><span data-stu-id="91e8d-124">This method returns an [**SWbemObjectSet**](swbemobjectset.md).</span></span>

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  <span data-ttu-id="91e8d-125">Utilizzare le tecniche standard di [raccolta](accessing-a-collection.md) del linguaggio di scripting per accedere a ogni oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="91e8d-125">Use standard scripting language [collection](accessing-a-collection.md) techniques to access each returned object.</span></span>

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

<span data-ttu-id="91e8d-126">Nella procedura riportata di seguito viene descritto come eseguire una query di dati sincrona utilizzando C++.</span><span class="sxs-lookup"><span data-stu-id="91e8d-126">The following procedure describes how to issue a synchronous data query using C++.</span></span>

<span data-ttu-id="91e8d-127">**Per eseguire una query sincrona in C++**</span><span class="sxs-lookup"><span data-stu-id="91e8d-127">**To issue a synchronous query in C++**</span></span>

1.  <span data-ttu-id="91e8d-128">Descrivere la query a WMI tramite una chiamata a [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span><span class="sxs-lookup"><span data-stu-id="91e8d-128">Describe your query to WMI through a call to [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="91e8d-129">Il metodo [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) accetta una stringa di ricerca WQL come parametro che descrive la query.</span><span class="sxs-lookup"><span data-stu-id="91e8d-129">The [**ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) method takes a WQL search string as a parameter that describes your query.</span></span> <span data-ttu-id="91e8d-130">WMI esegue la query e restituisce un puntatore di interfaccia [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="91e8d-130">WMI performs the query and returns an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface pointer.</span></span> <span data-ttu-id="91e8d-131">Tramite l'interfaccia **IEnumWbemClassObject** è possibile accedere alle classi o alle istanze che costituiscono il set di risultati.</span><span class="sxs-lookup"><span data-stu-id="91e8d-131">Through the **IEnumWbemClassObject** interface, you can access the classes or instances that make up the result set.</span></span>

2.  <span data-ttu-id="91e8d-132">Dopo aver ricevuto la query, è possibile enumerare la query con una chiamata a [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next).</span><span class="sxs-lookup"><span data-stu-id="91e8d-132">After you receive your query, you can enumerate your query with a call to [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next).</span></span> <span data-ttu-id="91e8d-133">Per ulteriori informazioni, vedere [enumerazione di WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="91e8d-133">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

    <span data-ttu-id="91e8d-134">Nell'esempio di codice seguente sono necessari i riferimenti seguenti e le \# istruzioni include per la compilazione corretta.</span><span class="sxs-lookup"><span data-stu-id="91e8d-134">The following code example requires the following references and \#include statements to compile correctly.</span></span>

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    <span data-ttu-id="91e8d-135">Nell'esempio di codice riportato di seguito viene illustrato come eseguire una query per gli oggetti che rappresentano gli utenti e i gruppi in WMI.</span><span class="sxs-lookup"><span data-stu-id="91e8d-135">The following code example describes how to query for the objects that represent the users and groups in WMI.</span></span>

    ```C++
    void ExecQuerySync(IWbemServices *pSvc)
    {
        // Query for all users and groups.

        BSTR Language = SysAllocString(L"WQL");
        BSTR Query = SysAllocString(L"SELECT * FROM __Namespace");

        // Initialize the IEnumWbemClassObject pointer.
        IEnumWbemClassObject *pEnum = 0;

        // Issue the query.
        HRESULT hRes = pSvc->ExecQuery(
            Language,
            Query,
            WBEM_FLAG_FORWARD_ONLY,         // Flags
            0,                              // Context
            &pEnum
            );

        SysFreeString(Query);
        SysFreeString(Language);

        if (hRes != 0)
        {
            printf("Error\n");
            return;
        }
        
        ULONG uTotal = 0;

        // Retrieve the objects in the result set.
        for (;;)
        {
            IWbemClassObject *pObj = 0;
            ULONG uReturned = 0;

            hRes = pEnum->Next(
                0,                  // Time out
                1,                  // One object
                &pObj,
                &uReturned
                );

            uTotal += uReturned;

            if (uReturned == 0)
                break;

            // Use the object.
            
            // ...
            
            // Release it.
            // ===========
            
            pObj->Release();    // Release objects not owned.            
        }

        // All done.
        pEnum->Release();
    }
    ```

    

 

 
