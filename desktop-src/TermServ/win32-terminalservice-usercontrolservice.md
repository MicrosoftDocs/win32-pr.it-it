---
title: Metodo UserControlService della classe Win32_Service (Servizi Desktop remoto)
description: "Metodo UserControlService della classe Win32_Service (Servizi Desktop remoto): tenta di inviare un codice di controllo definito dall'utente al servizio a cui si fa riferimento."
ms.assetid: 7B9020C1-2183-4FC4-ABCF-CE34111FF5D3
ms.tgt_platform: multiple
keywords:
- Metodo UserControlService Servizi Desktop remoto
- Il metodo UserControlService Servizi Desktop remoto , Win32_Service classe
- Win32_Service classe Servizi Desktop remoto , metodo UserControlService
topic_type:
- apiref
api_name:
- Win32_Service.UserControlService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e71a33056f596afaf577968a5c725b3f64f79b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090609"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="1e483-106">Metodo UserControlService della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="1e483-106">UserControlService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="1e483-107">Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** tenta di inviare un codice di controllo definito dall'utente al servizio a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="1e483-107">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="1e483-108">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="1e483-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1e483-109">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1e483-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1e483-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e483-110">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="1e483-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e483-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e483-112">*Codice di controllo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1e483-112">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e483-113">Specifica i valori definiti (da 128 a 255) che forniscono comandi di controllo specifici per un utente.</span><span class="sxs-lookup"><span data-stu-id="1e483-113">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e483-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e483-114">Return value</span></span>

<span data-ttu-id="1e483-115">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="1e483-115">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="1e483-116">Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="1e483-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1e483-117">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)</span><span class="sxs-lookup"><span data-stu-id="1e483-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1e483-118">**0**</span><span class="sxs-lookup"><span data-stu-id="1e483-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-119">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="1e483-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-120">**1**</span><span class="sxs-lookup"><span data-stu-id="1e483-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-121">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="1e483-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-122">**2**</span><span class="sxs-lookup"><span data-stu-id="1e483-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-123">L'utente non aveva l'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="1e483-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-124">**3**</span><span class="sxs-lookup"><span data-stu-id="1e483-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-125">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="1e483-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-126">**4**</span><span class="sxs-lookup"><span data-stu-id="1e483-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-127">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="1e483-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-128">**5**</span><span class="sxs-lookup"><span data-stu-id="1e483-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-129">Il codice di controllo richiesto non può essere inviato al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State)** è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="1e483-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-130">**6**</span><span class="sxs-lookup"><span data-stu-id="1e483-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-131">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="1e483-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-132">**7**</span><span class="sxs-lookup"><span data-stu-id="1e483-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-133">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="1e483-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-134">**8**</span><span class="sxs-lookup"><span data-stu-id="1e483-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-135">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="1e483-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-136">**9**</span><span class="sxs-lookup"><span data-stu-id="1e483-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-137">Impossibile trovare il percorso della directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="1e483-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-138">**10**</span><span class="sxs-lookup"><span data-stu-id="1e483-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-139">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1e483-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-140">**11**</span><span class="sxs-lookup"><span data-stu-id="1e483-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-141">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="1e483-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-142">**12**</span><span class="sxs-lookup"><span data-stu-id="1e483-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-143">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1e483-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-144">**13**</span><span class="sxs-lookup"><span data-stu-id="1e483-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-145">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="1e483-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-146">**14**</span><span class="sxs-lookup"><span data-stu-id="1e483-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-147">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1e483-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-148">**15**</span><span class="sxs-lookup"><span data-stu-id="1e483-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-149">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="1e483-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-150">**16**</span><span class="sxs-lookup"><span data-stu-id="1e483-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-151">Questo servizio viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1e483-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-152">**17**</span><span class="sxs-lookup"><span data-stu-id="1e483-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-153">Il servizio non ha thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1e483-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-154">**18**</span><span class="sxs-lookup"><span data-stu-id="1e483-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-155">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="1e483-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-156">**19**</span><span class="sxs-lookup"><span data-stu-id="1e483-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-157">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="1e483-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-158">**20**</span><span class="sxs-lookup"><span data-stu-id="1e483-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-159">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="1e483-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-160">**21**</span><span class="sxs-lookup"><span data-stu-id="1e483-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-161">Al servizio sono stati passati parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="1e483-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-162">**22**</span><span class="sxs-lookup"><span data-stu-id="1e483-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-163">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="1e483-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-164">**23**</span><span class="sxs-lookup"><span data-stu-id="1e483-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-165">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1e483-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1e483-166">**24**</span><span class="sxs-lookup"><span data-stu-id="1e483-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="1e483-167">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="1e483-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e483-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e483-168">Requirements</span></span>



| <span data-ttu-id="1e483-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e483-169">Requirement</span></span> | <span data-ttu-id="1e483-170">Valore</span><span class="sxs-lookup"><span data-stu-id="1e483-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e483-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e483-171">Minimum supported client</span></span><br/> | <span data-ttu-id="1e483-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e483-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e483-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e483-173">Minimum supported server</span></span><br/> | <span data-ttu-id="1e483-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e483-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e483-175">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1e483-175">Namespace</span></span><br/>                | <span data-ttu-id="1e483-176">TerminalServices \\ CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="1e483-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1e483-177">MOF</span><span class="sxs-lookup"><span data-stu-id="1e483-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e483-178"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e483-178"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e483-179">DLL</span><span class="sxs-lookup"><span data-stu-id="1e483-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e483-180"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e483-180"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e483-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e483-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e483-182">**Servizio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="1e483-182">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="1e483-183">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="1e483-183">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="1e483-184">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="1e483-184">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> </dl>

 

