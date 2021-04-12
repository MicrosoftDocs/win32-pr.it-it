---
description: Modifica le autorizzazioni di sicurezza per il file di voce di directory specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo ChangeSecurityPermissions).
ms.assetid: 787e48af-7cb4-4d0b-a2f1-ffa696466ef2
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissionsEx della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4bcadd4a4ad115a1a367db4f2a2f645eb6a4742c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225623"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_directory-class"></a><span data-ttu-id="92d1c-103">Metodo ChangeSecurityPermissionsEx della classe di \_ directory Win32</span><span class="sxs-lookup"><span data-stu-id="92d1c-103">ChangeSecurityPermissionsEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="92d1c-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** modifica le autorizzazioni di sicurezza per il file di voce di directory specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="92d1c-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the directory entry file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="92d1c-105">Se il file logico è una directory, questo metodo è ricorsivo e modifica le autorizzazioni di sicurezza di tutti i file e le sottodirectory in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="92d1c-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="92d1c-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="92d1c-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="92d1c-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="92d1c-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="92d1c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92d1c-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="92d1c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="92d1c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92d1c-110">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92d1c-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-111">Espressione che viene risolta in un'istanza di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="92d1c-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="92d1c-112">Questo parametro contiene nuove autorizzazioni di sicurezza per l'istanza [**del \_ paging Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="92d1c-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-113">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92d1c-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-114">Privilegio di sicurezza da modificare.</span><span class="sxs-lookup"><span data-stu-id="92d1c-114">Security privilege to be modified.</span></span> <span data-ttu-id="92d1c-115">Per modificare, ad esempio, la sicurezza del proprietario e dell'elenco di controllo di accesso discrezionale (DACL), utilizzare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="92d1c-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="92d1c-116">-oppure-</span><span class="sxs-lookup"><span data-stu-id="92d1c-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="92d1c-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)</span><span class="sxs-lookup"><span data-stu-id="92d1c-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="92d1c-118">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="92d1c-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="92d1c-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)</span><span class="sxs-lookup"><span data-stu-id="92d1c-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="92d1c-120">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="92d1c-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="92d1c-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="92d1c-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="92d1c-122">Modificare l'elenco DACL del file logico.</span><span class="sxs-lookup"><span data-stu-id="92d1c-122">Change the DACL list of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="92d1c-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="92d1c-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="92d1c-124">Modificare l'elenco di controllo di accesso di sistema (SACL) del file logico.</span><span class="sxs-lookup"><span data-stu-id="92d1c-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="92d1c-125">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92d1c-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-126">Nome del file o della directory in cui il metodo **ChangeSecurityPermissionsEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="92d1c-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="92d1c-127">Questo parametro è null se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="92d1c-127">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-128">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="92d1c-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-129">Denomina il file o la directory figlio da utilizzare come punto di partenza per **ChangeSecurityPermissionsEx**.</span><span class="sxs-lookup"><span data-stu-id="92d1c-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="92d1c-130">In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="92d1c-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="92d1c-131">Se questo parametro è null, l'operazione viene eseguita nel file o nella directory specificata nella chiamata **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="92d1c-131">If this parameter is null, the operation is performed on the file or directory that is specified in the **ExecMethod** call.</span></span> <span data-ttu-id="92d1c-132">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="92d1c-132">This parameter is optional.</span></span>

<span data-ttu-id="92d1c-133">Se si usa *StartFileName* , è necessario impostare *ricorsivo* su true.</span><span class="sxs-lookup"><span data-stu-id="92d1c-133">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-134">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="92d1c-134">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-135">Se **true**, la modifica della proprietà viene applicata in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="92d1c-135">If **true**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="92d1c-136">Per le istanze di file, il parametro di input *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="92d1c-136">For file instances, the *Recursive* input parameter is ignored.</span></span> <span data-ttu-id="92d1c-137">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="92d1c-137">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92d1c-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92d1c-138">Return value</span></span>

<span data-ttu-id="92d1c-139">Restituisce un valore pari a 0 (zero) se le autorizzazioni vengono modificate e un numero diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="92d1c-139">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="92d1c-140">**Success**</span><span class="sxs-lookup"><span data-stu-id="92d1c-140">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-141">0</span><span class="sxs-lookup"><span data-stu-id="92d1c-141">0</span></span>

<span data-ttu-id="92d1c-142">La richiesta ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="92d1c-142">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-143">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="92d1c-143">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-144">2</span><span class="sxs-lookup"><span data-stu-id="92d1c-144">2</span></span>

<span data-ttu-id="92d1c-145">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="92d1c-145">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-146">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="92d1c-146">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-147">8</span><span class="sxs-lookup"><span data-stu-id="92d1c-147">8</span></span>

<span data-ttu-id="92d1c-148">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="92d1c-148">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-149">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="92d1c-149">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-150">9</span><span class="sxs-lookup"><span data-stu-id="92d1c-150">9</span></span>

<span data-ttu-id="92d1c-151">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="92d1c-151">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-152">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="92d1c-152">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-153">10</span><span class="sxs-lookup"><span data-stu-id="92d1c-153">10</span></span>

<span data-ttu-id="92d1c-154">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="92d1c-154">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-155">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="92d1c-155">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-156">11</span><span class="sxs-lookup"><span data-stu-id="92d1c-156">11</span></span>

<span data-ttu-id="92d1c-157">Il file system non è un file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="92d1c-157">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-158">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="92d1c-158">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-159">12</span><span class="sxs-lookup"><span data-stu-id="92d1c-159">12</span></span>

<span data-ttu-id="92d1c-160">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="92d1c-160">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-161">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="92d1c-161">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-162">13</span><span class="sxs-lookup"><span data-stu-id="92d1c-162">13</span></span>

<span data-ttu-id="92d1c-163">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="92d1c-163">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-164">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="92d1c-164">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-165">14</span><span class="sxs-lookup"><span data-stu-id="92d1c-165">14</span></span>

<span data-ttu-id="92d1c-166">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="92d1c-166">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-167">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="92d1c-167">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-168">15</span><span class="sxs-lookup"><span data-stu-id="92d1c-168">15</span></span>

<span data-ttu-id="92d1c-169">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="92d1c-169">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-170">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="92d1c-170">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-171">16</span><span class="sxs-lookup"><span data-stu-id="92d1c-171">16</span></span>

<span data-ttu-id="92d1c-172">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="92d1c-172">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-173">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="92d1c-173">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-174">17</span><span class="sxs-lookup"><span data-stu-id="92d1c-174">17</span></span>

<span data-ttu-id="92d1c-175">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="92d1c-175">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="92d1c-176">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="92d1c-176">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="92d1c-177">21</span><span class="sxs-lookup"><span data-stu-id="92d1c-177">21</span></span>

<span data-ttu-id="92d1c-178">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="92d1c-178">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92d1c-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92d1c-179">Requirements</span></span>



| <span data-ttu-id="92d1c-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="92d1c-180">Requirement</span></span> | <span data-ttu-id="92d1c-181">Valore</span><span class="sxs-lookup"><span data-stu-id="92d1c-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92d1c-182">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92d1c-182">Minimum supported client</span></span><br/> | <span data-ttu-id="92d1c-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92d1c-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92d1c-184">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92d1c-184">Minimum supported server</span></span><br/> | <span data-ttu-id="92d1c-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92d1c-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92d1c-186">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="92d1c-186">Namespace</span></span><br/>                | <span data-ttu-id="92d1c-187">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="92d1c-187">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="92d1c-188">MOF</span><span class="sxs-lookup"><span data-stu-id="92d1c-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92d1c-189"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92d1c-189"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="92d1c-190">DLL</span><span class="sxs-lookup"><span data-stu-id="92d1c-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92d1c-191"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92d1c-191"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92d1c-192">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92d1c-192">See also</span></span>

<dl> <dt>

<span data-ttu-id="92d1c-193">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="92d1c-193">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="92d1c-194">**\_Directory Win32**</span><span class="sxs-lookup"><span data-stu-id="92d1c-194">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

