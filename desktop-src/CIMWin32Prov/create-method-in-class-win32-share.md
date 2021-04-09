---
description: Avvia la condivisione per una risorsa server.
ms.assetid: 36530e1b-9109-4a6c-bba9-d9358101f5e2
ms.tgt_platform: multiple
title: Metodo Create della classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7a74838d9f6c532d3433240a5b8a70846b63776
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966375"
---
# <a name="create-method-of-the-win32_share-class"></a><span data-ttu-id="6a4fa-103">Metodo Create della \_ classe Share Win32</span><span class="sxs-lookup"><span data-stu-id="6a4fa-103">Create method of the Win32\_Share class</span></span>

<span data-ttu-id="6a4fa-104">Il metodo **create**   [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) avvia la condivisione per una risorsa server.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-104">The **Create**   [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method initiates sharing for a server resource.</span></span>

<span data-ttu-id="6a4fa-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="6a4fa-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6a4fa-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6a4fa-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a4fa-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a4fa-107">Syntax</span></span>


```mof
uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="6a4fa-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a4fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a4fa-109">*Percorso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a4fa-109">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4fa-110">Percorso locale della condivisione di Windows.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-110">Local path of the Windows share.</span></span>

<span data-ttu-id="6a4fa-111">Esempio, "C: \\ Program Files".</span><span class="sxs-lookup"><span data-stu-id="6a4fa-111">Example, "C:\\Program Files".</span></span>

</dd> <dt>

<span data-ttu-id="6a4fa-112">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a4fa-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4fa-113">Passa l'alias a un percorso configurato come una condivisione in un computer in cui è in esecuzione Windows.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-113">Passes the alias to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="6a4fa-114">Esempio "public".</span><span class="sxs-lookup"><span data-stu-id="6a4fa-114">Example, "public".</span></span>

</dd> <dt>

<span data-ttu-id="6a4fa-115">*Tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6a4fa-115">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4fa-116">Passa il tipo di risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-116">Passes the type of resource being shared.</span></span> <span data-ttu-id="6a4fa-117">I tipi includono le unità disco, le code di stampa, le comunicazioni interprocesso (IPC) e i dispositivi generali.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-117">Types includes disk drives, print queues, interprocess communications (IPC), and general devices.</span></span> <span data-ttu-id="6a4fa-118">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-118">Can be one of the following values.</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="6a4fa-119">**Unità disco** (0)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-119">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="6a4fa-120">**Coda di stampa** (1)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-120">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="6a4fa-121">**Dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-121">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="6a4fa-122">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-122">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="6a4fa-123">**Amministrazione unità disco** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-123">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="6a4fa-124">**Amministrazione coda di stampa** (2147483649)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-124">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="6a4fa-125">**Amministratore del dispositivo** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-125">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="6a4fa-126">**Amministratore IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-126">**IPC Admin** (2147483651)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="6a4fa-127">*MaximumAllowed* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6a4fa-127">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4fa-128">Limite per il numero massimo di utenti autorizzati a usare simultaneamente questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-128">Limit on the maximum number of users allowed to concurrently use this resource.</span></span>

<span data-ttu-id="6a4fa-129">Esempio: 10.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-129">Example: 10.</span></span> <span data-ttu-id="6a4fa-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-130">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="6a4fa-131">*Descrizione* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6a4fa-131">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4fa-132">Commento facoltativo per descrivere la risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-132">Optional comment to describe the resource being shared.</span></span> <span data-ttu-id="6a4fa-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-133">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="6a4fa-134">*Password* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6a4fa-134">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4fa-135">Password (quando il server è in esecuzione con sicurezza a livello di condivisione) per la risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-135">Password (when the server is running with share-level security) for the shared resource.</span></span> <span data-ttu-id="6a4fa-136">Se il server è in esecuzione con sicurezza a livello di utente, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-136">If the server is running with user-level security, this parameter is ignored.</span></span> <span data-ttu-id="6a4fa-137">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-137">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="6a4fa-138">*Accesso* \[ a in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6a4fa-138">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a4fa-139">Descrittore di sicurezza per le autorizzazioni a livello utente.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-139">Security descriptor for user level permissions.</span></span> <span data-ttu-id="6a4fa-140">Un descrittore di sicurezza contiene informazioni sulle autorizzazioni, il proprietario e le funzionalità di accesso della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-140">A security descriptor contains information about the permissions, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="6a4fa-141">Se questo parametro non viene specificato o è **null**, tutti hanno accesso in lettura alla condivisione.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-141">If this parameter is not supplied or is **NULL**, then Everyone has read access to the share.</span></span> <span data-ttu-id="6a4fa-142">Per ulteriori informazioni, vedere [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) e [modifica della sicurezza di accesso per gli oggetti a protezione diretta](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="6a4fa-142">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) and [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a4fa-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a4fa-143">Return value</span></span>

<span data-ttu-id="6a4fa-144">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-144">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="6a4fa-145">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6a4fa-145">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6a4fa-146">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6a4fa-146">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6a4fa-147">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-147">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6a4fa-148">**Accesso negato** (2)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-148">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6a4fa-149">**Errore sconosciuto** (8)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-149">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="6a4fa-150">**Nome non valido** (9)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-150">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="6a4fa-151">**Livello non valido** (10)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-151">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="6a4fa-152">**Parametro non valido** (21)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-152">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="6a4fa-153">**Condivisione duplicata** (22)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-153">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="6a4fa-154">**Percorso reindirizzato** (23)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-154">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="6a4fa-155">**Dispositivo o directory sconosciuta** (24)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-155">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="6a4fa-156">**Nome NET non trovato** (25)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-156">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="6a4fa-157">**Altro** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="6a4fa-157">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="6a4fa-158">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a4fa-158">Remarks</span></span>

<span data-ttu-id="6a4fa-159">**Create** è un metodo statico.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-159">**Create** is a static method.</span></span>

<span data-ttu-id="6a4fa-160">È possibile eseguire correttamente **create** solo i membri del gruppo locale Administrators o account Operators o quelli con appartenenza a gruppi di operatori di comunicazione, stampa o server.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-160">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute **Create**.</span></span> <span data-ttu-id="6a4fa-161">L'operatore Print può aggiungere solo code di stampa.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-161">The Print operator can only add printer queues.</span></span> <span data-ttu-id="6a4fa-162">L'operatore di comunicazione può aggiungere solo le code del dispositivo di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-162">The Communication operator can only add communication device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="6a4fa-163">Esempio</span><span class="sxs-lookup"><span data-stu-id="6a4fa-163">Examples</span></span>

<span data-ttu-id="6a4fa-164">L'esempio PowerShell [Export and import fileshares](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) Esporta e importa le condivisioni file e imposta le autorizzazioni di condivisione.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-164">The [Export and Import Fileshares](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) PowerShell sample exports and imports file shares and sets share permissions.</span></span> <span data-ttu-id="6a4fa-165">Analogamente, l'esempio [creare una condivisione e impostare le autorizzazioni](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) crea anche una nuova condivisione e imposta le autorizzazioni di condivisione.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-165">Similarly, the [Create a Share and Set Permissions](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) sample also creates a new share and sets the share permissions.</span></span>

<span data-ttu-id="6a4fa-166">Il codice di PowerShell seguente crea una condivisione.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-166">The following PowerShell code creates a share.</span></span>


```PowerShell
# create pointer to class
$comp=[WMICLASS]"Win32_share"

# create a new share
$comp.create("c:\","mynewshare",0)

# see results
gwmi win32_share 
```



<span data-ttu-id="6a4fa-167">Nell'esempio di codice precedente vengono restituiti gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6a4fa-167">The previous code sample returns the following:</span></span>

``` syntax
__GENUS          : 2
__CLASS          : __PARAMETERS
__SUPERCLASS     : 
__DYNASTY        : __PARAMETERS
__RELPATH        : 
__PROPERTY_COUNT : 1
__DERIVATION     : {}
__SERVER         : 
__NAMESPACE      : 
__PATH           : 
ReturnValue      : 2
PSComputerName   : 

Name        : ADMIN$
Path        : C:\Windows
Description : Remote Admin

Name        : C$
Path        : C:\
Description : Default share

Name        : CCMLOGS$
Path        : C:\Windows\CCM\Logs
Description : Public Share

Name        : ccmsetup$
Path        : C:\Windows\ccmsetup
Description : Public Share

Name        : Drop
Path        : C:\Drop
Description : 

Name        : IPC$
Path        : 
Description : Remote IPC

Name        : Share
Path        : C:\Share
Description : 
```

<span data-ttu-id="6a4fa-168">Nell' \# esempio di codice C riportato di seguito viene descritto come chiamare il metodo create.</span><span class="sxs-lookup"><span data-stu-id="6a4fa-168">The following C\# code sample describe how to call the create method.</span></span>


```CSharp
private static void makeShare(string servername, string filepath, string sharename)
{
try
 {
 // assemble the string so the scope represents the remote server
 string scope = string.Format("\\\\{0}\\root\\cimv2", servername);

 // connect to WMI on the remote server
 ManagementScope ms = new ManagementScope(scope);

 // create a new instance of the Win32_Share WMI object
 ManagementClass cls = new ManagementClass("Win32_Share");

 // set the scope of the new instance to that created above
 cls.Scope = ms;

 // assemble the arguments to be passed to the Create method
 object[] methodargs = { filepath, sharename, "0" };

 // invoke the Create method to create the share
 object result = cls.InvokeMethod("Create", methodargs);
 }
catch (SystemException e)
 {
  Console.WriteLine("Error attempting to create share {0}:", sharename);
  Console.WriteLine(e.Message);
 }

}
```



## <a name="requirements"></a><span data-ttu-id="6a4fa-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a4fa-169">Requirements</span></span>



| <span data-ttu-id="6a4fa-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a4fa-170">Requirement</span></span> | <span data-ttu-id="6a4fa-171">Valore</span><span class="sxs-lookup"><span data-stu-id="6a4fa-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a4fa-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a4fa-172">Minimum supported client</span></span><br/> | <span data-ttu-id="6a4fa-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a4fa-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a4fa-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a4fa-174">Minimum supported server</span></span><br/> | <span data-ttu-id="6a4fa-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a4fa-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a4fa-176">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6a4fa-176">Namespace</span></span><br/>                | <span data-ttu-id="6a4fa-177">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6a4fa-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a4fa-178">MOF</span><span class="sxs-lookup"><span data-stu-id="6a4fa-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a4fa-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a4fa-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a4fa-180">DLL</span><span class="sxs-lookup"><span data-stu-id="6a4fa-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a4fa-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a4fa-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a4fa-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a4fa-182">See also</span></span>

<dl> <dt>

<span data-ttu-id="6a4fa-183">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a4fa-183">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6a4fa-184">**\_Condivisione Win32**</span><span class="sxs-lookup"><span data-stu-id="6a4fa-184">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

