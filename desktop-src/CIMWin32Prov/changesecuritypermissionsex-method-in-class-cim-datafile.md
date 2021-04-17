---
description: Modifica le autorizzazioni di sicurezza per il file di dati logico specificato nel percorso dell'oggetto. questo metodo è una versione estesa del metodo ChangeSecurityPermissions.
ms.assetid: baf50a6e-f624-464e-946d-975aeba88ac2
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissionsEx della classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c97f9b17fd148a0686a96fb46f77694a2b78b21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523794"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_datafile-class"></a><span data-ttu-id="fd558-103">Metodo ChangeSecurityPermissionsEx della classe del file di \_ DataFile CIM</span><span class="sxs-lookup"><span data-stu-id="fd558-103">ChangeSecurityPermissionsEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="fd558-104">Il metodo **ChangeSecurityPermissionsEx** modifica le autorizzazioni di sicurezza per il file di dati logico specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md) ).</span><span class="sxs-lookup"><span data-stu-id="fd558-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical data file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md) method).</span></span> <span data-ttu-id="fd558-105">Se il file logico è effettivamente una directory, questo metodo agirà in modo ricorsivo, modificando le autorizzazioni di sicurezza per tutti i file e le sottodirectory contenute nella directory.</span><span class="sxs-lookup"><span data-stu-id="fd558-105">If the logical file is actually a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd558-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="fd558-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fd558-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fd558-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fd558-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="fd558-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fd558-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fd558-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd558-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd558-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="fd558-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd558-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd558-112">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd558-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd558-113">Specifica le informazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fd558-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="fd558-114">Un ACL **null** nella struttura [**del \_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede un accesso illimitato.</span><span class="sxs-lookup"><span data-stu-id="fd558-114">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span> <span data-ttu-id="fd558-115">Per ulteriori informazioni sulle implicazioni dell'accesso illimitato, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="fd558-115">For more information about the implications of unlimited access, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="fd558-116">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd558-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd558-117">Privilegi di sicurezza da modificare.</span><span class="sxs-lookup"><span data-stu-id="fd558-117">Security privilege to modify.</span></span> <span data-ttu-id="fd558-118">Per modificare, ad esempio, la sicurezza del proprietario e del DACL, usare:</span><span class="sxs-lookup"><span data-stu-id="fd558-118">For example, to change the owner and DACL security, use:</span></span>

<span data-ttu-id="fd558-119">`Option = 1 + 4` o `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`</span><span class="sxs-lookup"><span data-stu-id="fd558-119">`Option = 1 + 4` or `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`</span></span>

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="fd558-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)</span><span class="sxs-lookup"><span data-stu-id="fd558-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fd558-121">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="fd558-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="fd558-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)</span><span class="sxs-lookup"><span data-stu-id="fd558-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fd558-123">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="fd558-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="fd558-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="fd558-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fd558-125">Modificare l'ACL del file logico.</span><span class="sxs-lookup"><span data-stu-id="fd558-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="fd558-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="fd558-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="fd558-127">Modificare l'ACL di sistema del file logico.</span><span class="sxs-lookup"><span data-stu-id="fd558-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fd558-128">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fd558-128">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd558-129">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="fd558-129">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="fd558-130">Questo parametro è **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="fd558-130">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="fd558-131">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="fd558-131">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fd558-132">Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="fd558-132">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="fd558-133">In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="fd558-133">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="fd558-134">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificati nella chiamata **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="fd558-134">If this parameter is **null**, the operation is performed on the file (or directory) specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="fd558-135">Se si usa *StartFileName* , è necessario impostare *ricorsivo* su true.</span><span class="sxs-lookup"><span data-stu-id="fd558-135">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="fd558-136">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="fd558-136">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fd558-137">Se **true**, il metodo viene anche applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza di [**\_ DataFile DataFile**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="fd558-137">If **True**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="fd558-138">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="fd558-138">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd558-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd558-139">Return value</span></span>

<span data-ttu-id="fd558-140">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="fd558-140">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="fd558-141">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="fd558-141">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="fd558-142">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="fd558-142">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="fd558-143">**Success**</span><span class="sxs-lookup"><span data-stu-id="fd558-143">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="fd558-144">0</span><span class="sxs-lookup"><span data-stu-id="fd558-144">0</span></span>

<span data-ttu-id="fd558-145">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="fd558-145">Success.</span></span>

</dd> <dt>

<span data-ttu-id="fd558-146">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="fd558-146">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="fd558-147">2</span><span class="sxs-lookup"><span data-stu-id="fd558-147">2</span></span>

<span data-ttu-id="fd558-148">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="fd558-148">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="fd558-149">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="fd558-149">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="fd558-150">8</span><span class="sxs-lookup"><span data-stu-id="fd558-150">8</span></span>

<span data-ttu-id="fd558-151">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="fd558-151">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="fd558-152">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="fd558-152">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="fd558-153">9</span><span class="sxs-lookup"><span data-stu-id="fd558-153">9</span></span>

<span data-ttu-id="fd558-154">Il nome di oggetto specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="fd558-154">Object name specified is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="fd558-155">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="fd558-155">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="fd558-156">10</span><span class="sxs-lookup"><span data-stu-id="fd558-156">10</span></span>

<span data-ttu-id="fd558-157">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="fd558-157">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="fd558-158">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="fd558-158">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="fd558-159">11</span><span class="sxs-lookup"><span data-stu-id="fd558-159">11</span></span>

<span data-ttu-id="fd558-160">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="fd558-160">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="fd558-161">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="fd558-161">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="fd558-162">12</span><span class="sxs-lookup"><span data-stu-id="fd558-162">12</span></span>

<span data-ttu-id="fd558-163">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="fd558-163">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="fd558-164">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="fd558-164">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="fd558-165">13</span><span class="sxs-lookup"><span data-stu-id="fd558-165">13</span></span>

<span data-ttu-id="fd558-166">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="fd558-166">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="fd558-167">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="fd558-167">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="fd558-168">14</span><span class="sxs-lookup"><span data-stu-id="fd558-168">14</span></span>

<span data-ttu-id="fd558-169">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="fd558-169">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="fd558-170">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="fd558-170">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="fd558-171">15</span><span class="sxs-lookup"><span data-stu-id="fd558-171">15</span></span>

<span data-ttu-id="fd558-172">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="fd558-172">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="fd558-173">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="fd558-173">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="fd558-174">16</span><span class="sxs-lookup"><span data-stu-id="fd558-174">16</span></span>

<span data-ttu-id="fd558-175">Il file di avvio non è valido.</span><span class="sxs-lookup"><span data-stu-id="fd558-175">The start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="fd558-176">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="fd558-176">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="fd558-177">17</span><span class="sxs-lookup"><span data-stu-id="fd558-177">17</span></span>

<span data-ttu-id="fd558-178">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="fd558-178">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="fd558-179">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="fd558-179">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fd558-180">21</span><span class="sxs-lookup"><span data-stu-id="fd558-180">21</span></span>

<span data-ttu-id="fd558-181">Un parametro non è valido.</span><span class="sxs-lookup"><span data-stu-id="fd558-181">A parameter is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd558-182">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd558-182">Remarks</span></span>

<span data-ttu-id="fd558-183">Il metodo **ChangeSecurityPermissionsEx** nel file di [**\_ DataFile CIM**](cim-datafile.md) viene implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="fd558-183">The **ChangeSecurityPermissionsEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="fd558-184">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="fd558-184">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fd558-185">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="fd558-185">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd558-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd558-186">Requirements</span></span>



| <span data-ttu-id="fd558-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd558-187">Requirement</span></span> | <span data-ttu-id="fd558-188">Valore</span><span class="sxs-lookup"><span data-stu-id="fd558-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd558-189">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd558-189">Minimum supported client</span></span><br/> | <span data-ttu-id="fd558-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd558-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd558-191">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd558-191">Minimum supported server</span></span><br/> | <span data-ttu-id="fd558-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd558-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd558-193">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fd558-193">Namespace</span></span><br/>                | <span data-ttu-id="fd558-194">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fd558-194">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fd558-195">MOF</span><span class="sxs-lookup"><span data-stu-id="fd558-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd558-196"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd558-196"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd558-197">DLL</span><span class="sxs-lookup"><span data-stu-id="fd558-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd558-198"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd558-198"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd558-199">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd558-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd558-200">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="fd558-200">**CIM\_DataFile**</span></span>](changesecuritypermissionsex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="fd558-201">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="fd558-201">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="fd558-202">Attività WMI: file e cartelle</span><span class="sxs-lookup"><span data-stu-id="fd558-202">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="fd558-203">**Costanti dei diritti di accesso a file e directory**</span><span class="sxs-lookup"><span data-stu-id="fd558-203">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

