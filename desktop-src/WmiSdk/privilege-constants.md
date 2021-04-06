---
description: Il parametro strPrivilege del metodo SWbemPrivilegeSet. AddAsString e il parametro iPrivilege per SWbemPrivilegeSet. Add richiedono stringhe di privilegio da WbemPrivilegeEnum.
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: Costanti Privilege (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- wbemPrivilegeCreateToken
- wbemPrivilegePrimaryToken
- wbemPrivilegeLockMemory
- wbemPrivilegeIncreaseQuota
- wbemPrivilegeMachineAccount
- wbemPrivilegeTcb
- wbemPrivilegeSecurity
- wbemPrivilegeTakeOwnership
- wbemPrivilegeLoadDriver
- wbemPrivilegeSystemProfile
- wbemPrivilegeSystemtime
- wbemPrivilegeProfileSingleProcess
- wbemPrivilegeIncreaseBasePriority
- wbemPrivilegeCreatePagefile
- wbemPrivilegeCreatePermanent
- wbemPrivilegeBackup
- wbemPrivilegeRestore
- wbemPrivilegeShutdown
- wbemPrivilegeDebug
- wbemPrivilegeAudit
- wbemPrivilegeSystemEnvironment
- wbemPrivilegeChangeNotify
- wbemPrivilegeRemoteShutdown
- wbemPrivilegeUndock
- wbemPrivilegeSyncAgent
- wbemPrivilegeEnableDelegation
- wbemPrivilegeManageVolume
api_type:
- HeaderDef
api_location:
- Wbemdisp.h
ms.openlocfilehash: 73fb9167af63f40f3a6e1c00470d871f749d228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759767"
---
# <a name="privilege-constants"></a><span data-ttu-id="a8170-103">Costanti Privilege</span><span class="sxs-lookup"><span data-stu-id="a8170-103">Privilege Constants</span></span>

<span data-ttu-id="a8170-104">Il parametro *strPrivilege* del metodo [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) e il parametro *iPrivilege* per [**SWbemPrivilegeSet. Add**](swbemprivilegeset-add.md) richiedono stringhe di privilegio da [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span><span class="sxs-lookup"><span data-stu-id="a8170-104">The *strPrivilege* parameter of the [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) method and the *iPrivilege* parameter for [**SWbemPrivilegeSet.Add**](swbemprivilegeset-add.md) require privilege strings from [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span> <span data-ttu-id="a8170-105">Per ulteriori informazioni sull'utilizzo delle costanti Privilege, vedere [esecuzione di operazioni con privilegi](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="a8170-105">For more information about how to use privilege constants, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="a8170-106">Le costanti seguenti sono definite in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span><span class="sxs-lookup"><span data-stu-id="a8170-106">The following constants are defined in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span> <span data-ttu-id="a8170-107">Nell'elenco seguente sono incluse le costanti equivalenti per C++ e le stringhe per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="a8170-107">The following list includes the equivalent constants for C++ and strings for scripting.</span></span> <span data-ttu-id="a8170-108">Per creare il nome breve dello scripting, rimuovere "se" e "Privilege" dal nome della costante C++.</span><span class="sxs-lookup"><span data-stu-id="a8170-108">To form the scripting short name, remove the "Se" and "Privilege" from the C++ constant name.</span></span>

<span data-ttu-id="a8170-109">Nell'esempio di codice VBScript seguente viene illustrato come abilitare il privilegio RemoteShutdown in uno script.</span><span class="sxs-lookup"><span data-stu-id="a8170-109">The following VBScript code example shows how to enable the RemoteShutdown privilege in a script.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



<span data-ttu-id="a8170-110">Molti metodi WMI richiedono l'abilitazione di una o più autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="a8170-110">Many WMI methods require that one or more permission be enabled.</span></span> <span data-ttu-id="a8170-111">Se a un account non è stato concesso un privilegio, non è possibile abilitarlo per la chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="a8170-111">If an account has not been granted a privilege, it cannot be enabled for the method call.</span></span>

<dl> <dt>

<span data-ttu-id="a8170-112"><span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**</span><span class="sxs-lookup"><span data-stu-id="a8170-112"><span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="a8170-113">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-114">Costante C++: **se \_ creare \_ il \_ nome del token** stringa: **SeCreateTokenPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-114">C++ constant: **SE\_CREATE\_TOKEN\_NAME** string: **SeCreateTokenPrivilege**</span></span>

<span data-ttu-id="a8170-115">Nome breve scripting: **creazione Okta**</span><span class="sxs-lookup"><span data-stu-id="a8170-115">Scripting short name: **CreateToken**</span></span>

<span data-ttu-id="a8170-116">Obbligatorio per creare un oggetto token primario.</span><span class="sxs-lookup"><span data-stu-id="a8170-116">Required to create a primary token object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-117"><span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**</span><span class="sxs-lookup"><span data-stu-id="a8170-117"><span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-118">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="a8170-118">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-119">Costante C++: **SeAssignPrimaryTokenPrivilege** stringa: **SeAssignPrimaryTokenPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-119">C++ constant: **SeAssignPrimaryTokenPrivilege** string: **SeAssignPrimaryTokenPrivilege**</span></span>

<span data-ttu-id="a8170-120">Nome breve scripting: **AssignPrimaryToken**</span><span class="sxs-lookup"><span data-stu-id="a8170-120">Scripting short name: **AssignPrimaryToken**</span></span>

<span data-ttu-id="a8170-121">Obbligatorio per sostituire un token a livello di processo.</span><span class="sxs-lookup"><span data-stu-id="a8170-121">Required to replace a process-level token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-122"><span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**</span><span class="sxs-lookup"><span data-stu-id="a8170-122"><span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-123">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="a8170-123">3 (0x3)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-124">Costante C++: **se si \_ blocca il \_ \_ nome della memoria** stringa: **SeLockMemoryPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-124">C++ constant: **SE\_LOCK\_MEMORY\_NAME** string: **SeLockMemoryPrivilege**</span></span>

<span data-ttu-id="a8170-125">Nome breve scripting: **LockMemory**</span><span class="sxs-lookup"><span data-stu-id="a8170-125">Scripting short name: **LockMemory**</span></span>

<span data-ttu-id="a8170-126">Obbligatorio per bloccare le pagine in memoria.</span><span class="sxs-lookup"><span data-stu-id="a8170-126">Required to lock pages in memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-127"><span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**</span><span class="sxs-lookup"><span data-stu-id="a8170-127"><span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-128">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="a8170-128">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-129">Costante C++: **se \_ aumenta \_ il \_ nome della quota** stringa: **SeIncreaseQuotaPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-129">C++ constant: **SE\_INCREASE\_QUOTA\_NAME** string: **SeIncreaseQuotaPrivilege**</span></span>

<span data-ttu-id="a8170-130">Nome breve scripting: **IncreaseQuotaPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-130">Scripting short name: **IncreaseQuotaPrivilege**</span></span>

<span data-ttu-id="a8170-131">Obbligatorio per modificare le quote di memoria per un processo.</span><span class="sxs-lookup"><span data-stu-id="a8170-131">Required to adjust memory quotas for a process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-132"><span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**</span><span class="sxs-lookup"><span data-stu-id="a8170-132"><span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-133">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="a8170-133">5 (0x5)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-134">Costante C++: **se \_ macine \_ \_ nome account** stringa: **SeMachineAccountPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-134">C++ constant: **SE\_MACINE\_ACCOUNT\_NAME** string: **SeMachineAccountPrivilege**</span></span>

<span data-ttu-id="a8170-135">Nome breve scripting: **MachineAccount**</span><span class="sxs-lookup"><span data-stu-id="a8170-135">Scripting short name: **MachineAccount**</span></span>

<span data-ttu-id="a8170-136">Obbligatorio per aggiungere workstation a un dominio.</span><span class="sxs-lookup"><span data-stu-id="a8170-136">Required to add workstations to a domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-137"><span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**</span><span class="sxs-lookup"><span data-stu-id="a8170-137"><span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-138">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="a8170-138">6 (0x6)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-139">Costante C++: **se \_ TCB \_ nome** stringa: **SeTcbPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-139">C++ constant: **SE\_TCB\_NAME** string: **SeTcbPrivilege**</span></span>

<span data-ttu-id="a8170-140">Nome breve scripting: **TCB**</span><span class="sxs-lookup"><span data-stu-id="a8170-140">Scripting short name: **Tcb**</span></span>

<span data-ttu-id="a8170-141">Obbligatorio per agire come parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a8170-141">Required to act as part of the operating system.</span></span> <span data-ttu-id="a8170-142">Il titolare fa parte della base dei computer attendibili.</span><span class="sxs-lookup"><span data-stu-id="a8170-142">The holder is part of the trusted computer base.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-143"><span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**</span><span class="sxs-lookup"><span data-stu-id="a8170-143"><span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-144">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="a8170-144">7 (0x7)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-145">Costante C++: **se \_ \_ nome sicurezza** stringa: **SeSecurityPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-145">C++ constant: **SE\_SECURITY\_NAME** string: **SeSecurityPrivilege**</span></span>

<span data-ttu-id="a8170-146">Nome breve scripting: **sicurezza**</span><span class="sxs-lookup"><span data-stu-id="a8170-146">Scripting short name: **Security**</span></span>

<span data-ttu-id="a8170-147">Necessaria per gestire il controllo e il registro di protezione NT.</span><span class="sxs-lookup"><span data-stu-id="a8170-147">Required to manage auditing and the NT security log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-148"><span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="a8170-148"><span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-149">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="a8170-149">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-150">Costante C++: **se \_ accetta \_ il \_ nome della proprietà** stringa: **SeTakeOwnershipPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-150">C++ constant: **SE\_TAKE\_OWNERSHIP\_NAME** string: **SeTakeOwnershipPrivilege**</span></span>

<span data-ttu-id="a8170-151">Nome breve scripting: **TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="a8170-151">Scripting short name: **TakeOwnership**</span></span>

<span data-ttu-id="a8170-152">Obbligatorio per assumere la proprietà di file o altri oggetti senza avere una [*voce di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE) nell'elenco di controllo di *accesso discrezionale* (DACL).</span><span class="sxs-lookup"><span data-stu-id="a8170-152">Required to assume ownership of files or other objects without having an [*Access Control Entry*](/windows/desktop/SecGloss/a-gly) (ACE) in the *discretionary access control list* (DACL).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-153"><span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**</span><span class="sxs-lookup"><span data-stu-id="a8170-153"><span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-154">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="a8170-154">9 (0x9)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-155">Costante C++: se si carica la stringa del **\_ \_ driver** : **SeLoadDriverPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-155">C++ constant: **SE\_LOAD\_DRIVER** string: **SeLoadDriverPrivilege**</span></span>

<span data-ttu-id="a8170-156">Nome breve scripting: **LoadDriver**</span><span class="sxs-lookup"><span data-stu-id="a8170-156">Scripting short name: **LoadDriver**</span></span>

<span data-ttu-id="a8170-157">Necessario per caricare o scaricare un driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8170-157">Required to load or unload a device driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-158"><span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**</span><span class="sxs-lookup"><span data-stu-id="a8170-158"><span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-159">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="a8170-159">10 (0xA)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-160">Costante C++: **se \_ \_ il \_ nome del profilo di sistema** è stringa: **SeSystemProfilePrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-160">C++ constant: **SE\_SYSTEM\_PROFILE\_NAME** string: **SeSystemProfilePrivilege**</span></span>

<span data-ttu-id="a8170-161">Nome breve scripting: **systemprofile**</span><span class="sxs-lookup"><span data-stu-id="a8170-161">Scripting short name: **SystemProfile**</span></span>

<span data-ttu-id="a8170-162">Obbligatorio per raccogliere informazioni sul profilo sulle prestazioni del sistema.</span><span class="sxs-lookup"><span data-stu-id="a8170-162">Required to gather profile information about system performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-163"><span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**</span><span class="sxs-lookup"><span data-stu-id="a8170-163"><span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-164">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="a8170-164">11 (0xB)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-165">Costante C++: **se \_** è la \_ stringa del nome SYSTEMTIME: **SeSystemTimePrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-165">C++ constant: **SE\_SYSTEMTIME**\_NAME string: **SeSystemtimePrivilege**</span></span>

<span data-ttu-id="a8170-166">Nome breve scripting: **SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="a8170-166">Scripting short name: **Systemtime**</span></span>

<span data-ttu-id="a8170-167">Obbligatorio per modificare l'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="a8170-167">Required to change the system time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-168"><span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**</span><span class="sxs-lookup"><span data-stu-id="a8170-168"><span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-169">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="a8170-169">12 (0xC)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-170">Costante C++: **se \_ il \_ \_ \_ nome del singolo processo** è stringa: **SeProfileSingleProcessPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-170">C++ constant: **SE\_PROF\_SINGLE\_PROCESS\_NAME** string: **SeProfileSingleProcessPrivilege**</span></span>

<span data-ttu-id="a8170-171">Nome breve scripting: **ProfileSingleProcess**</span><span class="sxs-lookup"><span data-stu-id="a8170-171">Scripting short name: **ProfileSingleProcess**</span></span>

<span data-ttu-id="a8170-172">Obbligatorio per raccogliere informazioni sul profilo per un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="a8170-172">Required to gather profile information for a single process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-173"><span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**</span><span class="sxs-lookup"><span data-stu-id="a8170-173"><span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-174">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="a8170-174">13 (0xD)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-175">Costante C++: **se \_ Inc \_ base \_ \_ nome priorità** stringa: **SeIncreaseBasePriorityPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-175">C++ constant: **SE\_INC\_BASE\_PRIORITY\_NAME** string: **SeIncreaseBasePriorityPrivilege**</span></span>

<span data-ttu-id="a8170-176">Nome breve scripting: **IncreaseBasePriority**</span><span class="sxs-lookup"><span data-stu-id="a8170-176">Scripting short name: **IncreaseBasePriority**</span></span>

<span data-ttu-id="a8170-177">Obbligatorio per aumentare la priorità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="a8170-177">Required to increase scheduling priority.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-178"><span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**</span><span class="sxs-lookup"><span data-stu-id="a8170-178"><span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-179">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="a8170-179">14 (0xE)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-180">Costante C++: **se \_ creare \_ il \_ nome del file di paging** stringa: **SeCreatePagefilePrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-180">C++ constant: **SE\_CREATE\_PAGEFILE\_NAME** string: **SeCreatePagefilePrivilege**</span></span>

<span data-ttu-id="a8170-181">Nome breve scripting: **CreatePagefile**</span><span class="sxs-lookup"><span data-stu-id="a8170-181">Scripting short name: **CreatePagefile**</span></span>

<span data-ttu-id="a8170-182">Necessario per creare un pagefile.</span><span class="sxs-lookup"><span data-stu-id="a8170-182">Required to create a pagefile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-183"><span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**</span><span class="sxs-lookup"><span data-stu-id="a8170-183"><span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-184">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="a8170-184">15 (0xF)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-185">Costante C++: **se crea una stringa di \_ \_ \_ nome permanente** : **SeCreatePermanentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-185">C++ constant: **SE\_CREATE\_PERMANENT\_NAME** string: **SeCreatePermanentPrivilege**</span></span>

<span data-ttu-id="a8170-186">Nome breve scripting: **CreatePermanent**</span><span class="sxs-lookup"><span data-stu-id="a8170-186">Scripting short name: **CreatePermanent**</span></span>

<span data-ttu-id="a8170-187">Obbligatorio per creare oggetti condivisi permanenti.</span><span class="sxs-lookup"><span data-stu-id="a8170-187">Required to create permanent shared objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-188"><span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**</span><span class="sxs-lookup"><span data-stu-id="a8170-188"><span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-189">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="a8170-189">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-190">Costante C++: **se \_ \_ nome backup** stringa: **SeBackupPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-190">C++ constant: **SE\_BACKUP\_NAME** string: **SeBackupPrivilege**</span></span>

<span data-ttu-id="a8170-191">Nome breve scripting: **backup**</span><span class="sxs-lookup"><span data-stu-id="a8170-191">Scripting short name: **Backup**</span></span>

<span data-ttu-id="a8170-192">Obbligatorio per eseguire il backup di file e directory, indipendentemente dall'ACL specificato per il file.</span><span class="sxs-lookup"><span data-stu-id="a8170-192">Required to backup files and directories, regardless of the ACL specified for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-193"><span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**</span><span class="sxs-lookup"><span data-stu-id="a8170-193"><span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-194">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="a8170-194">17 (0x11)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-195">Costante C++: **se \_ ripristinare il \_ nome** stringa: **SeRestorePrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-195">C++ constant: **SE\_RESTORE\_NAME** string: **SeRestorePrivilege**</span></span>

<span data-ttu-id="a8170-196">Nome breve scripting: **Restore**</span><span class="sxs-lookup"><span data-stu-id="a8170-196">Scripting short name: **Restore**</span></span>

<span data-ttu-id="a8170-197">Obbligatorio per ripristinare i file e le directory, indipendentemente dall'ACL specificato per il file.</span><span class="sxs-lookup"><span data-stu-id="a8170-197">Required to restore files and directories, regardless of the ACL specified for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-198"><span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**</span><span class="sxs-lookup"><span data-stu-id="a8170-198"><span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-199">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="a8170-199">18 (0x12)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-200">Costante C++: **se si \_ Arresta il \_ nome** stringa: **SeShutdownPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-200">C++ constant: **SE\_SHUTDOWN\_NAME** string: **SeShutdownPrivilege**</span></span>

<span data-ttu-id="a8170-201">Nome breve scripting: **Shutdown**</span><span class="sxs-lookup"><span data-stu-id="a8170-201">Scripting short name: **Shutdown**</span></span>

<span data-ttu-id="a8170-202">Necessario per arrestare il sistema locale.</span><span class="sxs-lookup"><span data-stu-id="a8170-202">Required to shut down the local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-203"><span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**</span><span class="sxs-lookup"><span data-stu-id="a8170-203"><span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-204">19 (0x13)</span><span class="sxs-lookup"><span data-stu-id="a8170-204">19 (0x13)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-205">Costante C++: **se \_ il \_ nome di debug** stringa: **SeDebugPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-205">C++ constant: **SE\_DEBUG\_NAME** string: **SeDebugPrivilege**</span></span>

<span data-ttu-id="a8170-206">Nome breve scripting: **debug**</span><span class="sxs-lookup"><span data-stu-id="a8170-206">Scripting short name: **Debug**</span></span>

<span data-ttu-id="a8170-207">Necessario per eseguire il debug e la modifica della memoria di un processo di proprietà di un altro account.</span><span class="sxs-lookup"><span data-stu-id="a8170-207">Required to debug and adjust the memory of a process owned by another account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-208"><span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**</span><span class="sxs-lookup"><span data-stu-id="a8170-208"><span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-209">20 (0x14)</span><span class="sxs-lookup"><span data-stu-id="a8170-209">20 (0x14)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-210">Costante C++: **se \_ controllo \_ nome** stringa: **SeAuditPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-210">C++ constant: **SE\_AUDIT\_NAME** string: **SeAuditPrivilege**</span></span>

<span data-ttu-id="a8170-211">Nome breve scripting: **Audit**</span><span class="sxs-lookup"><span data-stu-id="a8170-211">Scripting short name: **Audit**</span></span>

<span data-ttu-id="a8170-212">Obbligatorio per generare voci di controllo nel registro di sicurezza di NT.</span><span class="sxs-lookup"><span data-stu-id="a8170-212">Required to generate audit entries in the NT Security log.</span></span> <span data-ttu-id="a8170-213">Solo i server protetti devono disporre di questo privilegio.</span><span class="sxs-lookup"><span data-stu-id="a8170-213">Only secure servers should have this privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-214"><span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**</span><span class="sxs-lookup"><span data-stu-id="a8170-214"><span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-215">21 (0x15)</span><span class="sxs-lookup"><span data-stu-id="a8170-215">21 (0x15)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-216">Costante C++: **se \_ il \_ \_ nome dell'ambiente di sistema** è stringa: **SeSystemEnvironmentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-216">C++ constant: **SE\_SYSTEM\_ENVIRONMENT\_NAME** string: **SeSystemEnvironmentPrivilege**</span></span>

<span data-ttu-id="a8170-217">Nome breve scripting: **SystemEnvironment**</span><span class="sxs-lookup"><span data-stu-id="a8170-217">Scripting short name: **SystemEnvironment**</span></span>

<span data-ttu-id="a8170-218">Obbligatorio per modificare la RAM non volatile dei sistemi che usano questo tipo di memoria per archiviare i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="a8170-218">Required to modify the nonvolatile RAM of systems that use this type of memory to store configuration data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-219"><span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="a8170-219"><span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-220">22 (0x16)</span><span class="sxs-lookup"><span data-stu-id="a8170-220">22 (0x16)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-221">Costante C++: **se la \_ modifica \_ notifica il \_ nome** stringa: **SeChangeNotifyPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-221">C++ constant: **SE\_CHANGE\_NOTIFY\_NAME** string: **SeChangeNotifyPrivilege**</span></span>

<span data-ttu-id="a8170-222">Nome breve scripting: **ChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="a8170-222">Scripting short name: **ChangeNotify**</span></span>

<span data-ttu-id="a8170-223">Necessaria per ricevere notifiche delle modifiche a file o directory e ignorare i controlli di accesso attraversati.</span><span class="sxs-lookup"><span data-stu-id="a8170-223">Required to receive notifications of changes to files or directories and bypass traversal access checks.</span></span> <span data-ttu-id="a8170-224">Questo privilegio è abilitato per impostazione predefinita per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="a8170-224">This privilege is enabled by default for all users.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-225"><span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**</span><span class="sxs-lookup"><span data-stu-id="a8170-225"><span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-226">23 (0x17)</span><span class="sxs-lookup"><span data-stu-id="a8170-226">23 (0x17)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-227">Costante C++: se la stringa del **\_ \_ \_ nome di arresto remoto** è: **SeRemoteShutdownPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-227">C++ constant: **SE\_REMOTE\_SHUTDOWN\_NAME** string: **SeRemoteShutdownPrivilege**</span></span>

<span data-ttu-id="a8170-228">Nome breve scripting: **RemoteShutdown**</span><span class="sxs-lookup"><span data-stu-id="a8170-228">Scripting short name: **RemoteShutdown**</span></span>

<span data-ttu-id="a8170-229">Necessario per arrestare un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="a8170-229">Required to shut down a remote computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-230"><span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**</span><span class="sxs-lookup"><span data-stu-id="a8170-230"><span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-231">24 (0x18)</span><span class="sxs-lookup"><span data-stu-id="a8170-231">24 (0x18)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-232">Costante C++: se la stringa del **\_ \_ nome viene disancorata** : **SeUndockPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-232">C++ constant: **SE\_UNDOCK\_NAME** string: **SeUndockPrivilege**</span></span>

<span data-ttu-id="a8170-233">Nome breve dello script: **Undock**</span><span class="sxs-lookup"><span data-stu-id="a8170-233">Scripting short name: **Undock**</span></span>

<span data-ttu-id="a8170-234">Necessario per rimuovere un computer portatile da una stazione di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="a8170-234">Required to remove a laptop from a docking station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-235"><span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**</span><span class="sxs-lookup"><span data-stu-id="a8170-235"><span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-236">25 (0x19)</span><span class="sxs-lookup"><span data-stu-id="a8170-236">25 (0x19)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-237">Costante C++: **se \_ il \_ \_ nome dell'agente di sincronizzazione** è stringa: **SeSyncAgentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-237">C++ constant: **SE\_SYNC\_AGENT\_NAME** string: **SeSyncAgentPrivilege**</span></span>

<span data-ttu-id="a8170-238">Nome breve scripting: **SyncAgent**</span><span class="sxs-lookup"><span data-stu-id="a8170-238">Scripting short name: **SyncAgent**</span></span>

<span data-ttu-id="a8170-239">Obbligatorio per sincronizzare i dati del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="a8170-239">Required to synchronize directory service data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-240"><span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**</span><span class="sxs-lookup"><span data-stu-id="a8170-240"><span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-241">26 (0x1A)</span><span class="sxs-lookup"><span data-stu-id="a8170-241">26 (0x1A)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-242">Costante C++: **se \_ Abilita \_ il \_ nome della delega** stringa: **SeEnableDelegationPrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-242">C++ constant: **SE\_ENABLE\_DELEGATION\_NAME** string: **SeEnableDelegationPrivilege**</span></span>

<span data-ttu-id="a8170-243">Nome breve scripting: **EnableDelegation**</span><span class="sxs-lookup"><span data-stu-id="a8170-243">Scripting short name: **EnableDelegation**</span></span>

<span data-ttu-id="a8170-244">Necessario per consentire l'attendibilità degli account computer e utente per la delega.</span><span class="sxs-lookup"><span data-stu-id="a8170-244">Required to enable computer and user accounts to be trusted for delegation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8170-245"><span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**</span><span class="sxs-lookup"><span data-stu-id="a8170-245"><span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8170-246">27 (0x1B)</span><span class="sxs-lookup"><span data-stu-id="a8170-246">27 (0x1B)</span></span>
</dt> <dt>



<span data-ttu-id="a8170-247">Costante C++: **se \_ Gestisci \_ \_ nome volume** stringa: **SeManageVolumePrivilege**</span><span class="sxs-lookup"><span data-stu-id="a8170-247">C++ constant: **SE\_MANAGE\_VOLUME\_NAME** string: **SeManageVolumePrivilege**</span></span>

<span data-ttu-id="a8170-248">Nome breve scripting: **ManageVolume**</span><span class="sxs-lookup"><span data-stu-id="a8170-248">Scripting short name: **ManageVolume**</span></span>

<span data-ttu-id="a8170-249">Obbligatorio per eseguire le attività di manutenzione del volume.</span><span class="sxs-lookup"><span data-stu-id="a8170-249">Required to perform volume maintenance tasks.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8170-250">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8170-250">Requirements</span></span>



| <span data-ttu-id="a8170-251">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8170-251">Requirement</span></span> | <span data-ttu-id="a8170-252">Valore</span><span class="sxs-lookup"><span data-stu-id="a8170-252">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8170-253">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8170-253">Minimum supported client</span></span><br/> | <span data-ttu-id="a8170-254">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8170-254">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8170-255">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8170-255">Minimum supported server</span></span><br/> | <span data-ttu-id="a8170-256">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8170-256">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8170-257">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8170-257">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8170-258"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8170-258"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8170-259">IDL</span><span class="sxs-lookup"><span data-stu-id="a8170-259">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8170-260"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8170-260"><dt>Wbemdisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8170-261">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8170-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8170-262">Esecuzione di script di costanti API</span><span class="sxs-lookup"><span data-stu-id="a8170-262">Scripting API Constants</span></span>](scripting-api-constants.md)
</dt> <dt>

[<span data-ttu-id="a8170-263">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="a8170-263">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="a8170-264">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="a8170-264">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="a8170-265">Esecuzione di operazioni con privilegi</span><span class="sxs-lookup"><span data-stu-id="a8170-265">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="a8170-266">Esecuzione di operazioni con privilegi tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="a8170-266">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

