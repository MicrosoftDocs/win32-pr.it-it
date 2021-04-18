---
description: L'arresto&\# 8194; Il metodo della classe WMI Scarica i programmi e le dll fino a quando non è sicuro disattivare il computer.
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Metodo Shutdown della classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af80442087a0498849388f0da10946b08e282712
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483965"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="c1549-103">Metodo Shutdown della classe Win32 \_ OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c1549-103">Shutdown method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="c1549-104">Il metodo **Shutdown** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) Scarica i programmi e le dll fino a quando non è sicuro disattivare il computer.</span><span class="sxs-lookup"><span data-stu-id="c1549-104">The **Shutdown** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method unloads programs and DLLs until it is safe to turn off the computer.</span></span>

<span data-ttu-id="c1549-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c1549-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c1549-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c1549-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c1549-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1549-107">Syntax</span></span>


```mof
uint32 Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="c1549-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1549-108">Parameters</span></span>

<span data-ttu-id="c1549-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c1549-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1549-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1549-110">Return value</span></span>

<span data-ttu-id="c1549-111">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c1549-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="c1549-112">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="c1549-112">Any other number indicates an error.</span></span> <span data-ttu-id="c1549-113">Per i codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c1549-113">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c1549-114">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c1549-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c1549-115">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="c1549-115">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c1549-116">**Altro** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="c1549-116">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="c1549-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1549-117">Remarks</span></span>

<span data-ttu-id="c1549-118">Occasionalmente, i computer devono essere rimossi dalla rete, ad esempio per la manutenzione pianificata, perché il computer non funziona correttamente o per completare un processo di configurazione.</span><span class="sxs-lookup"><span data-stu-id="c1549-118">Computers occasionally need to be removed from the network, perhaps for scheduled maintenance, because the computer is not functioning correctly, or to complete a configuration process.</span></span> <span data-ttu-id="c1549-119">Se, ad esempio, un server DHCP distribuisce indirizzi IP errati, potrebbe essere necessario arrestare il computer fino a quando non è possibile inviare un tecnico del servizio per risolvere il problema.</span><span class="sxs-lookup"><span data-stu-id="c1549-119">For example, if a DHCP server is handing out erroneous IP addresses, you might want to shut the computer down until a service technician can be dispatched to fix the problem.</span></span> <span data-ttu-id="c1549-120">Se si ritiene che si sia verificata una violazione della sicurezza, potrebbe essere necessario arrestare determinati server per assicurarsi che non sia possibile accedervi fino a quando il problema di sicurezza non è stato risolto.</span><span class="sxs-lookup"><span data-stu-id="c1549-120">If you suspect that a security breach has occurred, you might need to shut down certain servers to ensure that they cannot be accessed until the security issue has been resolved.</span></span> <span data-ttu-id="c1549-121">Per alcune operazioni di configurazione, ad esempio la modifica del nome di un computer, è necessario riavviare il computer prima che la modifica abbia effetto.</span><span class="sxs-lookup"><span data-stu-id="c1549-121">Some configuration operations (such as changing a computer name) require you to restart the computer before the change takes effect.</span></span>

<span data-ttu-id="c1549-122">Questo metodo arresta immediatamente il computer, se possibile.</span><span class="sxs-lookup"><span data-stu-id="c1549-122">This method immediately shuts the computer down, if possible.</span></span> <span data-ttu-id="c1549-123">Il sistema arresta tutti i processi in esecuzione, Scarica tutti i buffer di file sul disco e quindi spegne il sistema.</span><span class="sxs-lookup"><span data-stu-id="c1549-123">The system stops all running processes, flushes all file buffers to the disk, and then powers down the system.</span></span> <span data-ttu-id="c1549-124">Il processo chiamante deve avere il privilegio **se \_ Shutdown \_ Name** , come descritto nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="c1549-124">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege, as described in the following example.</span></span>


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



<span data-ttu-id="c1549-125">Per ulteriori informazioni sull'impostazione di un privilegio, vedere [esecuzione di operazioni con privilegi](/windows/desktop/WmiSdk/executing-privileged-operations) ed esecuzione di [operazioni con privilegi tramite VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript).</span><span class="sxs-lookup"><span data-stu-id="c1549-125">For more information on setting a privilege, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations) and [Executing Privileged Operations Using VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript).</span></span> <span data-ttu-id="c1549-126">Per altre opzioni di arresto, ad esempio una disconnessione o un arresto forzato, vedere il metodo [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="c1549-126">For additional shutdown options, such as a logoff or a forced shutdown, see the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="c1549-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="c1549-127">Examples</span></span>

<span data-ttu-id="c1549-128">Il codice VBScript seguente arresta il computer locale.</span><span class="sxs-lookup"><span data-stu-id="c1549-128">The following VBScript code shuts the local computer down.</span></span>

> [!Note]  
> <span data-ttu-id="c1549-129">È necessario disporre del privilegio shutdown per richiamare correttamente il metodo Shutdown.</span><span class="sxs-lookup"><span data-stu-id="c1549-129">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



<span data-ttu-id="c1549-130">Il codice Perl seguente arresta il computer locale.</span><span class="sxs-lookup"><span data-stu-id="c1549-130">The following Perl code shuts the local computer down.</span></span>

> [!Note]  
> <span data-ttu-id="c1549-131">È necessario disporre del privilegio shutdown per richiamare correttamente il metodo Shutdown.</span><span class="sxs-lookup"><span data-stu-id="c1549-131">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```
use strict;
use Win32::OLE;

my $OpSysSet;

eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
      ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if(!$@ && defined $OpSysSet)
{
 close (STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Shutdown();
  if (!defined $RetVal || $RetVal != 0)
  { 
   print Win32::OLE->LastError, "\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="c1549-132">Il codice VBScript seguente arresta il computer remoto specificato.</span><span class="sxs-lookup"><span data-stu-id="c1549-132">The following VBScript code shuts the specified remote computer down.</span></span> <span data-ttu-id="c1549-133">Immettere il *\_ \_ nome del sistema remoto* con il nome del sistema remoto da arrestare.</span><span class="sxs-lookup"><span data-stu-id="c1549-133">Fill in *REMOTE\_SYSTEM\_NAME* with the name of the remote system to shutdown.</span></span>

> [!Note]  
> <span data-ttu-id="c1549-134">Per richiamare correttamente il metodo **Shutdown** , è necessario avere il privilegio RemoteShutdown.</span><span class="sxs-lookup"><span data-stu-id="c1549-134">You must have the RemoteShutdown privilege to successfully invoke the **Shutdown** method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



## <a name="requirements"></a><span data-ttu-id="c1549-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1549-135">Requirements</span></span>



| <span data-ttu-id="c1549-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1549-136">Requirement</span></span> | <span data-ttu-id="c1549-137">Valore</span><span class="sxs-lookup"><span data-stu-id="c1549-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1549-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1549-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c1549-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1549-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c1549-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1549-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c1549-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1549-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c1549-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c1549-142">Namespace</span></span><br/>                | <span data-ttu-id="c1549-143">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c1549-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c1549-144">MOF</span><span class="sxs-lookup"><span data-stu-id="c1549-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1549-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1549-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1549-146">DLL</span><span class="sxs-lookup"><span data-stu-id="c1549-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1549-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1549-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1549-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1549-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1549-149">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c1549-149">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c1549-150">**\_OperatingSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="c1549-150">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="c1549-151">Attività WMI: gestione desktop</span><span class="sxs-lookup"><span data-stu-id="c1549-151">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[<span data-ttu-id="c1549-152">Esecuzione di operazioni con privilegi tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="c1549-152">Executing Privileged Operations Using VBScript</span></span>](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

