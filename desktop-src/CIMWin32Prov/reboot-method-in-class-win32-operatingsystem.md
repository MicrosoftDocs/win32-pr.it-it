---
description: Il riavvio&\# 8194; Il metodo della classe WMI arresta il sistema del computer e quindi lo riavvia.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Metodo reboot della classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4577f708d2f7ec7416ab3455da91b4e35fa079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966279"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="37466-103">Metodo reboot della \_ classe Win32 OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="37466-103">Reboot method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="37466-104">Il metodo **Riavvia** la [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) arresta il sistema del computer e quindi lo riavvia.</span><span class="sxs-lookup"><span data-stu-id="37466-104">The **Reboot** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method shuts down the computer system, then restarts it.</span></span>

<span data-ttu-id="37466-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="37466-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="37466-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="37466-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="37466-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37466-107">Syntax</span></span>


```mof
uint32 Reboot();
```



## <a name="parameters"></a><span data-ttu-id="37466-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="37466-108">Parameters</span></span>

<span data-ttu-id="37466-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="37466-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37466-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37466-110">Return value</span></span>

<span data-ttu-id="37466-111">Restituisce zero (0) per indicare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="37466-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="37466-112">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="37466-112">Any other number indicates an error.</span></span> <span data-ttu-id="37466-113">Per i codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="37466-113">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="37466-114">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="37466-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="37466-115">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="37466-115">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="37466-116">**Altro** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="37466-116">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="37466-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="37466-117">Remarks</span></span>

<span data-ttu-id="37466-118">La possibilità di riavviare a livello di codice un computer consente agli amministratori di eseguire molte attività di gestione dei computer in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="37466-118">The ability to programmatically restart a computer allows administrators to perform many computer management tasks remotely.</span></span>

<span data-ttu-id="37466-119">Se, ad esempio, si crea uno script per installare il software o apportare una modifica alla configurazione che richiede il riavvio di un computer, è possibile includere il comando Riavvia nello script ed eseguire l'intera operazione in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="37466-119">For example, if you create a script to install software or make a configuration change that requires restarting a computer, you can include the restart command in the script and perform the entire operation remotely.</span></span> <span data-ttu-id="37466-120">Il metodo di **riavvio** può essere utilizzato per riavviare un computer.</span><span class="sxs-lookup"><span data-stu-id="37466-120">The **Reboot** method can be used to restart a computer.</span></span> <span data-ttu-id="37466-121">Analogamente al metodo [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) , il metodo **reboot** richiede l'utente le cui credenziali di sicurezza vengono utilizzate dallo script per disporre del privilegio di arresto.</span><span class="sxs-lookup"><span data-stu-id="37466-121">Like the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method, the **Reboot** method requires the user whose security credentials are being used by the script to possess the Shutdown privilege.</span></span>

## <a name="examples"></a><span data-ttu-id="37466-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="37466-122">Examples</span></span>

<span data-ttu-id="37466-123">Nell'esempio di codice VBScript seguente viene richiamato il metodo reboot della classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="37466-123">The following VBScript code sample invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="37466-124">È necessario disporre del privilegio shutdown per richiamare correttamente il metodo Shutdown.</span><span class="sxs-lookup"><span data-stu-id="37466-124">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



<span data-ttu-id="37466-125">Il codice Perl seguente richiama il metodo reboot della classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="37466-125">The following Perl code invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="37466-126">È necessario disporre del privilegio shutdown per richiamare correttamente il metodo Shutdown.</span><span class="sxs-lookup"><span data-stu-id="37466-126">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```
use Win32::OLE;
use strict;
my $OpSysSet;
eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
 ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if (!$@ && defined $OpSysSet)
{
 close(STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Reboot(); 
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



<span data-ttu-id="37466-127">Il codice VBScript seguente richiama il metodo reboot della classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) in un sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="37466-127">The following VBScript invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class on a remote system.</span></span> <span data-ttu-id="37466-128">Immettere \_ \_ il nome del sistema remoto con il nome del sistema remoto da riavviare.</span><span class="sxs-lookup"><span data-stu-id="37466-128">Fill in REMOTE\_SYSTEM\_NAME with the name of the remote system to reboot.</span></span>

> [!Note]  
> <span data-ttu-id="37466-129">È necessario avere il privilegio RemoteShutdown per richiamare correttamente il metodo Reboot</span><span class="sxs-lookup"><span data-stu-id="37466-129">You must have the RemoteShutdown privilege to successfully invoke the Reboot method</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



<span data-ttu-id="37466-130">che segue Perl richiama il metodo di riavvio della classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) in un sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="37466-130">he following Perl invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class on a remote system.</span></span> <span data-ttu-id="37466-131">Immettere \_ \_ il nome del sistema remoto con il nome del sistema remoto da riavviare.</span><span class="sxs-lookup"><span data-stu-id="37466-131">Fill in REMOTE\_SYSTEM\_NAME with the name of the remote system to reboot.</span></span>

> [!Note]  
> <span data-ttu-id="37466-132">È necessario disporre del privilegio RemoteShutdown per richiamare correttamente il metodo di riavvio.</span><span class="sxs-lookup"><span data-stu-id="37466-132">You must have the RemoteShutdown privilege to successfully invoke the Reboot method.</span></span>

 


```
use strict;
use Win32::OLE;

use constant REMOTE_SYSTEM_NAME => "MACHINENAME";
use constant USERNAME => "USER";
use constant PASSWORD => "PASSWORD";
use constant NAMESPACE => "root\\cimv2";
use constant wbemPrivilegeRemoteShutdown => 23;
use constant wbemImpersonationLevelImpersonate => 3;
close(STDERR);
my ($locator, $services, $OpSysSet);
eval {
  $locator = Win32::OLE->new('WbemScripting.SWbemLocator');
  $locator->{Security_}->{impersonationlevel} = wbemImpersonationLevelImpersonate;
  $services = $locator->ConnectServer(REMOTE_SYSTEM_NAME, NAMESPACE, USERNAME, PASSWORD);
  $services->{Security_}->{Privileges}->Add(wbemPrivilegeRemoteShutdown);
  $OpSysSet = $services->ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true");
 };

if (!$@ && defined $OpSysSet)
{
 foreach my $OpSys (in $OpSysSet)
 {
  $OpSys->Reboot();
 }
}
else
{
 print Win32::OLE->LastError, "\n";
 exit(1);
}
```



## <a name="requirements"></a><span data-ttu-id="37466-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37466-133">Requirements</span></span>



| <span data-ttu-id="37466-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="37466-134">Requirement</span></span> | <span data-ttu-id="37466-135">Valore</span><span class="sxs-lookup"><span data-stu-id="37466-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37466-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37466-136">Minimum supported client</span></span><br/> | <span data-ttu-id="37466-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37466-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="37466-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37466-138">Minimum supported server</span></span><br/> | <span data-ttu-id="37466-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37466-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="37466-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="37466-140">Namespace</span></span><br/>                | <span data-ttu-id="37466-141">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="37466-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="37466-142">MOF</span><span class="sxs-lookup"><span data-stu-id="37466-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37466-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37466-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="37466-144">DLL</span><span class="sxs-lookup"><span data-stu-id="37466-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37466-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37466-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37466-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37466-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="37466-147">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="37466-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="37466-148">**\_OperatingSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="37466-148">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="37466-149">**CIM \_ OperatingSystem. Shutdown, metodo**</span><span class="sxs-lookup"><span data-stu-id="37466-149">**CIM\_OperatingSystem.Shutdown method**</span></span>](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="37466-150">Attività WMI: gestione desktop</span><span class="sxs-lookup"><span data-stu-id="37466-150">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

