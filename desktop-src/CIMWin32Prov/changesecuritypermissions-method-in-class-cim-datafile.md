---
description: Modifica le autorizzazioni di sicurezza per il file di dati logico specificato nel percorso dell'oggetto.
ms.assetid: b0a66411-f973-42ce-a3fe-25c31234a964
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissions della classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faa2e3ce2f2454d76ff9e55cc10cf09e9b5f715e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127122"
---
# <a name="changesecuritypermissions-method-of-the-cim_datafile-class"></a><span data-ttu-id="c8835-103">Metodo ChangeSecurityPermissions della classe del file di \_ DataFile CIM</span><span class="sxs-lookup"><span data-stu-id="c8835-103">ChangeSecurityPermissions method of the CIM\_DataFile class</span></span>

<span data-ttu-id="c8835-104">Il metodo **ChangeSecurityPermissions** modifica le autorizzazioni di sicurezza per il file di dati logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c8835-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical data file specified in the object path.</span></span> <span data-ttu-id="c8835-105">Se il file logico è una directory, questo metodo agirà in modo ricorsivo, modificando le autorizzazioni di sicurezza per tutti i file e le sottodirectory presenti nella directory.</span><span class="sxs-lookup"><span data-stu-id="c8835-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="c8835-106">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="c8835-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8835-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="c8835-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c8835-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c8835-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c8835-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c8835-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c8835-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c8835-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8835-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8835-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="c8835-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8835-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8835-113">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8835-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8835-114">Specifica le informazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c8835-114">Specifies the security information.</span></span>

> [!Note]  
> <span data-ttu-id="c8835-115">Un elenco di controllo di accesso (ACL) **null** nella struttura del [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede un accesso illimitato.</span><span class="sxs-lookup"><span data-stu-id="c8835-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span> <span data-ttu-id="c8835-116">Per informazioni sulle implicazioni dell'accesso illimitato, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="c8835-116">For information about the implications of unlimited access, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="c8835-117">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8835-117">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8835-118">Privilegi di sicurezza da modificare.</span><span class="sxs-lookup"><span data-stu-id="c8835-118">Security privilege to modify.</span></span> <span data-ttu-id="c8835-119">Per modificare, ad esempio, la sicurezza del proprietario e del DACL, usare:</span><span class="sxs-lookup"><span data-stu-id="c8835-119">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="c8835-120">oppure</span><span class="sxs-lookup"><span data-stu-id="c8835-120">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="c8835-121"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)</span><span class="sxs-lookup"><span data-stu-id="c8835-121"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c8835-122">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="c8835-122">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="c8835-123"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)</span><span class="sxs-lookup"><span data-stu-id="c8835-123"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c8835-124">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="c8835-124">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="c8835-125"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="c8835-125"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c8835-126">Modificare l'ACL del file logico.</span><span class="sxs-lookup"><span data-stu-id="c8835-126">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="c8835-127"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="c8835-127"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c8835-128">Modificare l'ACL di sistema del file logico.</span><span class="sxs-lookup"><span data-stu-id="c8835-128">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8835-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8835-129">Return value</span></span>

<span data-ttu-id="c8835-130">Restituisce un valore pari a 0 in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="c8835-130">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="c8835-131">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c8835-131">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c8835-132">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c8835-132">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c8835-133">**Success**</span><span class="sxs-lookup"><span data-stu-id="c8835-133">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c8835-134">0</span><span class="sxs-lookup"><span data-stu-id="c8835-134">0</span></span>

<span data-ttu-id="c8835-135">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c8835-135">Success.</span></span>

</dd> <dt>

<span data-ttu-id="c8835-136">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="c8835-136">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="c8835-137">2</span><span class="sxs-lookup"><span data-stu-id="c8835-137">2</span></span>

<span data-ttu-id="c8835-138">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="c8835-138">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="c8835-139">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="c8835-139">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="c8835-140">8</span><span class="sxs-lookup"><span data-stu-id="c8835-140">8</span></span>

<span data-ttu-id="c8835-141">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="c8835-141">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="c8835-142">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="c8835-142">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="c8835-143">9</span><span class="sxs-lookup"><span data-stu-id="c8835-143">9</span></span>

<span data-ttu-id="c8835-144">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="c8835-144">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="c8835-145">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="c8835-145">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="c8835-146">10</span><span class="sxs-lookup"><span data-stu-id="c8835-146">10</span></span>

<span data-ttu-id="c8835-147">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="c8835-147">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c8835-148">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="c8835-148">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="c8835-149">11</span><span class="sxs-lookup"><span data-stu-id="c8835-149">11</span></span>

</dd> <dt>

<span data-ttu-id="c8835-150">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="c8835-150">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="c8835-151">12</span><span class="sxs-lookup"><span data-stu-id="c8835-151">12</span></span>

<span data-ttu-id="c8835-152">Piattaforma non basata su Windows NT.</span><span class="sxs-lookup"><span data-stu-id="c8835-152">Platform not Windows NT-based.</span></span>

</dd> <dt>

<span data-ttu-id="c8835-153">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="c8835-153">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="c8835-154">13</span><span class="sxs-lookup"><span data-stu-id="c8835-154">13</span></span>

<span data-ttu-id="c8835-155">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="c8835-155">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c8835-156">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="c8835-156">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="c8835-157">14</span><span class="sxs-lookup"><span data-stu-id="c8835-157">14</span></span>

<span data-ttu-id="c8835-158">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="c8835-158">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c8835-159">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="c8835-159">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="c8835-160">15</span><span class="sxs-lookup"><span data-stu-id="c8835-160">15</span></span>

<span data-ttu-id="c8835-161">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="c8835-161">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c8835-162">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="c8835-162">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="c8835-163">16</span><span class="sxs-lookup"><span data-stu-id="c8835-163">16</span></span>

<span data-ttu-id="c8835-164">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="c8835-164">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="c8835-165">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="c8835-165">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="c8835-166">17</span><span class="sxs-lookup"><span data-stu-id="c8835-166">17</span></span>

<span data-ttu-id="c8835-167">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="c8835-167">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="c8835-168">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="c8835-168">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c8835-169">21</span><span class="sxs-lookup"><span data-stu-id="c8835-169">21</span></span>

<span data-ttu-id="c8835-170">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="c8835-170">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8835-171">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8835-171">Remarks</span></span>

<span data-ttu-id="c8835-172">Il metodo **ChangeSecurityPermissions** nel file di [**\_ DataFile CIM**](cim-datafile.md) viene implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="c8835-172">The **ChangeSecurityPermissions** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="c8835-173">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="c8835-173">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c8835-174">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c8835-174">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8835-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8835-175">Requirements</span></span>



| <span data-ttu-id="c8835-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8835-176">Requirement</span></span> | <span data-ttu-id="c8835-177">Valore</span><span class="sxs-lookup"><span data-stu-id="c8835-177">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8835-178">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8835-178">Minimum supported client</span></span><br/> | <span data-ttu-id="c8835-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8835-179">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8835-180">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8835-180">Minimum supported server</span></span><br/> | <span data-ttu-id="c8835-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8835-181">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8835-182">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c8835-182">Namespace</span></span><br/>                | <span data-ttu-id="c8835-183">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c8835-183">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c8835-184">MOF</span><span class="sxs-lookup"><span data-stu-id="c8835-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8835-185"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8835-185"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8835-186">DLL</span><span class="sxs-lookup"><span data-stu-id="c8835-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8835-187"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8835-187"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8835-188">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8835-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8835-189">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="c8835-189">**CIM\_DataFile**</span></span>](changesecuritypermissions-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="c8835-190">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="c8835-190">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="c8835-191">Attività WMI: file e cartelle</span><span class="sxs-lookup"><span data-stu-id="c8835-191">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="c8835-192">**Costanti dei diritti di accesso a file e directory**</span><span class="sxs-lookup"><span data-stu-id="c8835-192">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

