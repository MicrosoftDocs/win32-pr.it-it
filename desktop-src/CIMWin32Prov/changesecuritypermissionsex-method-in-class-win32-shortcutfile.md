---
description: Modifica le autorizzazioni di sicurezza per il file di collegamento logico specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo ChangeSecurityPermissions).
ms.assetid: 9a5c9fa9-ccd9-4792-969f-28f52ab9bc52
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissionsEx della classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 124f8d883b89379e4b36c5dd33b029718fbbd469
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523505"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="bfd21-103">Metodo ChangeSecurityPermissionsEx della \_ classe ShortcutFile Win32</span><span class="sxs-lookup"><span data-stu-id="bfd21-103">ChangeSecurityPermissionsEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="bfd21-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** modifica le autorizzazioni di sicurezza per il file di collegamento logico specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="bfd21-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical shortcut file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="bfd21-105">Se il file logico è una directory, questo metodo è ricorsivo e modifica le autorizzazioni di sicurezza di tutti i file e le sottodirectory in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="bfd21-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="bfd21-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="bfd21-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bfd21-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="bfd21-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfd21-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bfd21-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="bfd21-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bfd21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfd21-110">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfd21-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-111">Espressione che viene risolta in un'istanza di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="bfd21-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="bfd21-112">Questo parametro contiene nuove autorizzazioni di sicurezza per l'istanza [**del \_ paging Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="bfd21-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-113">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfd21-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-114">Privilegio di sicurezza da modificare.</span><span class="sxs-lookup"><span data-stu-id="bfd21-114">Security privilege to be modified.</span></span> <span data-ttu-id="bfd21-115">Per modificare, ad esempio, la sicurezza del proprietario e dell'elenco di controllo di accesso discrezionale (DACL), utilizzare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="bfd21-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="bfd21-116">oppure</span><span class="sxs-lookup"><span data-stu-id="bfd21-116">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="bfd21-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)</span><span class="sxs-lookup"><span data-stu-id="bfd21-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bfd21-118">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="bfd21-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="bfd21-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)</span><span class="sxs-lookup"><span data-stu-id="bfd21-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bfd21-120">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="bfd21-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="bfd21-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="bfd21-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bfd21-122">Modificare l'elenco di controllo di accesso discrezionale (DACL) del file logico.</span><span class="sxs-lookup"><span data-stu-id="bfd21-122">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="bfd21-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="bfd21-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="bfd21-124">Modificare l'elenco di controllo di accesso di sistema (SACL) del file logico.</span><span class="sxs-lookup"><span data-stu-id="bfd21-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bfd21-125">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bfd21-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-126">Nome del file o della directory in cui il metodo **ChangeSecurityPermissionsEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="bfd21-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="bfd21-127">Questo parametro è **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="bfd21-127">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-128">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="bfd21-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-129">Denomina il file o la directory figlio da utilizzare come punto di partenza per **ChangeSecurityPermissionsEx**.</span><span class="sxs-lookup"><span data-stu-id="bfd21-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="bfd21-130">In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="bfd21-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="bfd21-131">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="bfd21-131">If this parameter is **NULL**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-132">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="bfd21-132">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-133">Se **true**, la modifica della proprietà viene applicata in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="bfd21-133">If **true**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="bfd21-134">Per le istanze di file, il parametro *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="bfd21-134">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfd21-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bfd21-135">Return value</span></span>

<span data-ttu-id="bfd21-136">Restituisce un valore pari a 0 (zero) se le autorizzazioni vengono modificate e un numero diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="bfd21-136">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="bfd21-137">**Success**</span><span class="sxs-lookup"><span data-stu-id="bfd21-137">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-138">0</span><span class="sxs-lookup"><span data-stu-id="bfd21-138">0</span></span>

<span data-ttu-id="bfd21-139">La richiesta ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="bfd21-139">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-140">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="bfd21-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-141">2</span><span class="sxs-lookup"><span data-stu-id="bfd21-141">2</span></span>

<span data-ttu-id="bfd21-142">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="bfd21-142">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-143">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="bfd21-143">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-144">8</span><span class="sxs-lookup"><span data-stu-id="bfd21-144">8</span></span>

<span data-ttu-id="bfd21-145">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="bfd21-145">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-146">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="bfd21-146">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-147">9</span><span class="sxs-lookup"><span data-stu-id="bfd21-147">9</span></span>

<span data-ttu-id="bfd21-148">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="bfd21-148">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-149">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="bfd21-149">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-150">10</span><span class="sxs-lookup"><span data-stu-id="bfd21-150">10</span></span>

<span data-ttu-id="bfd21-151">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="bfd21-151">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-152">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="bfd21-152">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-153">11</span><span class="sxs-lookup"><span data-stu-id="bfd21-153">11</span></span>

<span data-ttu-id="bfd21-154">Il file system non è file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="bfd21-154">The file system is not NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-155">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="bfd21-155">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-156">12</span><span class="sxs-lookup"><span data-stu-id="bfd21-156">12</span></span>

<span data-ttu-id="bfd21-157">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="bfd21-157">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-158">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="bfd21-158">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-159">13</span><span class="sxs-lookup"><span data-stu-id="bfd21-159">13</span></span>

<span data-ttu-id="bfd21-160">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="bfd21-160">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-161">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="bfd21-161">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-162">14</span><span class="sxs-lookup"><span data-stu-id="bfd21-162">14</span></span>

<span data-ttu-id="bfd21-163">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="bfd21-163">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-164">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="bfd21-164">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-165">15</span><span class="sxs-lookup"><span data-stu-id="bfd21-165">15</span></span>

<span data-ttu-id="bfd21-166">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="bfd21-166">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-167">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="bfd21-167">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-168">16</span><span class="sxs-lookup"><span data-stu-id="bfd21-168">16</span></span>

<span data-ttu-id="bfd21-169">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="bfd21-169">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-170">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="bfd21-170">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-171">17</span><span class="sxs-lookup"><span data-stu-id="bfd21-171">17</span></span>

<span data-ttu-id="bfd21-172">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="bfd21-172">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="bfd21-173">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="bfd21-173">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="bfd21-174">21</span><span class="sxs-lookup"><span data-stu-id="bfd21-174">21</span></span>

<span data-ttu-id="bfd21-175">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="bfd21-175">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfd21-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfd21-176">Requirements</span></span>



| <span data-ttu-id="bfd21-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfd21-177">Requirement</span></span> | <span data-ttu-id="bfd21-178">Valore</span><span class="sxs-lookup"><span data-stu-id="bfd21-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd21-179">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfd21-179">Minimum supported client</span></span><br/> | <span data-ttu-id="bfd21-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bfd21-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bfd21-181">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfd21-181">Minimum supported server</span></span><br/> | <span data-ttu-id="bfd21-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfd21-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bfd21-183">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bfd21-183">Namespace</span></span><br/>                | <span data-ttu-id="bfd21-184">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="bfd21-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bfd21-185">MOF</span><span class="sxs-lookup"><span data-stu-id="bfd21-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfd21-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfd21-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfd21-187">DLL</span><span class="sxs-lookup"><span data-stu-id="bfd21-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfd21-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfd21-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfd21-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bfd21-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="bfd21-190">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bfd21-190">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bfd21-191">**\_ShortcutFile Win32**</span><span class="sxs-lookup"><span data-stu-id="bfd21-191">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

