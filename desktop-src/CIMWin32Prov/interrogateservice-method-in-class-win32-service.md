---
description: Richiede che il servizio a cui si fa riferimento aggiorni lo stato a Service Manager.
ms.assetid: a4ea8753-1859-4d97-b9ca-47598c7e7654
ms.tgt_platform: multiple
title: Metodo InterrogateService della classe Win32_Service (provider WMI CIMWin32)
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
ms.openlocfilehash: 7ad1f56afcbe42ced19da823c454291a7b5282d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126477"
---
# <a name="interrogateservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="212e3-103">Metodo InterrogateService della classe Win32_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="212e3-103">InterrogateService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="212e3-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** richiede che il servizio a cui si fa riferimento aggiorni lo stato a Service Manager.</span><span class="sxs-lookup"><span data-stu-id="212e3-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="212e3-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="212e3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="212e3-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="212e3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="212e3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="212e3-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="212e3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="212e3-108">Parameters</span></span>

<span data-ttu-id="212e3-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="212e3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="212e3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="212e3-110">Return value</span></span>

<span data-ttu-id="212e3-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="212e3-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="212e3-112">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="212e3-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="212e3-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="212e3-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="212e3-114">**0**</span><span class="sxs-lookup"><span data-stu-id="212e3-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-115">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="212e3-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-116">**1**</span><span class="sxs-lookup"><span data-stu-id="212e3-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-117">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="212e3-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-118">**2**</span><span class="sxs-lookup"><span data-stu-id="212e3-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-119">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="212e3-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-120">**3**</span><span class="sxs-lookup"><span data-stu-id="212e3-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-121">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="212e3-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-122">**4**</span><span class="sxs-lookup"><span data-stu-id="212e3-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-123">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="212e3-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-124">**5**</span><span class="sxs-lookup"><span data-stu-id="212e3-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-125">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="212e3-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-126">**6**</span><span class="sxs-lookup"><span data-stu-id="212e3-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-127">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="212e3-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-128">**7**</span><span class="sxs-lookup"><span data-stu-id="212e3-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-129">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="212e3-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-130">**8**</span><span class="sxs-lookup"><span data-stu-id="212e3-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-131">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="212e3-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-132">**9**</span><span class="sxs-lookup"><span data-stu-id="212e3-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-133">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="212e3-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-134">**10**</span><span class="sxs-lookup"><span data-stu-id="212e3-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-135">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="212e3-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-136">**11**</span><span class="sxs-lookup"><span data-stu-id="212e3-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-137">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="212e3-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-138">**12**</span><span class="sxs-lookup"><span data-stu-id="212e3-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-139">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="212e3-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-140">**13**</span><span class="sxs-lookup"><span data-stu-id="212e3-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-141">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="212e3-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-142">**14**</span><span class="sxs-lookup"><span data-stu-id="212e3-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-143">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="212e3-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-144">**15**</span><span class="sxs-lookup"><span data-stu-id="212e3-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-145">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="212e3-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-146">**16**</span><span class="sxs-lookup"><span data-stu-id="212e3-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-147">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="212e3-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-148">**17**</span><span class="sxs-lookup"><span data-stu-id="212e3-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-149">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="212e3-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-150">**18**</span><span class="sxs-lookup"><span data-stu-id="212e3-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-151">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="212e3-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-152">**19**</span><span class="sxs-lookup"><span data-stu-id="212e3-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-153">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="212e3-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-154">**20**</span><span class="sxs-lookup"><span data-stu-id="212e3-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-155">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="212e3-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-156">**21**</span><span class="sxs-lookup"><span data-stu-id="212e3-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-157">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="212e3-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-158">**22**</span><span class="sxs-lookup"><span data-stu-id="212e3-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-159">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="212e3-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-160">**23**</span><span class="sxs-lookup"><span data-stu-id="212e3-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-161">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="212e3-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="212e3-162">**24**</span><span class="sxs-lookup"><span data-stu-id="212e3-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="212e3-163">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="212e3-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="212e3-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="212e3-164">Requirements</span></span>



| <span data-ttu-id="212e3-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="212e3-165">Requirement</span></span> | <span data-ttu-id="212e3-166">Valore</span><span class="sxs-lookup"><span data-stu-id="212e3-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="212e3-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="212e3-167">Minimum supported client</span></span><br/> | <span data-ttu-id="212e3-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="212e3-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="212e3-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="212e3-169">Minimum supported server</span></span><br/> | <span data-ttu-id="212e3-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="212e3-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="212e3-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="212e3-171">Namespace</span></span><br/>                | <span data-ttu-id="212e3-172">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="212e3-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="212e3-173">MOF</span><span class="sxs-lookup"><span data-stu-id="212e3-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="212e3-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="212e3-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="212e3-175">DLL</span><span class="sxs-lookup"><span data-stu-id="212e3-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="212e3-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="212e3-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="212e3-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="212e3-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="212e3-178">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="212e3-178">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

<span data-ttu-id="212e3-179">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="212e3-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="212e3-180">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="212e3-180">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="212e3-181">Attività WMI: Servizi</span><span class="sxs-lookup"><span data-stu-id="212e3-181">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

