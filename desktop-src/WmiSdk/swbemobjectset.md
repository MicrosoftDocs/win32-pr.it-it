---
description: Un oggetto SWbemObjectSet è una raccolta di oggetti SWbemObject. Per ulteriori informazioni, vedere Accesso a una raccolta. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: Oggetto SWbemObjectSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet
- ISWbemObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a6992658214d7ea5acbadbea396992edf0e3e9d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233798"
---
# <a name="swbemobjectset-object"></a><span data-ttu-id="08a85-105">Oggetto SWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="08a85-105">SWbemObjectSet object</span></span>

<span data-ttu-id="08a85-106">Un oggetto **SWbemObjectSet** è una raccolta di oggetti [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="08a85-106">An **SWbemObjectSet** object is a collection of [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="08a85-107">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="08a85-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="08a85-108">Questo oggetto non può essere creato dalla chiamata **CreateObject** di VBScript.</span><span class="sxs-lookup"><span data-stu-id="08a85-108">This object cannot be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="08a85-109">È possibile ottenere un oggetto **SWbemObjectSet** chiamando uno dei metodi seguenti o i relativi equivalenti asincroni:</span><span class="sxs-lookup"><span data-stu-id="08a85-109">You can get an **SWbemObjectSet** object by calling any of the following methods or their asynchronous equivalents:</span></span>

-   [<span data-ttu-id="08a85-110">**SWbemObject. Associator\_**</span><span class="sxs-lookup"><span data-stu-id="08a85-110">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
-   [<span data-ttu-id="08a85-111">**SWbemObject. Instances\_**</span><span class="sxs-lookup"><span data-stu-id="08a85-111">**SWbemObject.Instances\_**</span></span>](swbemobject-instances-.md)
-   [<span data-ttu-id="08a85-112">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="08a85-112">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
-   [<span data-ttu-id="08a85-113">**SWbemObject. sottoclassi\_**</span><span class="sxs-lookup"><span data-stu-id="08a85-113">**SWbemObject.Subclasses\_**</span></span>](swbemobject-subclasses-.md)
-   [<span data-ttu-id="08a85-114">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="08a85-114">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
-   [<span data-ttu-id="08a85-115">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="08a85-115">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
-   [<span data-ttu-id="08a85-116">**SWbemServices. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="08a85-116">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)
-   [<span data-ttu-id="08a85-117">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="08a85-117">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="08a85-118">**SWbemServices. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="08a85-118">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)

> [!Note]  
> <span data-ttu-id="08a85-119">L'oggetto **SWbemObjectSet** non supporta i metodi facoltativi di **aggiunta** e **rimozione** della raccolta.</span><span class="sxs-lookup"><span data-stu-id="08a85-119">The **SWbemObjectSet** object does not support the optional **Add** and **Remove** collection methods.</span></span>

 

> [!Note]  
> <span data-ttu-id="08a85-120">Poiché è possibile che la chiamata al sink non venga restituita allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="08a85-120">Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="08a85-121">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="08a85-121">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="08a85-122">Membri</span><span class="sxs-lookup"><span data-stu-id="08a85-122">Members</span></span>

<span data-ttu-id="08a85-123">L'oggetto **SWbemObjectSet** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="08a85-123">The **SWbemObjectSet** object has these types of members:</span></span>

-   [<span data-ttu-id="08a85-124">Metodi</span><span class="sxs-lookup"><span data-stu-id="08a85-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="08a85-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="08a85-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="08a85-126">Metodi</span><span class="sxs-lookup"><span data-stu-id="08a85-126">Methods</span></span>

<span data-ttu-id="08a85-127">L'oggetto **SWbemObjectSet** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="08a85-127">The **SWbemObjectSet** object has these methods.</span></span>



| <span data-ttu-id="08a85-128">Metodo</span><span class="sxs-lookup"><span data-stu-id="08a85-128">Method</span></span>                              | <span data-ttu-id="08a85-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08a85-129">Description</span></span>                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08a85-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="08a85-130">**Item**</span></span>](swbemobjectset-item.md) | <span data-ttu-id="08a85-131">Recupera un oggetto [**SWbemObject**](swbemobject.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="08a85-131">Retrieves an [**SWbemObject**](swbemobject.md) object from the collection.</span></span> <span data-ttu-id="08a85-132">Si tratta del metodo predefinito dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="08a85-132">This is the default method of the object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="08a85-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="08a85-133">Properties</span></span>

<span data-ttu-id="08a85-134">L'oggetto **SWbemObjectSet** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="08a85-134">The **SWbemObjectSet** object has these properties.</span></span>



| <span data-ttu-id="08a85-135">Proprietà</span><span class="sxs-lookup"><span data-stu-id="08a85-135">Property</span></span>                                                  | <span data-ttu-id="08a85-136">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="08a85-136">Access type</span></span>          | <span data-ttu-id="08a85-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08a85-137">Description</span></span>                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="08a85-138">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="08a85-138">**Count**</span></span>](swbemobjectset-count.md)<br/>          | <span data-ttu-id="08a85-139">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="08a85-139">Read-only</span></span><br/> | <span data-ttu-id="08a85-140">Numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="08a85-140">The number of items in the collection.</span></span><br/>        |
| [<span data-ttu-id="08a85-141">**Sicurezza\_**</span><span class="sxs-lookup"><span data-stu-id="08a85-141">**Security\_**</span></span>](swbemobjectset-security-.md)<br/> | <span data-ttu-id="08a85-142">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="08a85-142">Read-only</span></span><br/> | <span data-ttu-id="08a85-143">Utilizzato per leggere o modificare le impostazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="08a85-143">Used to read or change the security settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="08a85-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="08a85-144">Remarks</span></span>

<span data-ttu-id="08a85-145">Un **SWbemObjectSet** è una raccolta di zero o più oggetti [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="08a85-145">An **SWbemObjectSet** is a collection of zero or more [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="08a85-146">Ogni **SWbemObject** in un **SWbemObjectSet** può rappresentare uno dei due elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="08a85-146">Each **SWbemObject** in a **SWbemObjectSet** can represent one of two things:</span></span>

-   <span data-ttu-id="08a85-147">Istanza di una risorsa gestita da WMI.</span><span class="sxs-lookup"><span data-stu-id="08a85-147">An instance of a WMI-managed resource.</span></span>
-   <span data-ttu-id="08a85-148">Istanza di una definizione di classe.</span><span class="sxs-lookup"><span data-stu-id="08a85-148">An instance of a class definition.</span></span>

<span data-ttu-id="08a85-149">L'uso più comune di questa classe in WMI è come valore restituito per una chiamata a [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) o [**InstancesOf**](swbemservices-instancesof.md) , come descritto nell'esempio di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="08a85-149">The most common use of this class in WMI is as the return value for an [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) or [**InstancesOf**](swbemservices-instancesof.md) call, as described in the following code sample:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



<span data-ttu-id="08a85-150">Nella maggior parte dei casi, l'unica cosa che si può fare con un **SWbemObjectSet** è enumerare tutti gli oggetti contenuti nella raccolta stessa.</span><span class="sxs-lookup"><span data-stu-id="08a85-150">For the most part, the only thing you will ever do with an **SWbemObjectSet** is enumerate all the objects contained within the collection itself.</span></span> <span data-ttu-id="08a85-151">Tuttavia, **SWbemObjectSet** include un numero di proprietà che può essere utile per gli script di amministrazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="08a85-151">However, **SWbemObjectSet** does include a property Count that can be useful in system administration scripting.</span></span> <span data-ttu-id="08a85-152">Come suggerisce il nome, Count indica il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="08a85-152">As the name implies, Count tells you the number of items in the collection.</span></span> <span data-ttu-id="08a85-153">Questo script, ad esempio, recupera una raccolta di tutti i servizi installati in un computer e quindi restituisce il numero totale di servizi trovati:</span><span class="sxs-lookup"><span data-stu-id="08a85-153">For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:</span></span>

<span data-ttu-id="08a85-154">Per ulteriori informazioni sull'utilizzo di questa classe, vedere [enumerazione di WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="08a85-154">For more information on how to use this class, see [Enumerating WMI](enumerating-wmi.md).</span></span>

## <a name="examples"></a><span data-ttu-id="08a85-155">Esempio</span><span class="sxs-lookup"><span data-stu-id="08a85-155">Examples</span></span>

<span data-ttu-id="08a85-156">Nell'esempio di codice VBScript seguente viene illustrato il modo in cui vengono modificate le raccolte di **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="08a85-156">The following VBScript code sample illustrates how **SWbemObjectSet** collections are manipulated.</span></span>


```VB
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



<span data-ttu-id="08a85-157">Nell'esempio di codice Perl seguente viene illustrato come vengono modificate le raccolte di **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="08a85-157">The following Perl code sample illustrates how **SWbemObjectSet** collections are manipulated.</span></span>


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="08a85-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08a85-158">Requirements</span></span>



| <span data-ttu-id="08a85-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="08a85-159">Requirement</span></span> | <span data-ttu-id="08a85-160">Valore</span><span class="sxs-lookup"><span data-stu-id="08a85-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08a85-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08a85-161">Minimum supported client</span></span><br/> | <span data-ttu-id="08a85-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08a85-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08a85-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08a85-163">Minimum supported server</span></span><br/> | <span data-ttu-id="08a85-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08a85-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08a85-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08a85-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="08a85-166"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="08a85-166"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="08a85-167">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="08a85-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="08a85-168"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="08a85-168"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="08a85-169">DLL</span><span class="sxs-lookup"><span data-stu-id="08a85-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08a85-170"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08a85-170"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="08a85-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="08a85-171">CLSID</span></span><br/>                    | <span data-ttu-id="08a85-172">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="08a85-172">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="08a85-173">IID</span><span class="sxs-lookup"><span data-stu-id="08a85-173">IID</span></span><br/>                      | <span data-ttu-id="08a85-174">\_ISWBEMOBJECTSET IID</span><span class="sxs-lookup"><span data-stu-id="08a85-174">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="08a85-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08a85-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a85-176">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="08a85-176">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




