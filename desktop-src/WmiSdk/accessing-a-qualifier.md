---
description: Un qualificatore è un tag che fornisce ulteriori informazioni su un oggetto, un metodo o una proprietà WMI.
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: Accesso a un qualificatore WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88a5826255046bc0898dae43b9aa25ec5c7648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317575"
---
# <a name="accessing-a-wmi-qualifier"></a><span data-ttu-id="550d3-103">Accesso a un qualificatore WMI</span><span class="sxs-lookup"><span data-stu-id="550d3-103">Accessing a WMI Qualifier</span></span>

<span data-ttu-id="550d3-104">Un qualificatore è un tag che fornisce ulteriori informazioni su un oggetto, un metodo o una proprietà WMI.</span><span class="sxs-lookup"><span data-stu-id="550d3-104">A qualifier is a tag that provides more information about a WMI object, method, or property.</span></span> <span data-ttu-id="550d3-105">In alcuni casi, potrebbe essere necessario accedere ai dati archiviati in un qualificatore.</span><span class="sxs-lookup"><span data-stu-id="550d3-105">At times, you may need to access the data stored in a qualifier.</span></span> <span data-ttu-id="550d3-106">Ad esempio, un'attività comune consiste nel determinare se un provider implementa un metodo tentando di recuperare il qualificatore **implementato** per il metodo.</span><span class="sxs-lookup"><span data-stu-id="550d3-106">For example, a common task is to determine if a provider implements a method by attempting to retrieve the **Implemented** qualifier for that method.</span></span> <span data-ttu-id="550d3-107">Per ulteriori informazioni, vedere [qualificatori WMI](wmi-qualifiers.md) e [aggiunta di un qualificatore](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="550d3-107">For more information, see [WMI Qualifiers](wmi-qualifiers.md) and [Adding a Qualifier](adding-a-qualifier.md).</span></span>

<span data-ttu-id="550d3-108">È possibile recuperare i qualificatori in un oggetto WMI in PowerShell recuperando prima l'oggetto e quindi esaminando i qualificatori come per qualsiasi altra proprietà.</span><span class="sxs-lookup"><span data-stu-id="550d3-108">You can retrieve the qualifiers on a WMI object in PowerShell by first retrieving the object, and then examining the qualifiers as you would any other property.</span></span>

<span data-ttu-id="550d3-109">**Per recuperare un qualificatore usando PowerShell**</span><span class="sxs-lookup"><span data-stu-id="550d3-109">**To retrieve a qualifier using PowerShell**</span></span>

-   <span data-ttu-id="550d3-110">Recuperare l'oggetto di cui si desidera visualizzare i qualificatori utilizzando [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), quindi accedere ai qualificatori tramite la proprietà **Qualifiers** :</span><span class="sxs-lookup"><span data-stu-id="550d3-110">Retrieve the object whose qualifiers you want to view using [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), and then access the qualifiers through the **Qualifiers** property:</span></span>

    ```PowerShell
    $myDisk = get-wmiObject Win32_LogicalDisk
    $myDisk.qualifiers

    #or

    get-wmiObject Win32_LogicalDisk | format-list qualifiers

    #or

    $myDisk = get-wmiObject Win32_LogicalDisk
    foreach ($qual in $myDisk.Qualifiers)
    { $qual }
    ```

    

    <span data-ttu-id="550d3-111">Per ulteriori informazioni, vedere [recupero di un'istanza di WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="550d3-111">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="550d3-112">È possibile recuperare i qualificatori in un'istanza WMI in C# recuperando prima l'oggetto e quindi esaminando i qualificatori come raccolta.</span><span class="sxs-lookup"><span data-stu-id="550d3-112">You can retrieve the qualifiers on a WMI instance in C# by first retrieving the object, and then examining the qualifiers as a collection.</span></span>

<span data-ttu-id="550d3-113">**Per recuperare un qualificatore usando C# (Microsoft.System. Gestione**</span><span class="sxs-lookup"><span data-stu-id="550d3-113">**To retrieve a qualifier using C# (Microsoft.System.Management)**</span></span>

1.  <span data-ttu-id="550d3-114">Recuperare la classe di cui si desidera visualizzare i qualificatori creando un oggetto CimInstance, utilizzando il nome e lo spazio dei nomi della classe specificati.</span><span class="sxs-lookup"><span data-stu-id="550d3-114">Retrieve the class whose qualifiers you want to view by creating a CimInstance object, using the specified class name and namespace.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    <span data-ttu-id="550d3-115">Per ulteriori informazioni, vedere [recupero di un'istanza di WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="550d3-115">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="550d3-116">È possibile recuperare i qualificatori di classe da [CimInstance. CimClass. CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), i qualificatori di proprietà da [CimInstance. CimClass. CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))e i qualificatori di metodo da [CimInstance. CimClass. CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="550d3-116">You can retrieve the class qualifiers from the [CimInstance.CimClass.CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), the property qualifiers from [CimInstance.CimClass.CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85)), and the method qualifiers from [CimInstance.CimClass.CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).</span></span>

    ```CSharp
    Console.WriteLine("Class: " + myDrive.ToString());
    foreach (CimQualifier qualifier in myDrive.CimClass.CimClassQualifiers)
    {
       Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
    }

    foreach (CimPropertyDeclaration property in myDrive.CimClass.CimClassProperties)
    {
       Console.WriteLine(property.Name.ToString());
       foreach (CimQualifier qualifier in property.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }

    foreach (CimMethodDeclaration method in myDrive.CimClass.CimClassMethods)
    {
       Console.WriteLine(method.Name.ToString());
       foreach (CimQualifier qualifier in method.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }
    ```

    

    <span data-ttu-id="550d3-117">Per ulteriori informazioni, vedere [recupero di un'istanza di WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="550d3-117">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="550d3-118">È possibile recuperare i qualificatori in un oggetto WMI in C# recuperando prima l'oggetto e quindi esaminando i qualificatori come raccolta.</span><span class="sxs-lookup"><span data-stu-id="550d3-118">You can retrieve the qualifiers on a WMI object in C# by first retrieving the object, and then examining the qualifiers as a collection.</span></span>

> [!Note]  
> <span data-ttu-id="550d3-119">**System. Management** era lo spazio dei nomi .NET originale utilizzato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate rispetto alle controparti **Microsoft. Management. Infrastructure** più moderne.</span><span class="sxs-lookup"><span data-stu-id="550d3-119">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="550d3-120">**Per recuperare un qualificatore usando C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="550d3-120">**To retrieve a qualifier using C# (System.Management)**</span></span>

1.  <span data-ttu-id="550d3-121">Recuperare l'oggetto di cui si desidera visualizzare i qualificatori utilizzando [ManagementObject](/dotnet/api/system.management.managementobject).</span><span class="sxs-lookup"><span data-stu-id="550d3-121">Retrieve the object whose qualifiers you want to view using [ManagementObject](/dotnet/api/system.management.managementobject).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    <span data-ttu-id="550d3-122">Per ulteriori informazioni, vedere [recupero di un'istanza di WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="550d3-122">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="550d3-123">Inserire i qualificatori in un [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection)ed enumerare i valori [QualifierData](/dotnet/api/system.management.qualifierdata) .</span><span class="sxs-lookup"><span data-stu-id="550d3-123">Place the qualifiers into a [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection), and enumerate through the [QualifierData](/dotnet/api/system.management.qualifierdata) values.</span></span>

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    <span data-ttu-id="550d3-124">Per ulteriori informazioni, vedere [recupero di un'istanza di WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="550d3-124">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="550d3-125">Nella procedura riportata di seguito viene descritto come recuperare un qualificatore utilizzando VBScript.</span><span class="sxs-lookup"><span data-stu-id="550d3-125">The following procedure describes how to retrieve a qualifier using VBScript.</span></span>

<span data-ttu-id="550d3-126">**Per recuperare un qualificatore tramite VBScript**</span><span class="sxs-lookup"><span data-stu-id="550d3-126">**To retrieve a qualifier using VBScript**</span></span>

1.  <span data-ttu-id="550d3-127">Recuperare l'oggetto di cui si desidera visualizzare i qualificatori, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="550d3-127">Retrieve the object whose qualifiers you want to view, as shown in the following example:</span></span>

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    <span data-ttu-id="550d3-128">Il modo più comune per recuperare un oggetto consiste nell'usare il metodo [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) .</span><span class="sxs-lookup"><span data-stu-id="550d3-128">The most common way to retrieve an object is by using the [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method.</span></span> <span data-ttu-id="550d3-129">Per ulteriori informazioni, vedere [recupero di un'istanza di WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="550d3-129">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="550d3-130">Accedere ai qualificatori dell'oggetto tramite la proprietà [**SWbemObject. Qualifiers \_**](swbemobject-qualifiers-.md) , come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="550d3-130">Access the qualifiers of the object through the [**SWbemObject.Qualifiers\_**](swbemobject-qualifiers-.md) property, as shown in the following example:</span></span>

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

<span data-ttu-id="550d3-131">Nell'esempio di codice riportato di seguito viene descritto come accedere a tutti i qualificatori in un oggetto [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) .</span><span class="sxs-lookup"><span data-stu-id="550d3-131">The following code example describes how to access all the qualifiers on a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object.</span></span>


```VB
On Error Resume Next
Set Process = GetObject("winmgmts:Win32_Process")
WScript.Echo ""
WScript.Echo "Class name is", Process.Path_.Class

'Get the qualifiers
WScript.Echo ""
WScript.Echo "Qualifiers:"
WScript.Echo ""
for each Qualifier in Process.Qualifiers_
    WScript.Echo " " & Qualifier.Name
next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



<span data-ttu-id="550d3-132">Nella procedura riportata di seguito viene descritto come recuperare un qualificatore utilizzando C++.</span><span class="sxs-lookup"><span data-stu-id="550d3-132">The following procedure describes how to retrieve a qualifier using C++.</span></span>

<span data-ttu-id="550d3-133">**Per recuperare un qualificatore mediante C++**</span><span class="sxs-lookup"><span data-stu-id="550d3-133">**To retrieve a qualifier using C++**</span></span>

1.  <span data-ttu-id="550d3-134">Recuperare l'oggetto di cui si desidera visualizzare i qualificatori.</span><span class="sxs-lookup"><span data-stu-id="550d3-134">Retrieve the object whose qualifiers you want to view.</span></span>

    <span data-ttu-id="550d3-135">Il modo più comune per recuperare un oggetto consiste nell'usare una chiamata a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="550d3-135">The most common way to retrieve an object is by using a call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span> <span data-ttu-id="550d3-136">Per ulteriori informazioni, vedere [recupero di dati di istanze o classi WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="550d3-136">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="550d3-137">Recuperare il set di qualificatori per una determinata proprietà con una chiamata ai metodi [**IWbemClassObject:: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) o [**IWbemClassObject:: GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) .</span><span class="sxs-lookup"><span data-stu-id="550d3-137">Retrieve the qualifier set for a given property with a call to [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) or [**IWbemClassObject::GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) methods.</span></span>

3.  <span data-ttu-id="550d3-138">Accedere ai qualificatori dell'oggetto tramite l'interfaccia [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) restituita.</span><span class="sxs-lookup"><span data-stu-id="550d3-138">Access the qualifiers of the object through the returned [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="550d3-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="550d3-139">Examples</span></span>

<span data-ttu-id="550d3-140">Per ulteriori informazioni sul recupero dei qualificatori, vedere l'esempio di codice PowerShell [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) nella raccolta TechNet.</span><span class="sxs-lookup"><span data-stu-id="550d3-140">For more information on retrieving qualifiers, see the [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell code sample on the TechNet Gallery.</span></span>

 

 
