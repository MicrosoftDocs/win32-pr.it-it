---
description: Tenta di inviare un codice di controllo definito dall'utente al servizio a cui si fa riferimento.
ms.assetid: a7132c9b-6faf-4182-a5b8-3f2334c1a74b
ms.tgt_platform: multiple
title: Metodo UserControlService della classe Win32_Service (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8c523617826bd5d608b8c6b1ee242863f7591a61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966302"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="ba659-103">Metodo UserControlService della classe Win32_Service (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ba659-103">UserControlService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ba659-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** tenta di inviare un codice di controllo definito dall'utente al servizio a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="ba659-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="ba659-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="ba659-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ba659-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ba659-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ba659-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba659-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="ba659-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba659-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba659-109">*ControlCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba659-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba659-110">Specifica i valori definiti (da 128 a 255) che forniscono i comandi di controllo specifici per un utente.</span><span class="sxs-lookup"><span data-stu-id="ba659-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba659-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba659-111">Return value</span></span>

<span data-ttu-id="ba659-112">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="ba659-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="ba659-113">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ba659-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ba659-114">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ba659-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ba659-115">**0**</span><span class="sxs-lookup"><span data-stu-id="ba659-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-116">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="ba659-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-117">**1**</span><span class="sxs-lookup"><span data-stu-id="ba659-117">**1**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-118">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="ba659-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-119">**2**</span><span class="sxs-lookup"><span data-stu-id="ba659-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-120">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="ba659-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-121">**3**</span><span class="sxs-lookup"><span data-stu-id="ba659-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-122">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="ba659-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-123">**4**</span><span class="sxs-lookup"><span data-stu-id="ba659-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-124">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="ba659-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-125">**5**</span><span class="sxs-lookup"><span data-stu-id="ba659-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-126">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="ba659-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-127">**6**</span><span class="sxs-lookup"><span data-stu-id="ba659-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-128">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="ba659-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-129">**7**</span><span class="sxs-lookup"><span data-stu-id="ba659-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-130">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="ba659-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-131">**8**</span><span class="sxs-lookup"><span data-stu-id="ba659-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-132">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="ba659-132">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-133">**9**</span><span class="sxs-lookup"><span data-stu-id="ba659-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-134">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="ba659-134">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-135">**10**</span><span class="sxs-lookup"><span data-stu-id="ba659-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-136">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ba659-136">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-137">**11**</span><span class="sxs-lookup"><span data-stu-id="ba659-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-138">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="ba659-138">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-139">**12**</span><span class="sxs-lookup"><span data-stu-id="ba659-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-140">Una dipendenza su cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="ba659-140">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-141">**13**</span><span class="sxs-lookup"><span data-stu-id="ba659-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-142">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="ba659-142">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-143">**14**</span><span class="sxs-lookup"><span data-stu-id="ba659-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-144">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="ba659-144">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-145">**15**</span><span class="sxs-lookup"><span data-stu-id="ba659-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-146">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ba659-146">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-147">**16**</span><span class="sxs-lookup"><span data-stu-id="ba659-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-148">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="ba659-148">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-149">**17**</span><span class="sxs-lookup"><span data-stu-id="ba659-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-150">Il servizio non dispone di un thread di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ba659-150">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-151">**18**</span><span class="sxs-lookup"><span data-stu-id="ba659-151">**18**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-152">Il servizio ha dipendenze circolari all'avvio.</span><span class="sxs-lookup"><span data-stu-id="ba659-152">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-153">**19**</span><span class="sxs-lookup"><span data-stu-id="ba659-153">**19**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-154">Un servizio è in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="ba659-154">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-155">**20**</span><span class="sxs-lookup"><span data-stu-id="ba659-155">**20**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-156">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="ba659-156">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-157">**21**</span><span class="sxs-lookup"><span data-stu-id="ba659-157">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-158">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="ba659-158">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-159">**22**</span><span class="sxs-lookup"><span data-stu-id="ba659-159">**22**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-160">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="ba659-160">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-161">**23**</span><span class="sxs-lookup"><span data-stu-id="ba659-161">**23**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-162">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="ba659-162">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ba659-163">**24**</span><span class="sxs-lookup"><span data-stu-id="ba659-163">**24**</span></span>
</dt> <dd>

<span data-ttu-id="ba659-164">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ba659-164">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba659-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba659-165">Requirements</span></span>



| <span data-ttu-id="ba659-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba659-166">Requirement</span></span> | <span data-ttu-id="ba659-167">Valore</span><span class="sxs-lookup"><span data-stu-id="ba659-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba659-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba659-168">Minimum supported client</span></span><br/> | <span data-ttu-id="ba659-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba659-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ba659-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba659-170">Minimum supported server</span></span><br/> | <span data-ttu-id="ba659-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba659-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ba659-172">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ba659-172">Namespace</span></span><br/>                | <span data-ttu-id="ba659-173">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ba659-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ba659-174">MOF</span><span class="sxs-lookup"><span data-stu-id="ba659-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba659-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba659-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba659-176">DLL</span><span class="sxs-lookup"><span data-stu-id="ba659-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba659-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba659-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba659-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba659-178">See also</span></span>

<dl> <dt>

<span data-ttu-id="ba659-179">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ba659-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ba659-180">**\_Servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="ba659-180">**Win32\_Service**</span></span>](win32-service.md)
</dt> </dl>

 

