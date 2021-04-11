---
description: GetOwner&\# 8194; Il metodo della classe WMI recupera il nome utente e il nome di dominio in cui è in esecuzione il processo.
ms.assetid: bbd6d22b-ca54-42f3-8098-d3034048ec4d
ms.tgt_platform: multiple
title: Metodo GetOwner della classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwner
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 007acbe997f555e9a439ed27740a447d3bf7fe4d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126483"
---
# <a name="getowner-method-of-the-win32_process-class"></a><span data-ttu-id="3cc75-103">Metodo GetOwner della classe di \_ processo Win32</span><span class="sxs-lookup"><span data-stu-id="3cc75-103">GetOwner method of the Win32\_Process class</span></span>

<span data-ttu-id="3cc75-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwner** Recupera il nome utente e il nome di dominio in cui è in esecuzione il processo.</span><span class="sxs-lookup"><span data-stu-id="3cc75-104">The **GetOwner** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method retrieves the user name and domain name under which the process is running.</span></span>

<span data-ttu-id="3cc75-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3cc75-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3cc75-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3cc75-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3cc75-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3cc75-107">Syntax</span></span>


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a><span data-ttu-id="3cc75-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3cc75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cc75-109">*Utente* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="3cc75-109">*User* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cc75-110">Restituisce il nome utente del proprietario del processo.</span><span class="sxs-lookup"><span data-stu-id="3cc75-110">Returns the user name of the owner of this process.</span></span>

</dd> <dt>

<span data-ttu-id="3cc75-111">*Dominio* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3cc75-111">*Domain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cc75-112">Restituisce il nome di dominio in cui è in esecuzione il processo.</span><span class="sxs-lookup"><span data-stu-id="3cc75-112">Returns the domain name under which this process is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cc75-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3cc75-113">Return value</span></span>

<span data-ttu-id="3cc75-114">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3cc75-114">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="3cc75-115">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="3cc75-115">Any other number indicates an error.</span></span> <span data-ttu-id="3cc75-116">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3cc75-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3cc75-117">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3cc75-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3cc75-118">**Completamento** completato (0)</span><span class="sxs-lookup"><span data-stu-id="3cc75-118">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3cc75-119">**Accesso negato** (2)</span><span class="sxs-lookup"><span data-stu-id="3cc75-119">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3cc75-120">**Privilegio insufficiente** (3)</span><span class="sxs-lookup"><span data-stu-id="3cc75-120">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3cc75-121">**Errore sconosciuto** (8)</span><span class="sxs-lookup"><span data-stu-id="3cc75-121">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3cc75-122">**Percorso non trovato** (9)</span><span class="sxs-lookup"><span data-stu-id="3cc75-122">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3cc75-123">**Parametro non valido** (21)</span><span class="sxs-lookup"><span data-stu-id="3cc75-123">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="3cc75-124">**Altro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="3cc75-124">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="3cc75-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="3cc75-125">Examples</span></span>

<span data-ttu-id="3cc75-126">[Il monitoraggio elaborazione CPU PCT per nome con proprietario](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) L'esempio VBScript raccoglie la percentuale di utilizzo della CPU o del processore e cerca il proprietario del processo.</span><span class="sxs-lookup"><span data-stu-id="3cc75-126">[The Monitor Process CPU Pct by Name with Owner](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) VBScript sample collects the CPU or Processor utilization percent and looks up the process owner.</span></span>

<span data-ttu-id="3cc75-127">L' [elenco di tutti i server in cui viene eseguito l'accesso a un elenco di utenti](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) in PowerShell esegue query su WMI per il proprietario di tutti i processi explorer.exe.</span><span class="sxs-lookup"><span data-stu-id="3cc75-127">The [Get all servers that a list of users is logged onto](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) PowerShell sample querys WMI for the owner of all explorer.exe processes.</span></span>

<span data-ttu-id="3cc75-128">Nell'esempio di codice VBScript seguente viene ottenuto il proprietario per ogni processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3cc75-128">The following VBScript code example obtains the owner for each running process.</span></span>


```VB
strComputer = "."
Set colProcesses = GetObject("winmgmts:" & _
   "{impersonationLevel=impersonate}!\\" & strComputer & _
   "\root\cimv2").ExecQuery("Select * from Win32_Process")

For Each objProcess in colProcesses

    Return = objProcess.GetOwner(strNameOfUser)
    If Return <> 0 Then
        Wscript.Echo "Could not get owner info for process " & _  
            objProcess.Name & VBNewLine _
            & "Error = " & Return
    Else 
        Wscript.Echo "Process " _
            & objProcess.Name & " is owned by " _ 
            & "\" & strNameOfUser & "."
    End If
Next
```



## <a name="requirements"></a><span data-ttu-id="3cc75-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3cc75-129">Requirements</span></span>



| <span data-ttu-id="3cc75-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cc75-130">Requirement</span></span> | <span data-ttu-id="3cc75-131">Valore</span><span class="sxs-lookup"><span data-stu-id="3cc75-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cc75-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3cc75-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3cc75-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3cc75-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3cc75-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3cc75-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3cc75-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3cc75-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3cc75-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3cc75-136">Namespace</span></span><br/>                | <span data-ttu-id="3cc75-137">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3cc75-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3cc75-138">MOF</span><span class="sxs-lookup"><span data-stu-id="3cc75-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cc75-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3cc75-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cc75-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3cc75-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cc75-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cc75-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cc75-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3cc75-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="3cc75-143">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3cc75-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3cc75-144">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="3cc75-144">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

