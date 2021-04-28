---
description: 'Metodo StartService della classe Win32_Service (provider WMI CIMWin32): tenta di inserire il servizio di riferimento nello stato di avvio.'
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
ms.openlocfilehash: a630b9d926ff5377312f1c67630a20816ab38b6c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086159"
---
# <a name="startservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="aabfd-103">Metodo StartService della classe Win32_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="aabfd-103">StartService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="aabfd-104">Il **metodo StartService** tenta di inserire il servizio a cui si fa riferimento nello stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="aabfd-104">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="aabfd-105">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="aabfd-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="aabfd-106">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="aabfd-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="aabfd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aabfd-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="aabfd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aabfd-108">Parameters</span></span>

<span data-ttu-id="aabfd-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="aabfd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aabfd-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aabfd-110">Return value</span></span>

<span data-ttu-id="aabfd-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="aabfd-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="aabfd-112">Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="aabfd-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="aabfd-113">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="aabfd-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="aabfd-114">**0**</span><span class="sxs-lookup"><span data-stu-id="aabfd-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-115">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="aabfd-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-116">**1**</span><span class="sxs-lookup"><span data-stu-id="aabfd-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-117">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="aabfd-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-118">**2**</span><span class="sxs-lookup"><span data-stu-id="aabfd-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-119">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="aabfd-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-120">**3**</span><span class="sxs-lookup"><span data-stu-id="aabfd-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-121">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="aabfd-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-122">**4**</span><span class="sxs-lookup"><span data-stu-id="aabfd-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-123">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="aabfd-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-124">**5**</span><span class="sxs-lookup"><span data-stu-id="aabfd-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-125">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="aabfd-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-126">**6**</span><span class="sxs-lookup"><span data-stu-id="aabfd-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-127">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="aabfd-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-128">**7**</span><span class="sxs-lookup"><span data-stu-id="aabfd-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-129">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="aabfd-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-130">**8**</span><span class="sxs-lookup"><span data-stu-id="aabfd-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-131">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="aabfd-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-132">**9**</span><span class="sxs-lookup"><span data-stu-id="aabfd-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-133">Impossibile trovare il percorso della directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="aabfd-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-134">**10**</span><span class="sxs-lookup"><span data-stu-id="aabfd-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-135">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="aabfd-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-136">**11**</span><span class="sxs-lookup"><span data-stu-id="aabfd-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-137">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="aabfd-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-138">**12**</span><span class="sxs-lookup"><span data-stu-id="aabfd-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-139">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="aabfd-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-140">**13**</span><span class="sxs-lookup"><span data-stu-id="aabfd-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-141">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="aabfd-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-142">**14**</span><span class="sxs-lookup"><span data-stu-id="aabfd-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-143">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="aabfd-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-144">**15**</span><span class="sxs-lookup"><span data-stu-id="aabfd-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-145">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="aabfd-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-146">**16**</span><span class="sxs-lookup"><span data-stu-id="aabfd-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-147">Questo servizio viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="aabfd-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-148">**17**</span><span class="sxs-lookup"><span data-stu-id="aabfd-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-149">Il servizio non ha thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="aabfd-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-150">**18**</span><span class="sxs-lookup"><span data-stu-id="aabfd-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-151">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="aabfd-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-152">**19**</span><span class="sxs-lookup"><span data-stu-id="aabfd-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-153">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="aabfd-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-154">**20**</span><span class="sxs-lookup"><span data-stu-id="aabfd-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-155">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="aabfd-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-156">**21**</span><span class="sxs-lookup"><span data-stu-id="aabfd-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-157">Al servizio sono stati passati parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="aabfd-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-158">**22**</span><span class="sxs-lookup"><span data-stu-id="aabfd-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-159">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="aabfd-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-160">**23**</span><span class="sxs-lookup"><span data-stu-id="aabfd-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-161">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="aabfd-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="aabfd-162">**24**</span><span class="sxs-lookup"><span data-stu-id="aabfd-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="aabfd-163">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="aabfd-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aabfd-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="aabfd-164">Remarks</span></span>

<span data-ttu-id="aabfd-165">Anche se potrebbe sembrare che non vi sia alcuna differenza pratica tra un servizio arrestato e un servizio in pausa, i due stati appaiono in modo diverso rispetto a Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="aabfd-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="aabfd-166">Un servizio arrestato è un servizio che non è in esecuzione e deve eseguire l'intera procedura di avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="aabfd-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="aabfd-167">Un servizio sospeso, tuttavia, è ancora in esecuzione, ma ha avuto il suo funzionamento sospeso.</span><span class="sxs-lookup"><span data-stu-id="aabfd-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="aabfd-168">Per questo problema, un servizio sospeso non deve eseguire l'intera procedura di avvio del servizio, ma richiede una procedura diversa per riprendere il funzionamento.</span><span class="sxs-lookup"><span data-stu-id="aabfd-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="aabfd-169">È necessario utilizzare il metodo appropriato per avviare un servizio arrestato o per riprendere un servizio sospeso.</span><span class="sxs-lookup"><span data-stu-id="aabfd-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="aabfd-170">I [**metodi \_ startService**](win32-service.md) e [**ResumeService**](resumeservice-method-in-class-win32-service.md) del servizio Win32 devono essere usati nelle situazioni seguenti: </span><span class="sxs-lookup"><span data-stu-id="aabfd-170">The [**Win32\_Service**](win32-service.md) methods **StartService** and [**ResumeService**](resumeservice-method-in-class-win32-service.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="aabfd-171">Se un servizio è attualmente arrestato, è necessario usare il **metodo StartService** per riavviarlo. [**ResumeService**](resumeservice-method-in-class-win32-service.md) non può avviare un servizio attualmente arrestato.</span><span class="sxs-lookup"><span data-stu-id="aabfd-171">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](resumeservice-method-in-class-win32-service.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="aabfd-172">Se un servizio è in pausa, è necessario usare [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="aabfd-172">If a service is paused, you must use [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span></span> <span data-ttu-id="aabfd-173">Se si usa il **metodo StartService** in un servizio sospeso, viene visualizzato il messaggio "Il servizio è già in esecuzione".</span><span class="sxs-lookup"><span data-stu-id="aabfd-173">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="aabfd-174">Tuttavia, il servizio rimane in pausa fino a quando non viene inviato il codice di controllo del servizio di ripresa.</span><span class="sxs-lookup"><span data-stu-id="aabfd-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="aabfd-175">Se si avvia un servizio arrestato che dipende da un altro servizio, vengono avviati entrambi i servizi.</span><span class="sxs-lookup"><span data-stu-id="aabfd-175">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="aabfd-176">Quando un servizio viene avviato con questo metodo, i servizi dipendenti non vengono avviati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="aabfd-176">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="aabfd-177">È necessario usare la classe di associazione [**Win32 \_ DependentService**](win32-dependentservice.md) e la query [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) per individuare i dipendenti e avviarli separatamente.</span><span class="sxs-lookup"><span data-stu-id="aabfd-177">You must use the association class [**Win32\_DependentService**](win32-dependentservice.md) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="examples"></a><span data-ttu-id="aabfd-178">Esempio</span><span class="sxs-lookup"><span data-stu-id="aabfd-178">Examples</span></span>

<span data-ttu-id="aabfd-179">L'esempio di PowerShell [Remotely Enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) abilita il Desktop remoto remoto.</span><span class="sxs-lookup"><span data-stu-id="aabfd-179">The [Remotely Enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell sample remotely enables the Remote Desktop service.</span></span>

<span data-ttu-id="aabfd-180">L'esempio di PowerShell [Arresta, Avvia, Abilita](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) o Disabilita servizio avvia, arresta, abilita o disabilita un servizio.</span><span class="sxs-lookup"><span data-stu-id="aabfd-180">The [Stop, Start, Enable or Disable Service](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) PowerShell sample starts, stops, enables, or disables a service.</span></span>

<span data-ttu-id="aabfd-181">L'esempio di codice VBSScript seguente illustra come avviare un servizio specifico da istanze del [**servizio Win32. \_**](win32-service.md)</span><span class="sxs-lookup"><span data-stu-id="aabfd-181">The following VBSScript code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StartService()
 if RetVal = 0 then WScript.Echo "Service started"
 if RetVal = 10 then WScript.Echo "Service already running"
next
```



<span data-ttu-id="aabfd-182">Nell'esempio di codice Perl seguente viene illustrato come avviare un servizio specifico da istanze del [**servizio Win32. \_**](win32-service.md)</span><span class="sxs-lookup"><span data-stu-id="aabfd-182">The following Perl code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


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



<span data-ttu-id="aabfd-183">L'esempio di codice VBScript seguente, NetDDE, dipende dal servizio NetDDEDSDM.</span><span class="sxs-lookup"><span data-stu-id="aabfd-183">The following VBScript code example, NetDDE, is dependent on the NetDDEDSDM service.</span></span> <span data-ttu-id="aabfd-184">Lo script individua la classe da cui dipende NetDDE e lo avvia, che non avvia automaticamente NetDDE.</span><span class="sxs-lookup"><span data-stu-id="aabfd-184">The script locates the class on which NetDDE depends and starts it, which does not automatically start NetDDE.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="aabfd-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aabfd-185">Requirements</span></span>



| <span data-ttu-id="aabfd-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="aabfd-186">Requirement</span></span> | <span data-ttu-id="aabfd-187">Valore</span><span class="sxs-lookup"><span data-stu-id="aabfd-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aabfd-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aabfd-188">Minimum supported client</span></span><br/> | <span data-ttu-id="aabfd-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aabfd-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aabfd-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aabfd-190">Minimum supported server</span></span><br/> | <span data-ttu-id="aabfd-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aabfd-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aabfd-192">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aabfd-192">Namespace</span></span><br/>                | <span data-ttu-id="aabfd-193">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="aabfd-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aabfd-194">MOF</span><span class="sxs-lookup"><span data-stu-id="aabfd-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aabfd-195"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="aabfd-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aabfd-196">DLL</span><span class="sxs-lookup"><span data-stu-id="aabfd-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aabfd-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aabfd-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aabfd-198">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aabfd-198">See also</span></span>

<dl> <dt>

<span data-ttu-id="aabfd-199">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aabfd-199">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="aabfd-200">**Servizio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="aabfd-200">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="aabfd-201">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="aabfd-201">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

