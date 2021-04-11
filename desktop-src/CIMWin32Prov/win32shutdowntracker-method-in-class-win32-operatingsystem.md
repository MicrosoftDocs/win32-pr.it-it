---
description: Il metodo Win32ShutdownTracker fornisce lo stesso set di opzioni di arresto supportate dal metodo Win32Shutdown in Win32 \_ OperatingSystem, ma consente anche di specificare i commenti, il motivo dell'arresto o il timeout.
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Metodo Win32ShutdownTracker della classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32ShutdownTracker
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c86972d014da906b98ad8d3bd8e98d01f1cfcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126072"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="0728b-103">Metodo Win32ShutdownTracker della \_ classe OperatingSystem Win32</span><span class="sxs-lookup"><span data-stu-id="0728b-103">Win32ShutdownTracker method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="0728b-104">Il metodo **Win32ShutdownTracker** fornisce lo stesso set di opzioni di arresto supportate dal metodo [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) in [**Win32 \_ OperatingSystem**](win32-operatingsystem.md), ma consente anche di specificare i commenti, il motivo dell'arresto o il timeout.</span><span class="sxs-lookup"><span data-stu-id="0728b-104">The **Win32ShutdownTracker** method provides the same set of shutdown options supported by the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method in [**Win32\_OperatingSystem**](win32-operatingsystem.md), but it also allows you to specify comments, a reason for shutdown, or a timeout.</span></span>

## <a name="syntax"></a><span data-ttu-id="0728b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0728b-105">Syntax</span></span>


```mof
uint32 Win32ShutdownTracker(
  [in] uint32 Timeout,
  [in] string Comment,
  [in] uint32 ReasonCode,
  [in] sint32 Flags
);
```



## <a name="parameters"></a><span data-ttu-id="0728b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0728b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0728b-107">*Timeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0728b-107">*Timeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0728b-108">Tempo, in secondi, prima dell'arresto.</span><span class="sxs-lookup"><span data-stu-id="0728b-108">Time, in seconds, before shutdown takes place.</span></span> <span data-ttu-id="0728b-109">Il valore predefinito è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="0728b-109">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="0728b-110">*Commento* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0728b-110">*Comment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0728b-111">Messaggio da visualizzare nella finestra di dialogo di arresto, anch ' esso archiviato come commento nella voce del registro eventi.</span><span class="sxs-lookup"><span data-stu-id="0728b-111">Message to display in the shutdown dialog box that is also stored as a comment in the event log entry.</span></span>

</dd> <dt>

<span data-ttu-id="0728b-112">*ReasonCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0728b-112">*ReasonCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0728b-113">Motivo per l'avvio dell'arresto.</span><span class="sxs-lookup"><span data-stu-id="0728b-113">Reason for initiating the shutdown.</span></span>

</dd> <dt>

<span data-ttu-id="0728b-114">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0728b-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0728b-115">Set di flag bitmap per arrestare il computer.</span><span class="sxs-lookup"><span data-stu-id="0728b-115">Bitmapped set of flags to shut the computer down.</span></span> <span data-ttu-id="0728b-116">Per forzare un comando, aggiungere il flag di forzatura (4) al valore del comando.</span><span class="sxs-lookup"><span data-stu-id="0728b-116">To force a command, add the Force flag (4) to the command value.</span></span> <span data-ttu-id="0728b-117">L'utilizzo di Force in combinazione con l'arresto o il riavvio di un computer remoto arresta immediatamente tutti gli elementi, inclusi WMI, COM e così via, oppure riavvia il computer remoto.</span><span class="sxs-lookup"><span data-stu-id="0728b-117">Using Force in conjunction with Shutdown or Reboot on a remote computer immediately shuts down everything (including WMI, COM, and so on), or reboots the remote computer.</span></span> <span data-ttu-id="0728b-118">Ciò comporta un valore restituito indeterminato.</span><span class="sxs-lookup"><span data-stu-id="0728b-118">This results in an indeterminate return value.</span></span>

<dt>

<span data-ttu-id="0728b-119">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="0728b-119">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0728b-120">Disconnetti</span><span class="sxs-lookup"><span data-stu-id="0728b-120">Log Off</span></span>

</dd> <dt>

<span data-ttu-id="0728b-121">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="0728b-121">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="0728b-122">Disconnessione forzata (0 + 4)</span><span class="sxs-lookup"><span data-stu-id="0728b-122">Forced Log Off (0 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="0728b-123">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0728b-123">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0728b-124">Arresta</span><span class="sxs-lookup"><span data-stu-id="0728b-124">Shutdown</span></span>

</dd> <dt>

<span data-ttu-id="0728b-125">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="0728b-125">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="0728b-126">Arresto forzato (1 + 4)</span><span class="sxs-lookup"><span data-stu-id="0728b-126">Forced Shutdown (1 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="0728b-127">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="0728b-127">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="0728b-128">Riavvio</span><span class="sxs-lookup"><span data-stu-id="0728b-128">Reboot</span></span>

</dd> <dt>

<span data-ttu-id="0728b-129">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="0728b-129">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="0728b-130">Riavvio forzato (2 + 4)</span><span class="sxs-lookup"><span data-stu-id="0728b-130">Forced Reboot (2 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="0728b-131">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="0728b-131">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="0728b-132">Spegnimento</span><span class="sxs-lookup"><span data-stu-id="0728b-132">Power Off</span></span>

</dd> <dt>

<span data-ttu-id="0728b-133">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="0728b-133">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="0728b-134">Spegnimento forzato (8 + 4)</span><span class="sxs-lookup"><span data-stu-id="0728b-134">Forced Power Off (8 + 4)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0728b-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0728b-135">Return value</span></span>

<span data-ttu-id="0728b-136">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0728b-136">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="0728b-137">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="0728b-137">Any other number indicates an error.</span></span> <span data-ttu-id="0728b-138">Per i codici di errore, vedere [**costanti di errore WMI**](../wmisdk/wmi-error-constants.md) o [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0728b-138">For error codes, see [**WMI Error Constants**](../wmisdk/wmi-error-constants.md) or [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0728b-139">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0728b-139">For general **HRESULT** values, see [System Error Codes](../debug/system-error-codes.md).</span></span>

<dl> <dt>

<span data-ttu-id="0728b-140">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="0728b-140">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0728b-141">**Altro** (1-4294967295)</span><span class="sxs-lookup"><span data-stu-id="0728b-141">**Other** (1–4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="0728b-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="0728b-142">Remarks</span></span>

<span data-ttu-id="0728b-143">Il processo chiamante deve avere il privilegio di **\_ arresto del \_ nome** .</span><span class="sxs-lookup"><span data-stu-id="0728b-143">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege.</span></span>

## <a name="examples"></a><span data-ttu-id="0728b-144">Esempio</span><span class="sxs-lookup"><span data-stu-id="0728b-144">Examples</span></span>

<span data-ttu-id="0728b-145">Nell'esempio di codice VBScript seguente viene descritto come chiamare **Win32ShutdownTracker**.</span><span class="sxs-lookup"><span data-stu-id="0728b-145">The following VBScript code sample describes how to call **Win32ShutdownTracker**.</span></span>


```VB
Set objArgs = Wscript.Arguments 

intTimeOut = objArgs(0) 'Countdown time (in seconds) before action
strComment = objArgs(1) 'Message to display
intFlags = objArgs(2) 'Set of flags to shutdown the computer:
'0 = Logoff, 4 = Forced Logoff (0+4), 1 = Shutdown, 2 = Reboot, 6 = Forced Reboot (2+4), 8 = Power Off, 12 = Forced Power Off (8+4) - 2 (Reboot) 

strComputer = "." 

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,(Shutdown)}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery ("Select * from Win32_OperatingSystem") 

For Each objOperatingSystem in colOperatingSystems 
objOperatingSystem.Win32ShutdownTracker intTimeOut,strComment,0,intFlags 
Next
```



## <a name="requirements"></a><span data-ttu-id="0728b-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0728b-146">Requirements</span></span>



| <span data-ttu-id="0728b-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="0728b-147">Requirement</span></span> | <span data-ttu-id="0728b-148">Valore</span><span class="sxs-lookup"><span data-stu-id="0728b-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0728b-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0728b-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0728b-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0728b-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0728b-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0728b-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0728b-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0728b-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0728b-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0728b-153">Namespace</span></span><br/>                | <span data-ttu-id="0728b-154">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0728b-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0728b-155">MOF</span><span class="sxs-lookup"><span data-stu-id="0728b-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0728b-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0728b-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0728b-157">DLL</span><span class="sxs-lookup"><span data-stu-id="0728b-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0728b-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0728b-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0728b-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0728b-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0728b-160">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0728b-160">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="0728b-161">**\_OperatingSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="0728b-161">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="0728b-162">**Win32Shutdown**</span><span class="sxs-lookup"><span data-stu-id="0728b-162">**Win32Shutdown**</span></span>](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
