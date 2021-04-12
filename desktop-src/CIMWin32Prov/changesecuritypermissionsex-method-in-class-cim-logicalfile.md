---
description: Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto. questo metodo è una versione estesa del metodo ChangeSecurityPermissions.
ms.assetid: 29155533-0898-4f8f-af08-f3ea46c8c1d3
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissionsEx della classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af2dc82ef54b6f32eee20f17cd61c0769cc64b1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523513"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="2f2d4-103">Metodo ChangeSecurityPermissionsEx della classe CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="2f2d4-103">ChangeSecurityPermissionsEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="2f2d4-104">Il metodo **ChangeSecurityPermissionsEx** modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md) ).</span><span class="sxs-lookup"><span data-stu-id="2f2d4-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md) method).</span></span> <span data-ttu-id="2f2d4-105">Se il file logico è una directory, questo metodo agirà in modo ricorsivo, modificando le autorizzazioni di sicurezza per tutti i file e le sottodirectory presenti nella directory.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f2d4-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2f2d4-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2f2d4-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2f2d4-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="2f2d4-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2f2d4-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2f2d4-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f2d4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f2d4-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="2f2d4-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f2d4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f2d4-112">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f2d4-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-113">Specifica le informazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-113">Specifies the security information.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-114">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f2d4-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-115">Privilegi di sicurezza da modificare.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-115">Security privilege to modify.</span></span> <span data-ttu-id="2f2d4-116">Per modificare, ad esempio, la sicurezza del proprietario e del DACL, utilizzare</span><span class="sxs-lookup"><span data-stu-id="2f2d4-116">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="2f2d4-117">oppure</span><span class="sxs-lookup"><span data-stu-id="2f2d4-117">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span data-ttu-id="2f2d4-118"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)</span><span class="sxs-lookup"><span data-stu-id="2f2d4-118"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Change\_Owner\_Security\_Information** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2f2d4-119">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span data-ttu-id="2f2d4-120"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)</span><span class="sxs-lookup"><span data-stu-id="2f2d4-120"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Change\_Group\_Security\_Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2f2d4-121">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="2f2d4-122"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="2f2d4-122"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Change\_Dacl\_Security\_Information** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2f2d4-123">Modificare l'ACL del file logico.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-123">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="2f2d4-124"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="2f2d4-124"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Change\_Sacl\_Security\_Information** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2f2d4-125">Modificare l'ACL di sistema del file logico.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-125">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2f2d4-126">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2f2d4-126">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-127">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-127">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="2f2d4-128">Se il metodo ha esito positivo, il valore di questo parametro è **null** .</span><span class="sxs-lookup"><span data-stu-id="2f2d4-128">This parameter has a value of **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-129">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2f2d4-129">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-130">Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-130">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="2f2d4-131">In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-131">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="2f2d4-132">Se il valore del parametro è **null**, l'operazione viene eseguita nel file o nella directory specificata nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="2f2d4-132">If the parameter value is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-133">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2f2d4-133">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-134">Se **true**, le autorizzazioni di sicurezza vengono applicate in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="2f2d4-134">If **TRUE**, the security permissions are applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="2f2d4-135">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-135">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f2d4-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f2d4-136">Return value</span></span>

<span data-ttu-id="2f2d4-137">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-137">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="2f2d4-138">**Success**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-138">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-139">0</span><span class="sxs-lookup"><span data-stu-id="2f2d4-139">0</span></span>

<span data-ttu-id="2f2d4-140">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-140">Success.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-141">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-141">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-142">2</span><span class="sxs-lookup"><span data-stu-id="2f2d4-142">2</span></span>

<span data-ttu-id="2f2d4-143">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-143">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-144">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-144">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-145">8</span><span class="sxs-lookup"><span data-stu-id="2f2d4-145">8</span></span>

<span data-ttu-id="2f2d4-146">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-146">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-147">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-147">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-148">9</span><span class="sxs-lookup"><span data-stu-id="2f2d4-148">9</span></span>

<span data-ttu-id="2f2d4-149">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-149">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-150">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-150">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-151">10</span><span class="sxs-lookup"><span data-stu-id="2f2d4-151">10</span></span>

<span data-ttu-id="2f2d4-152">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-152">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-153">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-153">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-154">11</span><span class="sxs-lookup"><span data-stu-id="2f2d4-154">11</span></span>

<span data-ttu-id="2f2d4-155">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-155">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-156">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-156">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-157">12</span><span class="sxs-lookup"><span data-stu-id="2f2d4-157">12</span></span>

<span data-ttu-id="2f2d4-158">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-158">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-159">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-159">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-160">13</span><span class="sxs-lookup"><span data-stu-id="2f2d4-160">13</span></span>

<span data-ttu-id="2f2d4-161">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-161">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-162">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-162">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-163">14</span><span class="sxs-lookup"><span data-stu-id="2f2d4-163">14</span></span>

<span data-ttu-id="2f2d4-164">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-164">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-165">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-165">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-166">15</span><span class="sxs-lookup"><span data-stu-id="2f2d4-166">15</span></span>

<span data-ttu-id="2f2d4-167">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-167">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-168">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-168">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-169">16</span><span class="sxs-lookup"><span data-stu-id="2f2d4-169">16</span></span>

<span data-ttu-id="2f2d4-170">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-170">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-171">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-171">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-172">17</span><span class="sxs-lookup"><span data-stu-id="2f2d4-172">17</span></span>

<span data-ttu-id="2f2d4-173">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-173">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="2f2d4-174">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-174">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2f2d4-175">21</span><span class="sxs-lookup"><span data-stu-id="2f2d4-175">21</span></span>

<span data-ttu-id="2f2d4-176">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-176">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f2d4-177">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f2d4-177">Remarks</span></span>

<span data-ttu-id="2f2d4-178">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-178">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="2f2d4-179">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="2f2d4-179">To use this method, you must implement it in your own provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f2d4-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f2d4-180">Requirements</span></span>



| <span data-ttu-id="2f2d4-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f2d4-181">Requirement</span></span> | <span data-ttu-id="2f2d4-182">Valore</span><span class="sxs-lookup"><span data-stu-id="2f2d4-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f2d4-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f2d4-183">Minimum supported client</span></span><br/> | <span data-ttu-id="2f2d4-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f2d4-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f2d4-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f2d4-185">Minimum supported server</span></span><br/> | <span data-ttu-id="2f2d4-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f2d4-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f2d4-187">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2f2d4-187">Namespace</span></span><br/>                | <span data-ttu-id="2f2d4-188">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2f2d4-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2f2d4-189">MOF</span><span class="sxs-lookup"><span data-stu-id="2f2d4-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f2d4-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f2d4-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f2d4-191">DLL</span><span class="sxs-lookup"><span data-stu-id="2f2d4-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f2d4-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f2d4-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f2d4-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f2d4-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f2d4-194">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-194">**CIM\_LogicalFile**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="2f2d4-195">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="2f2d4-195">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

