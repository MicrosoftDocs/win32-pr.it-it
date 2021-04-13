---
title: Metodo Delete della classe Win32_Service (Servizi Desktop remoto)
description: Eliminazione \ 8194; Il metodo della classe WMI Elimina un servizio esistente.
ms.assetid: 0F012D6B-BD29-4AC3-AC7E-78EC02C1FF43
ms.tgt_platform: multiple
keywords:
- Elimina Servizi Desktop remoto del metodo
- Metodo Delete Servizi Desktop remoto, classe Win32_Service
- Classe Win32_Service Servizi Desktop remoto, metodo Delete
topic_type:
- apiref
api_name:
- Win32_Service.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89e2c30ef39d7b36baf62a486477fcf4a7fa2842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518922"
---
# <a name="delete-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="d5804-106">Metodo Delete della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="d5804-106">Delete method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="d5804-107">Il metodo **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) Elimina un servizio esistente.</span><span class="sxs-lookup"><span data-stu-id="d5804-107">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="d5804-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="d5804-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d5804-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d5804-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5804-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5804-110">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="d5804-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5804-111">Parameters</span></span>

<span data-ttu-id="d5804-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d5804-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5804-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5804-113">Return value</span></span>

<span data-ttu-id="d5804-114">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="d5804-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="d5804-115">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d5804-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d5804-116">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d5804-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d5804-117">**0**</span><span class="sxs-lookup"><span data-stu-id="d5804-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-118">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="d5804-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-119">**1**</span><span class="sxs-lookup"><span data-stu-id="d5804-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-120">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="d5804-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-121">**2**</span><span class="sxs-lookup"><span data-stu-id="d5804-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-122">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="d5804-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-123">**3**</span><span class="sxs-lookup"><span data-stu-id="d5804-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-124">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="d5804-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-125">**4**</span><span class="sxs-lookup"><span data-stu-id="d5804-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-126">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="d5804-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-127">**5**</span><span class="sxs-lookup"><span data-stu-id="d5804-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-128">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="d5804-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-129">**6**</span><span class="sxs-lookup"><span data-stu-id="d5804-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-130">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="d5804-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-131">**7**</span><span class="sxs-lookup"><span data-stu-id="d5804-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-132">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="d5804-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-133">**8**</span><span class="sxs-lookup"><span data-stu-id="d5804-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-134">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="d5804-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-135">**9**</span><span class="sxs-lookup"><span data-stu-id="d5804-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-136">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="d5804-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-137">**10**</span><span class="sxs-lookup"><span data-stu-id="d5804-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-138">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d5804-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-139">**11**</span><span class="sxs-lookup"><span data-stu-id="d5804-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-140">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="d5804-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-141">**12**</span><span class="sxs-lookup"><span data-stu-id="d5804-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-142">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d5804-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-143">**13**</span><span class="sxs-lookup"><span data-stu-id="d5804-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-144">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="d5804-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-145">**14**</span><span class="sxs-lookup"><span data-stu-id="d5804-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-146">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d5804-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-147">**15**</span><span class="sxs-lookup"><span data-stu-id="d5804-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-148">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="d5804-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-149">**16**</span><span class="sxs-lookup"><span data-stu-id="d5804-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-150">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d5804-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-151">**17**</span><span class="sxs-lookup"><span data-stu-id="d5804-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-152">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d5804-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-153">**18**</span><span class="sxs-lookup"><span data-stu-id="d5804-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-154">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="d5804-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-155">**19**</span><span class="sxs-lookup"><span data-stu-id="d5804-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-156">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="d5804-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-157">**20**</span><span class="sxs-lookup"><span data-stu-id="d5804-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-158">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="d5804-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-159">**21**</span><span class="sxs-lookup"><span data-stu-id="d5804-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-160">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="d5804-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-161">**22**</span><span class="sxs-lookup"><span data-stu-id="d5804-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-162">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="d5804-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-163">**23**</span><span class="sxs-lookup"><span data-stu-id="d5804-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-164">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d5804-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="d5804-165">**24**</span><span class="sxs-lookup"><span data-stu-id="d5804-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="d5804-166">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="d5804-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5804-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5804-167">Remarks</span></span>

<span data-ttu-id="d5804-168">Con l'evoluzione dell'organizzazione, è possibile decidere di rimuovere determinati servizi da determinati computer.</span><span class="sxs-lookup"><span data-stu-id="d5804-168">As your organization changes, you might decide to remove certain services from certain computers.</span></span> <span data-ttu-id="d5804-169">I servizi interni e di terze parti possono essere rimossi tramite WMI, mentre i servizi del sistema operativo possono essere rimossi usando Sysocmgr.exe.</span><span class="sxs-lookup"><span data-stu-id="d5804-169">In-house and third-party services can be removed by using WMI, while operating system services can be removed by using Sysocmgr.exe.</span></span>

<span data-ttu-id="d5804-170">Quando si prepara la rimozione dei servizi, tenere presenti le seguenti informazioni:</span><span class="sxs-lookup"><span data-stu-id="d5804-170">When preparing to remove services, keep the following information in mind:</span></span>

-   <span data-ttu-id="d5804-171">Prima di rimuoverli, è necessario arrestare i servizi.</span><span class="sxs-lookup"><span data-stu-id="d5804-171">Services must be stopped before you remove them.</span></span> <span data-ttu-id="d5804-172">Se il servizio è in esecuzione quando si esegue il comando di eliminazione, il servizio viene contrassegnato per l'eliminazione, ma continua a essere eseguito fino a quando non viene interrotto e tutti gli handle aperti non vengono chiusi.</span><span class="sxs-lookup"><span data-stu-id="d5804-172">If the service is running when you issue the delete command, the service is marked for deletion, but it continues to run until it stops and all open handles are closed.</span></span>

    <span data-ttu-id="d5804-173">Se il servizio non viene mai arrestato, il servizio non verrà mai eliminato.</span><span class="sxs-lookup"><span data-stu-id="d5804-173">If the service is never stopped, that service will never be deleted.</span></span>

-   <span data-ttu-id="d5804-174">La rimozione di un servizio non comporta la rimozione del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="d5804-174">Removing a service does not remove the service's executable file.</span></span>

    <span data-ttu-id="d5804-175">La rimozione di un servizio tramite WMI comporta l'eliminazione delle voci del registro di sistema correlate in HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Services.</span><span class="sxs-lookup"><span data-stu-id="d5804-175">Removing a service by using WMI deletes the related registry entries under HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services.</span></span> <span data-ttu-id="d5804-176">Di conseguenza, il servizio non viene più installato e non è disponibile tramite lo snap-in servizi.</span><span class="sxs-lookup"><span data-stu-id="d5804-176">As a result, the service is no longer installed and is not available through the Services snap-in.</span></span> <span data-ttu-id="d5804-177">Tuttavia, WMI non elimina il file eseguibile, vale a dire che è possibile reinstallare facilmente il servizio.</span><span class="sxs-lookup"><span data-stu-id="d5804-177">However, WMI does not delete the executable file, meaning you could easily reinstall the service.</span></span> <span data-ttu-id="d5804-178">Per eliminare il file eseguibile, è necessario recuperare il nome del percorso e quindi eliminare il file.</span><span class="sxs-lookup"><span data-stu-id="d5804-178">To delete the executable file, you must retrieve the path name and then delete the file.</span></span>

-   <span data-ttu-id="d5804-179">La rimozione di un servizio di base di Windows 2000 (ad esempio, DHCP) tramite WMI Elimina le voci del registro di sistema per il servizio, ma non rimuove il collegamento dal menu strumenti di amministrazione o rimuove il servizio dalla procedura guidata componenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="d5804-179">Removing a base Windows 2000 service (for example, DHCP) by using WMI deletes the registry entries for that service but does not remove the shortcut from the Administrative Tools menu or remove the service from the Windows Components Wizard.</span></span> <span data-ttu-id="d5804-180">Questo può confondere chiunque tenti di determinare come è stato configurato il computer.</span><span class="sxs-lookup"><span data-stu-id="d5804-180">This can confuse anyone trying to determine how the computer has been configured.</span></span>

    <span data-ttu-id="d5804-181">Se ad esempio si rimuove il servizio DHCP utilizzando uno script WMI, il servizio DHCP non sarà più elencato nello snap-in servizi.</span><span class="sxs-lookup"><span data-stu-id="d5804-181">For example, if you remove the DHCP service by using a WMI script, the DHCP service is no longer listed in the Services snap-in.</span></span> <span data-ttu-id="d5804-182">Tuttavia, un collegamento non funzionale alla console DHCP rimane nel menu strumenti di amministrazione e, se si avvia la creazione guidata componenti di Windows, significa che il servizio DHCP è installato.</span><span class="sxs-lookup"><span data-stu-id="d5804-182">However, a nonfunctioning shortcut to the DHCP console remains in the Administrative Tools menu, and if you start the Windows Component Wizard, it indicates that the DHCP service is installed.</span></span>

    <span data-ttu-id="d5804-183">Per questo motivo, è consigliabile usare sempre Sysocmgr.exe per rimuovere a livello di codice i servizi di Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d5804-183">Because of this, you should always use Sysocmgr.exe to programmatically remove Windows 2000 services.</span></span>

## <a name="examples"></a><span data-ttu-id="d5804-184">Esempio</span><span class="sxs-lookup"><span data-stu-id="d5804-184">Examples</span></span>

<span data-ttu-id="d5804-185">Nell'esempio di codice VBScript riportato di seguito viene descritto come eliminare un servizio.</span><span class="sxs-lookup"><span data-stu-id="d5804-185">The following VBScript code sample describes how to delete a service.</span></span>


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



<span data-ttu-id="d5804-186">Nell'esempio di codice Perl seguente viene illustrato come eliminare un servizio.</span><span class="sxs-lookup"><span data-stu-id="d5804-186">The following Perl code sample describes how to delete a service.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d5804-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5804-187">Requirements</span></span>



| <span data-ttu-id="d5804-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5804-188">Requirement</span></span> | <span data-ttu-id="d5804-189">Valore</span><span class="sxs-lookup"><span data-stu-id="d5804-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5804-190">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5804-190">Minimum supported client</span></span><br/> | <span data-ttu-id="d5804-191">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5804-191">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5804-192">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5804-192">Minimum supported server</span></span><br/> | <span data-ttu-id="d5804-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5804-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5804-194">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d5804-194">Namespace</span></span><br/>                | <span data-ttu-id="d5804-195">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d5804-195">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d5804-196">MOF</span><span class="sxs-lookup"><span data-stu-id="d5804-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5804-197"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5804-197"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5804-198">DLL</span><span class="sxs-lookup"><span data-stu-id="d5804-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5804-199"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5804-199"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5804-200">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5804-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5804-201">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="d5804-201">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="d5804-202">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d5804-202">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="d5804-203">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="d5804-203">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="d5804-204">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="d5804-204">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

