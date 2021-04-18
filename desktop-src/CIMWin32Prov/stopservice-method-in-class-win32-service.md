---
description: Inserisce il servizio, rappresentato dall' \_ oggetto servizio Win32, nello stato interrotto.
ms.assetid: cc2c71f7-12e6-4ba4-bfb4-f23845d798b5
ms.tgt_platform: multiple
title: Metodo StopService della classe Win32_Service (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90d979754a3d6f034c353229dbaa1b1dbaedea79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304873"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash"></a><span data-ttu-id="172de-103">Metodo StopService della classe Win32_Service (Sdoias. h)</span><span class="sxs-lookup"><span data-stu-id="172de-103">StopService method of the Win32_Service class (Sdoias.h)</span></span>

<span data-ttu-id="172de-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** posiziona il servizio, rappresentato dall' [**oggetto \_ servizio Win32**](win32-service.md) , nello stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="172de-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service, represented by the [**Win32\_Service**](win32-service.md) object, in the stopped state.</span></span>

<span data-ttu-id="172de-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="172de-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="172de-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="172de-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="172de-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="172de-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="172de-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="172de-108">Parameters</span></span>

<span data-ttu-id="172de-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="172de-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="172de-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="172de-110">Return value</span></span>

<span data-ttu-id="172de-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="172de-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="172de-112">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="172de-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="172de-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="172de-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="172de-114">**0**</span><span class="sxs-lookup"><span data-stu-id="172de-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="172de-115">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="172de-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="172de-116">**1**</span><span class="sxs-lookup"><span data-stu-id="172de-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="172de-117">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="172de-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="172de-118">**2**</span><span class="sxs-lookup"><span data-stu-id="172de-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="172de-119">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="172de-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="172de-120">**3**</span><span class="sxs-lookup"><span data-stu-id="172de-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="172de-121">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="172de-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="172de-122">**4**</span><span class="sxs-lookup"><span data-stu-id="172de-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="172de-123">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="172de-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="172de-124">**5**</span><span class="sxs-lookup"><span data-stu-id="172de-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="172de-125">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="172de-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="172de-126">**6**</span><span class="sxs-lookup"><span data-stu-id="172de-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="172de-127">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="172de-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="172de-128">**7**</span><span class="sxs-lookup"><span data-stu-id="172de-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="172de-129">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="172de-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="172de-130">**8**</span><span class="sxs-lookup"><span data-stu-id="172de-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="172de-131">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="172de-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="172de-132">**9**</span><span class="sxs-lookup"><span data-stu-id="172de-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="172de-133">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="172de-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="172de-134">**10**</span><span class="sxs-lookup"><span data-stu-id="172de-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="172de-135">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="172de-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="172de-136">**11**</span><span class="sxs-lookup"><span data-stu-id="172de-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="172de-137">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="172de-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="172de-138">**12**</span><span class="sxs-lookup"><span data-stu-id="172de-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="172de-139">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="172de-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="172de-140">**13**</span><span class="sxs-lookup"><span data-stu-id="172de-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="172de-141">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="172de-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="172de-142">**14**</span><span class="sxs-lookup"><span data-stu-id="172de-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="172de-143">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="172de-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="172de-144">**15**</span><span class="sxs-lookup"><span data-stu-id="172de-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="172de-145">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="172de-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="172de-146">**16**</span><span class="sxs-lookup"><span data-stu-id="172de-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="172de-147">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="172de-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="172de-148">**17**</span><span class="sxs-lookup"><span data-stu-id="172de-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="172de-149">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="172de-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="172de-150">**18**</span><span class="sxs-lookup"><span data-stu-id="172de-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="172de-151">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="172de-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="172de-152">**19**</span><span class="sxs-lookup"><span data-stu-id="172de-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="172de-153">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="172de-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="172de-154">**20**</span><span class="sxs-lookup"><span data-stu-id="172de-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="172de-155">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="172de-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="172de-156">**21**</span><span class="sxs-lookup"><span data-stu-id="172de-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="172de-157">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="172de-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="172de-158">**22**</span><span class="sxs-lookup"><span data-stu-id="172de-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="172de-159">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="172de-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="172de-160">**23**</span><span class="sxs-lookup"><span data-stu-id="172de-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="172de-161">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="172de-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="172de-162">**24**</span><span class="sxs-lookup"><span data-stu-id="172de-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="172de-163">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="172de-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="172de-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="172de-164">Remarks</span></span>

<span data-ttu-id="172de-165">Dopo aver determinato i servizi che possono essere arrestati o sospesi, è possibile usare i metodi **StopService** e [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) per arrestare e sospendere i servizi.</span><span class="sxs-lookup"><span data-stu-id="172de-165">After you have determined which services can be stopped or paused, you can use the **StopService** and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="172de-166">La decisione di arrestare un servizio anziché sospenderla, o viceversa, dipende da diversi fattori, inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="172de-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="172de-167">Il servizio è in grado di essere sospeso?</span><span class="sxs-lookup"><span data-stu-id="172de-167">Is the service capable of being paused?</span></span> <span data-ttu-id="172de-168">In caso contrario, l'unica opzione è arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="172de-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="172de-169">È necessario continuare a gestire le richieste client per chiunque si sia già connessi al servizio?</span><span class="sxs-lookup"><span data-stu-id="172de-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="172de-170">In tal caso, sospendere un servizio in genere consente di gestire i client esistenti negando l'accesso ai nuovi client.</span><span class="sxs-lookup"><span data-stu-id="172de-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="172de-171">Al contrario, quando si arresta un servizio, tutti i client vengono immediatamente disconnessi.</span><span class="sxs-lookup"><span data-stu-id="172de-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="172de-172">È necessario riconfigurare un servizio e fare in modo che le modifiche abbiano effetto immediato?</span><span class="sxs-lookup"><span data-stu-id="172de-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="172de-173">Sebbene sia possibile modificare le proprietà del servizio mentre un servizio viene sospeso, la maggior parte di esse non diventano effettive fino a quando il servizio non viene effettivamente arrestato e riavviato.</span><span class="sxs-lookup"><span data-stu-id="172de-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="172de-174">Il codice di scripting necessario per arrestare un servizio è quasi identico al codice necessario per sospendere il servizio.</span><span class="sxs-lookup"><span data-stu-id="172de-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

<span data-ttu-id="172de-175">Se si tenta di arrestare un servizio che dispone di servizi dipendenti in esecuzione, il metodo **StopService** ha esito negativo con un valore restituito pari a 3.</span><span class="sxs-lookup"><span data-stu-id="172de-175">If you attempt to stop a service which has dependent services running, the **StopService** method fails with a return value of 3.</span></span> <span data-ttu-id="172de-176">I servizi dipendenti devono essere arrestati per primi.</span><span class="sxs-lookup"><span data-stu-id="172de-176">The dependent services must be stopped first.</span></span>

<span data-ttu-id="172de-177">Se si arresta un servizio, controllare immediatamente il [**\_ servizio Win32**](win32-service.md).**Proprietà state** , perché il valore può comunque visualizzare il servizio come in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="172de-177">If you stop a service, then immediately check the [**Win32\_Service**](win32-service.md).**State** property, as the value may still show the service as running.</span></span>

## <a name="examples"></a><span data-ttu-id="172de-178">Esempio</span><span class="sxs-lookup"><span data-stu-id="172de-178">Examples</span></span>

<span data-ttu-id="172de-179">[Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell Sample imposta lo stato del servizio per i computer remoti.</span><span class="sxs-lookup"><span data-stu-id="172de-179">[The Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell sample Sets service state for remote machines.</span></span>

<span data-ttu-id="172de-180">L'esempio di [arresto di un servizio e del relativo VBScript dipendente](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) interrompe un servizio e tutti i servizi dipendenti.</span><span class="sxs-lookup"><span data-stu-id="172de-180">The [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript sample stops a service and all dependent services.</span></span>

<span data-ttu-id="172de-181">Nell'esempio di codice VBScript seguente viene illustrato come arrestare un servizio.</span><span class="sxs-lookup"><span data-stu-id="172de-181">The following VBScript code sample demonstrates how to shut down a service.</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StopService()
 if RetVal = 0 then 
  WScript.Echo "Service stopped" 
 elseif RetVal = 5 then 
  WScript.Echo "Service already stopped" 
 end if
next
```



<span data-ttu-id="172de-182">Nell'esempio di codice Perl seguente viene illustrato come arrestare un servizio.</span><span class="sxs-lookup"><span data-stu-id="172de-182">The following Perl code sample demonstrates how to shut down a service.</span></span>


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  my $Result = $ServiceInst->StopService();
  if ($Result == 0)
  {
   print "\nService stopped\n";
  }
  elsif ($Result == 5) 
  {
   print "\nService already stopped\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="172de-183">L'esempio di codice VBScript seguente mostra che non è possibile arrestare il servizio NetDDE fino a quando i servizi dipendenti non sono stati arrestati.</span><span class="sxs-lookup"><span data-stu-id="172de-183">The following VBScript code example shows that you cannot stop the NetDDE service until the dependent services have been stopped.</span></span> <span data-ttu-id="172de-184">Per eseguire lo script, verificare che il servizio NetDDE e i relativi servizi dipendenti siano in esecuzione tramite lo snap-in MMC Services. msc o il comando **net start** .</span><span class="sxs-lookup"><span data-stu-id="172de-184">To run the script, ensure that the NetDDE service and its dependent services are running by using the Services.msc MMC snap-in or the **Net Start** command.</span></span>

<span data-ttu-id="172de-185">La classe [**Win32 \_ DependentService**](win32-dependentservice.md) consente di individuare le dipendenze del servizio tramite un [associatori di](/windows/desktop/WmiSdk/associators-of-statement) query.</span><span class="sxs-lookup"><span data-stu-id="172de-185">The [**Win32\_DependentService**](win32-dependentservice.md) class allows you to locate service dependencies through an [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & _
    strComputer & "\root\cimv2")

Set objNetDDEservice = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")

WScript.Echo "NetDDE service state: " & objNetDDEService.State
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return  & _
    "  Service cannot be stopped because " & _
    "dependent services are running"

Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " _
        & "AssocClass=Win32_DependentService " & _
    "Role=Antecedent" )

For Each objService in colServiceList
   WScript.Echo "Dependent service: " & objService.Name & _
   "   State: " & objService.State
   WScript.Echo "Stopping dependent service " & objService.Name
   objService.StopService()    
Next

Wscript.Sleep 20000
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return
```



## <a name="requirements"></a><span data-ttu-id="172de-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="172de-186">Requirements</span></span>



| <span data-ttu-id="172de-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="172de-187">Requirement</span></span> | <span data-ttu-id="172de-188">Valore</span><span class="sxs-lookup"><span data-stu-id="172de-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="172de-189">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="172de-189">Minimum supported client</span></span><br/> | <span data-ttu-id="172de-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="172de-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="172de-191">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="172de-191">Minimum supported server</span></span><br/> | <span data-ttu-id="172de-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="172de-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="172de-193">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="172de-193">Namespace</span></span><br/>                | <span data-ttu-id="172de-194">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="172de-194">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="172de-195">Intestazione</span><span class="sxs-lookup"><span data-stu-id="172de-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="172de-196"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="172de-196"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="172de-197">MOF</span><span class="sxs-lookup"><span data-stu-id="172de-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="172de-198"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="172de-198"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="172de-199">DLL</span><span class="sxs-lookup"><span data-stu-id="172de-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="172de-200"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="172de-200"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="172de-201">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="172de-201">See also</span></span>

<dl> <dt>

<span data-ttu-id="172de-202">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="172de-202">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="172de-203">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="172de-203">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="172de-204">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="172de-204">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="172de-205">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="172de-205">**PauseService**</span></span>](pauseservice-method-in-class-win32-systemdriver.md)
</dt> </dl>

 

