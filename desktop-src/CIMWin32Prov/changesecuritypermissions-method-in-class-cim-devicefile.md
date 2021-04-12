---
description: Modifica le autorizzazioni di sicurezza per il file di dispositivo logico specificato nel percorso dell'oggetto.
ms.assetid: 4b3e1a0e-3c9e-45bb-8c7b-cbbc8f9d1265
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissions della classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a772c17695a537e4a9a8518bf05b052c0417f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483557"
---
# <a name="changesecuritypermissions-method-of-the-cim_devicefile-class"></a><span data-ttu-id="31cb6-103">Metodo ChangeSecurityPermissions della classe CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="31cb6-103">ChangeSecurityPermissions method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="31cb6-104">Il metodo **ChangeSecurityPermissions** modifica le autorizzazioni di sicurezza per il file di dispositivo logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="31cb6-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical device file specified in the object path.</span></span> <span data-ttu-id="31cb6-105">Se il file logico è una directory, questo metodo agirà in modo ricorsivo, modificando le autorizzazioni di sicurezza per tutti i file e le sottodirectory presenti nella directory.</span><span class="sxs-lookup"><span data-stu-id="31cb6-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="31cb6-106">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="31cb6-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31cb6-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="31cb6-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="31cb6-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="31cb6-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="31cb6-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="31cb6-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="31cb6-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="31cb6-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="31cb6-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31cb6-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="31cb6-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="31cb6-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31cb6-113">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31cb6-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-114">Specifica le informazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="31cb6-114">Specifies the security information.</span></span>

> [!Caution]  
> <span data-ttu-id="31cb6-115">Un elenco di controllo di accesso (ACL) **null** nella struttura del [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede un accesso illimitato.</span><span class="sxs-lookup"><span data-stu-id="31cb6-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="31cb6-116">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31cb6-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-117">Privilegi di sicurezza da modificare.</span><span class="sxs-lookup"><span data-stu-id="31cb6-117">Security privilege to modify.</span></span> <span data-ttu-id="31cb6-118">Per modificare, ad esempio, la sicurezza del proprietario e del DACL, usare:</span><span class="sxs-lookup"><span data-stu-id="31cb6-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="31cb6-119">oppure</span><span class="sxs-lookup"><span data-stu-id="31cb6-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="31cb6-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)</span><span class="sxs-lookup"><span data-stu-id="31cb6-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="31cb6-121">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="31cb6-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="31cb6-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)</span><span class="sxs-lookup"><span data-stu-id="31cb6-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="31cb6-123">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="31cb6-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="31cb6-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="31cb6-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="31cb6-125">Modificare l'ACL del file logico.</span><span class="sxs-lookup"><span data-stu-id="31cb6-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="31cb6-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="31cb6-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="31cb6-127">Modificare l'ACL di sistema del file logico.</span><span class="sxs-lookup"><span data-stu-id="31cb6-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31cb6-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31cb6-128">Return value</span></span>

<span data-ttu-id="31cb6-129">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="31cb6-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="31cb6-130">**Success**</span><span class="sxs-lookup"><span data-stu-id="31cb6-130">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-131">0</span><span class="sxs-lookup"><span data-stu-id="31cb6-131">0</span></span>

<span data-ttu-id="31cb6-132">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="31cb6-132">Success.</span></span>

</dd> <dt>

<span data-ttu-id="31cb6-133">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="31cb6-133">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-134">2</span><span class="sxs-lookup"><span data-stu-id="31cb6-134">2</span></span>

<span data-ttu-id="31cb6-135">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="31cb6-135">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="31cb6-136">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="31cb6-136">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-137">8</span><span class="sxs-lookup"><span data-stu-id="31cb6-137">8</span></span>

<span data-ttu-id="31cb6-138">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="31cb6-138">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="31cb6-139">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="31cb6-139">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-140">9</span><span class="sxs-lookup"><span data-stu-id="31cb6-140">9</span></span>

<span data-ttu-id="31cb6-141">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="31cb6-141">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="31cb6-142">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="31cb6-142">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-143">10</span><span class="sxs-lookup"><span data-stu-id="31cb6-143">10</span></span>

<span data-ttu-id="31cb6-144">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="31cb6-144">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="31cb6-145">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="31cb6-145">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-146">11</span><span class="sxs-lookup"><span data-stu-id="31cb6-146">11</span></span>

<span data-ttu-id="31cb6-147">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="31cb6-147">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="31cb6-148">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="31cb6-148">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-149">12</span><span class="sxs-lookup"><span data-stu-id="31cb6-149">12</span></span>

<span data-ttu-id="31cb6-150">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="31cb6-150">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="31cb6-151">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="31cb6-151">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-152">13</span><span class="sxs-lookup"><span data-stu-id="31cb6-152">13</span></span>

<span data-ttu-id="31cb6-153">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="31cb6-153">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="31cb6-154">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="31cb6-154">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-155">14</span><span class="sxs-lookup"><span data-stu-id="31cb6-155">14</span></span>

<span data-ttu-id="31cb6-156">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="31cb6-156">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="31cb6-157">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="31cb6-157">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-158">15</span><span class="sxs-lookup"><span data-stu-id="31cb6-158">15</span></span>

<span data-ttu-id="31cb6-159">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="31cb6-159">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="31cb6-160">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="31cb6-160">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-161">16</span><span class="sxs-lookup"><span data-stu-id="31cb6-161">16</span></span>

<span data-ttu-id="31cb6-162">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="31cb6-162">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="31cb6-163">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="31cb6-163">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-164">17</span><span class="sxs-lookup"><span data-stu-id="31cb6-164">17</span></span>

<span data-ttu-id="31cb6-165">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="31cb6-165">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="31cb6-166">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="31cb6-166">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="31cb6-167">21</span><span class="sxs-lookup"><span data-stu-id="31cb6-167">21</span></span>

<span data-ttu-id="31cb6-168">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="31cb6-168">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31cb6-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="31cb6-169">Remarks</span></span>

<span data-ttu-id="31cb6-170">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="31cb6-170">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="31cb6-171">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="31cb6-171">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="31cb6-172">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="31cb6-172">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="31cb6-173">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="31cb6-173">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="31cb6-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31cb6-174">Requirements</span></span>



| <span data-ttu-id="31cb6-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="31cb6-175">Requirement</span></span> | <span data-ttu-id="31cb6-176">Valore</span><span class="sxs-lookup"><span data-stu-id="31cb6-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31cb6-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31cb6-177">Minimum supported client</span></span><br/> | <span data-ttu-id="31cb6-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31cb6-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31cb6-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31cb6-179">Minimum supported server</span></span><br/> | <span data-ttu-id="31cb6-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31cb6-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31cb6-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="31cb6-181">Namespace</span></span><br/>                | <span data-ttu-id="31cb6-182">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="31cb6-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="31cb6-183">MOF</span><span class="sxs-lookup"><span data-stu-id="31cb6-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31cb6-184"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31cb6-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="31cb6-185">DLL</span><span class="sxs-lookup"><span data-stu-id="31cb6-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31cb6-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31cb6-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31cb6-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31cb6-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31cb6-188">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="31cb6-188">**CIM\_DeviceFile**</span></span>](changesecuritypermissions-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="31cb6-189">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="31cb6-189">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

