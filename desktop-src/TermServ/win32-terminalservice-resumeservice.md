---
title: Metodo ResumeService della classe Win32_Service (Servizi Desktop remoto)
description: 'Metodo ResumeService della classe Win32_Service (Servizi Desktop remoto): tenta di posizionare il servizio di riferimento nello stato ripreso.'
ms.assetid: AA020A0A-E69C-44AB-B259-A73460728770
ms.tgt_platform: multiple
keywords:
- Metodo ResumeService Servizi Desktop remoto
- Metodo ResumeService Servizi Desktop remoto , Win32_Service classe
- Win32_Service classe Servizi Desktop remoto , metodo ResumeService
topic_type:
- apiref
api_name:
- Win32_Service.ResumeService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f8e7dcfc9b9bd5b408e36d8a909aa10c84519c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090589"
---
# <a name="resumeservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="8f152-106">Metodo ResumeService della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="8f152-106">ResumeService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="8f152-107">Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** tenta di posizionare il servizio di riferimento nello stato ripreso.</span><span class="sxs-lookup"><span data-stu-id="8f152-107">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="8f152-108">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8f152-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8f152-109">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8f152-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f152-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f152-110">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="8f152-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f152-111">Parameters</span></span>

<span data-ttu-id="8f152-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8f152-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8f152-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f152-113">Return value</span></span>

<span data-ttu-id="8f152-114">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="8f152-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="8f152-115">Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8f152-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8f152-116">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8f152-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8f152-117">**0**</span><span class="sxs-lookup"><span data-stu-id="8f152-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-118">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="8f152-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-119">**1**</span><span class="sxs-lookup"><span data-stu-id="8f152-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-120">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="8f152-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-121">**2**</span><span class="sxs-lookup"><span data-stu-id="8f152-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-122">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="8f152-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-123">**3**</span><span class="sxs-lookup"><span data-stu-id="8f152-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-124">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="8f152-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-125">**4**</span><span class="sxs-lookup"><span data-stu-id="8f152-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-126">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="8f152-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-127">**5**</span><span class="sxs-lookup"><span data-stu-id="8f152-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-128">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="8f152-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-129">**6**</span><span class="sxs-lookup"><span data-stu-id="8f152-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-130">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="8f152-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-131">**7**</span><span class="sxs-lookup"><span data-stu-id="8f152-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-132">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="8f152-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-133">**8**</span><span class="sxs-lookup"><span data-stu-id="8f152-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-134">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="8f152-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-135">**9**</span><span class="sxs-lookup"><span data-stu-id="8f152-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-136">Impossibile trovare il percorso della directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="8f152-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-137">**10**</span><span class="sxs-lookup"><span data-stu-id="8f152-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-138">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8f152-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-139">**11**</span><span class="sxs-lookup"><span data-stu-id="8f152-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-140">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="8f152-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-141">**12**</span><span class="sxs-lookup"><span data-stu-id="8f152-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-142">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="8f152-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-143">**13**</span><span class="sxs-lookup"><span data-stu-id="8f152-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-144">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="8f152-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-145">**14**</span><span class="sxs-lookup"><span data-stu-id="8f152-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-146">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="8f152-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-147">**15**</span><span class="sxs-lookup"><span data-stu-id="8f152-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-148">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="8f152-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-149">**16**</span><span class="sxs-lookup"><span data-stu-id="8f152-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-150">Questo servizio viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="8f152-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-151">**17**</span><span class="sxs-lookup"><span data-stu-id="8f152-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-152">Il servizio non ha thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8f152-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-153">**18**</span><span class="sxs-lookup"><span data-stu-id="8f152-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-154">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="8f152-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-155">**19**</span><span class="sxs-lookup"><span data-stu-id="8f152-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-156">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="8f152-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-157">**20**</span><span class="sxs-lookup"><span data-stu-id="8f152-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-158">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="8f152-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-159">**21**</span><span class="sxs-lookup"><span data-stu-id="8f152-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-160">Al servizio sono stati passati parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="8f152-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-161">**22**</span><span class="sxs-lookup"><span data-stu-id="8f152-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-162">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="8f152-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-163">**23**</span><span class="sxs-lookup"><span data-stu-id="8f152-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-164">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="8f152-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8f152-165">**24**</span><span class="sxs-lookup"><span data-stu-id="8f152-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="8f152-166">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="8f152-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f152-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f152-167">Remarks</span></span>

<span data-ttu-id="8f152-168">Anche se potrebbe non esserci alcuna differenza pratica tra un servizio arrestato e un servizio sospeso, i due stati appaiono in modo diverso rispetto a Gestione configurazione servizi.</span><span class="sxs-lookup"><span data-stu-id="8f152-168">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="8f152-169">Un servizio arrestato è un servizio che non è in esecuzione e deve eseguire l'intera procedura di avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="8f152-169">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="8f152-170">Un servizio sospeso, tuttavia, è ancora in esecuzione, ma il suo funzionamento è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="8f152-170">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="8f152-171">Per questo, un servizio sospeso non deve eseguire l'intera procedura di avvio del servizio, ma richiede una procedura diversa per riprendere il funzionamento.</span><span class="sxs-lookup"><span data-stu-id="8f152-171">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="8f152-172">È necessario usare il metodo appropriato per avviare un servizio arrestato o per riprendere un servizio sospeso.</span><span class="sxs-lookup"><span data-stu-id="8f152-172">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="8f152-173">I [**metodi \_ del servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) [**StartService**](win32-terminalservice-startservice.md) **e ResumeService** devono essere usati nelle situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8f152-173">The [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) methods [**StartService**](win32-terminalservice-startservice.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="8f152-174">Se un servizio è attualmente arrestato, è necessario usare il [**metodo StartService**](win32-terminalservice-startservice.md) per riavviarlo. **ResumeService** non può avviare un servizio attualmente arrestato.</span><span class="sxs-lookup"><span data-stu-id="8f152-174">If a service is currently stopped, you must use the [**StartService**](win32-terminalservice-startservice.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="8f152-175">Se un servizio è sospeso, è necessario usare **ResumeService**.</span><span class="sxs-lookup"><span data-stu-id="8f152-175">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="8f152-176">Se si usa il [**metodo StartService**](win32-terminalservice-startservice.md) in un servizio sospeso, viene visualizzato il messaggio "Il servizio è già in esecuzione".</span><span class="sxs-lookup"><span data-stu-id="8f152-176">If you use the [**StartService**](win32-terminalservice-startservice.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="8f152-177">Tuttavia, il servizio rimane sospeso fino a quando non viene inviato il codice di controllo del servizio di ripresa.</span><span class="sxs-lookup"><span data-stu-id="8f152-177">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="8f152-178">Esempio</span><span class="sxs-lookup"><span data-stu-id="8f152-178">Examples</span></span>

<span data-ttu-id="8f152-179">[L'esempio Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript restarts any auto-start services that have been paused (Riprendi servizi di avvio automatico sospesi in VBScript) riavvia tutti i servizi di avvio automatico sospesi.</span><span class="sxs-lookup"><span data-stu-id="8f152-179">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f152-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f152-180">Requirements</span></span>



| <span data-ttu-id="8f152-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f152-181">Requirement</span></span> | <span data-ttu-id="8f152-182">Valore</span><span class="sxs-lookup"><span data-stu-id="8f152-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f152-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f152-183">Minimum supported client</span></span><br/> | <span data-ttu-id="8f152-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f152-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f152-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f152-185">Minimum supported server</span></span><br/> | <span data-ttu-id="8f152-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f152-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f152-187">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8f152-187">Namespace</span></span><br/>                | <span data-ttu-id="8f152-188">TerminalServices \\ CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="8f152-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8f152-189">MOF</span><span class="sxs-lookup"><span data-stu-id="8f152-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f152-190"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f152-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f152-191">DLL</span><span class="sxs-lookup"><span data-stu-id="8f152-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f152-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f152-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f152-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f152-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f152-194">**Servizio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="8f152-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="8f152-195">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8f152-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="8f152-196">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="8f152-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="8f152-197">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="8f152-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

