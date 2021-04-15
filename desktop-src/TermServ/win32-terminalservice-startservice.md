---
title: Metodo StartService della classe Win32_Service (Servizi Desktop remoto)
description: Tenta di collocare il servizio a cui si fa riferimento nello stato di avvio.
ms.assetid: 4DA05C48-03A0-4D4B-9E69-0404393C219C
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo StartService
- Metodo StartService Servizi Desktop remoto, classe Win32_Service
- Classe Win32_Service Servizi Desktop remoto, metodo StartService
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
ms.openlocfilehash: 9e37a17922fe0f4f3f5a3e4f1cd4d8eb67dc2858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400569"
---
# <a name="startservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="3c01d-106">Metodo StartService della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="3c01d-106">StartService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="3c01d-107">Il metodo **StartService** tenta di collocare il servizio a cui si fa riferimento nello stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="3c01d-107">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="3c01d-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3c01d-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3c01d-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3c01d-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3c01d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c01d-110">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="3c01d-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c01d-111">Parameters</span></span>

<span data-ttu-id="3c01d-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3c01d-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c01d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c01d-113">Return value</span></span>

<span data-ttu-id="3c01d-114">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="3c01d-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="3c01d-115">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3c01d-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3c01d-116">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3c01d-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3c01d-117">**0**</span><span class="sxs-lookup"><span data-stu-id="3c01d-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-118">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="3c01d-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-119">**1**</span><span class="sxs-lookup"><span data-stu-id="3c01d-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-120">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="3c01d-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-121">**2**</span><span class="sxs-lookup"><span data-stu-id="3c01d-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-122">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="3c01d-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-123">**3**</span><span class="sxs-lookup"><span data-stu-id="3c01d-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-124">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="3c01d-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-125">**4**</span><span class="sxs-lookup"><span data-stu-id="3c01d-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-126">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="3c01d-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-127">**5**</span><span class="sxs-lookup"><span data-stu-id="3c01d-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-128">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="3c01d-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-129">**6**</span><span class="sxs-lookup"><span data-stu-id="3c01d-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-130">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="3c01d-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-131">**7**</span><span class="sxs-lookup"><span data-stu-id="3c01d-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-132">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="3c01d-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-133">**8**</span><span class="sxs-lookup"><span data-stu-id="3c01d-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-134">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="3c01d-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-135">**9**</span><span class="sxs-lookup"><span data-stu-id="3c01d-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-136">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="3c01d-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-137">**10**</span><span class="sxs-lookup"><span data-stu-id="3c01d-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-138">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3c01d-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-139">**11**</span><span class="sxs-lookup"><span data-stu-id="3c01d-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-140">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="3c01d-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-141">**12**</span><span class="sxs-lookup"><span data-stu-id="3c01d-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-142">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3c01d-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-143">**13**</span><span class="sxs-lookup"><span data-stu-id="3c01d-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-144">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="3c01d-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-145">**14**</span><span class="sxs-lookup"><span data-stu-id="3c01d-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-146">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3c01d-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-147">**15**</span><span class="sxs-lookup"><span data-stu-id="3c01d-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-148">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="3c01d-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-149">**16**</span><span class="sxs-lookup"><span data-stu-id="3c01d-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-150">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3c01d-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-151">**17**</span><span class="sxs-lookup"><span data-stu-id="3c01d-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-152">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3c01d-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-153">**18**</span><span class="sxs-lookup"><span data-stu-id="3c01d-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-154">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="3c01d-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-155">**19**</span><span class="sxs-lookup"><span data-stu-id="3c01d-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-156">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="3c01d-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-157">**20**</span><span class="sxs-lookup"><span data-stu-id="3c01d-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-158">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="3c01d-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-159">**21**</span><span class="sxs-lookup"><span data-stu-id="3c01d-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-160">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="3c01d-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-161">**22**</span><span class="sxs-lookup"><span data-stu-id="3c01d-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-162">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="3c01d-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-163">**23**</span><span class="sxs-lookup"><span data-stu-id="3c01d-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-164">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3c01d-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3c01d-165">**24**</span><span class="sxs-lookup"><span data-stu-id="3c01d-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="3c01d-166">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="3c01d-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c01d-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c01d-167">Remarks</span></span>

<span data-ttu-id="3c01d-168">Sebbene sia possibile che non esistano differenze pratiche tra un servizio interrotto e un servizio sospeso, i due stati vengono visualizzati in modo diverso rispetto a SCM.</span><span class="sxs-lookup"><span data-stu-id="3c01d-168">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="3c01d-169">Un servizio interrotto è un servizio che non è in esecuzione e che deve seguire l'intera procedura di avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="3c01d-169">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="3c01d-170">Un servizio sospeso, tuttavia, è ancora in esecuzione, ma il suo funzionamento è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="3c01d-170">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="3c01d-171">Per questo motivo, non è necessario che un servizio sospeso attraversi l'intera procedura di avvio del servizio, ma è necessaria una procedura diversa per riprendere il funzionamento.</span><span class="sxs-lookup"><span data-stu-id="3c01d-171">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="3c01d-172">È necessario utilizzare il metodo appropriato per avviare un servizio che è stato interrotto o per riprendere un servizio che è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="3c01d-172">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="3c01d-173">I metodi del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) **StartService** e [**ResumeService**](win32-terminalservice-resumeservice.md) devono essere utilizzati nelle situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3c01d-173">The [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) methods **StartService** and [**ResumeService**](win32-terminalservice-resumeservice.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="3c01d-174">Se un servizio è attualmente arrestato, è necessario usare il metodo **StartService** per riavviarlo; [**ResumeService**](win32-terminalservice-resumeservice.md) non è in grado di avviare un servizio attualmente arrestato.</span><span class="sxs-lookup"><span data-stu-id="3c01d-174">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](win32-terminalservice-resumeservice.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="3c01d-175">Se un servizio viene sospeso, è necessario utilizzare [**ResumeService**](win32-terminalservice-resumeservice.md).</span><span class="sxs-lookup"><span data-stu-id="3c01d-175">If a service is paused, you must use [**ResumeService**](win32-terminalservice-resumeservice.md).</span></span> <span data-ttu-id="3c01d-176">Se si usa il metodo **StartService** in un servizio in pausa, viene visualizzato il messaggio "il servizio è già in esecuzione".</span><span class="sxs-lookup"><span data-stu-id="3c01d-176">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="3c01d-177">Tuttavia, il servizio rimane sospeso fino a quando non viene inviato il codice di controllo del servizio di ripresa.</span><span class="sxs-lookup"><span data-stu-id="3c01d-177">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="3c01d-178">Se si avvia un servizio interrotto che dipende da un altro servizio, vengono avviati entrambi i servizi.</span><span class="sxs-lookup"><span data-stu-id="3c01d-178">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="3c01d-179">Quando un servizio viene avviato con questo metodo, tutti i servizi dipendenti non vengono avviati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3c01d-179">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="3c01d-180">Per individuare i dipendenti e avviarli separatamente, è necessario utilizzare la classe di associazione [**Win32 \_ DependentService**](/windows/desktop/CIMWin32Prov/win32-dependentservice) e gli [associatori di](/windows/desktop/WmiSdk/associators-of-statement) query.</span><span class="sxs-lookup"><span data-stu-id="3c01d-180">You must use the association class [**Win32\_DependentService**](/windows/desktop/CIMWin32Prov/win32-dependentservice) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c01d-181">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c01d-181">Requirements</span></span>



| <span data-ttu-id="3c01d-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c01d-182">Requirement</span></span> | <span data-ttu-id="3c01d-183">Valore</span><span class="sxs-lookup"><span data-stu-id="3c01d-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c01d-184">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c01d-184">Minimum supported client</span></span><br/> | <span data-ttu-id="3c01d-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c01d-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c01d-186">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c01d-186">Minimum supported server</span></span><br/> | <span data-ttu-id="3c01d-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c01d-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c01d-188">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3c01d-188">Namespace</span></span><br/>                | <span data-ttu-id="3c01d-189">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3c01d-189">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3c01d-190">MOF</span><span class="sxs-lookup"><span data-stu-id="3c01d-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c01d-191"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c01d-191"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c01d-192">DLL</span><span class="sxs-lookup"><span data-stu-id="3c01d-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c01d-193"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c01d-193"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c01d-194">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c01d-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c01d-195">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="3c01d-195">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="3c01d-196">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3c01d-196">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="3c01d-197">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="3c01d-197">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="3c01d-198">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="3c01d-198">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

