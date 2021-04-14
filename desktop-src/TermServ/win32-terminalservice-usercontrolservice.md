---
title: Metodo UserControlService della classe Win32_Service (Servizi Desktop remoto)
description: Tenta di inviare un codice di controllo definito dall'utente al servizio a cui si fa riferimento.
ms.assetid: 7B9020C1-2183-4FC4-ABCF-CE34111FF5D3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo UserControlService
- Metodo UserControlService Servizi Desktop remoto, classe Win32_Service
- Classe Win32_Service Servizi Desktop remoto, metodo UserControlService
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
ms.openlocfilehash: 15b1ea4f5e82814aad7549085070b0583993024b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478845"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="3e75b-106">Metodo UserControlService della classe Win32_Service (Servizi Desktop remoto)</span><span class="sxs-lookup"><span data-stu-id="3e75b-106">UserControlService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="3e75b-107">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** tenta di inviare un codice di controllo definito dall'utente al servizio a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="3e75b-107">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="3e75b-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3e75b-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3e75b-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3e75b-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e75b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e75b-110">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="3e75b-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e75b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e75b-112">*ControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e75b-112">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-113">Specifica i valori definiti (da 128 a 255) che forniscono i comandi di controllo specifici per un utente.</span><span class="sxs-lookup"><span data-stu-id="3e75b-113">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e75b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e75b-114">Return value</span></span>

<span data-ttu-id="3e75b-115">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="3e75b-115">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="3e75b-116">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3e75b-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3e75b-117">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3e75b-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3e75b-118">**0**</span><span class="sxs-lookup"><span data-stu-id="3e75b-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-119">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="3e75b-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-120">**1**</span><span class="sxs-lookup"><span data-stu-id="3e75b-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-121">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="3e75b-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-122">**2**</span><span class="sxs-lookup"><span data-stu-id="3e75b-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-123">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="3e75b-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-124">**3**</span><span class="sxs-lookup"><span data-stu-id="3e75b-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-125">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="3e75b-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-126">**4**</span><span class="sxs-lookup"><span data-stu-id="3e75b-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-127">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="3e75b-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-128">**5**</span><span class="sxs-lookup"><span data-stu-id="3e75b-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-129">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="3e75b-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-130">**6**</span><span class="sxs-lookup"><span data-stu-id="3e75b-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-131">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="3e75b-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-132">**7**</span><span class="sxs-lookup"><span data-stu-id="3e75b-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-133">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="3e75b-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-134">**8**</span><span class="sxs-lookup"><span data-stu-id="3e75b-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-135">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="3e75b-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-136">**9**</span><span class="sxs-lookup"><span data-stu-id="3e75b-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-137">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="3e75b-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-138">**10**</span><span class="sxs-lookup"><span data-stu-id="3e75b-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-139">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3e75b-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-140">**11**</span><span class="sxs-lookup"><span data-stu-id="3e75b-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-141">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="3e75b-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-142">**12**</span><span class="sxs-lookup"><span data-stu-id="3e75b-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-143">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3e75b-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-144">**13**</span><span class="sxs-lookup"><span data-stu-id="3e75b-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-145">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="3e75b-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-146">**14**</span><span class="sxs-lookup"><span data-stu-id="3e75b-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-147">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3e75b-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-148">**15**</span><span class="sxs-lookup"><span data-stu-id="3e75b-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-149">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="3e75b-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-150">**16**</span><span class="sxs-lookup"><span data-stu-id="3e75b-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-151">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3e75b-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-152">**17**</span><span class="sxs-lookup"><span data-stu-id="3e75b-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-153">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3e75b-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-154">**18**</span><span class="sxs-lookup"><span data-stu-id="3e75b-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-155">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="3e75b-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-156">**19**</span><span class="sxs-lookup"><span data-stu-id="3e75b-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-157">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="3e75b-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-158">**20**</span><span class="sxs-lookup"><span data-stu-id="3e75b-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-159">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="3e75b-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-160">**21**</span><span class="sxs-lookup"><span data-stu-id="3e75b-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-161">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="3e75b-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-162">**22**</span><span class="sxs-lookup"><span data-stu-id="3e75b-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-163">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="3e75b-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-164">**23**</span><span class="sxs-lookup"><span data-stu-id="3e75b-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-165">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3e75b-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="3e75b-166">**24**</span><span class="sxs-lookup"><span data-stu-id="3e75b-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="3e75b-167">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="3e75b-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e75b-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e75b-168">Requirements</span></span>



| <span data-ttu-id="3e75b-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e75b-169">Requirement</span></span> | <span data-ttu-id="3e75b-170">Valore</span><span class="sxs-lookup"><span data-stu-id="3e75b-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e75b-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e75b-171">Minimum supported client</span></span><br/> | <span data-ttu-id="3e75b-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e75b-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e75b-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e75b-173">Minimum supported server</span></span><br/> | <span data-ttu-id="3e75b-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e75b-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e75b-175">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3e75b-175">Namespace</span></span><br/>                | <span data-ttu-id="3e75b-176">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3e75b-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3e75b-177">MOF</span><span class="sxs-lookup"><span data-stu-id="3e75b-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e75b-178"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e75b-178"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e75b-179">DLL</span><span class="sxs-lookup"><span data-stu-id="3e75b-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e75b-180"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e75b-180"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e75b-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e75b-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e75b-182">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="3e75b-182">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="3e75b-183">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3e75b-183">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="3e75b-184">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="3e75b-184">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> </dl>

 

