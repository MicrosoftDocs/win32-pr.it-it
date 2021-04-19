---
description: Il&di creazione \# 8194; Il metodo della classe WMI crea un nuovo processo.
ms.assetid: be80abec-fab4-4403-bc29-d0d4a38e3c87
ms.tgt_platform: multiple
title: Metodo Create della classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 42c675f61fc8b42790aeb811ec275554b355a392
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304758"
---
# <a name="create-method-of-the-win32_process-class"></a><span data-ttu-id="8e57e-103">Metodo Create della classe di \_ processo Win32</span><span class="sxs-lookup"><span data-stu-id="8e57e-103">Create method of the Win32\_Process class</span></span>

<span data-ttu-id="8e57e-104">Il metodo **create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuovo processo.</span><span class="sxs-lookup"><span data-stu-id="8e57e-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new process.</span></span>

<span data-ttu-id="8e57e-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8e57e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8e57e-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8e57e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e57e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e57e-107">Syntax</span></span>


```mof
uint32 Create(
  [in]  string               CommandLine,
  [in]  string               CurrentDirectory,
  [in]  Win32_ProcessStartup ProcessStartupInformation,
  [out] uint32               ProcessId
);
```



## <a name="parameters"></a><span data-ttu-id="8e57e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e57e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e57e-109">*Riga* \[ di comando in\]</span><span class="sxs-lookup"><span data-stu-id="8e57e-109">*CommandLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e57e-110">Riga di comando da eseguire.</span><span class="sxs-lookup"><span data-stu-id="8e57e-110">Command line to execute.</span></span> <span data-ttu-id="8e57e-111">Il sistema aggiunge un carattere null alla riga di comando, tagliando la stringa se necessario, per indicare il file effettivamente utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8e57e-111">The system adds a null character to the command line, trimming the string if necessary, to indicate which file was actually used.</span></span>

</dd> <dt>

<span data-ttu-id="8e57e-112">*CurrentDirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e57e-112">*CurrentDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e57e-113">Unità e directory correnti per il processo figlio.</span><span class="sxs-lookup"><span data-stu-id="8e57e-113">Current drive and directory for the child process.</span></span> <span data-ttu-id="8e57e-114">Per la stringa è necessario che la directory corrente venga risolta in un percorso noto.</span><span class="sxs-lookup"><span data-stu-id="8e57e-114">The string requires that the current directory resolves to a known path.</span></span> <span data-ttu-id="8e57e-115">Un utente può specificare un percorso assoluto o un percorso relativo alla directory di lavoro corrente.</span><span class="sxs-lookup"><span data-stu-id="8e57e-115">A user can specify an absolute path or a path relative to the current working directory.</span></span> <span data-ttu-id="8e57e-116">Se questo parametro è **null**, il nuovo processo avrà lo stesso percorso del processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="8e57e-116">If this parameter is **NULL**, the new process will have the same path as the calling process.</span></span> <span data-ttu-id="8e57e-117">Questa opzione viene fornita principalmente per le shell che devono avviare un'applicazione e specificare l'unità iniziale e la directory di lavoro dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8e57e-117">This option is provided primarily for shells that must start an application and specify the application's initial drive and working directory.</span></span>

</dd> <dt>

<span data-ttu-id="8e57e-118">*ProcessStartupInformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e57e-118">*ProcessStartupInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e57e-119">Configurazione di avvio di un processo di Windows.</span><span class="sxs-lookup"><span data-stu-id="8e57e-119">The startup configuration of a Windows process.</span></span> <span data-ttu-id="8e57e-120">Per ulteriori informazioni, vedere [**Win32 \_ ProcessStartup**](win32-processstartup.md).</span><span class="sxs-lookup"><span data-stu-id="8e57e-120">For more information, see [**Win32\_ProcessStartup**](win32-processstartup.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e57e-121">*ProcessID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8e57e-121">*ProcessId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e57e-122">Identificatore globale del processo che può essere usato per identificare un processo.</span><span class="sxs-lookup"><span data-stu-id="8e57e-122">Global process identifier that can be used to identify a process.</span></span> <span data-ttu-id="8e57e-123">Il valore è valido dal momento in cui il processo viene creato fino al momento in cui il processo viene terminato.</span><span class="sxs-lookup"><span data-stu-id="8e57e-123">The value is valid from the time the process is created until the time the process is terminated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e57e-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e57e-124">Return value</span></span>

<span data-ttu-id="8e57e-125">Restituisce un valore pari a 0 (zero) se il processo è stato creato correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="8e57e-125">Returns a value of 0 (zero) if the process was successfully created, and any other number to indicate an error.</span></span> <span data-ttu-id="8e57e-126">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8e57e-126">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8e57e-127">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8e57e-127">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8e57e-128">**Completamento** completato (0)</span><span class="sxs-lookup"><span data-stu-id="8e57e-128">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8e57e-129">**Accesso negato** (2)</span><span class="sxs-lookup"><span data-stu-id="8e57e-129">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8e57e-130">**Privilegio insufficiente** (3)</span><span class="sxs-lookup"><span data-stu-id="8e57e-130">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8e57e-131">**Errore sconosciuto** (8)</span><span class="sxs-lookup"><span data-stu-id="8e57e-131">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8e57e-132">**Percorso non trovato** (9)</span><span class="sxs-lookup"><span data-stu-id="8e57e-132">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8e57e-133">**Parametro non valido** (21)</span><span class="sxs-lookup"><span data-stu-id="8e57e-133">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="8e57e-134">**Altro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="8e57e-134">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="8e57e-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e57e-135">Remarks</span></span>

<span data-ttu-id="8e57e-136">È possibile creare un'istanza della classe [**Win32 \_ ProcessStartup**](win32-processstartup.md) per configurare il processo prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8e57e-136">You can create an instance of the [**Win32\_ProcessStartup**](win32-processstartup.md) class to configure the process before calling this method.</span></span>

<span data-ttu-id="8e57e-137">È necessario specificare un percorso completo nei casi in cui il programma da avviare non sia nel percorso di ricerca di Winmgmt.exe.</span><span class="sxs-lookup"><span data-stu-id="8e57e-137">A fully qualified path must be specified in cases where the program to be launched is not in the search path of Winmgmt.exe.</span></span> <span data-ttu-id="8e57e-138">Se il processo appena creato tenta di interagire con gli oggetti nel sistema di destinazione senza i privilegi di accesso appropriati, viene terminato senza notifica a questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8e57e-138">If the newly created process attempts to interact with objects on the target system without the appropriate access privileges, it is terminated without notification to this method.</span></span>

<span data-ttu-id="8e57e-139">Per motivi di sicurezza, non è possibile usare il metodo **Win32 \_ Process. Create** per avviare un processo interattivo in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="8e57e-139">For security reasons the **Win32\_Process.Create** method cannot be used to start an interactive process remotely.</span></span>

<span data-ttu-id="8e57e-140">I processi creati con il metodo **Win32 \_ Process. Create** sono limitati dall'oggetto processo, a meno che non sia stato specificato il flag **Crea \_ fuga \_ dal \_ processo** .</span><span class="sxs-lookup"><span data-stu-id="8e57e-140">Processes created with the **Win32\_Process.Create** method are limited by the job object unless the **CREATE\_BREAKAWAY\_FROM\_JOB** flag is specified.</span></span> <span data-ttu-id="8e57e-141">Per ulteriori informazioni, vedere [**Win32 \_ ProcessStartup**](win32-processstartup.md) e [**\_ \_ ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).</span><span class="sxs-lookup"><span data-stu-id="8e57e-141">For more information, see [**Win32\_ProcessStartup**](win32-processstartup.md) and [**\_\_ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).</span></span>

## <a name="examples"></a><span data-ttu-id="8e57e-142">Esempio</span><span class="sxs-lookup"><span data-stu-id="8e57e-142">Examples</span></span>

<span data-ttu-id="8e57e-143">Nell'esempio VBScript riportato di seguito viene illustrato come richiamare un metodo CIM come se fosse un metodo di automazione di SWbemObject.</span><span class="sxs-lookup"><span data-stu-id="8e57e-143">The following VBScript example demonstrates how to invoke a CIM method as if it were an automation method of SWbemObject.</span></span>


```VB
on error resume next

set process = GetObject("winmgmts:Win32_Process")

result = process.Create ("notepad.exe",null,null,processid)

WScript.Echo "Method returned result = " & result
WScript.Echo "Id of new process is " & processid

if err <>0 then
 WScript.Echo Err.Description, "0x" & Hex(Err.Number)
end if
```



<span data-ttu-id="8e57e-144">Nell'esempio Perl seguente viene illustrato come richiamare un metodo CIM come se fosse un metodo di automazione di SWbemObject.</span><span class="sxs-lookup"><span data-stu-id="8e57e-144">The following Perl example demonstrates how to invoke a CIM method as if it were an automation method of SWbemObject.</span></span>


```VB
use strict;
use Win32::OLE;

my ($process, $outParam, $processid, $inParam, $objMethod);

eval { $process = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_Process"); };

if (!$@ && defined $process)
{
 $objMethod = $process->Methods_("Create");

 #Spawn an instance of inParameters and assign the values.
 $inParam = $objMethod->inParameters->SpawnInstance_ if (defined $objMethod);
 $inParam->{CommandLine} = "notepad.exe";
 $inParam->{CurrentDirectory} = undef;
 $inParam->{ProcessStartupInformation} = undef;

 $outParam = $process->ExecMethod_("Create", $inParam) if (defined $inParam);
 if ($outParam->{ReturnValue})
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
 else
 {
  print "Method returned result = $outParam->{ReturnValue}\n";
  print "Id of new process is $outParam->{ProcessId}\n"
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="8e57e-145">Nell'esempio di codice VBScript seguente viene creato un processo blocco note nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="8e57e-145">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="8e57e-146">[**Win32 \_ ProcessStartup**](win32-processstartup.md) viene usato per configurare le impostazioni del processo.</span><span class="sxs-lookup"><span data-stu-id="8e57e-146">[**Win32\_ProcessStartup**](win32-processstartup.md) is used to configure the process settings.</span></span>


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a><span data-ttu-id="8e57e-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e57e-147">Requirements</span></span>



| <span data-ttu-id="8e57e-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e57e-148">Requirement</span></span> | <span data-ttu-id="8e57e-149">Valore</span><span class="sxs-lookup"><span data-stu-id="8e57e-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e57e-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e57e-150">Minimum supported client</span></span><br/> | <span data-ttu-id="8e57e-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e57e-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e57e-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e57e-152">Minimum supported server</span></span><br/> | <span data-ttu-id="8e57e-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e57e-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e57e-154">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8e57e-154">Namespace</span></span><br/>                | <span data-ttu-id="8e57e-155">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8e57e-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e57e-156">MOF</span><span class="sxs-lookup"><span data-stu-id="8e57e-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e57e-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e57e-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e57e-158">DLL</span><span class="sxs-lookup"><span data-stu-id="8e57e-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e57e-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e57e-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e57e-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e57e-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="8e57e-161">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8e57e-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8e57e-162">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="8e57e-162">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="8e57e-163">Attività WMI: processi</span><span class="sxs-lookup"><span data-stu-id="8e57e-163">WMI Tasks: Processes</span></span>](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

