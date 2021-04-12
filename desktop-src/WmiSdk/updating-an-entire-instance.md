---
description: Il metodo più comune per aggiornare un'istanza di una classe WMI consiste nell'aggiornare l'intera istanza in una sola volta.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Aggiornamento di un'intera istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b334d1d89a7e936e2c9d80aebfbeecb430bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232619"
---
# <a name="updating-an-entire-instance"></a><span data-ttu-id="f6d17-103">Aggiornamento di un'intera istanza</span><span class="sxs-lookup"><span data-stu-id="f6d17-103">Updating an Entire Instance</span></span>

<span data-ttu-id="f6d17-104">Il metodo più comune per aggiornare un'istanza di una classe WMI consiste nell'aggiornare l'intera istanza in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="f6d17-104">The most common means of updating a WMI class instance is to update the entire instance at once.</span></span> <span data-ttu-id="f6d17-105">Tramite l'aggiornamento di un'intera istanza di, non è necessario che WMI analizzi l'istanza in singole proprietà e le invii all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6d17-105">By updating an entire instance, WMI does not have to parse the instance into individual properties and send them to your application.</span></span> <span data-ttu-id="f6d17-106">In alternativa, WMI può semplicemente inviare l'intera istanza.</span><span class="sxs-lookup"><span data-stu-id="f6d17-106">Instead, WMI can simply send you the entire instance.</span></span> <span data-ttu-id="f6d17-107">Al termine, WMI potrà quindi copiare l'intera istanza modificata sull'istanza originale.</span><span class="sxs-lookup"><span data-stu-id="f6d17-107">When you finish, WMI can then copy your entire changed instance over the original instance.</span></span>

<span data-ttu-id="f6d17-108">Nella procedura seguente viene descritto come modificare o aggiornare un'istanza di mediante PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f6d17-108">The following procedure describes how to modify or update an instance using PowerShell.</span></span>

<span data-ttu-id="f6d17-109">**Per modificare o aggiornare un'istanza tramite PowerShell**</span><span class="sxs-lookup"><span data-stu-id="f6d17-109">**To modify or update an instance using PowerShell**</span></span>

1.  <span data-ttu-id="f6d17-110">Recuperare una copia locale dell'oggetto con una chiamata a Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="f6d17-110">Retrieve a local copy of the object with a call to Get-WmiObject.</span></span>

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  <span data-ttu-id="f6d17-111">Se necessario, visualizzare le proprietà dell'oggetto con una chiamata alla raccolta Properties.</span><span class="sxs-lookup"><span data-stu-id="f6d17-111">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="f6d17-112">Sebbene non sia obbligatorio, è possibile che si desideri ottenere informazioni sul valore della proprietà prima di modificarla.</span><span class="sxs-lookup"><span data-stu-id="f6d17-112">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  <span data-ttu-id="f6d17-113">Apportare tutte le modifiche alle proprietà dell'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="f6d17-113">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="f6d17-114">In questo modo viene modificata solo la copia locale.</span><span class="sxs-lookup"><span data-stu-id="f6d17-114">Doing so changes only the local copy.</span></span> <span data-ttu-id="f6d17-115">Per salvare le modifiche in WMI, è necessario ricollocare l'intera copia nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="f6d17-115">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  <span data-ttu-id="f6d17-116">Posizionare nuovamente l'oggetto nel repository WMI utilizzando una chiamata al metodo Put.</span><span class="sxs-lookup"><span data-stu-id="f6d17-116">Place the object back into the WMI repository using a call to the Put method.</span></span>

    ```PowerShell
    $mySettings.Put()
    ```

    

<span data-ttu-id="f6d17-117">Nella procedura riportata di seguito viene descritto come modificare o aggiornare un'istanza di utilizzando C#.</span><span class="sxs-lookup"><span data-stu-id="f6d17-117">The following procedure describes how to modify or update an instance using C#.</span></span>

<span data-ttu-id="f6d17-118">**Per modificare o aggiornare un'istanza di utilizzando C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="f6d17-118">**To modify or update an instance using C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="f6d17-119">Recuperare una copia locale dell'oggetto con una chiamata a [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), come descritto in [recupero di un'istanza di WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="f6d17-119">Retrieve a local copy of the object with a call to [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), as described in [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "win32_logicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));

    CimSession session = CimSession.Create("localhost");
    CimInstance myDisk = session.GetInstance(Namespace, diskDrive);
    ```

    

2.  <span data-ttu-id="f6d17-120">Se necessario, visualizzare le proprietà dell'oggetto con una chiamata alla raccolta Properties.</span><span class="sxs-lookup"><span data-stu-id="f6d17-120">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="f6d17-121">Sebbene non sia obbligatorio, è possibile che si desideri ottenere informazioni sul valore della proprietà prima di modificarla.</span><span class="sxs-lookup"><span data-stu-id="f6d17-121">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  <span data-ttu-id="f6d17-122">Apportare tutte le modifiche alle proprietà dell'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="f6d17-122">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="f6d17-123">In questo modo viene modificata solo la copia locale.</span><span class="sxs-lookup"><span data-stu-id="f6d17-123">Doing so changes only the local copy.</span></span> <span data-ttu-id="f6d17-124">Per salvare le modifiche in WMI, è necessario ricollocare l'intera copia nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="f6d17-124">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  <span data-ttu-id="f6d17-125">Posizionare nuovamente l'oggetto nel repository WMI utilizzando una chiamata a [CimSession. ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6d17-125">Place the object back into the WMI repository using a call to [CimSession.ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).</span></span>

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

<span data-ttu-id="f6d17-126">Nella procedura seguente viene descritto come modificare o aggiornare un'istanza di mediante PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f6d17-126">The following procedure describes how to modify or update an instance using PowerShell.</span></span>

> [!Note]  
> <span data-ttu-id="f6d17-127">**System. Management** era lo spazio dei nomi .NET originale utilizzato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate rispetto alle controparti **Microsoft. Management. Infrastructure** più moderne.</span><span class="sxs-lookup"><span data-stu-id="f6d17-127">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="f6d17-128">**Per modificare o aggiornare un'istanza di utilizzando C# (Microsoft. Management)**</span><span class="sxs-lookup"><span data-stu-id="f6d17-128">**To modify or update an instance using C# (Microsoft.Management)**</span></span>

1.  <span data-ttu-id="f6d17-129">Recuperare una copia locale dell'oggetto con una chiamata a [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span><span class="sxs-lookup"><span data-stu-id="f6d17-129">Retrieve a local copy of the object with a call to [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  <span data-ttu-id="f6d17-130">Se necessario, visualizzare le proprietà dell'oggetto con una chiamata alla raccolta Properties.</span><span class="sxs-lookup"><span data-stu-id="f6d17-130">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="f6d17-131">Sebbene non sia obbligatorio, è possibile che si desideri ottenere informazioni sul valore della proprietà prima di modificarla.</span><span class="sxs-lookup"><span data-stu-id="f6d17-131">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  <span data-ttu-id="f6d17-132">Apportare tutte le modifiche alle proprietà dell'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="f6d17-132">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="f6d17-133">In questo modo viene modificata solo la copia locale.</span><span class="sxs-lookup"><span data-stu-id="f6d17-133">Doing so changes only the local copy.</span></span> <span data-ttu-id="f6d17-134">Per salvare le modifiche in WMI, è necessario ricollocare l'intera copia nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="f6d17-134">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  <span data-ttu-id="f6d17-135">Posizionare nuovamente l'oggetto nel repository WMI utilizzando una chiamata al metodo [ManagementObject. Put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) o.</span><span class="sxs-lookup"><span data-stu-id="f6d17-135">Place the object back into the WMI repository using a call to the [ManagementObject.Put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) or method.</span></span>

    ```CSharp
    myDisk.Put();
    ```

    

<span data-ttu-id="f6d17-136">Nella procedura riportata di seguito viene descritto come modificare o aggiornare un'istanza di utilizzando VBScript.</span><span class="sxs-lookup"><span data-stu-id="f6d17-136">The following procedure describes how to modify or update an instance using VBScript.</span></span>

<span data-ttu-id="f6d17-137">**Per modificare o aggiornare un'istanza di tramite VBScript**</span><span class="sxs-lookup"><span data-stu-id="f6d17-137">**To modify or update an instance using VBScript**</span></span>

1.  <span data-ttu-id="f6d17-138">Recuperare una copia locale dell'oggetto con una chiamata a **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="f6d17-138">Retrieve a local copy of the object with a call to **GetObject**.</span></span>
2.  <span data-ttu-id="f6d17-139">Se necessario, visualizzare le proprietà dell'oggetto con una chiamata al metodo [**Properties \_**](swbemobject-properties-.md) .</span><span class="sxs-lookup"><span data-stu-id="f6d17-139">If necessary, view the properties of the object with a call to the [**Properties\_**](swbemobject-properties-.md) method.</span></span>

    <span data-ttu-id="f6d17-140">Sebbene non sia obbligatorio, è possibile che si desideri ottenere informazioni sul valore della proprietà prima di modificarla.</span><span class="sxs-lookup"><span data-stu-id="f6d17-140">Although not required, you may wish to know the value of the property before you change it.</span></span>

3.  <span data-ttu-id="f6d17-141">Apportare tutte le modifiche alle proprietà dell'oggetto con una chiamata al metodo [**SWbemProperty. Value**](swbemproperty-value.md) .</span><span class="sxs-lookup"><span data-stu-id="f6d17-141">Make any changes to the object properties with a call to the [**SWbemProperty.Value**](swbemproperty-value.md) method.</span></span>

    <span data-ttu-id="f6d17-142">Il metodo **value** modifica solo la copia locale.</span><span class="sxs-lookup"><span data-stu-id="f6d17-142">The **Value** method changes only the local copy.</span></span> <span data-ttu-id="f6d17-143">Per salvare le modifiche in WMI, è necessario ricollocare l'intera copia nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="f6d17-143">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

4.  <span data-ttu-id="f6d17-144">Posizionare nuovamente l'oggetto nel repository WMI con una chiamata ai metodi [**SWbemObject. put \_**](swbemobject-put-.md) o [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="f6d17-144">Place the object back into the WMI repository with a call the [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md) methods.</span></span>

<span data-ttu-id="f6d17-145">Come implicano i nomi [**, \_ inserire**](swbemobject-put-.md) gli aggiornamenti in modo sincrono mentre [**PutAsync \_**](swbemobject-putasync-.md) gli aggiornamenti in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="f6d17-145">As the names imply, [**Put\_**](swbemobject-put-.md) updates synchronously while [**PutAsync\_**](swbemobject-putasync-.md) updates asynchronously.</span></span> <span data-ttu-id="f6d17-146">Entrambi i metodi vengono copiati sull'istanza originale con l'istanza modificata.</span><span class="sxs-lookup"><span data-stu-id="f6d17-146">Either method copies over the original instance with your modified instance.</span></span> <span data-ttu-id="f6d17-147">Tuttavia, per sfruttare i vantaggi dell'elaborazione asincrona, è necessario creare un oggetto [**SWbemSink**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="f6d17-147">However, to take advantage of asynchronous processing, you must create an [**SWbemSink**](swbemsink.md) object.</span></span> <span data-ttu-id="f6d17-148">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f6d17-148">For more information, see [Calling a method](calling-a-method.md).</span></span>

<span data-ttu-id="f6d17-149">Nella procedura riportata di seguito viene descritto come modificare o aggiornare un'istanza di utilizzando C++.</span><span class="sxs-lookup"><span data-stu-id="f6d17-149">The following procedure describes how to modify or update an instance using C++.</span></span>

<span data-ttu-id="f6d17-150">**Per modificare o aggiornare un'istanza di mediante C++**</span><span class="sxs-lookup"><span data-stu-id="f6d17-150">**To modify or update an instance using C++**</span></span>

1.  <span data-ttu-id="f6d17-151">Recuperare una copia locale dell'istanza con una chiamata a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="f6d17-151">Retrieve a local copy of the instance with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>
2.  <span data-ttu-id="f6d17-152">Se necessario, visualizzare le proprietà dell'oggetto con una chiamata a [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).</span><span class="sxs-lookup"><span data-stu-id="f6d17-152">If necessary, view the properties of the object with a call to [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).</span></span>

    <span data-ttu-id="f6d17-153">Sebbene non sia obbligatorio, è possibile che si desideri ottenere informazioni sul valore della proprietà prima di modificarla.</span><span class="sxs-lookup"><span data-stu-id="f6d17-153">Although not required, you may wish to know the value of the property before you change it.</span></span>

3.  <span data-ttu-id="f6d17-154">Apportare le modifiche necessarie alla copia con una chiamata a [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="f6d17-154">Make any necessary changes to the copy with a call to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="f6d17-155">Il metodo **put** modifica solo la copia locale.</span><span class="sxs-lookup"><span data-stu-id="f6d17-155">The **Put** method changes only the local copy.</span></span> <span data-ttu-id="f6d17-156">Per salvare le modifiche in WMI, è necessario ricollocare l'intera copia nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="f6d17-156">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

4.  <span data-ttu-id="f6d17-157">Inserire di nuovo la copia nel repository WMI con una chiamata al metodo [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .</span><span class="sxs-lookup"><span data-stu-id="f6d17-157">Place your copy back into the WMI repository with a call the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) methods.</span></span>

    <span data-ttu-id="f6d17-158">Come implicano i nomi, **PutInstance** viene aggiornato in modo sincrono durante la [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) degli aggiornamenti in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="f6d17-158">As the names imply, **PutInstance** updates synchronously while [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) updates asynchronously.</span></span> <span data-ttu-id="f6d17-159">Entrambi i metodi vengono copiati sull'istanza originale con l'istanza modificata.</span><span class="sxs-lookup"><span data-stu-id="f6d17-159">Either method copies over the original instance with your modified instance.</span></span> <span data-ttu-id="f6d17-160">Tuttavia, per sfruttare i vantaggi dell'elaborazione asincrona, è necessario implementare l'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="f6d17-160">However, to take advantage of asynchronous processing, you must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="f6d17-161">È necessario tenere presente che un'operazione di aggiornamento su un'istanza appartenente a una gerarchia di classi potrebbe non riuscire a causa di un errore che interessa un'altra classe della gerarchia.</span><span class="sxs-lookup"><span data-stu-id="f6d17-161">You should be aware that an update operation on an instance belonging to a class hierarchy might not succeed due to an error involving another class in the hierarchy.</span></span> <span data-ttu-id="f6d17-162">WMI chiama il metodo [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) di ogni provider responsabile per le classi da cui deriva la classe proprietaria dell'istanza originale.</span><span class="sxs-lookup"><span data-stu-id="f6d17-162">WMI calls the [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) method of each of the providers responsible for the classes from which the class owning the original instance derives.</span></span> <span data-ttu-id="f6d17-163">Se uno di questi provider ha esito negativo, la richiesta di aggiornamento originale ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f6d17-163">If any of these providers fail, the original update request fails.</span></span> <span data-ttu-id="f6d17-164">Per ulteriori informazioni, vedere la sezione Osservazioni di [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="f6d17-164">For more information, see the Remarks section of [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

<span data-ttu-id="f6d17-165">Per ulteriori informazioni, vedere [chiamata a un metodo del provider](calling-a-provider-method.md).</span><span class="sxs-lookup"><span data-stu-id="f6d17-165">For more information, see [Calling a Provider Method](calling-a-provider-method.md).</span></span>

> [!Note]  
> <span data-ttu-id="f6d17-166">Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="f6d17-166">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="f6d17-167">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f6d17-167">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 
