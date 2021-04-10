---
description: Inserisce il servizio rappresentato dall' \_ oggetto SystemDriver Win32 nello stato interrotto.
ms.assetid: 0fa8ef44-39eb-448e-8d33-38a5af9a0c13
ms.tgt_platform: multiple
title: Metodo StopService della classe Win32_SystemDriver (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb45a414ea9cc7198487dbb61d122722816f4728
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966130"
---
# <a name="stopservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="eb90e-103">Metodo StopService della \_ classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="eb90e-103">StopService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="eb90e-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** posiziona il servizio rappresentato dall' [**oggetto \_ SystemDriver Win32**](win32-systemdriver.md) nello stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="eb90e-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service represented by the [**Win32\_SystemDriver**](win32-systemdriver.md) object in the stopped state.</span></span>

<span data-ttu-id="eb90e-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="eb90e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="eb90e-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="eb90e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb90e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb90e-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="eb90e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb90e-108">Parameters</span></span>

<span data-ttu-id="eb90e-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="eb90e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb90e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb90e-110">Return value</span></span>

<span data-ttu-id="eb90e-111">Restituisce un valore pari a 0 (zero) se il servizio è stato arrestato correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="eb90e-111">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="eb90e-112">**0**</span><span class="sxs-lookup"><span data-stu-id="eb90e-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-113">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="eb90e-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-114">**1**</span><span class="sxs-lookup"><span data-stu-id="eb90e-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-115">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="eb90e-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-116">**2**</span><span class="sxs-lookup"><span data-stu-id="eb90e-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-117">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="eb90e-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-118">**3**</span><span class="sxs-lookup"><span data-stu-id="eb90e-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-119">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="eb90e-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-120">**4**</span><span class="sxs-lookup"><span data-stu-id="eb90e-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-121">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="eb90e-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-122">**5**</span><span class="sxs-lookup"><span data-stu-id="eb90e-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-123">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="eb90e-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-124">**6**</span><span class="sxs-lookup"><span data-stu-id="eb90e-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-125">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="eb90e-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-126">**7**</span><span class="sxs-lookup"><span data-stu-id="eb90e-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-127">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="eb90e-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-128">**8**</span><span class="sxs-lookup"><span data-stu-id="eb90e-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-129">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="eb90e-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-130">**9**</span><span class="sxs-lookup"><span data-stu-id="eb90e-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-131">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="eb90e-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-132">**10**</span><span class="sxs-lookup"><span data-stu-id="eb90e-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-133">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="eb90e-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-134">**11**</span><span class="sxs-lookup"><span data-stu-id="eb90e-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-135">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="eb90e-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-136">**12**</span><span class="sxs-lookup"><span data-stu-id="eb90e-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-137">Una dipendenza per cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="eb90e-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-138">**13**</span><span class="sxs-lookup"><span data-stu-id="eb90e-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-139">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="eb90e-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-140">**14**</span><span class="sxs-lookup"><span data-stu-id="eb90e-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-141">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="eb90e-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-142">**15**</span><span class="sxs-lookup"><span data-stu-id="eb90e-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-143">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="eb90e-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-144">**16**</span><span class="sxs-lookup"><span data-stu-id="eb90e-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-145">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="eb90e-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-146">**17**</span><span class="sxs-lookup"><span data-stu-id="eb90e-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-147">Nessun thread di esecuzione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="eb90e-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-148">**18**</span><span class="sxs-lookup"><span data-stu-id="eb90e-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-149">All'avvio del servizio sono state rilevate dipendenze circolari.</span><span class="sxs-lookup"><span data-stu-id="eb90e-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-150">**19**</span><span class="sxs-lookup"><span data-stu-id="eb90e-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-151">È presente un servizio in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="eb90e-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-152">**20**</span><span class="sxs-lookup"><span data-stu-id="eb90e-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-153">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="eb90e-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-154">**21**</span><span class="sxs-lookup"><span data-stu-id="eb90e-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-155">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="eb90e-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-156">**22**</span><span class="sxs-lookup"><span data-stu-id="eb90e-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-157">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="eb90e-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-158">**23**</span><span class="sxs-lookup"><span data-stu-id="eb90e-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-159">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="eb90e-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="eb90e-160">**24**</span><span class="sxs-lookup"><span data-stu-id="eb90e-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="eb90e-161">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="eb90e-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="eb90e-162">Esempio</span><span class="sxs-lookup"><span data-stu-id="eb90e-162">Examples</span></span>

<span data-ttu-id="eb90e-163">Il codice di PowerShell seguente arresta il servizio "classe stampante USB Microsoft".</span><span class="sxs-lookup"><span data-stu-id="eb90e-163">The following PowerShell code stops the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.StopService()
"Stop Service Called. Return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="eb90e-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb90e-164">Requirements</span></span>



| <span data-ttu-id="eb90e-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb90e-165">Requirement</span></span> | <span data-ttu-id="eb90e-166">Valore</span><span class="sxs-lookup"><span data-stu-id="eb90e-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb90e-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb90e-167">Minimum supported client</span></span><br/> | <span data-ttu-id="eb90e-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb90e-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb90e-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb90e-169">Minimum supported server</span></span><br/> | <span data-ttu-id="eb90e-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb90e-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb90e-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eb90e-171">Namespace</span></span><br/>                | <span data-ttu-id="eb90e-172">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="eb90e-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb90e-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb90e-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb90e-174"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb90e-174"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="eb90e-175">MOF</span><span class="sxs-lookup"><span data-stu-id="eb90e-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb90e-176"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb90e-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb90e-177">DLL</span><span class="sxs-lookup"><span data-stu-id="eb90e-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb90e-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb90e-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb90e-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb90e-179">See also</span></span>

<dl> <dt>

<span data-ttu-id="eb90e-180">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb90e-180">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="eb90e-181">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="eb90e-181">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

