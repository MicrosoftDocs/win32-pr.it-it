---
description: Metodo Delete della classe Win32_Service (provider WMI CIMWin32) - Eliminazione&\# 8194; Il metodo della classe WMI elimina un servizio esistente.
ms.assetid: aa4e7630-3b19-47dd-acd1-4d1735acb819
ms.tgt_platform: multiple
title: Metodo Delete della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4031184e23e99fc54237ed0b0b4196fe6c075c5b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089579"
---
# <a name="delete-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="43727-103">Metodo Delete della classe Win32_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="43727-103">Delete method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="43727-104">Il **metodo** [Elimina classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) elimina un servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="43727-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="43727-105">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="43727-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="43727-106">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="43727-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="43727-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43727-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="43727-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="43727-108">Parameters</span></span>

<span data-ttu-id="43727-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="43727-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43727-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43727-110">Return value</span></span>

<span data-ttu-id="43727-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="43727-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="43727-112">Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="43727-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="43727-113">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)</span><span class="sxs-lookup"><span data-stu-id="43727-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="43727-114">**0**</span><span class="sxs-lookup"><span data-stu-id="43727-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="43727-115">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="43727-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="43727-116">**1**</span><span class="sxs-lookup"><span data-stu-id="43727-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="43727-117">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="43727-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="43727-118">**2**</span><span class="sxs-lookup"><span data-stu-id="43727-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="43727-119">L'utente non aveva l'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="43727-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="43727-120">**3**</span><span class="sxs-lookup"><span data-stu-id="43727-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="43727-121">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="43727-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="43727-122">**4**</span><span class="sxs-lookup"><span data-stu-id="43727-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="43727-123">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="43727-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="43727-124">**5**</span><span class="sxs-lookup"><span data-stu-id="43727-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="43727-125">Il codice di controllo richiesto non può essere inviato al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**State)** è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="43727-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="43727-126">**6**</span><span class="sxs-lookup"><span data-stu-id="43727-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="43727-127">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="43727-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="43727-128">**7**</span><span class="sxs-lookup"><span data-stu-id="43727-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="43727-129">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="43727-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="43727-130">**8**</span><span class="sxs-lookup"><span data-stu-id="43727-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="43727-131">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="43727-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="43727-132">**9**</span><span class="sxs-lookup"><span data-stu-id="43727-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="43727-133">Impossibile trovare il percorso della directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="43727-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="43727-134">**10**</span><span class="sxs-lookup"><span data-stu-id="43727-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="43727-135">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="43727-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="43727-136">**11**</span><span class="sxs-lookup"><span data-stu-id="43727-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="43727-137">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="43727-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="43727-138">**12**</span><span class="sxs-lookup"><span data-stu-id="43727-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="43727-139">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="43727-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="43727-140">**13**</span><span class="sxs-lookup"><span data-stu-id="43727-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="43727-141">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="43727-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="43727-142">**14**</span><span class="sxs-lookup"><span data-stu-id="43727-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="43727-143">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="43727-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="43727-144">**15**</span><span class="sxs-lookup"><span data-stu-id="43727-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="43727-145">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="43727-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="43727-146">**16**</span><span class="sxs-lookup"><span data-stu-id="43727-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="43727-147">Questo servizio viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="43727-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="43727-148">**17**</span><span class="sxs-lookup"><span data-stu-id="43727-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="43727-149">Il servizio non ha thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="43727-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="43727-150">**18**</span><span class="sxs-lookup"><span data-stu-id="43727-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="43727-151">Il servizio presenta dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="43727-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="43727-152">**19**</span><span class="sxs-lookup"><span data-stu-id="43727-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="43727-153">Un servizio viene eseguito con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="43727-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="43727-154">**20**</span><span class="sxs-lookup"><span data-stu-id="43727-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="43727-155">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="43727-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="43727-156">**21**</span><span class="sxs-lookup"><span data-stu-id="43727-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="43727-157">Al servizio sono stati passati parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="43727-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="43727-158">**22**</span><span class="sxs-lookup"><span data-stu-id="43727-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="43727-159">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="43727-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="43727-160">**23**</span><span class="sxs-lookup"><span data-stu-id="43727-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="43727-161">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="43727-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="43727-162">**24**</span><span class="sxs-lookup"><span data-stu-id="43727-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="43727-163">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="43727-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43727-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="43727-164">Remarks</span></span>

<span data-ttu-id="43727-165">Quando l'organizzazione cambia, è possibile decidere di rimuovere determinati servizi da determinati computer.</span><span class="sxs-lookup"><span data-stu-id="43727-165">As your organization changes, you might decide to remove certain services from certain computers.</span></span> <span data-ttu-id="43727-166">I servizi all'interno e di terze parti possono essere rimossi tramite WMI, mentre i servizi del sistema operativo possono essere rimossi usando Sysocmgr.exe.</span><span class="sxs-lookup"><span data-stu-id="43727-166">In-house and third-party services can be removed by using WMI, while operating system services can be removed by using Sysocmgr.exe.</span></span>

<span data-ttu-id="43727-167">Quando si prepara la rimozione dei servizi, tenere presenti le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="43727-167">When preparing to remove services, keep the following information in mind:</span></span>

-   <span data-ttu-id="43727-168">I servizi devono essere arrestati prima di rimuoverli.</span><span class="sxs-lookup"><span data-stu-id="43727-168">Services must be stopped before you remove them.</span></span> <span data-ttu-id="43727-169">Se il servizio è in esecuzione quando si esegue il comando delete, il servizio viene contrassegnato per l'eliminazione, ma continua a essere eseguito fino all'arresto e alla chiusura di tutti gli handle aperti.</span><span class="sxs-lookup"><span data-stu-id="43727-169">If the service is running when you issue the delete command, the service is marked for deletion, but it continues to run until it stops and all open handles are closed.</span></span>

    <span data-ttu-id="43727-170">Se il servizio non viene mai arrestato, tale servizio non verrà mai eliminato.</span><span class="sxs-lookup"><span data-stu-id="43727-170">If the service is never stopped, that service will never be deleted.</span></span>

-   <span data-ttu-id="43727-171">La rimozione di un servizio non rimuove il file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="43727-171">Removing a service does not remove the service's executable file.</span></span>

    <span data-ttu-id="43727-172">La rimozione di un servizio tramite WMI elimina le voci del Registro di sistema correlate in HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ \\ CurrentControlSet Services.</span><span class="sxs-lookup"><span data-stu-id="43727-172">Removing a service by using WMI deletes the related registry entries under HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services.</span></span> <span data-ttu-id="43727-173">Di conseguenza, il servizio non è più installato e non è disponibile tramite lo snap-in Servizi.</span><span class="sxs-lookup"><span data-stu-id="43727-173">As a result, the service is no longer installed and is not available through the Services snap-in.</span></span> <span data-ttu-id="43727-174">TUTTAVIA, WMI non elimina il file eseguibile, pertanto è possibile reinstallare facilmente il servizio.</span><span class="sxs-lookup"><span data-stu-id="43727-174">However, WMI does not delete the executable file, meaning you could easily reinstall the service.</span></span> <span data-ttu-id="43727-175">Per eliminare il file eseguibile, è necessario recuperare il nome del percorso e quindi eliminare il file.</span><span class="sxs-lookup"><span data-stu-id="43727-175">To delete the executable file, you must retrieve the path name and then delete the file.</span></span>

-   <span data-ttu-id="43727-176">La rimozione di un servizio windows 2000 di base (ad esempio DHCP) tramite WMI elimina le voci del Registro di sistema per tale servizio, ma non rimuove il collegamento dal menu Strumenti di amministrazione o rimuove il servizio dall'Aggiunta guidata componenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="43727-176">Removing a base Windows 2000 service (for example, DHCP) by using WMI deletes the registry entries for that service but does not remove the shortcut from the Administrative Tools menu or remove the service from the Windows Components Wizard.</span></span> <span data-ttu-id="43727-177">Ciò può confondere chiunque stia tentando di determinare come è stato configurato il computer.</span><span class="sxs-lookup"><span data-stu-id="43727-177">This can confuse anyone trying to determine how the computer has been configured.</span></span>

    <span data-ttu-id="43727-178">Ad esempio, se si rimuove il servizio DHCP tramite uno script WMI, il servizio DHCP non è più elencato nello snap-in Servizi.</span><span class="sxs-lookup"><span data-stu-id="43727-178">For example, if you remove the DHCP service by using a WMI script, the DHCP service is no longer listed in the Services snap-in.</span></span> <span data-ttu-id="43727-179">Tuttavia, un collegamento non funzionante alla console DHCP rimane nel menu Strumenti di amministrazione e, se si avvia la Creazione guidata componenti di Windows, indica che il servizio DHCP è installato.</span><span class="sxs-lookup"><span data-stu-id="43727-179">However, a nonfunctioning shortcut to the DHCP console remains in the Administrative Tools menu, and if you start the Windows Component Wizard, it indicates that the DHCP service is installed.</span></span>

    <span data-ttu-id="43727-180">Per questo problema, è consigliabile usare sempre Sysocmgr.exe per rimuovere i servizi di Windows 2000 a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="43727-180">Because of this, you should always use Sysocmgr.exe to programmatically remove Windows 2000 services.</span></span>

## <a name="examples"></a><span data-ttu-id="43727-181">Esempio</span><span class="sxs-lookup"><span data-stu-id="43727-181">Examples</span></span>

<span data-ttu-id="43727-182">Nell'esempio di codice VBScript seguente viene descritto come eliminare un servizio.</span><span class="sxs-lookup"><span data-stu-id="43727-182">The following VBScript code sample describes how to delete a service.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colListOfServices = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE Name = 'DbService'")
For Each objService in colListOfServices
 objService.StopService()
 objService.Delete()
Next
```



<span data-ttu-id="43727-183">L'esempio di codice Perl seguente descrive come eliminare un servizio.</span><span class="sxs-lookup"><span data-stu-id="43727-183">The following Perl code sample describes how to delete a service.</span></span>


```
use strict;
use Win32::OLE;

my ($Service, $ServiceSet) ;
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='MyService'");};
unless($@)
{
 foreach $Service (in $ServiceSet)
 {
  my $RetVal = $Service->Delete();
  if ($RetVal == 0)  
  {
   print "Service deleted \n"; 
  }
  else  
  {
   print "Delete failed: %d", $RetVal;
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="43727-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43727-184">Requirements</span></span>



| <span data-ttu-id="43727-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="43727-185">Requirement</span></span> | <span data-ttu-id="43727-186">Valore</span><span class="sxs-lookup"><span data-stu-id="43727-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43727-187">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43727-187">Minimum supported client</span></span><br/> | <span data-ttu-id="43727-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43727-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43727-189">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43727-189">Minimum supported server</span></span><br/> | <span data-ttu-id="43727-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43727-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43727-191">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="43727-191">Namespace</span></span><br/>                | <span data-ttu-id="43727-192">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="43727-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="43727-193">MOF</span><span class="sxs-lookup"><span data-stu-id="43727-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43727-194"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="43727-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="43727-195">DLL</span><span class="sxs-lookup"><span data-stu-id="43727-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43727-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43727-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43727-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43727-197">See also</span></span>

<dl> <dt>

<span data-ttu-id="43727-198">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43727-198">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="43727-199">**Servizio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="43727-199">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="43727-200">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="43727-200">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

