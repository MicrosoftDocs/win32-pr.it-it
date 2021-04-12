---
description: Un oggetto SWbemPrivilegeSet è una raccolta di oggetti SWbemPrivilege in un oggetto SWbemSecurity che richiede privilegi specifici per un oggetto Strumentazione gestione Windows (WMI).
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: Oggetto SWbemPrivilegeSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet
- ISWbemPrivilegeSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b2946f8b1f745c0db123ed33dab312cbbe9d16c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344721"
---
# <a name="swbemprivilegeset-object"></a><span data-ttu-id="10dcd-103">Oggetto SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="10dcd-103">SWbemPrivilegeSet object</span></span>

<span data-ttu-id="10dcd-104">Un oggetto **SWbemPrivilegeSet** è una raccolta di oggetti [**SWbemPrivilege**](swbemprivilege.md) in un oggetto [**SWbemSecurity**](swbemsecurity.md) che richiede privilegi specifici per un oggetto Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="10dcd-104">An **SWbemPrivilegeSet** object is a collection of [**SWbemPrivilege**](swbemprivilege.md) objects in an [**SWbemSecurity**](swbemsecurity.md) object that requests specific privileges for a Windows Management Instrumentation (WMI) object.</span></span> <span data-ttu-id="10dcd-105">Vedere l'elenco dei privilegi nelle [**costanti Privilege**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="10dcd-105">See the list of privileges in [**Privilege Constants**](privilege-constants.md).</span></span> <span data-ttu-id="10dcd-106">Gli elementi vengono aggiunti alla raccolta usando i metodi [**Add**](swbemprivilegeset-add.md) e [**AddAsString**](swbemprivilegeset-addasstring.md) .</span><span class="sxs-lookup"><span data-stu-id="10dcd-106">Items are added to the collection using the [**Add**](swbemprivilegeset-add.md) and [**AddAsString**](swbemprivilegeset-addasstring.md) methods.</span></span> <span data-ttu-id="10dcd-107">Gli elementi vengono recuperati dalla raccolta usando il metodo [**Item**](swbemprivilegeset-item.md) e rimossi usando il metodo [**Remove**](swbemprivilegeset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="10dcd-107">Items are retrieved from the collection using the [**Item**](swbemprivilegeset-item.md) method, and removed using the [**Remove**](swbemprivilegeset-remove.md) method.</span></span> <span data-ttu-id="10dcd-108">Questo oggetto non può essere creato dalla chiamata al metodo [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript.</span><span class="sxs-lookup"><span data-stu-id="10dcd-108">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) method call.</span></span> <span data-ttu-id="10dcd-109">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="10dcd-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="10dcd-110">Un oggetto **SWbemPrivilegeSet** è un set di richieste di override dei privilegi per un oggetto specifico.</span><span class="sxs-lookup"><span data-stu-id="10dcd-110">An **SWbemPrivilegeSet** object is a set of privilege override requests for a specific object.</span></span> <span data-ttu-id="10dcd-111">Quando viene eseguita una chiamata API utilizzando questo oggetto, vengono tentate le richieste di override dei privilegi.</span><span class="sxs-lookup"><span data-stu-id="10dcd-111">When an API call is made using this object, the privilege override requests are attempted.</span></span> <span data-ttu-id="10dcd-112">L'oggetto **SWbemPrivilegeSet** non definisce i privilegi disponibili per l'utente o il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="10dcd-112">The **SWbemPrivilegeSet** object does not define the privileges available to the current user or process.</span></span> <span data-ttu-id="10dcd-113">In altre parole, ottenendo i privilegi per qualsiasi oggetto WMI non vengono identificate le impostazioni dei privilegi effettuate sulla connessione a WMI oppure i privilegi attivi quando un oggetto viene recapitato a un sink.</span><span class="sxs-lookup"><span data-stu-id="10dcd-113">In other words, obtaining the privileges for any WMI object does not identify the privilege settings that are made on the connection to WMI, or the privileges in effect when an object is delivered to a sink.</span></span>

## <a name="members"></a><span data-ttu-id="10dcd-114">Membri</span><span class="sxs-lookup"><span data-stu-id="10dcd-114">Members</span></span>

<span data-ttu-id="10dcd-115">L'oggetto **SWbemPrivilegeSet** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="10dcd-115">The **SWbemPrivilegeSet** object has these types of members:</span></span>

-   [<span data-ttu-id="10dcd-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="10dcd-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="10dcd-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="10dcd-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="10dcd-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="10dcd-118">Methods</span></span>

<span data-ttu-id="10dcd-119">L'oggetto **SWbemPrivilegeSet** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="10dcd-119">The **SWbemPrivilegeSet** object has these methods.</span></span>



| <span data-ttu-id="10dcd-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="10dcd-120">Method</span></span>                                               | <span data-ttu-id="10dcd-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10dcd-121">Description</span></span>                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10dcd-122">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="10dcd-122">**Add**</span></span>](swbemprivilegeset-add.md)                 | <span data-ttu-id="10dcd-123">Aggiunge un oggetto [**SWbemPrivilege**](swbemprivilege.md) alla raccolta **SWbemPrivilegeSet** usando una costante [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="10dcd-123">Adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection using a [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) constant.</span></span><br/> |
| [<span data-ttu-id="10dcd-124">**AddAsString**</span><span class="sxs-lookup"><span data-stu-id="10dcd-124">**AddAsString**</span></span>](swbemprivilegeset-addasstring.md) | <span data-ttu-id="10dcd-125">Aggiunge un oggetto [**SWbemPrivilege**](swbemprivilege.md) alla raccolta **SWbemPrivilegeSet** utilizzando una stringa di privilegio.</span><span class="sxs-lookup"><span data-stu-id="10dcd-125">Adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection using a privilege string.</span></span><br/>                                    |
| [<span data-ttu-id="10dcd-126">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="10dcd-126">**DeleteAll**</span></span>](swbemprivilegeset-deleteall.md)     | <span data-ttu-id="10dcd-127">Elimina tutti i privilegi dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="10dcd-127">Deletes all the privileges from the collection.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="10dcd-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="10dcd-128">**Item**</span></span>](swbemprivilegeset-item.md)               | <span data-ttu-id="10dcd-129">Recupera un oggetto [**SWbemPrivilege**](swbemprivilege.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="10dcd-129">Retrieves an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span> <span data-ttu-id="10dcd-130">Questo è il metodo predefinito di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="10dcd-130">This is the default method of this object.</span></span><br/>                                 |
| [<span data-ttu-id="10dcd-131">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="10dcd-131">**Remove**</span></span>](swbemprivilegeset-remove.md)           | <span data-ttu-id="10dcd-132">Rimuove un oggetto [**SWbemPrivilege**](swbemprivilege.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="10dcd-132">Removes an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span><br/>                                                                              |



 

### <a name="properties"></a><span data-ttu-id="10dcd-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="10dcd-133">Properties</span></span>

<span data-ttu-id="10dcd-134">L'oggetto **SWbemPrivilegeSet** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="10dcd-134">The **SWbemPrivilegeSet** object has these properties.</span></span>



| <span data-ttu-id="10dcd-135">Proprietà</span><span class="sxs-lookup"><span data-stu-id="10dcd-135">Property</span></span>                                            | <span data-ttu-id="10dcd-136">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="10dcd-136">Access type</span></span>          | <span data-ttu-id="10dcd-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10dcd-137">Description</span></span>                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="10dcd-138">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="10dcd-138">**Count**</span></span>](swbemprivilegeset-count.md)<br/> | <span data-ttu-id="10dcd-139">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="10dcd-139">Read-only</span></span><br/> | <span data-ttu-id="10dcd-140">Numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="10dcd-140">The number of items in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="10dcd-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="10dcd-141">Examples</span></span>

<span data-ttu-id="10dcd-142">Nell'esempio di codice VBScript seguente viene ottenuto un oggetto SWbemPrivileges e vengono aggiunti tutti i privilegi disponibili alla raccolta in base al valore del privilegio, come definito in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span><span class="sxs-lookup"><span data-stu-id="10dcd-142">The following VBScript code example obtains an SWbemPrivileges object and adds all the available privileges to the collection by privilege value, as defined in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\cimv2")
set colPrivileges = objWMIService.Security_.Privileges
For I = 1 To 27
colPrivileges.Add(I)
Next
' Display information about each privilege 
For Each objItem In colPrivileges
wscript.echo objItem.Identifier & vbtab & objItem.Name _
    & vbtab & objItem.Displayname _
    & vbtab & "Enabled = " & objItem.IsEnabled
Next
```



<span data-ttu-id="10dcd-143">Nell'esempio di codice VBScript riportato di seguito viene illustrato come aggiungere privilegi utilizzando l'oggetto **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="10dcd-143">The following VBScript code example demonstrates how to add privileges using the **SWbemPrivilegeSet** object.</span></span>


```VB
on error resume next

const wbemPrivilegeSecurity = 8
const wbemPrivilegeDebug = 20

set locator = CreateObject("WbemScripting.SWbemLocator")

' Add a single privilege using SWbemPrivilegeSet.Add

locator.Security_.Privileges.Add wbemPrivilegeSecurity 
Set Privilege = locator.Security_.Privileges(wbemPrivilegeSecurity)
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
locator.Security_.Privileges.Add 6535
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

locator.Security_.Privileges.Add wbemPrivilegeDebug 

locator.Security_.Privileges(wbemPrivilegeDebug).IsEnabled = false

' Add a single privilege using SWbemPrivilegeSet.AddAsString

Set Privilege = locator.Security_.Privileges.AddAsString ("SeChangeNotifyPrivilege")
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
locator.Security_.Privileges.AddAsString "SeChungeNotifyPrivilege"
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

WScript.Echo ""
for each Privilege in locator.Security_.Privileges
 WScript.Echo "[" & Privilege.DisplayName & "]", Privilege.Identifier, Privilege.Name, Privilege.IsEnabled
next

if err <> 0 then
 WScript.Echo Err.Number, Err.Description, Err.Source
end if 
```



<span data-ttu-id="10dcd-144">Nell'esempio di codice Perl seguente viene illustrato come aggiungere privilegi utilizzando l'oggetto **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="10dcd-144">The following Perl code example demonstrates how to add privileges using the **SWbemPrivilegeSet** object.</span></span>


```
use strict;
use Win32::OLE;

close(STDERR);

my ($locator, $Privilege);
my $wbemPrivilegeSecurity = 8;
my $wbemPrivilegeDebug = 20;

eval { $locator = new Win32::OLE 'WbemScripting.SWbemLocator';};

if (!$@ && defined $locator)
{
 # Add a single privilege using SWbemPrivilegeSet.Add
 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeSecurity);
 $Privilege = $locator->{Security_}->Privileges($wbemPrivilegeSecurity);
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
 eval { $locator->{Security_}->{Privileges}->Add(6535); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);

 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeDebug); 
 $locator->{Security_}->Privileges($wbemPrivilegeDebug)->{IsEnabled} = 0;

 # Add a single privilege using SWbemPrivilegeSet.AddAsString
 $Privilege = $locator->{Security_}->{Privileges}->AddAsString ("SeChangeNotifyPrivilege");
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
 eval {$locator->{Security_}->{Privileges}->AddAsString ("SeChungeNotifyPrivilege"); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);
 print "\n";

 foreach $Privilege (in {$locator->{Security_}->{Privileges}})
 {
  printf "[%s] %d %s %d \n" , $Privilege->{DisplayName}, $Privilege->{Identifier}, $Privilege->{Name}, $Privilege->{IsEnabled};
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="10dcd-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10dcd-145">Requirements</span></span>



| <span data-ttu-id="10dcd-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="10dcd-146">Requirement</span></span> | <span data-ttu-id="10dcd-147">Valore</span><span class="sxs-lookup"><span data-stu-id="10dcd-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10dcd-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10dcd-148">Minimum supported client</span></span><br/> | <span data-ttu-id="10dcd-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10dcd-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10dcd-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10dcd-150">Minimum supported server</span></span><br/> | <span data-ttu-id="10dcd-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10dcd-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10dcd-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10dcd-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="10dcd-153"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="10dcd-153"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="10dcd-154">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="10dcd-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="10dcd-155"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="10dcd-155"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="10dcd-156">DLL</span><span class="sxs-lookup"><span data-stu-id="10dcd-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10dcd-157"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10dcd-157"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="10dcd-158">CLSID</span><span class="sxs-lookup"><span data-stu-id="10dcd-158">CLSID</span></span><br/>                    | <span data-ttu-id="10dcd-159">\_SWBEMPRIVILEGESET CLSID</span><span class="sxs-lookup"><span data-stu-id="10dcd-159">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="10dcd-160">IID</span><span class="sxs-lookup"><span data-stu-id="10dcd-160">IID</span></span><br/>                      | <span data-ttu-id="10dcd-161">\_ISWBEMPRIVILEGESET IID</span><span class="sxs-lookup"><span data-stu-id="10dcd-161">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="10dcd-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10dcd-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10dcd-163">Esecuzione di operazioni con privilegi</span><span class="sxs-lookup"><span data-stu-id="10dcd-163">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="10dcd-164">Esecuzione di operazioni con privilegi tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="10dcd-164">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="10dcd-165">WbemPrivilegeEnum</span><span class="sxs-lookup"><span data-stu-id="10dcd-165">WbemPrivilegeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="10dcd-166">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="10dcd-166">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="10dcd-167">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="10dcd-167">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

