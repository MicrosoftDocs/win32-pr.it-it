---
description: Tenta di collocare il servizio gestito dal driver di sistema nello stato di avvio.
ms.assetid: 3f9d29aa-b549-4a55-be9c-01fad4932fe6
ms.tgt_platform: multiple
title: Metodo StartService della classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c189d9b5f24a3ccc803a588abb94337ee65a1da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225658"
---
# <a name="startservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="b1d29-103">Metodo StartService della \_ classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="b1d29-103">StartService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="b1d29-104">Il metodo **StartService** tenta di collocare il servizio gestito dal driver di sistema nello stato di avvio.</span><span class="sxs-lookup"><span data-stu-id="b1d29-104">The **StartService** method attempts to place the service managed by the system driver into its startup state.</span></span>

<span data-ttu-id="b1d29-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b1d29-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b1d29-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b1d29-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1d29-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1d29-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="b1d29-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1d29-108">Parameters</span></span>

<span data-ttu-id="b1d29-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b1d29-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1d29-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1d29-110">Return value</span></span>

<span data-ttu-id="b1d29-111">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b1d29-111">Returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b1d29-112">**0**</span><span class="sxs-lookup"><span data-stu-id="b1d29-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-113">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="b1d29-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-114">**1**</span><span class="sxs-lookup"><span data-stu-id="b1d29-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-115">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="b1d29-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-116">**2**</span><span class="sxs-lookup"><span data-stu-id="b1d29-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-117">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="b1d29-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-118">**3**</span><span class="sxs-lookup"><span data-stu-id="b1d29-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-119">Impossibile arrestare il servizio perché altri servizi in esecuzione dipendono dal servizio.</span><span class="sxs-lookup"><span data-stu-id="b1d29-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-120">**4**</span><span class="sxs-lookup"><span data-stu-id="b1d29-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-121">Il codice di controllo richiesto non è valido o non è accettabile per il servizio.</span><span class="sxs-lookup"><span data-stu-id="b1d29-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-122">**5**</span><span class="sxs-lookup"><span data-stu-id="b1d29-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-123">Impossibile inviare il codice di controllo richiesto al servizio perché lo stato del servizio ([**Win32 \_ BaseService**](win32-baseservice.md).**Proprietà state** ) è uguale a 0, 1 o 2.</span><span class="sxs-lookup"><span data-stu-id="b1d29-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-124">**6**</span><span class="sxs-lookup"><span data-stu-id="b1d29-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-125">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="b1d29-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-126">**7**</span><span class="sxs-lookup"><span data-stu-id="b1d29-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-127">Il servizio non ha risposto in tempo utile alla richiesta di avvio.</span><span class="sxs-lookup"><span data-stu-id="b1d29-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-128">**8**</span><span class="sxs-lookup"><span data-stu-id="b1d29-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-129">Errore sconosciuto durante l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="b1d29-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-130">**9**</span><span class="sxs-lookup"><span data-stu-id="b1d29-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-131">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="b1d29-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-132">**10**</span><span class="sxs-lookup"><span data-stu-id="b1d29-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-133">Il servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b1d29-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-134">**11**</span><span class="sxs-lookup"><span data-stu-id="b1d29-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-135">Il database a cui aggiungere il nuovo servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="b1d29-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-136">**12**</span><span class="sxs-lookup"><span data-stu-id="b1d29-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-137">Una dipendenza per cui si basa questo servizio è stata rimossa dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b1d29-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-138">**13**</span><span class="sxs-lookup"><span data-stu-id="b1d29-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-139">Impossibile trovare un servizio dipendente necessario.</span><span class="sxs-lookup"><span data-stu-id="b1d29-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-140">**14**</span><span class="sxs-lookup"><span data-stu-id="b1d29-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-141">Il servizio è stato disabilitato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b1d29-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-142">**15**</span><span class="sxs-lookup"><span data-stu-id="b1d29-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-143">Il servizio non dispone delle credenziali di autenticazione corrette per l'esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b1d29-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-144">**16**</span><span class="sxs-lookup"><span data-stu-id="b1d29-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-145">Questo servizio verrà rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b1d29-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-146">**17**</span><span class="sxs-lookup"><span data-stu-id="b1d29-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-147">Nessun thread di esecuzione per il servizio.</span><span class="sxs-lookup"><span data-stu-id="b1d29-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-148">**18**</span><span class="sxs-lookup"><span data-stu-id="b1d29-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-149">All'avvio del servizio sono state rilevate dipendenze circolari.</span><span class="sxs-lookup"><span data-stu-id="b1d29-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-150">**19**</span><span class="sxs-lookup"><span data-stu-id="b1d29-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-151">È presente un servizio in esecuzione con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="b1d29-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-152">**20**</span><span class="sxs-lookup"><span data-stu-id="b1d29-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-153">Il nome del servizio contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="b1d29-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-154">**21**</span><span class="sxs-lookup"><span data-stu-id="b1d29-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-155">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="b1d29-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-156">**22**</span><span class="sxs-lookup"><span data-stu-id="b1d29-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-157">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="b1d29-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-158">**23**</span><span class="sxs-lookup"><span data-stu-id="b1d29-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-159">Il servizio esiste già nel database dei servizi disponibili dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b1d29-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b1d29-160">**24**</span><span class="sxs-lookup"><span data-stu-id="b1d29-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="b1d29-161">Il servizio è attualmente sospeso nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b1d29-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b1d29-162">Esempio</span><span class="sxs-lookup"><span data-stu-id="b1d29-162">Examples</span></span>

<span data-ttu-id="b1d29-163">Il codice di PowerShell seguente avvia il servizio "classe stampante USB Microsoft".</span><span class="sxs-lookup"><span data-stu-id="b1d29-163">The following PowerShell code starts the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.StartService()
"Start Service Called. Return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="b1d29-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1d29-164">Requirements</span></span>



| <span data-ttu-id="b1d29-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1d29-165">Requirement</span></span> | <span data-ttu-id="b1d29-166">Valore</span><span class="sxs-lookup"><span data-stu-id="b1d29-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d29-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1d29-167">Minimum supported client</span></span><br/> | <span data-ttu-id="b1d29-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1d29-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1d29-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1d29-169">Minimum supported server</span></span><br/> | <span data-ttu-id="b1d29-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1d29-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1d29-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b1d29-171">Namespace</span></span><br/>                | <span data-ttu-id="b1d29-172">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b1d29-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b1d29-173">MOF</span><span class="sxs-lookup"><span data-stu-id="b1d29-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1d29-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1d29-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1d29-175">DLL</span><span class="sxs-lookup"><span data-stu-id="b1d29-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1d29-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1d29-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1d29-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1d29-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1d29-178">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b1d29-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b1d29-179">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="b1d29-179">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

