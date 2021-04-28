---
title: Metodo StartService della classe Win32_Service (Servizi Desktop remoto)
description: 'Metodo StartService della classe Win32_Service (Servizi Desktop remoto): tenta di impostare lo stato di avvio del servizio a cui si fa riferimento.'
ms.assetid: 4DA05C48-03A0-4D4B-9E69-0404393C219C
ms.tgt_platform: multiple
keywords:
- Metodo StartService Servizi Desktop remoto
- Metodo StartService Servizi Desktop remoto , Win32_Service classe
- Win32_Service classe Servizi Desktop remoto , metodo StartService
topic_type:
- apiref
api_name:
- Win32_Service.StartService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce4bd12150223d7cdc1340b7557ba309a1e07da4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084199"
---
# <a name="startservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="15d3e-106">Metodo StartService della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="15d3e-106">StartService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="15d3e-107">Il **metodo StartService** tenta di impostare lo stato di avvio del servizio a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="15d3e-107">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="15d3e-108">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="15d3e-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="15d3e-109">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="15d3e-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="15d3e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15d3e-110">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="15d3e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="15d3e-111">Parameters</span></span>

<span data-ttu-id="15d3e-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="15d3e-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15d3e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15d3e-113">Return value</span></span>

<span data-ttu-id="15d3e-114">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="15d3e-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="15d3e-115">Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="15d3e-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="15d3e-116">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)</span><span class="sxs-lookup"><span data-stu-id="15d3e-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="15d3e-117">**0**</span><span class="sxs-lookup"><span data-stu-id="15d3e-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-118">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="15d3e-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-119">**1**</span><span class="sxs-lookup"><span data-stu-id="15d3e-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-120">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="15d3e-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-121">**2**</span><span class="sxs-lookup"><span data-stu-id="15d3e-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-122">L'utente non aveva l'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="15d3e-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-123">**3**</span><span class="sxs-lookup"><span data-stu-id="15d3e-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-124">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="15d3e-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-125">**4**</span><span class="sxs-lookup"><span data-stu-id="15d3e-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-126">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="15d3e-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-127">**5**</span><span class="sxs-lookup"><span data-stu-id="15d3e-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-128">Il codice di controllo richiesto non può essere inviato al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State)** è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="15d3e-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-129">**6**</span><span class="sxs-lookup"><span data-stu-id="15d3e-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-130">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="15d3e-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-131">**7**</span><span class="sxs-lookup"><span data-stu-id="15d3e-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-132">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="15d3e-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-133">**8**</span><span class="sxs-lookup"><span data-stu-id="15d3e-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-134">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="15d3e-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-135">**9**</span><span class="sxs-lookup"><span data-stu-id="15d3e-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-136">Impossibile trovare il percorso della directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="15d3e-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-137">**10**</span><span class="sxs-lookup"><span data-stu-id="15d3e-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-138">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="15d3e-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-139">**11**</span><span class="sxs-lookup"><span data-stu-id="15d3e-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-140">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="15d3e-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-141">**12**</span><span class="sxs-lookup"><span data-stu-id="15d3e-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-142">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="15d3e-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-143">**13**</span><span class="sxs-lookup"><span data-stu-id="15d3e-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-144">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="15d3e-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-145">**14**</span><span class="sxs-lookup"><span data-stu-id="15d3e-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-146">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="15d3e-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-147">**15**</span><span class="sxs-lookup"><span data-stu-id="15d3e-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-148">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="15d3e-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-149">**16**</span><span class="sxs-lookup"><span data-stu-id="15d3e-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-150">Questo servizio viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="15d3e-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-151">**17**</span><span class="sxs-lookup"><span data-stu-id="15d3e-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-152">Il servizio non ha thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="15d3e-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-153">**18**</span><span class="sxs-lookup"><span data-stu-id="15d3e-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-154">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="15d3e-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-155">**19**</span><span class="sxs-lookup"><span data-stu-id="15d3e-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-156">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="15d3e-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-157">**20**</span><span class="sxs-lookup"><span data-stu-id="15d3e-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-158">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="15d3e-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-159">**21**</span><span class="sxs-lookup"><span data-stu-id="15d3e-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-160">Al servizio sono stati passati parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="15d3e-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-161">**22**</span><span class="sxs-lookup"><span data-stu-id="15d3e-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-162">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="15d3e-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-163">**23**</span><span class="sxs-lookup"><span data-stu-id="15d3e-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-164">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="15d3e-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="15d3e-165">**24**</span><span class="sxs-lookup"><span data-stu-id="15d3e-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="15d3e-166">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="15d3e-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15d3e-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="15d3e-167">Remarks</span></span>

<span data-ttu-id="15d3e-168">Anche se potrebbe non esserci alcuna differenza pratica tra un servizio arrestato e un servizio sospeso, i due stati appaiono in modo diverso rispetto a Gestione configurazione servizi.</span><span class="sxs-lookup"><span data-stu-id="15d3e-168">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="15d3e-169">Un servizio arrestato è un servizio che non è in esecuzione e deve eseguire l'intera procedura di avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="15d3e-169">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="15d3e-170">Un servizio sospeso, tuttavia, è ancora in esecuzione, ma il suo funzionamento è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="15d3e-170">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="15d3e-171">Per questo scopo, un servizio sospeso non deve eseguire l'intera procedura di avvio del servizio, ma richiede una procedura diversa per riprendere il funzionamento.</span><span class="sxs-lookup"><span data-stu-id="15d3e-171">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="15d3e-172">È necessario usare il metodo appropriato per avviare un servizio arrestato o per riprendere un servizio sospeso.</span><span class="sxs-lookup"><span data-stu-id="15d3e-172">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="15d3e-173">I [**metodi \_ del servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) **StartService** [**e ResumeService**](win32-terminalservice-resumeservice.md) devono essere usati nelle situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="15d3e-173">The [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) methods **StartService** and [**ResumeService**](win32-terminalservice-resumeservice.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="15d3e-174">Se un servizio è attualmente arrestato, è necessario usare il **metodo StartService** per riavviarlo. [**ResumeService non**](win32-terminalservice-resumeservice.md) può avviare un servizio attualmente arrestato.</span><span class="sxs-lookup"><span data-stu-id="15d3e-174">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](win32-terminalservice-resumeservice.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="15d3e-175">Se un servizio è sospeso, è necessario usare [**ResumeService**](win32-terminalservice-resumeservice.md).</span><span class="sxs-lookup"><span data-stu-id="15d3e-175">If a service is paused, you must use [**ResumeService**](win32-terminalservice-resumeservice.md).</span></span> <span data-ttu-id="15d3e-176">Se si usa il **metodo StartService** in un servizio sospeso, viene visualizzato il messaggio "Il servizio è già in esecuzione".</span><span class="sxs-lookup"><span data-stu-id="15d3e-176">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="15d3e-177">Tuttavia, il servizio rimane sospeso fino a quando non viene inviato il codice di controllo del servizio di ripresa.</span><span class="sxs-lookup"><span data-stu-id="15d3e-177">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="15d3e-178">Se si avvia un servizio arrestato che dipende da un altro servizio, vengono avviati entrambi i servizi.</span><span class="sxs-lookup"><span data-stu-id="15d3e-178">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="15d3e-179">Quando un servizio viene avviato con questo metodo, i servizi dipendenti non vengono avviati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="15d3e-179">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="15d3e-180">È necessario usare la classe di associazione [**Win32 \_ DependentService**](/windows/desktop/CIMWin32Prov/win32-dependentservice) e la query [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) per individuare i dipendenti e avviarli separatamente.</span><span class="sxs-lookup"><span data-stu-id="15d3e-180">You must use the association class [**Win32\_DependentService**](/windows/desktop/CIMWin32Prov/win32-dependentservice) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="requirements"></a><span data-ttu-id="15d3e-181">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15d3e-181">Requirements</span></span>



| <span data-ttu-id="15d3e-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="15d3e-182">Requirement</span></span> | <span data-ttu-id="15d3e-183">Valore</span><span class="sxs-lookup"><span data-stu-id="15d3e-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15d3e-184">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15d3e-184">Minimum supported client</span></span><br/> | <span data-ttu-id="15d3e-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15d3e-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15d3e-186">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15d3e-186">Minimum supported server</span></span><br/> | <span data-ttu-id="15d3e-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15d3e-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15d3e-188">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="15d3e-188">Namespace</span></span><br/>                | <span data-ttu-id="15d3e-189">TerminalServices \\ CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="15d3e-189">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="15d3e-190">MOF</span><span class="sxs-lookup"><span data-stu-id="15d3e-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15d3e-191"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="15d3e-191"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="15d3e-192">DLL</span><span class="sxs-lookup"><span data-stu-id="15d3e-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15d3e-193"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15d3e-193"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15d3e-194">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15d3e-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d3e-195">**Servizio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="15d3e-195">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="15d3e-196">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="15d3e-196">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="15d3e-197">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="15d3e-197">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="15d3e-198">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="15d3e-198">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

