---
description: Tenta di collocare il servizio gestito dal driver di sistema logico nello stato sospeso.
ms.assetid: f5e960c1-868b-4b7b-9ea5-0fb8a9cfbafa
ms.tgt_platform: multiple
title: Metodo PauseService della classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a85c49a8ea81cc9af9a99f238bdafb473ca85050
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966373"
---
# <a name="pauseservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="0b750-103">Metodo PauseService della \_ classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="0b750-103">PauseService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="0b750-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** tenta di collocare il servizio gestito dal driver di sistema logico nello stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="0b750-104">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service managed by the logical system driver in the paused state.</span></span>

<span data-ttu-id="0b750-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="0b750-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0b750-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0b750-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b750-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b750-107">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="0b750-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b750-108">Parameters</span></span>

<span data-ttu-id="0b750-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0b750-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b750-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b750-110">Return value</span></span>

<span data-ttu-id="0b750-111">Restituisce un valore pari a 0 (zero) se la richiesta **PauseService** è stata accettata, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="0b750-111">Returns a value of 0 (zero) if the **PauseService** request was accepted, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0b750-112">**0**</span><span class="sxs-lookup"><span data-stu-id="0b750-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-113">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="0b750-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-114">**1**</span><span class="sxs-lookup"><span data-stu-id="0b750-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-115">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="0b750-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-116">**2**</span><span class="sxs-lookup"><span data-stu-id="0b750-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-117">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="0b750-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-118">**3**</span><span class="sxs-lookup"><span data-stu-id="0b750-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-119">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="0b750-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-120">**4**</span><span class="sxs-lookup"><span data-stu-id="0b750-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-121">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="0b750-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-122">**5**</span><span class="sxs-lookup"><span data-stu-id="0b750-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-123">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="0b750-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-124">**6**</span><span class="sxs-lookup"><span data-stu-id="0b750-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-125">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="0b750-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-126">**7**</span><span class="sxs-lookup"><span data-stu-id="0b750-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-127">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="0b750-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-128">**8**</span><span class="sxs-lookup"><span data-stu-id="0b750-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-129">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="0b750-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-130">**9**</span><span class="sxs-lookup"><span data-stu-id="0b750-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-131">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="0b750-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-132">**10**</span><span class="sxs-lookup"><span data-stu-id="0b750-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-133">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0b750-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-134">**11**</span><span class="sxs-lookup"><span data-stu-id="0b750-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-135">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="0b750-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-136">**12**</span><span class="sxs-lookup"><span data-stu-id="0b750-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-137">Una dipendenza per cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="0b750-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-138">**13**</span><span class="sxs-lookup"><span data-stu-id="0b750-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-139">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="0b750-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-140">**14**</span><span class="sxs-lookup"><span data-stu-id="0b750-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-141">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="0b750-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-142">**15**</span><span class="sxs-lookup"><span data-stu-id="0b750-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-143">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="0b750-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-144">**16**</span><span class="sxs-lookup"><span data-stu-id="0b750-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-145">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="0b750-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-146">**17**</span><span class="sxs-lookup"><span data-stu-id="0b750-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-147">Nessun thread di esecuzione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="0b750-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-148">**18**</span><span class="sxs-lookup"><span data-stu-id="0b750-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-149">All'avvio del servizio sono state rilevate dipendenze circolari.</span><span class="sxs-lookup"><span data-stu-id="0b750-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-150">**19**</span><span class="sxs-lookup"><span data-stu-id="0b750-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-151">È presente un servizio in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="0b750-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-152">**20**</span><span class="sxs-lookup"><span data-stu-id="0b750-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-153">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="0b750-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-154">**21**</span><span class="sxs-lookup"><span data-stu-id="0b750-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-155">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="0b750-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-156">**22**</span><span class="sxs-lookup"><span data-stu-id="0b750-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-157">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="0b750-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-158">**23**</span><span class="sxs-lookup"><span data-stu-id="0b750-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-159">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="0b750-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="0b750-160">**24**</span><span class="sxs-lookup"><span data-stu-id="0b750-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="0b750-161">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="0b750-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="0b750-162">Esempio</span><span class="sxs-lookup"><span data-stu-id="0b750-162">Examples</span></span>

<span data-ttu-id="0b750-163">Il codice di PowerShell seguente tenta di sospendere il servizio "classe stampante USB Microsoft".</span><span class="sxs-lookup"><span data-stu-id="0b750-163">The following PowerShell code attempts to pause the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.PauseService()
"Pause Service called. The return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="0b750-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b750-164">Requirements</span></span>



| <span data-ttu-id="0b750-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b750-165">Requirement</span></span> | <span data-ttu-id="0b750-166">Valore</span><span class="sxs-lookup"><span data-stu-id="0b750-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b750-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b750-167">Minimum supported client</span></span><br/> | <span data-ttu-id="0b750-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b750-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b750-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b750-169">Minimum supported server</span></span><br/> | <span data-ttu-id="0b750-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b750-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b750-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0b750-171">Namespace</span></span><br/>                | <span data-ttu-id="0b750-172">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0b750-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b750-173">MOF</span><span class="sxs-lookup"><span data-stu-id="0b750-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b750-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b750-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b750-175">DLL</span><span class="sxs-lookup"><span data-stu-id="0b750-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b750-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b750-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b750-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b750-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="0b750-178">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b750-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0b750-179">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="0b750-179">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

