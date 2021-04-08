---
description: Modifica le autorizzazioni di sicurezza per il file di codec specificato nel percorso dell'oggetto. questo metodo è una versione estesa del metodo ChangeSecurityPermissions.
ms.assetid: 3eac4ae1-3c0e-4e81-8b23-9ad8698f723c
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissionsEx della classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 549c55a5066bdaba4699ec76ed3b7be23eb28b96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877682"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="89735-103">Metodo ChangeSecurityPermissionsEx della \_ classe Sqlcfile Win32</span><span class="sxs-lookup"><span data-stu-id="89735-103">ChangeSecurityPermissionsEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="89735-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** modifica le autorizzazioni di sicurezza per il file di codec specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="89735-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the codec file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="89735-105">Se il file logico è una directory, questo metodo è ricorsivo e modifica le autorizzazioni di sicurezza di tutti i file e le sottodirectory in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="89735-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="89735-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="89735-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="89735-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="89735-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="89735-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89735-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="89735-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="89735-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89735-110">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89735-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89735-111">Espressione che viene risolta in un'istanza di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="89735-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="89735-112">Questo descrittore contiene nuove autorizzazioni di sicurezza per l'istanza di [**Win32 \_ codecfile**](win32-codecfile.md).</span><span class="sxs-lookup"><span data-stu-id="89735-112">This descriptor contains new security permissions for the instance of [**Win32\_CodecFile**](win32-codecfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="89735-113">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89735-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89735-114">Privilegi di sicurezza effettivi da modificare.</span><span class="sxs-lookup"><span data-stu-id="89735-114">Actual security privilege to be modified.</span></span> <span data-ttu-id="89735-115">Per modificare, ad esempio, la sicurezza del proprietario e dell'elenco di controllo di accesso discrezionale (DACL), utilizzare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="89735-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="89735-116">-oppure-</span><span class="sxs-lookup"><span data-stu-id="89735-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="89735-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del proprietario** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="89735-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="89735-118">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="89735-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="89735-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="89735-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="89735-120">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="89735-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="89735-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="89735-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="89735-122">Modificare l'elenco di controllo di accesso discrezionale (DACL) del file logico.</span><span class="sxs-lookup"><span data-stu-id="89735-122">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="89735-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="89735-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="89735-124">Modificare l'elenco di controllo di accesso di sistema (SACL) del file logico.</span><span class="sxs-lookup"><span data-stu-id="89735-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="89735-125">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="89735-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89735-126">Nome del file o della directory in cui il metodo **ChangeSecurityPermissionsEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="89735-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="89735-127">Questo parametro è null quando il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="89735-127">This parameter is null when the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="89735-128">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="89735-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="89735-129">Denomina il file o la directory figlio da utilizzare come punto di partenza per **ChangeSecurityPermissionsEx**.</span><span class="sxs-lookup"><span data-stu-id="89735-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="89735-130">In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="89735-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="89735-131">Se questo parametro è null, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="89735-131">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="89735-132">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="89735-132">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="89735-133">Se **true**, le modifiche di proprietà vengono applicate in modo ricorsivo a file e directory nella directory specificata dall'istanza di [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="89735-133">If **true**, the changes of ownership are applied recursively to files and directories in the directory that the [**CIM\_LogicalFile**](cim-logicalfile.md) instance specifies.</span></span> <span data-ttu-id="89735-134">Per le istanze di file, il parametro di input *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="89735-134">For file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89735-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89735-135">Return value</span></span>

<span data-ttu-id="89735-136">Restituisce un valore pari a 0 (zero) se le autorizzazioni vengono modificate e un numero diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="89735-136">Returns an value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="89735-137">**Success**</span><span class="sxs-lookup"><span data-stu-id="89735-137">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="89735-138">0</span><span class="sxs-lookup"><span data-stu-id="89735-138">0</span></span>

<span data-ttu-id="89735-139">La richiesta ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="89735-139">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="89735-140">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="89735-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="89735-141">2</span><span class="sxs-lookup"><span data-stu-id="89735-141">2</span></span>

<span data-ttu-id="89735-142">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="89735-142">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="89735-143">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="89735-143">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="89735-144">8</span><span class="sxs-lookup"><span data-stu-id="89735-144">8</span></span>

<span data-ttu-id="89735-145">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="89735-145">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="89735-146">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="89735-146">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="89735-147">9</span><span class="sxs-lookup"><span data-stu-id="89735-147">9</span></span>

<span data-ttu-id="89735-148">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="89735-148">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="89735-149">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="89735-149">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="89735-150">10</span><span class="sxs-lookup"><span data-stu-id="89735-150">10</span></span>

<span data-ttu-id="89735-151">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="89735-151">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="89735-152">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="89735-152">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="89735-153">11</span><span class="sxs-lookup"><span data-stu-id="89735-153">11</span></span>

<span data-ttu-id="89735-154">Il file system non è un file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="89735-154">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="89735-155">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="89735-155">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="89735-156">12</span><span class="sxs-lookup"><span data-stu-id="89735-156">12</span></span>

<span data-ttu-id="89735-157">La piattaforma non è Windows NT o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="89735-157">The platform is not Windows NT or Windows 2000.</span></span>

</dd> <dt>

<span data-ttu-id="89735-158">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="89735-158">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="89735-159">13</span><span class="sxs-lookup"><span data-stu-id="89735-159">13</span></span>

<span data-ttu-id="89735-160">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="89735-160">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="89735-161">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="89735-161">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="89735-162">14</span><span class="sxs-lookup"><span data-stu-id="89735-162">14</span></span>

<span data-ttu-id="89735-163">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="89735-163">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="89735-164">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="89735-164">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="89735-165">15</span><span class="sxs-lookup"><span data-stu-id="89735-165">15</span></span>

<span data-ttu-id="89735-166">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="89735-166">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="89735-167">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="89735-167">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="89735-168">16</span><span class="sxs-lookup"><span data-stu-id="89735-168">16</span></span>

<span data-ttu-id="89735-169">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="89735-169">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="89735-170">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="89735-170">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="89735-171">17</span><span class="sxs-lookup"><span data-stu-id="89735-171">17</span></span>

<span data-ttu-id="89735-172">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="89735-172">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="89735-173">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="89735-173">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="89735-174">21</span><span class="sxs-lookup"><span data-stu-id="89735-174">21</span></span>

<span data-ttu-id="89735-175">Un parametro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="89735-175">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89735-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89735-176">Requirements</span></span>



| <span data-ttu-id="89735-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="89735-177">Requirement</span></span> | <span data-ttu-id="89735-178">Valore</span><span class="sxs-lookup"><span data-stu-id="89735-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89735-179">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89735-179">Minimum supported client</span></span><br/> | <span data-ttu-id="89735-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89735-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89735-181">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89735-181">Minimum supported server</span></span><br/> | <span data-ttu-id="89735-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89735-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89735-183">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89735-183">Namespace</span></span><br/>                | <span data-ttu-id="89735-184">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="89735-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89735-185">MOF</span><span class="sxs-lookup"><span data-stu-id="89735-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89735-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89735-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89735-187">DLL</span><span class="sxs-lookup"><span data-stu-id="89735-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89735-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89735-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89735-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89735-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="89735-190">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="89735-190">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="89735-191">**Codecfile Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="89735-191">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

