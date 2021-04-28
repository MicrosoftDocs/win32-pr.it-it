---
title: Metodo InterrogaeService della classe Win32_Service (Servizi Desktop remoto)
description: 'Metodo InterrogaeService della classe Win32_Service (Servizi Desktop remoto): richiede che il servizio a cui si fa riferimento aggiornerà lo stato a Service Manager.'
ms.assetid: 7B572049-416E-4429-BD53-119FF570B2D8
ms.tgt_platform: multiple
keywords:
- Metodo InterrogaeService Servizi Desktop remoto
- Il metodo InterrogaeService Servizi Desktop remoto , Win32_Service classe
- Win32_Service classe Servizi Desktop remoto , metodo InterrogaeService
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
ms.openlocfilehash: 850953b210ea11b9dd1000326d6793e3651ce538
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090659"
---
# <a name="interrogateservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="fdc20-106">Metodo InterrogaeService della Win32_Service classe (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="fdc20-106">InterrogateService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="fdc20-107">Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogaeService** richiede che il servizio a cui si fa riferimento aggiornerà lo stato a Service Manager.</span><span class="sxs-lookup"><span data-stu-id="fdc20-107">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="fdc20-108">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="fdc20-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fdc20-109">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fdc20-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fdc20-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fdc20-110">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="fdc20-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="fdc20-111">Parameters</span></span>

<span data-ttu-id="fdc20-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="fdc20-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fdc20-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fdc20-113">Return value</span></span>

<span data-ttu-id="fdc20-114">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="fdc20-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="fdc20-115">Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="fdc20-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="fdc20-116">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)</span><span class="sxs-lookup"><span data-stu-id="fdc20-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="fdc20-117">**0**</span><span class="sxs-lookup"><span data-stu-id="fdc20-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-118">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="fdc20-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-119">**1**</span><span class="sxs-lookup"><span data-stu-id="fdc20-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-120">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="fdc20-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-121">**2**</span><span class="sxs-lookup"><span data-stu-id="fdc20-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-122">L'utente non aveva l'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="fdc20-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-123">**3**</span><span class="sxs-lookup"><span data-stu-id="fdc20-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-124">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="fdc20-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-125">**4**</span><span class="sxs-lookup"><span data-stu-id="fdc20-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-126">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="fdc20-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-127">**5**</span><span class="sxs-lookup"><span data-stu-id="fdc20-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-128">Il codice di controllo richiesto non può essere inviato al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State)** è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="fdc20-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-129">**6**</span><span class="sxs-lookup"><span data-stu-id="fdc20-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-130">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="fdc20-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-131">**7**</span><span class="sxs-lookup"><span data-stu-id="fdc20-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-132">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="fdc20-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-133">**8**</span><span class="sxs-lookup"><span data-stu-id="fdc20-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-134">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="fdc20-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-135">**9**</span><span class="sxs-lookup"><span data-stu-id="fdc20-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-136">Impossibile trovare il percorso della directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="fdc20-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-137">**10**</span><span class="sxs-lookup"><span data-stu-id="fdc20-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-138">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fdc20-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-139">**11**</span><span class="sxs-lookup"><span data-stu-id="fdc20-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-140">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="fdc20-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-141">**12**</span><span class="sxs-lookup"><span data-stu-id="fdc20-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-142">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fdc20-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-143">**13**</span><span class="sxs-lookup"><span data-stu-id="fdc20-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-144">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="fdc20-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-145">**14**</span><span class="sxs-lookup"><span data-stu-id="fdc20-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-146">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fdc20-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-147">**15**</span><span class="sxs-lookup"><span data-stu-id="fdc20-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-148">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="fdc20-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-149">**16**</span><span class="sxs-lookup"><span data-stu-id="fdc20-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-150">Questo servizio viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fdc20-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-151">**17**</span><span class="sxs-lookup"><span data-stu-id="fdc20-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-152">Il servizio non ha thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fdc20-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-153">**18**</span><span class="sxs-lookup"><span data-stu-id="fdc20-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-154">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="fdc20-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-155">**19**</span><span class="sxs-lookup"><span data-stu-id="fdc20-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-156">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="fdc20-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-157">**20**</span><span class="sxs-lookup"><span data-stu-id="fdc20-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-158">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="fdc20-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-159">**21**</span><span class="sxs-lookup"><span data-stu-id="fdc20-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-160">Al servizio sono stati passati parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="fdc20-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-161">**22**</span><span class="sxs-lookup"><span data-stu-id="fdc20-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-162">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="fdc20-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-163">**23**</span><span class="sxs-lookup"><span data-stu-id="fdc20-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-164">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="fdc20-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="fdc20-165">**24**</span><span class="sxs-lookup"><span data-stu-id="fdc20-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="fdc20-166">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="fdc20-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fdc20-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdc20-167">Requirements</span></span>



| <span data-ttu-id="fdc20-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdc20-168">Requirement</span></span> | <span data-ttu-id="fdc20-169">Valore</span><span class="sxs-lookup"><span data-stu-id="fdc20-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc20-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdc20-170">Minimum supported client</span></span><br/> | <span data-ttu-id="fdc20-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fdc20-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fdc20-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdc20-172">Minimum supported server</span></span><br/> | <span data-ttu-id="fdc20-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdc20-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fdc20-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fdc20-174">Namespace</span></span><br/>                | <span data-ttu-id="fdc20-175">TerminalServices \\ CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="fdc20-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fdc20-176">MOF</span><span class="sxs-lookup"><span data-stu-id="fdc20-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdc20-177"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="fdc20-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdc20-178">DLL</span><span class="sxs-lookup"><span data-stu-id="fdc20-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdc20-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdc20-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdc20-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fdc20-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdc20-181">**Servizio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="fdc20-181">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="fdc20-182">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="fdc20-182">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="fdc20-183">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="fdc20-183">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="fdc20-184">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="fdc20-184">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

