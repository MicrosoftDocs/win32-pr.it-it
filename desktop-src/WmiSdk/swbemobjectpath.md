---
description: Usare i metodi e le proprietà dell'oggetto SWbemObjectPath per creare e convalidare il percorso di un oggetto. Questo oggetto può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: Oggetto SWbemObjectPath (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath
- ISWbemObjectPath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1e6836cd58970f3667d8f629a678d55bec5185a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309805"
---
# <a name="swbemobjectpath-object"></a><span data-ttu-id="7f5ff-104">Oggetto SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="7f5ff-104">SWbemObjectPath object</span></span>

<span data-ttu-id="7f5ff-105">Usare i metodi e le proprietà dell'oggetto **SWbemObjectPath** per creare e convalidare il percorso di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-105">Use the methods and properties of the **SWbemObjectPath** object to construct and validate an object path.</span></span> <span data-ttu-id="7f5ff-106">Questo oggetto può essere creato dalla chiamata **CreateObject** di VBScript.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-106">This object can be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="7f5ff-107">Membri</span><span class="sxs-lookup"><span data-stu-id="7f5ff-107">Members</span></span>

<span data-ttu-id="7f5ff-108">L'oggetto **SWbemObjectPath** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7f5ff-108">The **SWbemObjectPath** object has these types of members:</span></span>

-   [<span data-ttu-id="7f5ff-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="7f5ff-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="7f5ff-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7f5ff-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7f5ff-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="7f5ff-111">Methods</span></span>

<span data-ttu-id="7f5ff-112">L'oggetto **SWbemObjectPath** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-112">The **SWbemObjectPath** object has these methods.</span></span>



| <span data-ttu-id="7f5ff-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="7f5ff-113">Method</span></span>                                                   | <span data-ttu-id="7f5ff-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f5ff-114">Description</span></span>                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="7f5ff-115">**SetAsClass**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-115">**SetAsClass**</span></span>](swbemobjectpath-setasclass.md)         | <span data-ttu-id="7f5ff-116">Impone al percorso di indirizzare una classe WMI.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-116">Forces the path to address a WMI class.</span></span><br/>              |
| [<span data-ttu-id="7f5ff-117">**SetAsSingleton**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-117">**SetAsSingleton**</span></span>](swbemobjectpath-setassingleton.md) | <span data-ttu-id="7f5ff-118">Impone al percorso di indirizzare un'istanza WMI singleton.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-118">Forces the path to address a singleton WMI instance.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7f5ff-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7f5ff-119">Properties</span></span>

<span data-ttu-id="7f5ff-120">L'oggetto **SWbemObjectPath** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-120">The **SWbemObjectPath** object has these properties.</span></span>



| <span data-ttu-id="7f5ff-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7f5ff-121">Property</span></span>                                                              | <span data-ttu-id="7f5ff-122">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="7f5ff-122">Access type</span></span>           | <span data-ttu-id="7f5ff-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f5ff-123">Description</span></span>                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f5ff-124">**Authority**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-124">**Authority**</span></span>](swbemobjectpath-authority.md)<br/>             | <span data-ttu-id="7f5ff-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7f5ff-125">Read/write</span></span><br/> | <span data-ttu-id="7f5ff-126">Stringa che definisce il componente Authority del percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-126">String that defines the Authority component of the object path.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="7f5ff-127">**Classe**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-127">**Class**</span></span>](swbemobjectpath-class.md)<br/>                     | <span data-ttu-id="7f5ff-128">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7f5ff-128">Read/write</span></span><br/> | <span data-ttu-id="7f5ff-129">Nome della classe che fa parte del percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-129">Name of the class that is part of the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="7f5ff-130">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-130">**DisplayName**</span></span>](swbemobjectpath-displayname.md)<br/>         | <span data-ttu-id="7f5ff-131">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7f5ff-131">Read/write</span></span><br/> | <span data-ttu-id="7f5ff-132">Stringa che contiene il percorso in un form che può essere utilizzato come nome visualizzato del moniker.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-132">String that contains the path in a form that can be used as a moniker display name.</span></span> <span data-ttu-id="7f5ff-133">Vedere [creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="7f5ff-133">See [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span><br/> |
| [<span data-ttu-id="7f5ff-134">**IsClass**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-134">**IsClass**</span></span>](swbemobjectpath-isclass.md)<br/>                 | <span data-ttu-id="7f5ff-135">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f5ff-135">Read-only</span></span><br/>  | <span data-ttu-id="7f5ff-136">Valore booleano che indica se questo percorso rappresenta una classe.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-136">Boolean value that indicates if this path represents a class.</span></span> <span data-ttu-id="7f5ff-137">Questo è analogo alla proprietà [ \_ \_ genre](wmi-system-properties.md) nell'API com.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-137">This is analogous to the [\_\_Genus](wmi-system-properties.md) property in the COM API.</span></span><br/>                    |
| [<span data-ttu-id="7f5ff-138">**IsSingleton**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-138">**IsSingleton**</span></span>](swbemobjectpath-issingleton.md)<br/>         | <span data-ttu-id="7f5ff-139">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f5ff-139">Read-only</span></span><br/>  | <span data-ttu-id="7f5ff-140">Valore booleano che indica se questo percorso rappresenta un'istanza singleton.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-140">Boolean value that indicates if this path represents a singleton instance.</span></span><br/>                                                                                                |
| [<span data-ttu-id="7f5ff-141">**Chiavi**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-141">**Keys**</span></span>](swbemobjectpath-keys.md)<br/>                       | <span data-ttu-id="7f5ff-142">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f5ff-142">Read-only</span></span><br/>  | <span data-ttu-id="7f5ff-143">Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che contiene le associazioni del valore della chiave.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-143">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that contains the key value bindings.</span></span><br/>                                                                          |
| [<span data-ttu-id="7f5ff-144">**Locale**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-144">**Locale**</span></span>](swbemobjectpath-locale.md)<br/>                   | <span data-ttu-id="7f5ff-145">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7f5ff-145">Read/write</span></span><br/> | <span data-ttu-id="7f5ff-146">Stringa contenente le impostazioni locali per il percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-146">String that contains the locale for this object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="7f5ff-147">**Spazio dei nomi**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-147">**Namespace**</span></span>](swbemobjectpath-namespace.md)<br/>             | <span data-ttu-id="7f5ff-148">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7f5ff-148">Read/write</span></span><br/> | <span data-ttu-id="7f5ff-149">Nome dello spazio dei nomi che fa parte del percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-149">Name of the namespace that is part of the object path.</span></span> <span data-ttu-id="7f5ff-150">Corrisponde alla proprietà [ \_ \_ namespace](wmi-system-properties.md) nell'API com.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-150">This is the same as the [\_\_Namespace](wmi-system-properties.md) property in the COM API.</span></span><br/>                        |
| [<span data-ttu-id="7f5ff-151">**ParentNamespace**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-151">**ParentNamespace**</span></span>](swbemobjectpath-parentnamespace.md)<br/> | <span data-ttu-id="7f5ff-152">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f5ff-152">Read-only</span></span><br/>  | <span data-ttu-id="7f5ff-153">Nome dell'elemento padre dello spazio dei nomi che fa parte del percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-153">Name of the parent of the namespace that is part of the object path.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="7f5ff-154">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-154">**Path**</span></span>](swbemobjectpath-path.md)<br/>                       | <span data-ttu-id="7f5ff-155">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7f5ff-155">Read/write</span></span><br/> | <span data-ttu-id="7f5ff-156">Contiene il percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-156">Contains the absolute path.</span></span> <span data-ttu-id="7f5ff-157">Corrisponde alla proprietà di sistema [ \_ \_ path](wmi-system-properties.md) nell'API com.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-157">This is the same as the [\_\_Path](wmi-system-properties.md) system property in the COM API.</span></span> <span data-ttu-id="7f5ff-158">Si tratta della proprietà predefinita di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-158">This is the default property of this object.</span></span><br/>    |
| [<span data-ttu-id="7f5ff-159">**RelPath**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-159">**Relpath**</span></span>](swbemobjectpath-relpath.md)<br/>                 | <span data-ttu-id="7f5ff-160">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7f5ff-160">Read/write</span></span><br/> | <span data-ttu-id="7f5ff-161">Contiene il percorso relativo.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-161">Contains the relative path.</span></span> <span data-ttu-id="7f5ff-162">Corrisponde alla proprietà di sistema [ \_ \_ RelPath](wmi-system-properties.md) nell'API com.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-162">This is the same as the [\_\_Relpath](wmi-system-properties.md) system property in the COM API.</span></span><br/>                                              |
| [<span data-ttu-id="7f5ff-163">**Sicurezza\_**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-163">**Security\_**</span></span>](swbemobjectpath-security-.md)<br/>            | <span data-ttu-id="7f5ff-164">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f5ff-164">Read-only</span></span><br/>  | <span data-ttu-id="7f5ff-165">Utilizzato per leggere o modificare le impostazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-165">Used to read or change the security settings.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="7f5ff-166">**Server**</span><span class="sxs-lookup"><span data-stu-id="7f5ff-166">**Server**</span></span>](swbemobjectpath-server.md)<br/>                   | <span data-ttu-id="7f5ff-167">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7f5ff-167">Read/write</span></span><br/> | <span data-ttu-id="7f5ff-168">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-168">Name of the server.</span></span> <span data-ttu-id="7f5ff-169">Corrisponde alla proprietà di sistema del [ \_ \_ server](wmi-system-properties.md) nell'API com.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-169">This is the same as the [\_\_Server](wmi-system-properties.md) system property in the COM API.</span></span><br/>                                                       |



 

## <a name="examples"></a><span data-ttu-id="7f5ff-170">Esempio</span><span class="sxs-lookup"><span data-stu-id="7f5ff-170">Examples</span></span>

<span data-ttu-id="7f5ff-171">Nell'esempio di codice VBScript seguente viene illustrato come compilare i percorsi degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-171">The following VBScript code sample demonstrates how to build object paths.</span></span>


```VB
on error resume next 
Set ObjectPath = CreateObject("WbemScripting.SWbemObjectPath")
ObjectPath.Server = "dingle"
ObjectPath.Namespace = "root/default/something"
ObjectPath.Class = "ho"
ObjectPath.Keys.Add "fred1", 10
ObjectPath.Keys.Add "fred2", -34
ObjectPath.Keys.Add "fred3", 65234654
ObjectPath.Keys.Add "fred4", "Wahaay"
ObjectPath.Keys.Add "fred5", -786186777

if err <> 0 then 
 WScript.Echo err.number
end if 

WScript.Echo "Pass 1:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.ImpersonationLevel = 3

WScript.Echo "Pass 2:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.AuthenticationLevel = 5

WScript.Echo "Pass 3:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

Set Privileges = ObjectPath.Security_.Privileges
if err <> 0 then
 WScript.Echo Hex(Err.Number), Err.Description
end if
Privileges.Add 8
Privileges.Add 20, false

WScript.Echo "Pass 4:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.DisplayName = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah"

WScript.Echo "Pass 5:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""
```



<span data-ttu-id="7f5ff-172">Nell'esempio di codice Perl seguente viene illustrato come compilare i percorsi degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="7f5ff-172">The following Perl code sample demonstrates how to build object paths.</span></span>


```
use strict;
use Win32::OLE;
use constant FALSE=>"false";

my ( $ObjectPath, $Privileges );

eval { $ObjectPath = new Win32::OLE 'WbemScripting.SWbemObjectPath'; };
unless($@)
{
 eval
 {
  $ObjectPath->{Server} = "dingle";
  $ObjectPath->{Namespace} = "root/default/something";
  $ObjectPath->{Class} = "ho";
  $ObjectPath->{Keys}->Add("fred1", 10);
  $ObjectPath->{Keys}->Add("fred2", -34);
  $ObjectPath->{Keys}->Add("fred3", 65234654);
  $ObjectPath->{Keys}->Add("fred4", "Wahaay");
  $ObjectPath->{Keys}->Add("fred5", -786186777);
 };
 unless($@)
 {
  print "\n";
  print "Pass 1:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{ImpersonationLevel} = 3 ;

  print "Pass 2:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{AuthenticationLevel} = 5 ;

  print "Pass 3:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  eval { $Privileges = $ObjectPath->{Security_}->{Privileges}; };
  unless($@)
  {
   $Privileges->Add(8);
   $Privileges->Add(20,FALSE);

   print "Pass 4:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n\n";

   $ObjectPath->{DisplayName} = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah";

   print "Pass 5:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n";
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
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="7f5ff-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f5ff-173">Requirements</span></span>



| <span data-ttu-id="7f5ff-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f5ff-174">Requirement</span></span> | <span data-ttu-id="7f5ff-175">Valore</span><span class="sxs-lookup"><span data-stu-id="7f5ff-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f5ff-176">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f5ff-176">Minimum supported client</span></span><br/> | <span data-ttu-id="7f5ff-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f5ff-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f5ff-178">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f5ff-178">Minimum supported server</span></span><br/> | <span data-ttu-id="7f5ff-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f5ff-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f5ff-180">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f5ff-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f5ff-181"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f5ff-181"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f5ff-182">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7f5ff-182">Type library</span></span><br/>             | <dl> <span data-ttu-id="7f5ff-183"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7f5ff-183"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7f5ff-184">DLL</span><span class="sxs-lookup"><span data-stu-id="7f5ff-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f5ff-185"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f5ff-185"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7f5ff-186">CLSID</span><span class="sxs-lookup"><span data-stu-id="7f5ff-186">CLSID</span></span><br/>                    | <span data-ttu-id="7f5ff-187">\_SWBEMOBJECTPATH CLSID</span><span class="sxs-lookup"><span data-stu-id="7f5ff-187">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="7f5ff-188">IID</span><span class="sxs-lookup"><span data-stu-id="7f5ff-188">IID</span></span><br/>                      | <span data-ttu-id="7f5ff-189">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="7f5ff-189">IID\_ISWbemObjectPath</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="7f5ff-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f5ff-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f5ff-191">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="7f5ff-191">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




