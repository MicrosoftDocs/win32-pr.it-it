---
description: Tenta di collocare il servizio a cui si fa riferimento nello stato di avvio.
ms.assetid: b7a815a2-7bf6-436f-b3b4-de55eeb2de0e
ms.tgt_platform: multiple
title: Metodo StartService della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb530766781de4e23cc86778c1597a5c5c2a1014
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966134"
---
# <a name="startservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="c6322-103">Metodo StartService della classe Win32_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="c6322-103">StartService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c6322-104">Il metodo **StartService** tenta di collocare il servizio a cui si fa riferimento nello stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="c6322-104">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="c6322-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c6322-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c6322-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c6322-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c6322-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6322-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="c6322-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6322-108">Parameters</span></span>

<span data-ttu-id="c6322-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c6322-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6322-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6322-110">Return value</span></span>

<span data-ttu-id="c6322-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="c6322-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="c6322-112">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c6322-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c6322-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c6322-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c6322-114">**0**</span><span class="sxs-lookup"><span data-stu-id="c6322-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-115">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="c6322-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-116">**1**</span><span class="sxs-lookup"><span data-stu-id="c6322-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-117">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="c6322-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-118">**2**</span><span class="sxs-lookup"><span data-stu-id="c6322-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-119">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="c6322-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-120">**3**</span><span class="sxs-lookup"><span data-stu-id="c6322-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-121">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="c6322-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-122">**4**</span><span class="sxs-lookup"><span data-stu-id="c6322-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-123">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="c6322-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-124">**5**</span><span class="sxs-lookup"><span data-stu-id="c6322-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-125">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="c6322-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-126">**6**</span><span class="sxs-lookup"><span data-stu-id="c6322-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-127">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="c6322-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-128">**7**</span><span class="sxs-lookup"><span data-stu-id="c6322-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-129">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="c6322-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-130">**8**</span><span class="sxs-lookup"><span data-stu-id="c6322-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-131">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="c6322-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-132">**9**</span><span class="sxs-lookup"><span data-stu-id="c6322-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-133">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="c6322-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-134">**10**</span><span class="sxs-lookup"><span data-stu-id="c6322-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-135">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c6322-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-136">**11**</span><span class="sxs-lookup"><span data-stu-id="c6322-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-137">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="c6322-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-138">**12**</span><span class="sxs-lookup"><span data-stu-id="c6322-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-139">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c6322-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-140">**13**</span><span class="sxs-lookup"><span data-stu-id="c6322-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-141">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="c6322-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-142">**14**</span><span class="sxs-lookup"><span data-stu-id="c6322-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-143">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c6322-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-144">**15**</span><span class="sxs-lookup"><span data-stu-id="c6322-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-145">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c6322-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-146">**16**</span><span class="sxs-lookup"><span data-stu-id="c6322-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-147">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c6322-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-148">**17**</span><span class="sxs-lookup"><span data-stu-id="c6322-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-149">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c6322-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-150">**18**</span><span class="sxs-lookup"><span data-stu-id="c6322-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-151">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="c6322-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-152">**19**</span><span class="sxs-lookup"><span data-stu-id="c6322-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-153">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="c6322-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-154">**20**</span><span class="sxs-lookup"><span data-stu-id="c6322-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-155">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="c6322-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-156">**21**</span><span class="sxs-lookup"><span data-stu-id="c6322-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-157">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="c6322-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-158">**22**</span><span class="sxs-lookup"><span data-stu-id="c6322-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-159">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="c6322-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-160">**23**</span><span class="sxs-lookup"><span data-stu-id="c6322-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-161">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c6322-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c6322-162">**24**</span><span class="sxs-lookup"><span data-stu-id="c6322-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="c6322-163">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c6322-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6322-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6322-164">Remarks</span></span>

<span data-ttu-id="c6322-165">Sebbene sia possibile che non esistano differenze pratiche tra un servizio interrotto e un servizio sospeso, i due stati vengono visualizzati in modo diverso rispetto a SCM.</span><span class="sxs-lookup"><span data-stu-id="c6322-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="c6322-166">Un servizio interrotto è un servizio che non è in esecuzione e che deve seguire l'intera procedura di avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="c6322-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="c6322-167">Un servizio sospeso, tuttavia, è ancora in esecuzione, ma il suo funzionamento è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="c6322-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="c6322-168">Per questo motivo, non è necessario che un servizio sospeso attraversi l'intera procedura di avvio del servizio, ma è necessaria una procedura diversa per riprendere il funzionamento.</span><span class="sxs-lookup"><span data-stu-id="c6322-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="c6322-169">È necessario utilizzare il metodo appropriato per avviare un servizio che è stato interrotto o per riprendere un servizio che è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="c6322-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="c6322-170">I metodi del [**\_ servizio Win32**](win32-service.md) **StartService** e [**ResumeService**](resumeservice-method-in-class-win32-service.md) devono essere utilizzati nelle situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6322-170">The [**Win32\_Service**](win32-service.md) methods **StartService** and [**ResumeService**](resumeservice-method-in-class-win32-service.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="c6322-171">Se un servizio è attualmente arrestato, è necessario usare il metodo **StartService** per riavviarlo; [**ResumeService**](resumeservice-method-in-class-win32-service.md) non è in grado di avviare un servizio attualmente arrestato.</span><span class="sxs-lookup"><span data-stu-id="c6322-171">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](resumeservice-method-in-class-win32-service.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="c6322-172">Se un servizio viene sospeso, è necessario utilizzare [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="c6322-172">If a service is paused, you must use [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span></span> <span data-ttu-id="c6322-173">Se si usa il metodo **StartService** in un servizio in pausa, viene visualizzato il messaggio "il servizio è già in esecuzione".</span><span class="sxs-lookup"><span data-stu-id="c6322-173">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="c6322-174">Tuttavia, il servizio rimane sospeso fino a quando non viene inviato il codice di controllo del servizio di ripresa.</span><span class="sxs-lookup"><span data-stu-id="c6322-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="c6322-175">Se si avvia un servizio interrotto che dipende da un altro servizio, vengono avviati entrambi i servizi.</span><span class="sxs-lookup"><span data-stu-id="c6322-175">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="c6322-176">Quando un servizio viene avviato con questo metodo, tutti i servizi dipendenti non vengono avviati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c6322-176">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="c6322-177">Per individuare i dipendenti e avviarli separatamente, è necessario utilizzare la classe di associazione [**Win32 \_ DependentService**](win32-dependentservice.md) e gli [associatori di](/windows/desktop/WmiSdk/associators-of-statement) query.</span><span class="sxs-lookup"><span data-stu-id="c6322-177">You must use the association class [**Win32\_DependentService**](win32-dependentservice.md) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="examples"></a><span data-ttu-id="c6322-178">Esempio</span><span class="sxs-lookup"><span data-stu-id="c6322-178">Examples</span></span>

<span data-ttu-id="c6322-179">L'esempio di [abilitazione remota](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) di PowerShell per RDP Abilita in remoto il servizio desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c6322-179">The [Remotely Enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell sample remotely enables the Remote Desktop service.</span></span>

<span data-ttu-id="c6322-180">L'esempio di [arresto, avvio, abilitazione o disabilitazione](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) di PowerShell per il servizio avvia, arresta, Abilita o Disabilita un servizio.</span><span class="sxs-lookup"><span data-stu-id="c6322-180">The [Stop, Start, Enable or Disable Service](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) PowerShell sample starts, stops, enables, or disables a service.</span></span>

<span data-ttu-id="c6322-181">Nell'esempio di codice VBSScript seguente viene illustrato come avviare un servizio specifico dalle istanze [**del \_ servizio Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="c6322-181">The following VBSScript code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StartService()
 if RetVal = 0 then WScript.Echo "Service started"
 if RetVal = 10 then WScript.Echo "Service already running"
next
```



<span data-ttu-id="c6322-182">Nell'esempio di codice Perl seguente viene illustrato come avviare un servizio specifico dalle istanze [**del \_ servizio Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="c6322-182">The following Perl code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if(!$@ && defined $ServiceSet)
{
 foreach my $service (in $ServiceSet)
 {
  my $Result = $service->StartService();
  if ($Result == 0) 
  {
   print "\nService started\n";
  }
  elsif ($Result == 10)
  {
   print "\nService already running\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="c6322-183">Il seguente codice VBScript di esempio, NetDDE, dipende dal servizio NetDDEDSDM.</span><span class="sxs-lookup"><span data-stu-id="c6322-183">The following VBScript code example, NetDDE, is dependent on the NetDDEDSDM service.</span></span> <span data-ttu-id="c6322-184">Lo script individua la classe da cui dipende NetDDE e la avvia, che non avvia automaticamente NetDDE.</span><span class="sxs-lookup"><span data-stu-id="c6322-184">The script locates the class on which NetDDE depends and starts it, which does not automatically start NetDDE.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Stop NetDDE if it is running
Set objNetDDEService = objWMIService.Get("Win32_Service.Name='NetDDE'")
Return = objNetDDEService.StopService()

' NetDDE is in the dependent role to another service
Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " & "AssocClass=Win32_DependentService " & "Role=Dependent" )

' start the service on which NetDDE is dependent
For Each objService in colServiceList
    WScript.Echo "Starting " & objService.Name
    Return = objService.StartService()
    If Return = 0 Then
        WScript.Echo "Parent service " & objService.Name & " started successfully"
    Else
        WScript.Echo "Parent service " & objService.Name & " did not start. Return = " & Return
    End If
Next

' NetDDE is still stopped
Set objNetDDEService = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")
WScript.Echo "Dependent NetDDE service is " & objNetDDEService.State
```



## <a name="requirements"></a><span data-ttu-id="c6322-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6322-185">Requirements</span></span>



| <span data-ttu-id="c6322-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6322-186">Requirement</span></span> | <span data-ttu-id="c6322-187">Valore</span><span class="sxs-lookup"><span data-stu-id="c6322-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6322-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6322-188">Minimum supported client</span></span><br/> | <span data-ttu-id="c6322-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6322-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6322-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6322-190">Minimum supported server</span></span><br/> | <span data-ttu-id="c6322-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6322-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6322-192">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c6322-192">Namespace</span></span><br/>                | <span data-ttu-id="c6322-193">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c6322-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c6322-194">MOF</span><span class="sxs-lookup"><span data-stu-id="c6322-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6322-195"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6322-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6322-196">DLL</span><span class="sxs-lookup"><span data-stu-id="c6322-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6322-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6322-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6322-198">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6322-198">See also</span></span>

<dl> <dt>

<span data-ttu-id="c6322-199">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6322-199">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c6322-200">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="c6322-200">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="c6322-201">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="c6322-201">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

