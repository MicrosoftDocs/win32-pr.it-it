---
description: 'Metodo ResumeService della classe Win32_Service (provider WMI CIMWin32): tenta di posizionare il servizio di riferimento nello stato ripreso.'
ms.assetid: 3b4228bf-9ff5-44ab-bfe2-f7dd8fb62007
ms.tgt_platform: multiple
title: Metodo ResumeService della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73c21f282577207b63bcfa2d624c59ddfa3c9bcb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090979"
---
# <a name="resumeservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="de8c9-103">Metodo ResumeService della classe Win32_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="de8c9-103">ResumeService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="de8c9-104">Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** tenta di posizionare il servizio di riferimento nello stato ripreso.</span><span class="sxs-lookup"><span data-stu-id="de8c9-104">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="de8c9-105">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="de8c9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="de8c9-106">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="de8c9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="de8c9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de8c9-107">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="de8c9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="de8c9-108">Parameters</span></span>

<span data-ttu-id="de8c9-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="de8c9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de8c9-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de8c9-110">Return value</span></span>

<span data-ttu-id="de8c9-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="de8c9-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="de8c9-112">Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="de8c9-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="de8c9-113">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="de8c9-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="de8c9-114">**0**</span><span class="sxs-lookup"><span data-stu-id="de8c9-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-115">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="de8c9-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-116">**1**</span><span class="sxs-lookup"><span data-stu-id="de8c9-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-117">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="de8c9-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-118">**2**</span><span class="sxs-lookup"><span data-stu-id="de8c9-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-119">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="de8c9-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-120">**3**</span><span class="sxs-lookup"><span data-stu-id="de8c9-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-121">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="de8c9-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-122">**4**</span><span class="sxs-lookup"><span data-stu-id="de8c9-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-123">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="de8c9-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-124">**5**</span><span class="sxs-lookup"><span data-stu-id="de8c9-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-125">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="de8c9-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-126">**6**</span><span class="sxs-lookup"><span data-stu-id="de8c9-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-127">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="de8c9-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-128">**7**</span><span class="sxs-lookup"><span data-stu-id="de8c9-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-129">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="de8c9-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-130">**8**</span><span class="sxs-lookup"><span data-stu-id="de8c9-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-131">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="de8c9-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-132">**9**</span><span class="sxs-lookup"><span data-stu-id="de8c9-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-133">Impossibile trovare il percorso della directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="de8c9-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-134">**10**</span><span class="sxs-lookup"><span data-stu-id="de8c9-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-135">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="de8c9-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-136">**11**</span><span class="sxs-lookup"><span data-stu-id="de8c9-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-137">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="de8c9-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-138">**12**</span><span class="sxs-lookup"><span data-stu-id="de8c9-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-139">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="de8c9-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-140">**13**</span><span class="sxs-lookup"><span data-stu-id="de8c9-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-141">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="de8c9-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-142">**14**</span><span class="sxs-lookup"><span data-stu-id="de8c9-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-143">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="de8c9-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-144">**15**</span><span class="sxs-lookup"><span data-stu-id="de8c9-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-145">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="de8c9-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-146">**16**</span><span class="sxs-lookup"><span data-stu-id="de8c9-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-147">Questo servizio viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="de8c9-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-148">**17**</span><span class="sxs-lookup"><span data-stu-id="de8c9-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-149">Il servizio non ha thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="de8c9-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-150">**18**</span><span class="sxs-lookup"><span data-stu-id="de8c9-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-151">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="de8c9-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-152">**19**</span><span class="sxs-lookup"><span data-stu-id="de8c9-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-153">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="de8c9-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-154">**20**</span><span class="sxs-lookup"><span data-stu-id="de8c9-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-155">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="de8c9-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-156">**21**</span><span class="sxs-lookup"><span data-stu-id="de8c9-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-157">Al servizio sono stati passati parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="de8c9-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-158">**22**</span><span class="sxs-lookup"><span data-stu-id="de8c9-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-159">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="de8c9-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-160">**23**</span><span class="sxs-lookup"><span data-stu-id="de8c9-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-161">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="de8c9-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="de8c9-162">**24**</span><span class="sxs-lookup"><span data-stu-id="de8c9-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="de8c9-163">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="de8c9-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de8c9-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="de8c9-164">Remarks</span></span>

<span data-ttu-id="de8c9-165">Anche se potrebbe sembrare che non vi sia alcuna differenza pratica tra un servizio arrestato e un servizio in pausa, i due stati appaiono in modo diverso rispetto a Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="de8c9-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="de8c9-166">Un servizio arrestato è un servizio che non è in esecuzione e deve eseguire l'intera procedura di avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="de8c9-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="de8c9-167">Un servizio sospeso, tuttavia, è ancora in esecuzione, ma è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="de8c9-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="de8c9-168">Per questo problema, un servizio sospeso non deve eseguire l'intera procedura di avvio del servizio, ma richiede una procedura diversa per riprendere il funzionamento.</span><span class="sxs-lookup"><span data-stu-id="de8c9-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="de8c9-169">È necessario utilizzare il metodo appropriato per avviare un servizio arrestato o per riprendere un servizio sospeso.</span><span class="sxs-lookup"><span data-stu-id="de8c9-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="de8c9-170">I [**metodi \_ startService**](win32-service.md) e **ResumeService** del servizio Win32 devono essere usati nelle situazioni seguenti: [](startservice-method-in-class-win32-service.md)</span><span class="sxs-lookup"><span data-stu-id="de8c9-170">The [**Win32\_Service**](win32-service.md) methods [**StartService**](startservice-method-in-class-win32-service.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="de8c9-171">Se un servizio è attualmente arrestato, è necessario usare il [**metodo StartService**](startservice-method-in-class-win32-service.md) per riavviarlo. **ResumeService** non può avviare un servizio attualmente arrestato.</span><span class="sxs-lookup"><span data-stu-id="de8c9-171">If a service is currently stopped, you must use the [**StartService**](startservice-method-in-class-win32-service.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="de8c9-172">Se un servizio è in pausa, è necessario usare **ResumeService**.</span><span class="sxs-lookup"><span data-stu-id="de8c9-172">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="de8c9-173">Se si usa il [**metodo StartService**](startservice-method-in-class-win32-service.md) in un servizio sospeso, viene visualizzato il messaggio "Il servizio è già in esecuzione".</span><span class="sxs-lookup"><span data-stu-id="de8c9-173">If you use the [**StartService**](startservice-method-in-class-win32-service.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="de8c9-174">Tuttavia, il servizio rimane in pausa fino a quando non viene inviato il codice di controllo del servizio di ripresa.</span><span class="sxs-lookup"><span data-stu-id="de8c9-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="de8c9-175">Esempio</span><span class="sxs-lookup"><span data-stu-id="de8c9-175">Examples</span></span>

<span data-ttu-id="de8c9-176">[L'esempio Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript riavvia tutti i servizi di avvio automatico sospesi.</span><span class="sxs-lookup"><span data-stu-id="de8c9-176">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

<span data-ttu-id="de8c9-177">Nell'esempio di codice VBScript seguente viene descritto come riprendere un servizio sospeso dalle istanze del [**servizio Win32. \_**](win32-service.md)</span><span class="sxs-lookup"><span data-stu-id="de8c9-177">The following VBScript code sample describes how to resume a paused service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="de8c9-178">Il servizio deve supportare la sospensione ed essere già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="de8c9-178">The service must support pausing and be running already.</span></span>

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.ResumeService()
  if RetVal = 0 then 
   WScript.Echo "Service resumed"   
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



<span data-ttu-id="de8c9-179">L'esempio di codice Perl seguente descrive come riprendere un servizio sospeso dalle istanze del [**servizio Win32. \_**](win32-service.md)</span><span class="sxs-lookup"><span data-stu-id="de8c9-179">The following Perl code sample describes how to resume a paused service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="de8c9-180">Il servizio deve supportare la sospensione ed essere già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="de8c9-180">The service must support pausing and be running already.</span></span>

 


```Perl
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $Service (in $ServiceSet)
 {
  my $SupportsPause = $Service->{AcceptPause};
  if ($SupportsPause)
  {
   my $RetVal = $Service->ResumeService();
   if ($RetVal == 0)
   {
    print "\nService resumed\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print STDERR "\nPause not supported\n";
    }
    else
    {
     print STDERR "\nAn error occurred: ", $RetVal, "\n";
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
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="de8c9-181">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de8c9-181">Requirements</span></span>



| <span data-ttu-id="de8c9-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="de8c9-182">Requirement</span></span> | <span data-ttu-id="de8c9-183">Valore</span><span class="sxs-lookup"><span data-stu-id="de8c9-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de8c9-184">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de8c9-184">Minimum supported client</span></span><br/> | <span data-ttu-id="de8c9-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de8c9-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de8c9-186">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de8c9-186">Minimum supported server</span></span><br/> | <span data-ttu-id="de8c9-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de8c9-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de8c9-188">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="de8c9-188">Namespace</span></span><br/>                | <span data-ttu-id="de8c9-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="de8c9-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="de8c9-190">MOF</span><span class="sxs-lookup"><span data-stu-id="de8c9-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de8c9-191"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="de8c9-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="de8c9-192">DLL</span><span class="sxs-lookup"><span data-stu-id="de8c9-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de8c9-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de8c9-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de8c9-194">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de8c9-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="de8c9-195">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="de8c9-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="de8c9-196">**Servizio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="de8c9-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="de8c9-197">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="de8c9-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

