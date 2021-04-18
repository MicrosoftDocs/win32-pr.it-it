---
description: Il primo tipo di oggetto che è possibile recuperare è una classe WMI.
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: Recupero di una classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9378854eb483c6cdac7ddee47d581d8876270e97
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "106320825"
---
# <a name="retrieving-a-wmi-class"></a><span data-ttu-id="c16f9-103">Recupero di una classe WMI</span><span class="sxs-lookup"><span data-stu-id="c16f9-103">Retrieving a WMI Class</span></span>

<span data-ttu-id="c16f9-104">Il primo tipo di oggetto che è possibile recuperare è una classe WMI.</span><span class="sxs-lookup"><span data-stu-id="c16f9-104">The first type of object you can retrieve is a WMI class.</span></span> <span data-ttu-id="c16f9-105">Quando si recupera una classe WMI, si recupera effettivamente una definizione di classe, ovvero un elenco di proprietà, qualificatori e metodi che descrivono completamente la classe.</span><span class="sxs-lookup"><span data-stu-id="c16f9-105">When retrieving a WMI class, you actually retrieve a class definition, which is a listing of the properties, qualifiers, and methods that fully describe the class.</span></span> <span data-ttu-id="c16f9-106">Tuttavia, una definizione di classe è fondamentalmente la classe stessa.</span><span class="sxs-lookup"><span data-stu-id="c16f9-106">However, a class definition is basically the class itself.</span></span>

<span data-ttu-id="c16f9-107">PowerShell usa una query standard per recuperare le definizioni delle classi, usando la classe della **\_ metaclasse** .</span><span class="sxs-lookup"><span data-stu-id="c16f9-107">PowerShell uses a standard query to retrieve class definitions, using the **meta\_class** class.</span></span>

<span data-ttu-id="c16f9-108">**Per recuperare una definizione di classe in PowerShell**</span><span class="sxs-lookup"><span data-stu-id="c16f9-108">**To retrieve a class definition in PowerShell**</span></span>

-   <span data-ttu-id="c16f9-109">Usare [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) con una query per la **\_ metaclasse** con la clausola WHERE contenente il nome della classe da recuperare.</span><span class="sxs-lookup"><span data-stu-id="c16f9-109">Use the [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) with a query to **meta\_class**, with the WHERE clause containing the name of the class you with to retrieve.</span></span>

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    <span data-ttu-id="c16f9-110">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) è il cmdlet standard usato da PowerShell per recuperare le informazioni di classe e istanza da WMI.</span><span class="sxs-lookup"><span data-stu-id="c16f9-110">[Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) is the standard cmdlet PowerShell uses to retrieve class and instance information from WMI.</span></span> <span data-ttu-id="c16f9-111">La classe della **\_ metaclasse** definisce la query come query dello schema.</span><span class="sxs-lookup"><span data-stu-id="c16f9-111">The **meta\_class** class defines the query as a schema query.</span></span> <span data-ttu-id="c16f9-112">Senza la **classe \_ MetaClass** , questa query restituisce tutte le istanze di Win32 \_ disco logico.</span><span class="sxs-lookup"><span data-stu-id="c16f9-112">Without the **meta\_class** class, this query would return all instances of Win32\_LogicalDisk.</span></span> <span data-ttu-id="c16f9-113">Per ulteriori informazioni sull'esecuzione di query su WMI, vedere [istruzione SELECT per query dello schema](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="c16f9-113">For more information about querying WMI, see [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

<span data-ttu-id="c16f9-114">Il processo corrente per il recupero di una definizione WMI in C# consiste nell'usare la classe **CIMInstance** .</span><span class="sxs-lookup"><span data-stu-id="c16f9-114">The current process for retrieving a WMI definition in C# is to use **CIMInstance** class.</span></span>

<span data-ttu-id="c16f9-115">**Per recuperare una definizione di classe in C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="c16f9-115">**To retrieve a class definition in C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="c16f9-116">Utilizzando lo spazio dei nomi **Microsoft. Management. Infrastructure** , creare una classe **CIMInstance** con lo spazio dei nomi e il nome della classe specificati.</span><span class="sxs-lookup"><span data-stu-id="c16f9-116">Using the **Microsoft.Management.Infrastructure** namespace, create a **CIMInstance** class with the specified namespace and class name.</span></span>

    <span data-ttu-id="c16f9-117">La classe creata conterrà tutte le informazioni sulla classe, ma non i dati dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="c16f9-117">The created class will contain all of the class information, but no instance data.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  <span data-ttu-id="c16f9-118">In alternativa, come per PowerShell, è anche possibile eseguire una query usando il tag **meta \_ Class** come parte della query.</span><span class="sxs-lookup"><span data-stu-id="c16f9-118">Alternately, as with PowerShell, you could also perform a query, using the **meta\_class** tag as part of the query.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

<span data-ttu-id="c16f9-119">Come per PowerShell, C# usa una query di **\_ metaclasse** per recuperare le definizioni delle classi.</span><span class="sxs-lookup"><span data-stu-id="c16f9-119">As with PowerShell, C# uses a **meta\_class** query to retrieve class definitions.</span></span> <span data-ttu-id="c16f9-120">In alternativa, è possibile creare un oggetto **ManagementClass** per accedere direttamente alla definizione della classe.</span><span class="sxs-lookup"><span data-stu-id="c16f9-120">Alternately, you can create a **ManagementClass** object to access the class definition directly.</span></span>

> [!Note]  
> <span data-ttu-id="c16f9-121">**System. Management** era lo spazio dei nomi .NET originale utilizzato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate rispetto alle controparti **Microsoft. Management. Infrastructure** più moderne.</span><span class="sxs-lookup"><span data-stu-id="c16f9-121">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="c16f9-122">**Per recuperare una definizione di classe in C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="c16f9-122">**To retrieve a class definition in C# (System.Management)**</span></span>

1.  <span data-ttu-id="c16f9-123">È possibile usare [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) con una query per la **\_ metaclasse**, con la clausola WHERE contenente il nome della classe da recuperare.</span><span class="sxs-lookup"><span data-stu-id="c16f9-123">You can use the [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) with a query to **meta\_class**, with the WHERE clause containing the name of the class you with to retrieve.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    <span data-ttu-id="c16f9-124">[ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) è la classe standard utilizzata da .NET per recuperare le informazioni di classe e istanza da WMI.</span><span class="sxs-lookup"><span data-stu-id="c16f9-124">[ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) is the standard class .NET uses to retrieve class and instance information from WMI.</span></span> <span data-ttu-id="c16f9-125">[ManagementObjectSerarcher. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) restituisce un [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) che contiene la classe di definizione dello schema.</span><span class="sxs-lookup"><span data-stu-id="c16f9-125">[ManagementObjectSerarcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) returns a [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) that contains the schema definition class.</span></span> <span data-ttu-id="c16f9-126">La classe della **\_ metaclasse** definisce la query come query dello schema.</span><span class="sxs-lookup"><span data-stu-id="c16f9-126">The **meta\_class** class defines the query as a schema query.</span></span> <span data-ttu-id="c16f9-127">Senza la **classe \_ MetaClass** , questa query restituisce tutte le istanze di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="c16f9-127">Without the **meta\_class** class, this query would return all instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span> <span data-ttu-id="c16f9-128">Per ulteriori informazioni sull'esecuzione di query su WMI, vedere [istruzione SELECT per query dello schema](select-statement-for-schema-queries.md).</span><span class="sxs-lookup"><span data-stu-id="c16f9-128">For more information about querying WMI, see [SELECT Statement for Schema Queries](select-statement-for-schema-queries.md).</span></span>

2.  <span data-ttu-id="c16f9-129">In alternativa, creare un nuovo oggetto [ManagementClass](/dotnet/api/system.management.managementclass) , con il nome come percorso, per recuperare la classe.</span><span class="sxs-lookup"><span data-stu-id="c16f9-129">Alternately, create a new [ManagementClass](/dotnet/api/system.management.managementclass) object, with the name as the path, to retrieve the class.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

<span data-ttu-id="c16f9-130">È possibile recuperare una definizione di classe in VBScript in modo analogo al recupero di un'istanza specifica.</span><span class="sxs-lookup"><span data-stu-id="c16f9-130">You can retrieve a class definition in VBScript in a similar way to retrieving a specific instance.</span></span>

<span data-ttu-id="c16f9-131">**Per recuperare una definizione di classe in VBScript**</span><span class="sxs-lookup"><span data-stu-id="c16f9-131">**To retrieve a class definition in VBScript**</span></span>

1.  <span data-ttu-id="c16f9-132">Chiamare [**SWbemServices. Get**](swbemservices-get.md) ma non identificare un'istanza specifica nel percorso dell'oggetto per la classe.</span><span class="sxs-lookup"><span data-stu-id="c16f9-132">Call [**SWbemServices.Get**](swbemservices-get.md) but do not identify a specific instance in the object path for the class.</span></span>
2.  <span data-ttu-id="c16f9-133">Nell'esempio di codice seguente viene recuperata la definizione di classe per la classe che descrive le unità logiche del computer.</span><span class="sxs-lookup"><span data-stu-id="c16f9-133">The following code example retrieves the class definition for the class that describes logical drives on your computer.</span></span>

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    <span data-ttu-id="c16f9-134">Windows script host (WSH) supporta anche quanto segue.</span><span class="sxs-lookup"><span data-stu-id="c16f9-134">Windows Script Host (WSH) also supports the following.</span></span>

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    <span data-ttu-id="c16f9-135">In Active Server Pages (ASP) utilizzare [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) o [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) nello script sul lato server.</span><span class="sxs-lookup"><span data-stu-id="c16f9-135">On Active Server Pages (ASP) use [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) or [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) in the server-side script.</span></span> <span data-ttu-id="c16f9-136">Per ulteriori informazioni, vedere [creazione di Active Server pagine per WMI](creating-active-server-pages-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="c16f9-136">For more information, see [Creating Active Server Pages for WMI](creating-active-server-pages-for-wmi.md).</span></span>

3.  <span data-ttu-id="c16f9-137">È inoltre possibile specificare una classe o un'istanza, nel qual caso l'oggetto restituito è un oggetto WMI, ad esempio un'istanza di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), anziché un oggetto Services.</span><span class="sxs-lookup"><span data-stu-id="c16f9-137">A class or instance can also be specified, in which case the returned object is a WMI object, for example, an instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), rather than a services object.</span></span> <span data-ttu-id="c16f9-138">Si noti che non è possibile usare le funzioni [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) di VBScript per creare un'istanza dell'oggetto generico [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="c16f9-138">Note that you cannot use the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) functions to create an instance of the generic object [**SWbemObject**](swbemobject.md).</span></span>
4.  <span data-ttu-id="c16f9-139">Nelle pagine HTML eseguite in Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) e [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) possono avere esito negativo perché gli oggetti di script WMI, ad esempio i controlli ActiveX, non sono contrassegnati come sicuri per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="c16f9-139">In HTML pages running in Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) and [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) can fail because WMI scripting objects, like ActiveX controls, are not marked as safe for scripting.</span></span> <span data-ttu-id="c16f9-140">L'unica eccezione è rappresentata dall'oggetto [**SWbemDateTime**](swbemdatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="c16f9-140">The one exception is the [**SWbemDateTime**](swbemdatetime.md) object.</span></span> <span data-ttu-id="c16f9-141">L'unico modo in cui queste chiamate possono avere esito positivo è quando si riducono le impostazioni di sicurezza di IE, operazione sconsigliata.</span><span class="sxs-lookup"><span data-stu-id="c16f9-141">The only way that these calls can succeed is when you lower the IE security settings, which is not recommended.</span></span>

<span data-ttu-id="c16f9-142">Quando si recupera una classe in C++, chiamare la versione [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) di [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="c16f9-142">When retrieving a class in C++, call the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) version of [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="c16f9-143">**Per recuperare una definizione di classe in C++**</span><span class="sxs-lookup"><span data-stu-id="c16f9-143">**To retrieve a class definition in C++**</span></span>

1.  <span data-ttu-id="c16f9-144">Chiamare i metodi [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) per recuperare la definizione di una classe.</span><span class="sxs-lookup"><span data-stu-id="c16f9-144">Call the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods to retrieve the definition of a class.</span></span>
2.  <span data-ttu-id="c16f9-145">Una classe può avere più definizioni di classe, che in genere si verifica quando più di un provider di classi è caricato in uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="c16f9-145">One class can have multiple class definitions, which happens typically when you have more than one class provider loaded into one namespace.</span></span> <span data-ttu-id="c16f9-146">Quando una classe dispone di più definizioni di classe, WMI restituisce la prima definizione individuata e il codice di stato **\_ \_ \_ degli oggetti duplicati di WBEM** .</span><span class="sxs-lookup"><span data-stu-id="c16f9-146">When a class has multiple class definitions, WMI returns the first definition discovered and the **WBEM\_S\_DUPLICATE\_OBJECTS** status code.</span></span>

<span data-ttu-id="c16f9-147">Poiché [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) restituisce una definizione di classe, viene comunemente usato come primo passaggio nella creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="c16f9-147">Because [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) returns a class definition, it is commonly used as the first step in creating an instance.</span></span> <span data-ttu-id="c16f9-148">Per altre informazioni su come usare **GetObject**, vedere [creazione e dichiarazione di un'istanza con C++](creating-and-declaring-an-instance-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="c16f9-148">For more information on how to use **GetObject**, see [Creating and Declaring an Instance Using C++](creating-and-declaring-an-instance-using-c-.md).</span></span>

 

 
