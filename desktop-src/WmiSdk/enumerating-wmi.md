---
description: L'enumerazione è l'azione di spostarsi in un set di oggetti e possibilmente di modificare ogni oggetto come si fa.
ms.assetid: fe7e3259-9a7c-4f73-af30-192bbbace1b3
ms.tgt_platform: multiple
title: Enumerazione di WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94f4a1fcff06423bad9d2bf5570ec1b9705fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310374"
---
# <a name="enumerating-wmi"></a><span data-ttu-id="1a3aa-103">Enumerazione di WMI</span><span class="sxs-lookup"><span data-stu-id="1a3aa-103">Enumerating WMI</span></span>

<span data-ttu-id="1a3aa-104">L'enumerazione è l'azione di spostarsi in un set di oggetti e possibilmente di modificare ogni oggetto come si fa.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-104">Enumeration is the act of moving through a set of objects and possibly modifying each object as you do so.</span></span> <span data-ttu-id="1a3aa-105">È possibile, ad esempio, enumerare un set di oggetti [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) per trovare un numero di serie specifico.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-105">For example, you can enumerate through a set of [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) objects to find a particular serial number.</span></span> <span data-ttu-id="1a3aa-106">Si noti che, sebbene sia possibile enumerare qualsiasi oggetto, WMI restituisce solo gli oggetti a cui si ha accesso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-106">Note that although you can enumerate any object, WMI only returns objects to which you have security access.</span></span>

<span data-ttu-id="1a3aa-107">Le enumerazioni di set di dati di grandi dimensioni possono richiedere una grande quantità di risorse e peggiorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-107">Enumerations of large data sets can require a large amount of resources and degrade performance.</span></span> <span data-ttu-id="1a3aa-108">Per altre informazioni, vedere [miglioramento delle prestazioni di enumerazione](improving-enumeration-performance.md).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-108">For more information, see [Improving Enumeration Performance](improving-enumeration-performance.md).</span></span> <span data-ttu-id="1a3aa-109">È anche possibile richiedere dati con una query più specifica.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-109">You also can request data with a more specific query.</span></span> <span data-ttu-id="1a3aa-110">Per ulteriori informazioni, vedere [esecuzione di query su WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-110">For more information, see [Querying WMI](querying-wmi.md).</span></span>

<span data-ttu-id="1a3aa-111">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="1a3aa-111">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="1a3aa-112">Enumerazione di WMI tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="1a3aa-112">Enumerating WMI Using PowerShell</span></span>](#enumerating-wmi-using-powershell)
-   [<span data-ttu-id="1a3aa-113">Enumerazione di WMI mediante C# (Microsoft. Management. Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="1a3aa-113">Enumerating WMI Using C# (Microsoft.Management.Infrastructure)</span></span>](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)
-   [<span data-ttu-id="1a3aa-114">Enumerazione di WMI mediante C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="1a3aa-114">Enumerating WMI Using C# (System.Management)</span></span>](#enumerating-wmi-using-c-systemmanagement)
-   [<span data-ttu-id="1a3aa-115">Enumerazione di WMI tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="1a3aa-115">Enumerating WMI Using VBScript</span></span>](#enumerating-wmi-using-vbscript)
-   [<span data-ttu-id="1a3aa-116">Enumerazione di WMI mediante C++</span><span class="sxs-lookup"><span data-stu-id="1a3aa-116">Enumerating WMI Using C++</span></span>](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)

## <a name="enumerating-wmi-using-powershell"></a><span data-ttu-id="1a3aa-117">Enumerazione di WMI tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="1a3aa-117">Enumerating WMI Using PowerShell</span></span>

<span data-ttu-id="1a3aa-118">Se non si conosce il percorso dell'oggetto per un'istanza specifica o si vuole recuperare tutte le istanze per una classe specifica, usare [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx)con il nome della classe nel parametro *-Class* .</span><span class="sxs-lookup"><span data-stu-id="1a3aa-118">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), with the name of the class in the *-class* parameter.</span></span> <span data-ttu-id="1a3aa-119">Se si desidera utilizzare una query, è possibile utilizzare il parametro *-query* .</span><span class="sxs-lookup"><span data-stu-id="1a3aa-119">If you want to use a query, you can use the *-query* parameter.</span></span>

<span data-ttu-id="1a3aa-120">Nella procedura seguente viene descritto come enumerare le istanze di una classe usando PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-120">The following procedure describes how to enumerate the instances of a class using PowerShell.</span></span>

<span data-ttu-id="1a3aa-121">**Per enumerare le istanze di una classe usando PowerShell**</span><span class="sxs-lookup"><span data-stu-id="1a3aa-121">**To enumerate the instances of a class using PowerShell**</span></span>

1.  <span data-ttu-id="1a3aa-122">Enumerare le istanze con una chiamata al cmdlet [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1a3aa-122">Enumerate the instances with a call to [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) cmdlet.</span></span>

    <span data-ttu-id="1a3aa-123">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) restituisce una raccolta di uno o più oggetti WMI, tramite cui è possibile enumerare.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-123">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) returns a collection of one or more WMI objects, through which you can enumerate.</span></span> <span data-ttu-id="1a3aa-124">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-124">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

    <span data-ttu-id="1a3aa-125">Se si desidera recuperare un'istanza della classe WMI in un altro spazio dei nomi o in un computer diverso, specificare rispettivamente il computer e lo spazio dei nomi nei parametri *-computer* e *-namespace* .</span><span class="sxs-lookup"><span data-stu-id="1a3aa-125">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the *-computer* and *-namespace* parameters, respectively.</span></span> <span data-ttu-id="1a3aa-126">Per ulteriori informazioni, vedere [creazione di uno script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="1a3aa-127">Questa operazione funziona solo se si dispone dei privilegi di accesso appropriati.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-127">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="1a3aa-128">Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md) ed [esecuzione di operazioni con privilegi](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-128">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="1a3aa-129">Recuperare le singole istanze desiderate usando i membri della raccolta.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-129">Retrieve any individual instances you wish using the collection's members.</span></span>

<span data-ttu-id="1a3aa-130">Nell'esempio di codice seguente viene recuperata una raccolta di PowerShell, quindi viene visualizzata la proprietà Size per tutte le istanze di unità logiche nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-130">The following code example retrieves an PowerShell collection and then displays the size property for all instances of logical drives on the local computer.</span></span>


```PowerShell
$objCol = get-wmiobject -class "Win32_LogicalDisk"

# Or, alternately
#$objCol = get-wmiobject -Query "SELECT * FROM Win32_LogicalDisk"

foreach ($Drive in $objCol)
{
    if ($Drive.size -ne $null)
    { "Drive " + $Drive.deviceID + " contains " + $Drive.size + " bytes" }
    else
    { "Drive " + $Drive.deviceID + " is not available." }
}
```



## <a name="enumerating-wmi-using-c-microsoftmanagementinfrastructure"></a><span data-ttu-id="1a3aa-131">Enumerazione di WMI mediante C# (Microsoft. Management. Infrastructure)</span><span class="sxs-lookup"><span data-stu-id="1a3aa-131">Enumerating WMI Using C# (Microsoft.Management.Infrastructure)</span></span>

1.  <span data-ttu-id="1a3aa-132">Aggiungere un riferimento all'assembly di riferimento **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="1a3aa-132">Add a reference to the **Microsoft.Management.Infrastructure** reference assembly.</span></span> <span data-ttu-id="1a3aa-133">(Questo assembly viene fornito come parte di [Windows Software Development Kit (SDK) per Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx)).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-133">(This assembly ships as part of the [Windows Software Development Kit (SDK) for Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx).)</span></span>
2.  <span data-ttu-id="1a3aa-134">Aggiungere un'istruzione **using** per lo spazio dei nomi **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="1a3aa-134">Add a **using** statement for the **Microsoft.Management.Infrastructure** namespace.</span></span>

```CSharp
    using Microsoft.Management.Infrastructure;
```

    

3.  <span data-ttu-id="1a3aa-135">Creare un'istanza di un oggetto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1a3aa-135">Instantiate a [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object.</span></span> <span data-ttu-id="1a3aa-136">Il frammento di codice seguente usa il valore "localhost" standard per il metodo [**CimSession. Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1a3aa-136">The following snippet uses the standard "localhost" value for the [**CimSession.Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) method.</span></span>

```CSharp
    CimSession cimSession = CimSession.Create("localhost");
```

    

4.  <span data-ttu-id="1a3aa-137">Chiamare il metodo [**CimSession. QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) passando lo spazio dei nomi CIM desiderato e WQL da usare.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-137">Call the [**CimSession.QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) method passing the desired CIM namespace and WQL to use.</span></span> <span data-ttu-id="1a3aa-138">Il frammento di codice seguente restituisce due istanze che rappresentano due processi Windows standard in cui la proprietà Handle (che rappresenta un ID di processo o un PID) ha un valore pari a 0 o 4.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-138">The following snippet will return two instances representing two standard Windows processes where the handle property (representing a process ID, or PID) has a value of either 0 or 4.</span></span>

```CSharp
    IEnumerable<CimInstance> queryInstances =     
      cimSession.QueryInstances(@"root\cimv2", 
                                "WQL", 
                                @"select name from win32_process where handle = 0 or handle = 4");
```

    

5.  <span data-ttu-id="1a3aa-139">Scorrere gli oggetti [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) restituiti.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-139">Loop through the returned [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) objects.</span></span>

```CSharp
    foreach (CimInstance cimInstance in enumeratedInstances)
    { 
      Console.WriteLine("Process name: {0}", cimInstance.CimInstanceProperties["Name"].Value);  
    }
```

    

<span data-ttu-id="1a3aa-140">Nell'esempio di codice seguente vengono enumerate tutte le istanze della classe di [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) (che rappresenta processi attivi) nel computer locale e viene stampato il nome di ogni processo.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-140">The following code sample enumerates all instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class (which represents active processes) on the local machine, and prints the name of each process.</span></span>

> [!Note]  
> <span data-ttu-id="1a3aa-141">In un'applicazione reale si definiscono come parametri il nome del computer ("localhost") e lo spazio dei nomi CIM ("root \\ cimv2").</span><span class="sxs-lookup"><span data-stu-id="1a3aa-141">In a real application you would define as parameters the computer name ("localhost") and CIM namespace ("root\\cimv2").</span></span> <span data-ttu-id="1a3aa-142">Per motivi di semplicità, in questo esempio sono stati impostati come hardcoded.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-142">For purposes of simplicity, these have been hardcoded in this example.</span></span>

 


```CSharp
using System;
using System.Collections.Generic;
using Microsoft.Management.Infrastructure;

public partial class MI
{
    static void PrintCimInstance(CimInstance cimInstance)
    {
        Console.ForegroundColor = ConsoleColor.Blue;
        Console.WriteLine("{0} properties", cimInstance.CimSystemProperties.ClassName);
        Console.ResetColor();

        Console.WriteLine(String.Format("{0,-5}{1,-30}{2,-15}{3,-10}", 
                                        "Key?", "Property", "Type", "Value"));

        foreach (var enumeratedProperty in cimInstance.CimInstanceProperties)
        {
            bool isKey = ((enumeratedProperty.Flags & CimFlags.Key) == CimFlags.Key);

            if (enumeratedProperty.Value != null)
            {
                Console.WriteLine(
                    "{0,-5}{1,-30}{2,-15}{3,-10}",
                    isKey == true ? "Y" : string.Empty,
                    enumeratedProperty.Name,
                    enumeratedProperty.CimType,
                    enumeratedProperty.Value);
            }
        }
        Console.WriteLine();
    }

    public static void QueryInstance(string query)
    {
        try
        {
            CimSession cimSession = CimSession.Create("localhost");

            IEnumerable<CimInstance> queryInstances = 
              cimSession.QueryInstances(@"root\cimv2", "WQL", query);
            foreach (CimInstance cimInstance in queryInstances)
            {
                //Use the current instance. This example prints the instance. 
                PrintCimInstance(cimInstance);
            }
        }
         catch (CimException ex) 
        { 
            // Handle the exception as appropriate.
            // This example prints the message.
            Console.WriteLine(ex.Message); 
        }
    }
}
```


```CSharp

using System;

namespace MIClientManaged
{
    class Program
    {
        static void Main(string[] args)
        {
            while (true)
            {
                Console.Write(&quot;Enter WQL (x = Quit): &quot;);
                string query = Console.ReadLine().ToUpper();
                if (query.CompareTo(&quot;X&quot;) == 0) break;
                MI.QueryInstance(query);
            }
        }
    }
}
```





## <a name="enumerating-wmi-using-c-systemmanagement"></a><span data-ttu-id="1a3aa-143">Enumerazione di WMI mediante C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="1a3aa-143">Enumerating WMI Using C# (System.Management)</span></span>

<span data-ttu-id="1a3aa-144">Se non si conosce il percorso dell'oggetto per un'istanza specifica o si desidera recuperare tutte le istanze per una classe specifica, utilizzare l'oggetto [ManagementClass](/dotnet/api/system.management.managementclass) per recuperare un [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) contenente tutte le istanze di una determinata classe nello spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-144">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use the [ManagementClass](/dotnet/api/system.management.managementclass) object to retrieve a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) that contains all instances of a given class in the WMI namespace.</span></span> <span data-ttu-id="1a3aa-145">In alternativa, è possibile eseguire una query WMI tramite un [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) per ottenere lo stesso set di oggetti.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-145">Alternately, you can query WMI through a [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) to obtain the same set of objects.</span></span>

> [!Note]  
> <span data-ttu-id="1a3aa-146">**System. Management** era lo spazio dei nomi .NET originale utilizzato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate rispetto alle controparti **Microsoft. Management. Infrastructure** più moderne.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-146">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="1a3aa-147">Nella procedura riportata di seguito viene descritto come enumerare le istanze di una classe utilizzando C#.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-147">The following procedure describes how to enumerate the instances of a class using C#.</span></span>

<span data-ttu-id="1a3aa-148">**Per enumerare le istanze di una classe utilizzando C #**</span><span class="sxs-lookup"><span data-stu-id="1a3aa-148">**To enumerate the instances of a class using C#**</span></span>

1.  <span data-ttu-id="1a3aa-149">Enumerare le istanze con una chiamata a [ManagementClass. GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-149">Enumerate the instances with a call to [ManagementClass.GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).</span></span>

    <span data-ttu-id="1a3aa-150">Il metodo [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) restituisce una raccolta o un set di oggetti tramite cui è possibile eseguire l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-150">The [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) method returns a collection, or set, of objects through which you can enumerate.</span></span> <span data-ttu-id="1a3aa-151">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-151">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="1a3aa-152">La raccolta restituita è in realtà un oggetto [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) , pertanto è possibile chiamare qualsiasi metodo di tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-152">The returned collection is actually an [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) object, so any of the methods of that object can be called.</span></span>

    <span data-ttu-id="1a3aa-153">Se si desidera recuperare un'istanza della classe WMI in un altro spazio dei nomi o in un computer diverso, specificare il computer e lo spazio dei nomi nel parametro *path* .</span><span class="sxs-lookup"><span data-stu-id="1a3aa-153">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the *path* parameter.</span></span> <span data-ttu-id="1a3aa-154">Per ulteriori informazioni, vedere [creazione di uno script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-154">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="1a3aa-155">Questa operazione funziona solo se si dispone dei privilegi di accesso appropriati.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-155">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="1a3aa-156">Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md) ed [esecuzione di operazioni con privilegi](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-156">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="1a3aa-157">Recuperare le singole istanze desiderate usando i membri della raccolta.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-157">Retrieve any individual instances you wish using the collection's members.</span></span>

<span data-ttu-id="1a3aa-158">Nell'esempio di codice seguente viene recuperata una raccolta C# e quindi viene visualizzata la proprietà Size per tutte le istanze di unità logiche nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-158">The following code example retrieves an C# collection and then displays the size property for all instances of logical drives on the local computer.</span></span>


```PowerShell
using System.Management;
...

ManagementClass mc = new ManagementClass("Win32_LogicalDisk");
ManagementObjectCollection objCol = mc.GetInstances();

//or, alternately
//ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
//ManagementObjectCollection objCol = mgmtObjSearcher.Get();

if (objCol.Count != 0)
{
   foreach (ManagementObject Drive in objCol)
   {
      if (Drive["size"] != null)
      {
         Console.WriteLine("Drive {0} contains {1} bytes.", Drive["deviceID"], Drive["size"]);
      }
      else
      {
         Console.WriteLine("Drive {0} is not available.", Drive["deviceID"]);
      }
   }
}
Console.ReadLine();
```



## <a name="enumerating-wmi-using-vbscript"></a><span data-ttu-id="1a3aa-159">Enumerazione di WMI tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="1a3aa-159">Enumerating WMI Using VBScript</span></span>

<span data-ttu-id="1a3aa-160">Se non si conosce il percorso dell'oggetto per un'istanza specifica o si desidera recuperare tutte le istanze per una classe specifica, utilizzare il metodo [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) per restituire un'enumerazione [**SWbemObjectSet**](swbemobjectset.md) di tutte le istanze di una classe.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-160">If you do not know the object path for a specific instance, or you want to retrieve all the instances for a specific class, use the [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) method to return an [**SWbemObjectSet**](swbemobjectset.md) enumeration of all the instances of a class.</span></span> <span data-ttu-id="1a3aa-161">In alternativa, è possibile eseguire una query WMI tramite [**SWbemServices.ExecQuery**](swbemservices-execquery.md) per ottenere lo stesso set di oggetti.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-161">Alternatively you can query WMI through [**SWbemServices.ExecQuery**](swbemservices-execquery.md) to obtain the same set of objects.</span></span>

<span data-ttu-id="1a3aa-162">Nella procedura riportata di seguito viene descritto come enumerare le istanze di una classe utilizzando VBScript.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-162">The following procedure describes how to enumerate the instances of a class using VBScript.</span></span>

<span data-ttu-id="1a3aa-163">**Per enumerare le istanze di una classe tramite VBScript**</span><span class="sxs-lookup"><span data-stu-id="1a3aa-163">**To enumerate the instances of a class using VBScript**</span></span>

1.  <span data-ttu-id="1a3aa-164">Enumerare le istanze con una chiamata al metodo [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) .</span><span class="sxs-lookup"><span data-stu-id="1a3aa-164">Enumerate the instances with a call to the [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) method.</span></span>

    <span data-ttu-id="1a3aa-165">Il metodo [**InstancesOf**](swbemservices-instancesof.md) restituisce una raccolta o un set di oggetti tramite i quali è possibile enumerare.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-165">The [**InstancesOf**](swbemservices-instancesof.md) method returns a collection, or set, of objects through which you can enumerate.</span></span> <span data-ttu-id="1a3aa-166">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-166">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="1a3aa-167">La raccolta restituita è in realtà un oggetto [**SWbemObjectSet**](swbemobjectset.md) , pertanto è possibile chiamare qualsiasi metodo di tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-167">The returned collection is actually an [**SWbemObjectSet**](swbemobjectset.md) object, so any of the methods of that object can be called.</span></span>

    <span data-ttu-id="1a3aa-168">Se si desidera recuperare un'istanza della classe WMI in un altro spazio dei nomi o in un computer diverso, specificare il computer e lo spazio dei nomi nel moniker.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-168">If you wish to retrieve a WMI class instance in another namespace or on a different computer, specify the computer and namespace in the moniker.</span></span> <span data-ttu-id="1a3aa-169">Per ulteriori informazioni, vedere [creazione di uno script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-169">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span> <span data-ttu-id="1a3aa-170">Questa operazione funziona solo se si dispone dei privilegi di accesso appropriati.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-170">This only works if you have the appropriate access privileges.</span></span> <span data-ttu-id="1a3aa-171">Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md) ed [esecuzione di operazioni con privilegi](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-171">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

2.  <span data-ttu-id="1a3aa-172">Recuperare le singole istanze desiderate utilizzando i metodi Collections.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-172">Retrieve any individual instances you wish using the collections methods.</span></span>

<span data-ttu-id="1a3aa-173">Nell'esempio di codice seguente viene recuperato un oggetto [**SWbemServices**](swbemservices.md) , quindi viene eseguito il metodo [**InstancesOf**](swbemservices-instancesof.md) per visualizzare la proprietà Size per tutte le istanze di unità logiche nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-173">The following code example retrieves an [**SWbemServices**](swbemservices.md) object and then executes the [**InstancesOf**](swbemservices-instancesof.md) method to display the size property for all instances of logical drives on the local computer.</span></span>


```VB
Set objCol = GetObject("WinMgmts:").InstancesOf("Win32_LogicalDisk")
For Each Drive In objCol
    If Not IsNull(Drive.Size) Then    
       WScript.Echo ("Drive " & Drive.deviceid & " contains " & Drive.Size & " bytes")
    Else
       WScript.Echo ("Drive " & Drive.deviceid & " is not available.")
    End If
Next
```



## <a name="enumerating-wmi-using-c"></a><span data-ttu-id="1a3aa-174">Enumerazione di WMI mediante C++</span><span class="sxs-lookup"><span data-stu-id="1a3aa-174">Enumerating WMI Using C++</span></span>

<span data-ttu-id="1a3aa-175">Oltre a eseguire l'enumerazione di base, è possibile impostare diversi flag e proprietà per aumentare le prestazioni dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-175">In addition to performing basic enumeration, you can set several flags and properties to increase the performance of your enumeration.</span></span> <span data-ttu-id="1a3aa-176">Per altre informazioni, vedere [miglioramento delle prestazioni di enumerazione](improving-enumeration-performance.md).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-176">For more information, see [Improving Enumeration Performance](improving-enumeration-performance.md).</span></span>

<span data-ttu-id="1a3aa-177">**Per enumerare un set di oggetti in WMI**</span><span class="sxs-lookup"><span data-stu-id="1a3aa-177">**To enumerate an object set in WMI**</span></span>

1.  <span data-ttu-id="1a3aa-178">Creare un'interfaccia [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) che descrive il set di oggetti che si desidera enumerare.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-178">Create an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface describing the set of objects you wish to enumerate.</span></span>

    <span data-ttu-id="1a3aa-179">Un oggetto [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) contiene un elenco che descrive un set di oggetti WMI.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-179">An [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) object contains a list describing a set of WMI objects.</span></span> <span data-ttu-id="1a3aa-180">È possibile utilizzare i metodi **IEnumWbemClassObject** per enumerare gli inoltri, ignorare gli oggetti, iniziare dall'inizio e copiare l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-180">You can use the **IEnumWbemClassObject** methods to enumerate forwards, skip objects, begin at the beginning, and copy the enumerator.</span></span> <span data-ttu-id="1a3aa-181">Nella tabella seguente sono elencati i metodi utilizzati per creare gli enumeratori per i diversi tipi di oggetti WMI.</span><span class="sxs-lookup"><span data-stu-id="1a3aa-181">The following table lists the methods use to create enumerators for different types of WMI objects.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="1a3aa-182">Oggetto</span><span class="sxs-lookup"><span data-stu-id="1a3aa-182">Object</span></span></th>
    <th><span data-ttu-id="1a3aa-183">Metodo</span><span class="sxs-lookup"><span data-stu-id="1a3aa-183">Method</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="1a3aa-184">Classe</span><span class="sxs-lookup"><span data-stu-id="1a3aa-184">Class</span></span></td>
    <td><dl><span data-ttu-id="1a3aa-185"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices:: CreateClassEnum</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a3aa-185"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices::CreateClassEnum</strong></a></span></span><br />
<span data-ttu-id="1a3aa-186">[<strong>IWbemServices:: CreateClassEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)</span><span class="sxs-lookup"><span data-stu-id="1a3aa-186">[<strong>IWbemServices::CreateClassEnumAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="1a3aa-187">Istanza</span><span class="sxs-lookup"><span data-stu-id="1a3aa-187">Instance</span></span></td>
    <td><dl><span data-ttu-id="1a3aa-188"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices:: CreateInstanceEnum</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a3aa-188"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices::CreateInstanceEnum</strong></a></span></span><br />
<span data-ttu-id="1a3aa-189">[<strong>IWbemServices:: CreateInstanceEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)</span><span class="sxs-lookup"><span data-stu-id="1a3aa-189">[<strong>IWbemServices::CreateInstanceEnumAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="1a3aa-190">Risultato della query</span><span class="sxs-lookup"><span data-stu-id="1a3aa-190">Query result</span></span></td>
    <td><dl><span data-ttu-id="1a3aa-191"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices:: ExecQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a3aa-191"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices::ExecQuery</strong></a></span></span><br />
<span data-ttu-id="1a3aa-192">[<strong>IWbemServices:: ExecQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)</span><span class="sxs-lookup"><span data-stu-id="1a3aa-192">[<strong>IWbemServices::ExecQueryAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)</span></span><br />
    </dl></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="1a3aa-193">Notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="1a3aa-193">Event notification</span></span></td>
    <td><dl><span data-ttu-id="1a3aa-194"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices:: ExecNotificationQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a3aa-194"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices::ExecNotificationQuery</strong></a></span></span><br />
<span data-ttu-id="1a3aa-195">[<strong>IWbemServices:: ExecNotificationQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)</span><span class="sxs-lookup"><span data-stu-id="1a3aa-195">[<strong>IWbemServices::ExecNotificationQueryAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)</span></span><br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  <span data-ttu-id="1a3aa-196">Scorrere l'enumerazione restituita utilizzando più chiamate a [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) o [**IEnumWbemClassObject:: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-196">Traverse through the returned enumeration using multiple calls to [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) or [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).</span></span>

<span data-ttu-id="1a3aa-197">Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="1a3aa-197">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 
