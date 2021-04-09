---
description: Modifica le autorizzazioni di sicurezza per il file di paging logico specificato nel percorso dell'oggetto. questo metodo è una versione estesa del metodo ChangeSecurityPermissions.
ms.assetid: a852a7e6-f26a-4bd9-bb15-e4cdd577697c
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissionsEx della classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a01a214e626f9c64ccf460eb3f8c031d1b45ff85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877681"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="6a74b-103">Metodo ChangeSecurityPermissionsEx della classe di \_ paging Win32</span><span class="sxs-lookup"><span data-stu-id="6a74b-103">ChangeSecurityPermissionsEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="6a74b-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** modifica le autorizzazioni di sicurezza per il file di paging logico specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="6a74b-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical paging file that is specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="6a74b-105">Se il file logico è una directory, questo metodo è ricorsivo e modifica le autorizzazioni di sicurezza di tutti i file e le sottodirectory in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="6a74b-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="6a74b-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="6a74b-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6a74b-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6a74b-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a74b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a74b-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="6a74b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a74b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a74b-110">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a74b-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-111">Espressione che viene risolta in un'istanza di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="6a74b-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="6a74b-112">Questo parametro contiene nuove autorizzazioni di sicurezza per l'istanza [**del \_ paging Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="6a74b-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-113">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a74b-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-114">Privilegio di sicurezza da modificare.</span><span class="sxs-lookup"><span data-stu-id="6a74b-114">Security privilege to be modified.</span></span> <span data-ttu-id="6a74b-115">Per modificare, ad esempio, la sicurezza del proprietario e dell'elenco di controllo di accesso discrezionale (DACL), utilizzare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="6a74b-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="6a74b-116">-oppure-</span><span class="sxs-lookup"><span data-stu-id="6a74b-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="6a74b-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)</span><span class="sxs-lookup"><span data-stu-id="6a74b-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6a74b-118">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="6a74b-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="6a74b-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)</span><span class="sxs-lookup"><span data-stu-id="6a74b-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6a74b-120">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="6a74b-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="6a74b-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="6a74b-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6a74b-122">Modificare l'elenco DACL del file logico.</span><span class="sxs-lookup"><span data-stu-id="6a74b-122">Change the DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="6a74b-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="6a74b-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6a74b-124">Modificare l'elenco di controllo di accesso di sistema (SACL) del file logico.</span><span class="sxs-lookup"><span data-stu-id="6a74b-124">Change the system access control (SACL) list of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6a74b-125">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6a74b-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-126">Nome del file o della directory in cui il metodo **ChangeSecurityPermissionsEx** non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6a74b-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="6a74b-127">Questo parametro è **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="6a74b-127">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-128">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6a74b-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-129">Denomina il file o la directory figlio da utilizzare come punto di partenza per **ChangeSecurityPermissionsEx**.</span><span class="sxs-lookup"><span data-stu-id="6a74b-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="6a74b-130">In genere, il parametro *StartFileName* è il parametro *StartFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="6a74b-130">Typically, the *StartFileName* parameter is the *StartFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="6a74b-131">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="6a74b-131">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-132">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6a74b-132">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-133">Se **true**, la modifica della proprietà viene applicata in modo ricorsivo a file e directory nella directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="6a74b-133">If **true**, the change of ownership is applied recursively to files and directories in the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="6a74b-134">Per le istanze di file, il parametro *ricorsivo* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="6a74b-134">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a74b-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a74b-135">Return value</span></span>

<span data-ttu-id="6a74b-136">Restituisce un valore pari a 0 (zero) se le autorizzazioni vengono modificate e un numero diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="6a74b-136">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="6a74b-137">**Success**</span><span class="sxs-lookup"><span data-stu-id="6a74b-137">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-138">0</span><span class="sxs-lookup"><span data-stu-id="6a74b-138">0</span></span>

<span data-ttu-id="6a74b-139">La richiesta ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="6a74b-139">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-140">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="6a74b-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-141">2</span><span class="sxs-lookup"><span data-stu-id="6a74b-141">2</span></span>

<span data-ttu-id="6a74b-142">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="6a74b-142">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-143">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="6a74b-143">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-144">8</span><span class="sxs-lookup"><span data-stu-id="6a74b-144">8</span></span>

<span data-ttu-id="6a74b-145">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="6a74b-145">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-146">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="6a74b-146">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-147">9</span><span class="sxs-lookup"><span data-stu-id="6a74b-147">9</span></span>

<span data-ttu-id="6a74b-148">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6a74b-148">The name specified is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-149">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="6a74b-149">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-150">10</span><span class="sxs-lookup"><span data-stu-id="6a74b-150">10</span></span>

<span data-ttu-id="6a74b-151">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="6a74b-151">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-152">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="6a74b-152">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-153">11</span><span class="sxs-lookup"><span data-stu-id="6a74b-153">11</span></span>

<span data-ttu-id="6a74b-154">Il file system non è un file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="6a74b-154">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-155">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="6a74b-155">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-156">12</span><span class="sxs-lookup"><span data-stu-id="6a74b-156">12</span></span>

<span data-ttu-id="6a74b-157">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="6a74b-157">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-158">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="6a74b-158">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-159">13</span><span class="sxs-lookup"><span data-stu-id="6a74b-159">13</span></span>

<span data-ttu-id="6a74b-160">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="6a74b-160">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-161">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="6a74b-161">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-162">14</span><span class="sxs-lookup"><span data-stu-id="6a74b-162">14</span></span>

<span data-ttu-id="6a74b-163">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="6a74b-163">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-164">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="6a74b-164">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-165">15</span><span class="sxs-lookup"><span data-stu-id="6a74b-165">15</span></span>

<span data-ttu-id="6a74b-166">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="6a74b-166">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-167">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="6a74b-167">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-168">16</span><span class="sxs-lookup"><span data-stu-id="6a74b-168">16</span></span>

<span data-ttu-id="6a74b-169">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6a74b-169">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-170">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="6a74b-170">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-171">17</span><span class="sxs-lookup"><span data-stu-id="6a74b-171">17</span></span>

<span data-ttu-id="6a74b-172">Un privilegio necessario per l'operazione è mancante.</span><span class="sxs-lookup"><span data-stu-id="6a74b-172">A privilege required for the operation is missing.</span></span>

</dd> <dt>

<span data-ttu-id="6a74b-173">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="6a74b-173">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6a74b-174">21</span><span class="sxs-lookup"><span data-stu-id="6a74b-174">21</span></span>

<span data-ttu-id="6a74b-175">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="6a74b-175">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a74b-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a74b-176">Requirements</span></span>



| <span data-ttu-id="6a74b-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a74b-177">Requirement</span></span> | <span data-ttu-id="6a74b-178">Valore</span><span class="sxs-lookup"><span data-stu-id="6a74b-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a74b-179">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a74b-179">Minimum supported client</span></span><br/> | <span data-ttu-id="6a74b-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a74b-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a74b-181">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a74b-181">Minimum supported server</span></span><br/> | <span data-ttu-id="6a74b-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a74b-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a74b-183">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6a74b-183">Namespace</span></span><br/>                | <span data-ttu-id="6a74b-184">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6a74b-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a74b-185">MOF</span><span class="sxs-lookup"><span data-stu-id="6a74b-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a74b-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a74b-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a74b-187">DLL</span><span class="sxs-lookup"><span data-stu-id="6a74b-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a74b-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a74b-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a74b-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a74b-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="6a74b-190">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a74b-190">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6a74b-191">**\_Pagefile Win32**</span><span class="sxs-lookup"><span data-stu-id="6a74b-191">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

