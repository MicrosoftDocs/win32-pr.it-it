---
description: Il&di priorità \# 32; Il metodo della classe WMI tenta di modificare la priorità di esecuzione del processo.
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: Metodo di priorità della classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.SetPriority
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf08057ec075448d9912e37c33b6087c381f97d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524145"
---
# <a name="setpriority-method-of-the-win32_process-class"></a><span data-ttu-id="35dce-103">Metodo di priorità della classe di \_ processo Win32</span><span class="sxs-lookup"><span data-stu-id="35dce-103">SetPriority method of the Win32\_Process class</span></span>

<span data-ttu-id="35dce-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) di **priorità** tenta di modificare la priorità di esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="35dce-104">The **SetPriority** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to change the execution priority of the process.</span></span>

<span data-ttu-id="35dce-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="35dce-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="35dce-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="35dce-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="35dce-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35dce-107">Syntax</span></span>


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a><span data-ttu-id="35dce-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="35dce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35dce-109">*Priorità* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="35dce-109">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35dce-110">Nuova classe di priorità per il processo.</span><span class="sxs-lookup"><span data-stu-id="35dce-110">New priority class for the process.</span></span> <span data-ttu-id="35dce-111">Si noti che questi valori sono diversi da quelli indicati in modo esplicito nella proprietà **Priority** del [**\_ processo Win32**](win32-process.md).</span><span class="sxs-lookup"><span data-stu-id="35dce-111">Note that these values are different than those explicitly stated in the **Priority** property of [**Win32\_Process**](win32-process.md).</span></span>

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="35dce-112"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inattività** (64)</span><span class="sxs-lookup"><span data-stu-id="35dce-112"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="35dce-113">Specificata per un processo con thread eseguiti solo quando il sistema è inattivo.</span><span class="sxs-lookup"><span data-stu-id="35dce-113">Specified for a process with threads that run only when the system is idle.</span></span> <span data-ttu-id="35dce-114">I thread del processo vengono interrotti dai thread di un processo eseguito in una classe di priorità superiore, ad esempio, un screen saver.</span><span class="sxs-lookup"><span data-stu-id="35dce-114">The threads of the process are preempted by the threads of a process that run in a higher priority class, for example, a screen saver.</span></span> <span data-ttu-id="35dce-115">La classe di priorità inattiva viene ereditata dai processi figlio.</span><span class="sxs-lookup"><span data-stu-id="35dce-115">The idle-priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="35dce-116"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Inferiore al normale** (16384)</span><span class="sxs-lookup"><span data-stu-id="35dce-116"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="35dce-117">Indica un processo con priorità superiore alla **\_ \_ classe di priorità di inattività**, ma al di sotto della **\_ \_ classe di priorità normale**.</span><span class="sxs-lookup"><span data-stu-id="35dce-117">Indicates a process that has priority above **IDLE\_PRIORITY\_CLASS**, but below **NORMAL\_PRIORITY\_CLASS**.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="35dce-118"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normale** (32)</span><span class="sxs-lookup"><span data-stu-id="35dce-118"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="35dce-119">Specificato per un processo senza particolari esigenze di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="35dce-119">Specified for a process with no special scheduling needs.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="35dce-120"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Superiore al normale** (32768)</span><span class="sxs-lookup"><span data-stu-id="35dce-120"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="35dce-121">Indica un processo con priorità superiore alla **\_ \_ classe di priorità normale**, ma al di sotto della **\_ \_ classe con priorità alta**.</span><span class="sxs-lookup"><span data-stu-id="35dce-121">Indicates a process that has priority above **NORMAL\_PRIORITY\_CLASS**, but below **HIGH\_PRIORITY\_CLASS**.</span></span>

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span data-ttu-id="35dce-122"><span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**Priorità alta** (128)</span><span class="sxs-lookup"><span data-stu-id="35dce-122"><span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**High Priority** (128)</span></span>


</dt> <dd>

<span data-ttu-id="35dce-123">Specificato per un processo che esegue attività critiche al tempo che devono essere eseguite immediatamente.</span><span class="sxs-lookup"><span data-stu-id="35dce-123">Specified for a process that performs time-critical tasks that must be executed immediately.</span></span> <span data-ttu-id="35dce-124">I thread del processo hanno la precedenza sui thread dei processi con classe di priorità normal o idle.</span><span class="sxs-lookup"><span data-stu-id="35dce-124">The threads of the process preempt the threads of normal or idle priority class processes.</span></span> <span data-ttu-id="35dce-125">Un esempio è il Elenco attività, che deve rispondere rapidamente quando viene chiamato dall'utente, indipendentemente dal carico sul sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="35dce-125">An example is the Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="35dce-126">Prestare particolare attenzione quando si utilizza la classe con priorità alta, perché un'applicazione di classe con priorità alta può utilizzare quasi tutto il tempo di CPU disponibile.</span><span class="sxs-lookup"><span data-stu-id="35dce-126">Use extreme care when using the high-priority class, because a high-priority class application can use nearly all of the available CPU time.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="35dce-127"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tempo reale** (256)</span><span class="sxs-lookup"><span data-stu-id="35dce-127"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="35dce-128">Specificato per un processo con la massima priorità possibile.</span><span class="sxs-lookup"><span data-stu-id="35dce-128">Specified for a process that has the highest possible priority.</span></span> <span data-ttu-id="35dce-129">I thread del processo hanno la precedenza sui thread di tutti gli altri processi, inclusi i processi del sistema operativo che eseguono attività importanti.</span><span class="sxs-lookup"><span data-stu-id="35dce-129">The threads of the process preempt the threads of all of the other processes, including operating system processes that perform important tasks.</span></span> <span data-ttu-id="35dce-130">Ad esempio, un processo in tempo reale che viene eseguito per più di un intervallo molto breve può causare la mancata scaricamento delle cache del disco o la mancata risposta del mouse.</span><span class="sxs-lookup"><span data-stu-id="35dce-130">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush or a mouse to be unresponsive.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35dce-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35dce-131">Return value</span></span>

<span data-ttu-id="35dce-132">Restituisce uno dei valori elencati nell'elenco seguente o un valore diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="35dce-132">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="35dce-133">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="35dce-133">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="35dce-134">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="35dce-134">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="35dce-135">**Completamento** completato (0)</span><span class="sxs-lookup"><span data-stu-id="35dce-135">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="35dce-136">**Accesso negato** (2)</span><span class="sxs-lookup"><span data-stu-id="35dce-136">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="35dce-137">**Privilegio insufficiente** (3)</span><span class="sxs-lookup"><span data-stu-id="35dce-137">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="35dce-138">**Errore sconosciuto** (8)</span><span class="sxs-lookup"><span data-stu-id="35dce-138">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="35dce-139">**Percorso non trovato** (9)</span><span class="sxs-lookup"><span data-stu-id="35dce-139">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="35dce-140">**Parametro non valido** (21)</span><span class="sxs-lookup"><span data-stu-id="35dce-140">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="35dce-141">**Altro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="35dce-141">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="35dce-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="35dce-142">Remarks</span></span>

<span data-ttu-id="35dce-143">Per impostare la priorità su realtime, il chiamante deve disporre del privilegio di priorità di base **SeIncreaseBasePriorityPrivilege** (**se \_ Inc \_ \_ \_**).</span><span class="sxs-lookup"><span data-stu-id="35dce-143">To set the priority to Realtime, the caller must have **SeIncreaseBasePriorityPrivilege** (**SE\_INC\_BASE\_PRIORITY\_PRIVILEGE**).</span></span> <span data-ttu-id="35dce-144">Senza questo privilegio, la priorità più alta può essere impostata su è alta.</span><span class="sxs-lookup"><span data-stu-id="35dce-144">Without this privilege, the highest the priority can be set to is High Priority.</span></span>

## <a name="examples"></a><span data-ttu-id="35dce-145">Esempio</span><span class="sxs-lookup"><span data-stu-id="35dce-145">Examples</span></span>

<span data-ttu-id="35dce-146">L'esempio di [modifica della priorità di un processo in esecuzione](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript modifica la priorità di un'istanza in esecuzione di Notepad.exe da normale a superiore al normale.</span><span class="sxs-lookup"><span data-stu-id="35dce-146">The [Modify the Priority Of a Running Process](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) VBScript sample changes the priority of a running instance of Notepad.exe from Normal to Above Normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="35dce-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35dce-147">Requirements</span></span>



| <span data-ttu-id="35dce-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="35dce-148">Requirement</span></span> | <span data-ttu-id="35dce-149">Valore</span><span class="sxs-lookup"><span data-stu-id="35dce-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35dce-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35dce-150">Minimum supported client</span></span><br/> | <span data-ttu-id="35dce-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35dce-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35dce-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35dce-152">Minimum supported server</span></span><br/> | <span data-ttu-id="35dce-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35dce-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35dce-154">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="35dce-154">Namespace</span></span><br/>                | <span data-ttu-id="35dce-155">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="35dce-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="35dce-156">MOF</span><span class="sxs-lookup"><span data-stu-id="35dce-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35dce-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35dce-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="35dce-158">DLL</span><span class="sxs-lookup"><span data-stu-id="35dce-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35dce-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35dce-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35dce-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35dce-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="35dce-161">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="35dce-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="35dce-162">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="35dce-162">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

