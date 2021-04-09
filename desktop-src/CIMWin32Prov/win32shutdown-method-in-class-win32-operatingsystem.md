---
description: Win32Shutdown &\# 8194; Il metodo della classe WMI fornisce il set completo di opzioni di arresto supportate dai sistemi operativi Win32. Sono inclusi la disconnessione, l'arresto, il riavvio e la forzatura di una disconnessione, un arresto o un riavvio.
ms.assetid: 7108570a-81ba-46d5-8b05-de6194f93f18
ms.tgt_platform: multiple
title: Metodo Win32Shutdown della classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2cca60c376859438b40ca35be26a99b115634c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878214"
---
# <a name="win32shutdown-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="b64d7-104">Metodo Win32Shutdown della \_ classe OperatingSystem Win32</span><span class="sxs-lookup"><span data-stu-id="b64d7-104">Win32Shutdown method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="b64d7-105">Il metodo della   [classe WMI](../wmisdk/retrieving-a-class.md) **Win32Shutdown** fornisce il set completo di opzioni di arresto supportate dai sistemi operativi Win32.</span><span class="sxs-lookup"><span data-stu-id="b64d7-105">The **Win32Shutdown**   [WMI class](../wmisdk/retrieving-a-class.md) method provides the full set of shutdown options supported by Win32 operating systems.</span></span> <span data-ttu-id="b64d7-106">Sono inclusi la disconnessione, l'arresto, il riavvio e la forzatura di una disconnessione, un arresto o un riavvio.</span><span class="sxs-lookup"><span data-stu-id="b64d7-106">These include logoff, shutdown, reboot, and forcing a logoff, shutdown, or reboot.</span></span>

<span data-ttu-id="b64d7-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b64d7-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b64d7-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](../wmisdk/calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b64d7-108">For more information about using this method, see [Calling a Method](../wmisdk/calling-a-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b64d7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b64d7-109">Syntax</span></span>


```mof
uint32 Win32Shutdown(
  [in] sint32 Flags,
  [in] sint32 Reserved = 
);
```



## <a name="parameters"></a><span data-ttu-id="b64d7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b64d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b64d7-111">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b64d7-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b64d7-112">Set di flag bitmap per arrestare il computer.</span><span class="sxs-lookup"><span data-stu-id="b64d7-112">Bitmapped set of flags to shut the computer down.</span></span> <span data-ttu-id="b64d7-113">Per forzare un comando, aggiungere il flag di forzatura (4) al valore del comando.</span><span class="sxs-lookup"><span data-stu-id="b64d7-113">To force a command, add the Force flag (4) to the command value.</span></span> <span data-ttu-id="b64d7-114">L'utilizzo di Force in combinazione con l'arresto o il riavvio di un computer remoto arresta immediatamente tutti gli elementi, inclusi WMI, COM e così via, oppure riavvia il computer remoto.</span><span class="sxs-lookup"><span data-stu-id="b64d7-114">Using Force in conjunction with Shutdown or Reboot on a remote computer immediately shuts down everything (including WMI, COM, and so on), or reboots the remote computer.</span></span> <span data-ttu-id="b64d7-115">Ciò comporta un valore restituito indeterminato.</span><span class="sxs-lookup"><span data-stu-id="b64d7-115">This results in an indeterminate return value.</span></span>

<dt>

<span data-ttu-id="b64d7-116">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="b64d7-116">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="b64d7-117">**Disconnetti** : disconnette l'utente dal computer.</span><span class="sxs-lookup"><span data-stu-id="b64d7-117">**Log Off** - Logs the user off the computer.</span></span> <span data-ttu-id="b64d7-118">La disconnessione arresta tutti i processi associati al contesto di sicurezza del processo che ha chiamato la funzione Exit, registra l'utente corrente dal sistema e visualizza la finestra di dialogo Logon.</span><span class="sxs-lookup"><span data-stu-id="b64d7-118">Logging off stops all processes associated with the security context of the process that called the exit function, logs the current user off the system, and displays the logon dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b64d7-119">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="b64d7-119">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="b64d7-120">**Disconnessione forzata (0 + 4)** : disconnette immediatamente l'utente dal computer e non notifica alle applicazioni che la sessione di accesso sta per terminare.</span><span class="sxs-lookup"><span data-stu-id="b64d7-120">**Forced Log Off (0 + 4)** - Logs the user off the computer immediately and does not notify applications that the logon session is ending.</span></span> <span data-ttu-id="b64d7-121">Ciò può comportare la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="b64d7-121">This can result in a loss of data.</span></span>

</dd> <dt>

<span data-ttu-id="b64d7-122">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="b64d7-122">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="b64d7-123">**Arresta** : arresta il computer fino a un punto in cui è sicuro spegnere la potenza.</span><span class="sxs-lookup"><span data-stu-id="b64d7-123">**Shutdown** - Shuts down the computer to a point where it is safe to turn off the power.</span></span> <span data-ttu-id="b64d7-124">Tutti i buffer di file vengono scaricati su disco e tutti i processi in esecuzione vengono arrestati. Il messaggio viene visualizzato dagli utenti, `It is now safe to turn off your computer.`</span><span class="sxs-lookup"><span data-stu-id="b64d7-124">(All file buffers are flushed to disk, and all running processes are stopped.) Users see the message, `It is now safe to turn off your computer.`</span></span>

<span data-ttu-id="b64d7-125">Durante l'arresto, il sistema invia un messaggio a ogni applicazione in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b64d7-125">During shutdown the system sends a message to each running application.</span></span> <span data-ttu-id="b64d7-126">Le applicazioni eseguono qualsiasi pulizia durante l'elaborazione del messaggio e restituiscono true per indicare che possono essere interrotte.</span><span class="sxs-lookup"><span data-stu-id="b64d7-126">The applications perform any cleanup while processing the message and return True to indicate that they can be terminated.</span></span>

</dd> <dt>

<span data-ttu-id="b64d7-127">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="b64d7-127">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="b64d7-128">**Arresto forzato (1 + 4)** -arresta il computer fino a un punto in cui è sicuro spegnere la potenza.</span><span class="sxs-lookup"><span data-stu-id="b64d7-128">**Forced Shutdown (1 + 4)** - Shuts down the computer to a point where it is safe to turn off the power.</span></span> <span data-ttu-id="b64d7-129">Tutti i buffer di file vengono scaricati su disco e tutti i processi in esecuzione vengono arrestati. Il messaggio viene visualizzato dagli utenti,` It is now safe to turn off your computer.`</span><span class="sxs-lookup"><span data-stu-id="b64d7-129">(All file buffers are flushed to disk, and all running processes are stopped.) Users see the message,` It is now safe to turn off your computer.`</span></span>

<span data-ttu-id="b64d7-130">Quando si usa l'approccio di arresto forzato, tutti i servizi, incluso WMI, vengono arrestati immediatamente.</span><span class="sxs-lookup"><span data-stu-id="b64d7-130">When the forced shutdown approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="b64d7-131">Per questo motivo, non sarà possibile ricevere un valore restituito se si esegue lo script in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="b64d7-131">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="b64d7-132">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="b64d7-132">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="b64d7-133">**Riavvia** : arresta e riavvia il computer.</span><span class="sxs-lookup"><span data-stu-id="b64d7-133">**Reboot** - Shuts down and then restarts the computer.</span></span>

</dd> <dt>

<span data-ttu-id="b64d7-134">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="b64d7-134">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="b64d7-135">**Riavvio forzato (2 + 4)** : arresta e riavvia il computer.</span><span class="sxs-lookup"><span data-stu-id="b64d7-135">**Forced Reboot (2 + 4)** - Shuts down and then restarts the computer.</span></span>

<span data-ttu-id="b64d7-136">Quando si usa l'approccio per il riavvio forzato, tutti i servizi, incluso WMI, vengono arrestati immediatamente.</span><span class="sxs-lookup"><span data-stu-id="b64d7-136">When the forced reboot approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="b64d7-137">Per questo motivo, non sarà possibile ricevere un valore restituito se si esegue lo script in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="b64d7-137">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="b64d7-138">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="b64d7-138">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="b64d7-139">**Spegnimento: arresta** il computer e disattiva la potenza (se supportata dal computer in questione).</span><span class="sxs-lookup"><span data-stu-id="b64d7-139">**Power Off** - Shuts down the computer and turns off the power (if supported by the computer in question).</span></span>

</dd> <dt>

<span data-ttu-id="b64d7-140">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="b64d7-140">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="b64d7-141">Spegnimento **forzato (8 + 4)** -arresta il computer e disattiva la potenza (se supportata dal computer in questione).</span><span class="sxs-lookup"><span data-stu-id="b64d7-141">**Forced Power Off (8 + 4)** - Shuts down the computer and turns off the power (if supported by the computer in question).</span></span>

<span data-ttu-id="b64d7-142">Quando si usa l'approccio di spegnimento forzato, tutti i servizi, incluso WMI, vengono arrestati immediatamente.</span><span class="sxs-lookup"><span data-stu-id="b64d7-142">When the forced power off approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="b64d7-143">Per questo motivo, non sarà possibile ricevere un valore restituito se si esegue lo script in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="b64d7-143">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b64d7-144">*Riservato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b64d7-144">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b64d7-145">Un metodo per estendere **Win32Shutdown**.</span><span class="sxs-lookup"><span data-stu-id="b64d7-145">A means to extend **Win32Shutdown**.</span></span> <span data-ttu-id="b64d7-146">Attualmente, il parametro *riservato* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b64d7-146">Currently, the *Reserved* parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b64d7-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b64d7-147">Return value</span></span>

<span data-ttu-id="b64d7-148">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b64d7-148">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="b64d7-149">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="b64d7-149">Any other number indicates an error.</span></span> <span data-ttu-id="b64d7-150">Per i codici di errore, vedere [**costanti di errore WMI**](../wmisdk/wmi-error-constants.md) o [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b64d7-150">For error codes, see [**WMI Error Constants**](../wmisdk/wmi-error-constants.md) or [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b64d7-151">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b64d7-151">For general **HRESULT** values, see [System Error Codes](../debug/system-error-codes.md).</span></span>

<dl> <dt>

<span data-ttu-id="b64d7-152">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="b64d7-152">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b64d7-153">**Altro** (1-4294967295)</span><span class="sxs-lookup"><span data-stu-id="b64d7-153">**Other** (1–4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="b64d7-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="b64d7-154">Remarks</span></span>

<span data-ttu-id="b64d7-155">Per una gestione più efficiente dei computer in un'organizzazione, gli amministratori hanno la possibilità di arrestare o riavviare un computer in modalità remota o di disconnettere un utente in remoto.</span><span class="sxs-lookup"><span data-stu-id="b64d7-155">For more efficient management of computers in an organization, administrators need the ability to remotely shut down or restart a computer, or to remotely log off a user.</span></span> <span data-ttu-id="b64d7-156">La possibilità di eseguire queste attività consente agli amministratori di installare il software, riconfigurare le impostazioni del computer, rimuovere i computer dalla rete ed eseguire altre attività senza dover arrestare o riavviare manualmente ogni computer.</span><span class="sxs-lookup"><span data-stu-id="b64d7-156">The ability to carry out these tasks allows administrators to install software, reconfigure computer settings, remove computers from the network, and perform other tasks without having to manually shut down or restart each computer.</span></span>

<span data-ttu-id="b64d7-157">Ad esempio, per eseguire un aggiornamento della rete, potrebbe essere necessario arrestare tutti i computer in esecuzione in un particolare segmento di rete.</span><span class="sxs-lookup"><span data-stu-id="b64d7-157">For example, to perform a network upgrade, you might need to shut down all the computers running on a particular network segment.</span></span> <span data-ttu-id="b64d7-158">Per forzare un aggiornamento Criteri di gruppo, è necessario disconnettere gli utenti dal computer.</span><span class="sxs-lookup"><span data-stu-id="b64d7-158">To force a Group Policy upgrade, you need to log users off their computers.</span></span> <span data-ttu-id="b64d7-159">Se un virus del computer è presente in un punto qualsiasi dell'organizzazione, potrebbe essere necessario arrestare il maggior numero possibile di computer, prima che il virus abbia la possibilità di diffondersi.</span><span class="sxs-lookup"><span data-stu-id="b64d7-159">If a computer virus is present anywhere in your organization, you might want to shut down as many computers as possible, before the virus has an opportunity to spread.</span></span> <span data-ttu-id="b64d7-160">La possibilità di arrestare e riavviare i computer e di disconnettere gli utenti a livello di codice anziché manualmente può essere un notevole risparmio di tempo.</span><span class="sxs-lookup"><span data-stu-id="b64d7-160">The ability to shut down and restart computers and to log off users programmatically instead of manually can be an enormous time-saver.</span></span>

<span data-ttu-id="b64d7-161">Il processo chiamante deve avere il privilegio di **\_ arresto del \_ nome** .</span><span class="sxs-lookup"><span data-stu-id="b64d7-161">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege.</span></span>

<span data-ttu-id="b64d7-162">Il metodo [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) fornisce lo stesso set di opzioni di arresto supportate dal metodo **Win32Shutdown** in [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) ma consente anche di specificare i commenti, il motivo dell'arresto o il timeout.</span><span class="sxs-lookup"><span data-stu-id="b64d7-162">The [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) method provides the same set of shutdown options supported by the **Win32Shutdown** method in [**Win32\_OperatingSystem**](win32-operatingsystem.md) but it also allows you to specify comments, a reason for shutdown, or a timeout.</span></span>

<span data-ttu-id="b64d7-163">Il metodo Win32Shutdown non dispone di un parametro per il blocco di una workstation, lasciando l'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="b64d7-163">The Win32Shutdown method does not have a parameter for locking a workstation, leaving the user logged on.</span></span> <span data-ttu-id="b64d7-164">Tuttavia, le workstation possono essere bloccate dalla riga di comando usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="b64d7-164">However, workstations can be locked from the command line by using the following command:</span></span>

`% windir %\System32\rundll32.exe user32.dll,LockWorkStation`

## <a name="examples"></a><span data-ttu-id="b64d7-165">Esempio</span><span class="sxs-lookup"><span data-stu-id="b64d7-165">Examples</span></span>

<span data-ttu-id="b64d7-166">L'esempio di [disconnessione, riavvio o arresto di più computer](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) in TechNet Gallery USA Win32Shutdown per disconnettersi, arrestare, riavviare o spegnere (a seconda della selezione) i computer elencati nell'array di server.</span><span class="sxs-lookup"><span data-stu-id="b64d7-166">The [Log Out, Reboot, or Shut Down Multiple Computers](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) VBScript sample on TechNet Gallery uses Win32Shutdown to log off, shut down, reboot, or power off (depending on the selection) the computers listed in the Server array.</span></span>

<span data-ttu-id="b64d7-167">L'esempio [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell nella raccolta TechNet include un metodo che chiama Win32Shutdown in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="b64d7-167">The [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell sample on TechNet Gallery includes a method that calls Win32Shutdown on a remote computer.</span></span>

<span data-ttu-id="b64d7-168">L'esempio di PowerShell seguente usa il metodo Win32Shutdown per arrestare il computer specificato.</span><span class="sxs-lookup"><span data-stu-id="b64d7-168">The following PowerShell example uses the Win32Shutdown method to shut down the specified computer.</span></span>


```PowerShell
$computername= "."
$win32OS = get-wmiobject win32_operatingsystem -computername $computername
$win32OS.psbase.Scope.Options.EnablePrivileges = $true
$win32OS.win32shutdown(8)
```



<span data-ttu-id="b64d7-169">L'esempio di codice PowerShell seguente usa il cmdlet EnableAllPrivileges di Get-WmiObject per ottenere il privilegi appropriato.</span><span class="sxs-lookup"><span data-stu-id="b64d7-169">The following PowerShell code sample uses the EnableAllPrivileges from get-wmiobject cmdlet to achieve the proper priviliges.</span></span>


```PowerShell
$win32OS = get-wmiobject win32_operatingsystem -computername $computername -EnableAllPrivileges
$win32OS.win32shutdown(8)
```



<span data-ttu-id="b64d7-170">Il codice di esempio VB.NET seguente usa il metodo Shutdown per riavviare o disconnettersi da un sistema.</span><span class="sxs-lookup"><span data-stu-id="b64d7-170">The following VB.NET sample code uses the Shutdown method to reboot or log off a system.</span></span>


```VB
Dim

testResult AsSingle

Dim WMIServiceObject, ComputerObject AsObject 

'Now get some privileges 

WMIServiceObject = GetObject(
"Winmgmts:{impersonationLevel=impersonate,(Debug,Shutdown)}")
ForEach ComputerObject In WMIServiceObject.InstancesOf("Win32_OperatingSystem") 
    testResult = ComputerObject.Win32Shutdown(2 + 4, 0) 
    'reboot
    'testResult = ComputerObject.Win32Shutdown(0, 0) 'logoff 
    ' testResult = ComputerObject.Win32Shutdown(8 + 4, 0) 'shutdown 

If testResult <> 0 Then 

MsgBox("Sorry, an error has occurred while trying to perform selected operation") 

Else 

'Operation selected in statement above if condition would be carried out 

EndIf 

Next
```



## <a name="requirements"></a><span data-ttu-id="b64d7-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b64d7-171">Requirements</span></span>



| <span data-ttu-id="b64d7-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="b64d7-172">Requirement</span></span> | <span data-ttu-id="b64d7-173">Valore</span><span class="sxs-lookup"><span data-stu-id="b64d7-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b64d7-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b64d7-174">Minimum supported client</span></span><br/> | <span data-ttu-id="b64d7-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b64d7-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b64d7-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b64d7-176">Minimum supported server</span></span><br/> | <span data-ttu-id="b64d7-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b64d7-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b64d7-178">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b64d7-178">Namespace</span></span><br/>                | <span data-ttu-id="b64d7-179">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b64d7-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b64d7-180">MOF</span><span class="sxs-lookup"><span data-stu-id="b64d7-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b64d7-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b64d7-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b64d7-182">DLL</span><span class="sxs-lookup"><span data-stu-id="b64d7-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b64d7-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b64d7-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b64d7-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b64d7-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b64d7-185">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b64d7-185">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="b64d7-186">**\_OperatingSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="b64d7-186">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="b64d7-187">**Win32ShutdownTracker**</span><span class="sxs-lookup"><span data-stu-id="b64d7-187">**Win32ShutdownTracker**</span></span>](win32shutdowntracker-method-in-class-win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="b64d7-188">Attività WMI: gestione desktop</span><span class="sxs-lookup"><span data-stu-id="b64d7-188">WMI Tasks: Desktop Management</span></span>](../wmisdk/wmi-tasks--desktop-management.md)
</dt> <dt>

[<span data-ttu-id="b64d7-189">Esecuzione di operazioni con privilegi tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="b64d7-189">Executing Privileged Operations Using VBScript</span></span>](../wmisdk/executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

 
