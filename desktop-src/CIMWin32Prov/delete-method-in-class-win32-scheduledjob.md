---
description: Il&Delete \# 8194; Il metodo della classe WMI Elimina un processo pianificato.
ms.assetid: 064ff3f8-6d41-4f8d-a511-6c051bb48a5b
ms.tgt_platform: multiple
title: Metodo Delete della classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd375c3da85bd72bddfc97ed3f57e52103578441
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127759"
---
# <a name="delete-method-of-the-win32_scheduledjob-class"></a><span data-ttu-id="5217b-103">Metodo Delete della classe Win32 \_ ScheduledJob</span><span class="sxs-lookup"><span data-stu-id="5217b-103">Delete method of the Win32\_ScheduledJob class</span></span>

<span data-ttu-id="5217b-104">Il metodo **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) Elimina un processo pianificato.</span><span class="sxs-lookup"><span data-stu-id="5217b-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes a scheduled job.</span></span>

<span data-ttu-id="5217b-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="5217b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5217b-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5217b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5217b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5217b-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="5217b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5217b-108">Parameters</span></span>

<span data-ttu-id="5217b-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5217b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5217b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5217b-110">Return value</span></span>

<span data-ttu-id="5217b-111">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="5217b-111">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="5217b-112">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5217b-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5217b-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5217b-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5217b-114">**Operazione completata**</span><span class="sxs-lookup"><span data-stu-id="5217b-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="5217b-115">0</span><span class="sxs-lookup"><span data-stu-id="5217b-115">0</span></span>

<span data-ttu-id="5217b-116">La richiesta è stata accettata.</span><span class="sxs-lookup"><span data-stu-id="5217b-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="5217b-117">**Non supportato**</span><span class="sxs-lookup"><span data-stu-id="5217b-117">**Not supported**</span></span>
</dt> <dd>

<span data-ttu-id="5217b-118">1</span><span class="sxs-lookup"><span data-stu-id="5217b-118">1</span></span>

<span data-ttu-id="5217b-119">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="5217b-119">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5217b-120">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="5217b-120">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="5217b-121">2</span><span class="sxs-lookup"><span data-stu-id="5217b-121">2</span></span>

<span data-ttu-id="5217b-122">L'utente non dispone dell'accesso necessario.</span><span class="sxs-lookup"><span data-stu-id="5217b-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="5217b-123">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="5217b-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="5217b-124">8</span><span class="sxs-lookup"><span data-stu-id="5217b-124">8</span></span>

<span data-ttu-id="5217b-125">Processo interattivo.</span><span class="sxs-lookup"><span data-stu-id="5217b-125">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="5217b-126">**Impossibile trovare il percorso**</span><span class="sxs-lookup"><span data-stu-id="5217b-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="5217b-127">9</span><span class="sxs-lookup"><span data-stu-id="5217b-127">9</span></span>

<span data-ttu-id="5217b-128">Impossibile trovare il percorso di directory del file eseguibile del servizio.</span><span class="sxs-lookup"><span data-stu-id="5217b-128">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="5217b-129">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="5217b-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5217b-130">21</span><span class="sxs-lookup"><span data-stu-id="5217b-130">21</span></span>

<span data-ttu-id="5217b-131">Sono stati passati parametri non validi al servizio.</span><span class="sxs-lookup"><span data-stu-id="5217b-131">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="5217b-132">**Servizio non avviato**</span><span class="sxs-lookup"><span data-stu-id="5217b-132">**Service not started**</span></span>
</dt> <dd>

<span data-ttu-id="5217b-133">22</span><span class="sxs-lookup"><span data-stu-id="5217b-133">22</span></span>

<span data-ttu-id="5217b-134">L'account con cui viene eseguito il servizio non è valido o non dispone delle autorizzazioni necessarie per eseguire il servizio.</span><span class="sxs-lookup"><span data-stu-id="5217b-134">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="5217b-135">**Altri**</span><span class="sxs-lookup"><span data-stu-id="5217b-135">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="5217b-136">23 4294967295</span><span class="sxs-lookup"><span data-stu-id="5217b-136">23 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5217b-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5217b-137">Requirements</span></span>



| <span data-ttu-id="5217b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="5217b-138">Requirement</span></span> | <span data-ttu-id="5217b-139">Valore</span><span class="sxs-lookup"><span data-stu-id="5217b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5217b-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5217b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5217b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5217b-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5217b-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5217b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5217b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5217b-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5217b-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5217b-144">Namespace</span></span><br/>                | <span data-ttu-id="5217b-145">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5217b-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5217b-146">MOF</span><span class="sxs-lookup"><span data-stu-id="5217b-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5217b-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5217b-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5217b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="5217b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5217b-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5217b-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5217b-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5217b-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="5217b-151">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5217b-151">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5217b-152">**\_ScheduledJob Win32**</span><span class="sxs-lookup"><span data-stu-id="5217b-152">**Win32\_ScheduledJob**</span></span>](win32-scheduledjob.md)
</dt> </dl>

 

