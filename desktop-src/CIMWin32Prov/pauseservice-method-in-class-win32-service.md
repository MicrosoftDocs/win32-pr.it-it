---
description: Esegue un tentativo di sospensione del servizio.
ms.assetid: 5382457e-7f9c-48a5-9262-b815a1a4a605
ms.tgt_platform: multiple
title: Metodo PauseService della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b1dfa0b956442f74c17dd6a8c054c229a92466a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304517"
---
# <a name="pauseservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="9e0d3-103">Metodo PauseService della classe Win32_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="9e0d3-103">PauseService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="9e0d3-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** tenta di collocare il servizio nello stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-104">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="9e0d3-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="9e0d3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9e0d3-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9e0d3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9e0d3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e0d3-107">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="9e0d3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e0d3-108">Parameters</span></span>

<span data-ttu-id="9e0d3-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e0d3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e0d3-110">Return value</span></span>

<span data-ttu-id="9e0d3-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="9e0d3-112">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9e0d3-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9e0d3-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9e0d3-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9e0d3-114">**0**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-115">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-116">**1**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-117">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-118">**2**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-119">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-120">**3**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-121">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-122">**4**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-123">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-124">**5**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-125">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-126">**6**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-127">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-128">**7**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-129">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-130">**8**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-131">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-132">**9**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-133">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-134">**10**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-135">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-136">**11**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-137">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-138">**12**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-139">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-140">**13**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-141">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-142">**14**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-143">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-144">**15**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-145">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-146">**16**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-147">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-148">**17**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-149">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-150">**18**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-151">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-152">**19**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-153">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-154">**20**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-155">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-156">**21**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-157">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-158">**22**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-159">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-160">**23**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-161">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9e0d3-162">**24**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="9e0d3-163">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e0d3-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e0d3-164">Remarks</span></span>

<span data-ttu-id="9e0d3-165">Dopo aver determinato i servizi che possono essere arrestati o sospesi, è possibile usare i metodi [**StopService**](stopservice-method-in-class-win32-service.md) e [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) per arrestare e sospendere i servizi.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-165">After you have determined which services can be stopped or paused, you can use the [**StopService**](stopservice-method-in-class-win32-service.md) and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="9e0d3-166">La decisione di arrestare un servizio anziché sospenderla, o viceversa, dipende da diversi fattori, inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e0d3-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="9e0d3-167">Il servizio è in grado di essere sospeso?</span><span class="sxs-lookup"><span data-stu-id="9e0d3-167">Is the service capable of being paused?</span></span> <span data-ttu-id="9e0d3-168">In caso contrario, l'unica opzione è arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="9e0d3-169">È necessario continuare a gestire le richieste client per chiunque si sia già connessi al servizio?</span><span class="sxs-lookup"><span data-stu-id="9e0d3-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="9e0d3-170">In tal caso, sospendere un servizio in genere consente di gestire i client esistenti negando l'accesso ai nuovi client.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="9e0d3-171">Al contrario, quando si arresta un servizio, tutti i client vengono immediatamente disconnessi.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="9e0d3-172">È necessario riconfigurare un servizio e fare in modo che le modifiche abbiano effetto immediato?</span><span class="sxs-lookup"><span data-stu-id="9e0d3-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="9e0d3-173">Sebbene sia possibile modificare le proprietà del servizio mentre un servizio viene sospeso, la maggior parte di esse non diventano effettive fino a quando il servizio non viene effettivamente arrestato e riavviato.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="9e0d3-174">Il codice di scripting necessario per arrestare un servizio è quasi identico al codice necessario per sospendere il servizio.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="9e0d3-175">Esempio</span><span class="sxs-lookup"><span data-stu-id="9e0d3-175">Examples</span></span>

<span data-ttu-id="9e0d3-176">L'esempio di [sospensione dei servizi in esecuzione con un account VBScript specifico](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) mette in pausa tutti i servizi in esecuzione con l'account del servizio ipotetico "NETSVC".</span><span class="sxs-lookup"><span data-stu-id="9e0d3-176">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account "Netsvc".</span></span>

<span data-ttu-id="9e0d3-177">Nell'esempio di codice VBScript seguente viene illustrato come sospendere un servizio specifico dalle istanze del [**\_ servizio Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="9e0d3-177">The following VBScript code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="9e0d3-178">Il servizio deve supportare la sospensione ed essere già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-178">The service must support pausing and be running already.</span></span>

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.PauseService()
  if RetVal = 0 then 
   WScript.Echo "Service paused"   
  else
   if RetVal = 1 then 
    WScript.Echo "Pause not supported" 
   else WScript.Echo "An error occurred:" & RetVal
   End If
  End If
 else
  WScript.Echo "Service does not support pause"
 end if
next
```



<span data-ttu-id="9e0d3-179">Nell'esempio di codice Perl seguente viene illustrato come sospendere un servizio specifico dalle istanze del [**\_ servizio Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="9e0d3-179">The following Perl code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="9e0d3-180">Il servizio deve supportare la sospensione ed essere già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9e0d3-180">The service must support pausing and be running already.</span></span>

 


```
use strict;
use Win32::OLE;

my ($ServiceSet, $SupportsPause, $RetVal);  
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };
unless($@)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  if ($ServiceInst->{AcceptPause})
  {
   $RetVal = $ServiceInst->PauseService();
   if ($RetVal == 0)
   {
    print "\nService paused\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print "\nPause not supported\n" ;
    }
    else 
    {
     print "\nAn error occurred:", $RetVal, "\n";
    }
   } 
  }
  else
  {
   print "\nService does not support pause\n";
  }
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="9e0d3-181">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e0d3-181">Requirements</span></span>



| <span data-ttu-id="9e0d3-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e0d3-182">Requirement</span></span> | <span data-ttu-id="9e0d3-183">Valore</span><span class="sxs-lookup"><span data-stu-id="9e0d3-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e0d3-184">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e0d3-184">Minimum supported client</span></span><br/> | <span data-ttu-id="9e0d3-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e0d3-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e0d3-186">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e0d3-186">Minimum supported server</span></span><br/> | <span data-ttu-id="9e0d3-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e0d3-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e0d3-188">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9e0d3-188">Namespace</span></span><br/>                | <span data-ttu-id="9e0d3-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="9e0d3-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="9e0d3-190">MOF</span><span class="sxs-lookup"><span data-stu-id="9e0d3-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e0d3-191"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e0d3-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e0d3-192">DLL</span><span class="sxs-lookup"><span data-stu-id="9e0d3-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e0d3-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e0d3-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e0d3-194">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e0d3-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="9e0d3-195">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9e0d3-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9e0d3-196">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="9e0d3-197">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="9e0d3-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="9e0d3-198">**StopService**</span><span class="sxs-lookup"><span data-stu-id="9e0d3-198">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)
</dt> </dl>

 

