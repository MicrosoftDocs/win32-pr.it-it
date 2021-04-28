---
description: 'Metodo InterrogaeService della classe Win32_Service (provider WMI CIMWin32): richiede che il servizio a cui si fa riferimento aggiornerà lo stato a Service Manager.'
ms.assetid: a4ea8753-1859-4d97-b9ca-47598c7e7654
ms.tgt_platform: multiple
title: Metodo InterrogaeService della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9702bc3fbd0a9969db20a8f1326c31b9ea7d925d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096979"
---
# <a name="interrogateservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="4f042-103">Metodo InterrogaeService della classe Win32_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="4f042-103">InterrogateService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="4f042-104">Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogaeService** richiede che il servizio a cui si fa riferimento aggiornerà lo stato a Service Manager.</span><span class="sxs-lookup"><span data-stu-id="4f042-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="4f042-105">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4f042-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4f042-106">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4f042-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f042-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f042-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="4f042-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f042-108">Parameters</span></span>

<span data-ttu-id="4f042-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4f042-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f042-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f042-110">Return value</span></span>

<span data-ttu-id="4f042-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="4f042-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="4f042-112">Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="4f042-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4f042-113">Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)</span><span class="sxs-lookup"><span data-stu-id="4f042-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4f042-114">**0**</span><span class="sxs-lookup"><span data-stu-id="4f042-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-115">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="4f042-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-116">**1**</span><span class="sxs-lookup"><span data-stu-id="4f042-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-117">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="4f042-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-118">**2**</span><span class="sxs-lookup"><span data-stu-id="4f042-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-119">L'utente non aveva l'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="4f042-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-120">**3**</span><span class="sxs-lookup"><span data-stu-id="4f042-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-121">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="4f042-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-122">**4**</span><span class="sxs-lookup"><span data-stu-id="4f042-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-123">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="4f042-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-124">**5**</span><span class="sxs-lookup"><span data-stu-id="4f042-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-125">Il codice di controllo richiesto non può essere inviato al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**State)** è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="4f042-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-126">**6**</span><span class="sxs-lookup"><span data-stu-id="4f042-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-127">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="4f042-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-128">**7**</span><span class="sxs-lookup"><span data-stu-id="4f042-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-129">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="4f042-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-130">**8**</span><span class="sxs-lookup"><span data-stu-id="4f042-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-131">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="4f042-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-132">**9**</span><span class="sxs-lookup"><span data-stu-id="4f042-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-133">Impossibile trovare il percorso della directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="4f042-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-134">**10**</span><span class="sxs-lookup"><span data-stu-id="4f042-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-135">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4f042-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-136">**11**</span><span class="sxs-lookup"><span data-stu-id="4f042-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-137">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="4f042-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-138">**12**</span><span class="sxs-lookup"><span data-stu-id="4f042-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-139">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4f042-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-140">**13**</span><span class="sxs-lookup"><span data-stu-id="4f042-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-141">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="4f042-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-142">**14**</span><span class="sxs-lookup"><span data-stu-id="4f042-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-143">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4f042-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-144">**15**</span><span class="sxs-lookup"><span data-stu-id="4f042-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-145">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="4f042-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-146">**16**</span><span class="sxs-lookup"><span data-stu-id="4f042-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-147">Questo servizio viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4f042-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-148">**17**</span><span class="sxs-lookup"><span data-stu-id="4f042-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-149">Il servizio non ha thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4f042-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-150">**18**</span><span class="sxs-lookup"><span data-stu-id="4f042-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-151">Il servizio presenta dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="4f042-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-152">**19**</span><span class="sxs-lookup"><span data-stu-id="4f042-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-153">Un servizio viene eseguito con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="4f042-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-154">**20**</span><span class="sxs-lookup"><span data-stu-id="4f042-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-155">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="4f042-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-156">**21**</span><span class="sxs-lookup"><span data-stu-id="4f042-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-157">Al servizio sono stati passati parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="4f042-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-158">**22**</span><span class="sxs-lookup"><span data-stu-id="4f042-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-159">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="4f042-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-160">**23**</span><span class="sxs-lookup"><span data-stu-id="4f042-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-161">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="4f042-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-162">**24**</span><span class="sxs-lookup"><span data-stu-id="4f042-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="4f042-163">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="4f042-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f042-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f042-164">Requirements</span></span>



| <span data-ttu-id="4f042-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f042-165">Requirement</span></span> | <span data-ttu-id="4f042-166">Valore</span><span class="sxs-lookup"><span data-stu-id="4f042-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f042-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f042-167">Minimum supported client</span></span><br/> | <span data-ttu-id="4f042-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f042-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f042-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f042-169">Minimum supported server</span></span><br/> | <span data-ttu-id="4f042-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f042-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f042-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4f042-171">Namespace</span></span><br/>                | <span data-ttu-id="4f042-172">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4f042-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4f042-173">MOF</span><span class="sxs-lookup"><span data-stu-id="4f042-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f042-174"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f042-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f042-175">DLL</span><span class="sxs-lookup"><span data-stu-id="4f042-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f042-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f042-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f042-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f042-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f042-178">**Servizio \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="4f042-178">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

<span data-ttu-id="4f042-179">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4f042-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4f042-180">**Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="4f042-180">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="4f042-181">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="4f042-181">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

