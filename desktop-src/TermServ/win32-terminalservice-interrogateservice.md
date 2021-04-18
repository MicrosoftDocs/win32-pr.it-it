---
title: Metodo InterrogateService della classe Win32_Service (Servizi Desktop remoto)
description: Richiede che il servizio a cui si fa riferimento aggiorni lo stato a Service Manager.
ms.assetid: 7B572049-416E-4429-BD53-119FF570B2D8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo InterrogateService
- Metodo InterrogateService Servizi Desktop remoto, classe Win32_Service
- Classe Win32_Service Servizi Desktop remoto, metodo InterrogateService
topic_type:
- apiref
api_name:
- Win32_Service.InterrogateService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f53b3d5e1cced6b6820f9b7334551de47f333be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301606"
---
# <a name="interrogateservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="03a5e-106">Metodo InterrogateService della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="03a5e-106">InterrogateService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="03a5e-107">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** richiede che il servizio a cui si fa riferimento aggiorni lo stato a Service Manager.</span><span class="sxs-lookup"><span data-stu-id="03a5e-107">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="03a5e-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="03a5e-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="03a5e-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="03a5e-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="03a5e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03a5e-110">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="03a5e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="03a5e-111">Parameters</span></span>

<span data-ttu-id="03a5e-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="03a5e-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03a5e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03a5e-113">Return value</span></span>

<span data-ttu-id="03a5e-114">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="03a5e-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="03a5e-115">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="03a5e-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="03a5e-116">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="03a5e-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="03a5e-117">**0**</span><span class="sxs-lookup"><span data-stu-id="03a5e-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-118">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="03a5e-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-119">**1**</span><span class="sxs-lookup"><span data-stu-id="03a5e-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-120">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="03a5e-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-121">**2**</span><span class="sxs-lookup"><span data-stu-id="03a5e-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-122">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="03a5e-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-123">**3**</span><span class="sxs-lookup"><span data-stu-id="03a5e-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-124">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="03a5e-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-125">**4**</span><span class="sxs-lookup"><span data-stu-id="03a5e-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-126">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="03a5e-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-127">**5**</span><span class="sxs-lookup"><span data-stu-id="03a5e-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-128">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="03a5e-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-129">**6**</span><span class="sxs-lookup"><span data-stu-id="03a5e-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-130">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="03a5e-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-131">**7**</span><span class="sxs-lookup"><span data-stu-id="03a5e-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-132">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="03a5e-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-133">**8**</span><span class="sxs-lookup"><span data-stu-id="03a5e-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-134">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="03a5e-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-135">**9**</span><span class="sxs-lookup"><span data-stu-id="03a5e-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-136">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="03a5e-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-137">**10**</span><span class="sxs-lookup"><span data-stu-id="03a5e-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-138">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="03a5e-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-139">**11**</span><span class="sxs-lookup"><span data-stu-id="03a5e-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-140">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="03a5e-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-141">**12**</span><span class="sxs-lookup"><span data-stu-id="03a5e-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-142">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="03a5e-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-143">**13**</span><span class="sxs-lookup"><span data-stu-id="03a5e-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-144">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="03a5e-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-145">**14**</span><span class="sxs-lookup"><span data-stu-id="03a5e-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-146">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="03a5e-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-147">**15**</span><span class="sxs-lookup"><span data-stu-id="03a5e-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-148">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="03a5e-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-149">**16**</span><span class="sxs-lookup"><span data-stu-id="03a5e-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-150">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="03a5e-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-151">**17**</span><span class="sxs-lookup"><span data-stu-id="03a5e-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-152">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="03a5e-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-153">**18**</span><span class="sxs-lookup"><span data-stu-id="03a5e-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-154">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="03a5e-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-155">**19**</span><span class="sxs-lookup"><span data-stu-id="03a5e-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-156">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="03a5e-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-157">**20**</span><span class="sxs-lookup"><span data-stu-id="03a5e-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-158">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="03a5e-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-159">**21**</span><span class="sxs-lookup"><span data-stu-id="03a5e-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-160">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="03a5e-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-161">**22**</span><span class="sxs-lookup"><span data-stu-id="03a5e-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-162">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="03a5e-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-163">**23**</span><span class="sxs-lookup"><span data-stu-id="03a5e-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-164">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="03a5e-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-165">**24**</span><span class="sxs-lookup"><span data-stu-id="03a5e-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="03a5e-166">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="03a5e-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03a5e-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03a5e-167">Requirements</span></span>



| <span data-ttu-id="03a5e-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="03a5e-168">Requirement</span></span> | <span data-ttu-id="03a5e-169">Valore</span><span class="sxs-lookup"><span data-stu-id="03a5e-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03a5e-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03a5e-170">Minimum supported client</span></span><br/> | <span data-ttu-id="03a5e-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03a5e-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03a5e-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03a5e-172">Minimum supported server</span></span><br/> | <span data-ttu-id="03a5e-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03a5e-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03a5e-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="03a5e-174">Namespace</span></span><br/>                | <span data-ttu-id="03a5e-175">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="03a5e-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="03a5e-176">MOF</span><span class="sxs-lookup"><span data-stu-id="03a5e-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03a5e-177"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03a5e-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="03a5e-178">DLL</span><span class="sxs-lookup"><span data-stu-id="03a5e-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03a5e-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03a5e-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03a5e-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03a5e-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03a5e-181">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="03a5e-181">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="03a5e-182">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="03a5e-182">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="03a5e-183">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="03a5e-183">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="03a5e-184">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="03a5e-184">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

