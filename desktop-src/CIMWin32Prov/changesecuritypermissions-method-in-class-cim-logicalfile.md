---
description: Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.
ms.assetid: a3caa717-ad37-4e4f-9f4e-f37aed382fa4
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissions della classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 929e05047af203d8e2344afa8175228e3bd969fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305046"
---
# <a name="changesecuritypermissions-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="14977-103">Metodo ChangeSecurityPermissions della classe CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="14977-103">ChangeSecurityPermissions method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="14977-104">Il metodo **ChangeSecurityPermissions** modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="14977-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="14977-105">Se il file logico è una directory, **ChangeSecurityPermissions** agirà in modo ricorsivo, modificando le autorizzazioni di sicurezza per tutti i file e le sottodirectory contenute nella directory.</span><span class="sxs-lookup"><span data-stu-id="14977-105">If the logical file is a directory, then **ChangeSecurityPermissions** will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14977-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="14977-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="14977-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="14977-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="14977-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="14977-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="14977-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="14977-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="14977-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14977-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="14977-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="14977-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14977-112">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14977-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14977-113">Specifica le informazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="14977-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="14977-114">Un  elenco di controllo di accesso (ACL) null [**nel \_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede un accesso illimitato.</span><span class="sxs-lookup"><span data-stu-id="14977-114">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="14977-115">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14977-115">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14977-116">Privilegi di sicurezza da modificare.</span><span class="sxs-lookup"><span data-stu-id="14977-116">Security privilege to modify.</span></span> <span data-ttu-id="14977-117">Per modificare, ad esempio, la sicurezza del proprietario e del DACL, usare:</span><span class="sxs-lookup"><span data-stu-id="14977-117">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="14977-118">oppure</span><span class="sxs-lookup"><span data-stu-id="14977-118">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span data-ttu-id="14977-119"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)</span><span class="sxs-lookup"><span data-stu-id="14977-119"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Change\_Owner\_Security\_Information** (1)</span></span>


</dt> <dd>

<span data-ttu-id="14977-120">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="14977-120">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span data-ttu-id="14977-121"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)</span><span class="sxs-lookup"><span data-stu-id="14977-121"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Change\_Group\_Security\_Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="14977-122">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="14977-122">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="14977-123"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="14977-123"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Change\_Dacl\_Security\_Information** (4)</span></span>


</dt> <dd>

<span data-ttu-id="14977-124">Modificare l'ACL del file logico.</span><span class="sxs-lookup"><span data-stu-id="14977-124">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="14977-125"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="14977-125"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Change\_Sacl\_Security\_Information** (8)</span></span>


</dt> <dd>

<span data-ttu-id="14977-126">Modificare l'ACL di sistema del file logico.</span><span class="sxs-lookup"><span data-stu-id="14977-126">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14977-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14977-127">Return value</span></span>

<span data-ttu-id="14977-128">Restituisce un valore pari a 0 in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="14977-128">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="14977-129">**Success**</span><span class="sxs-lookup"><span data-stu-id="14977-129">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="14977-130">0</span><span class="sxs-lookup"><span data-stu-id="14977-130">0</span></span>

<span data-ttu-id="14977-131">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="14977-131">Success.</span></span>

</dd> <dt>

<span data-ttu-id="14977-132">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="14977-132">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="14977-133">2</span><span class="sxs-lookup"><span data-stu-id="14977-133">2</span></span>

<span data-ttu-id="14977-134">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="14977-134">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="14977-135">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="14977-135">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="14977-136">8</span><span class="sxs-lookup"><span data-stu-id="14977-136">8</span></span>

<span data-ttu-id="14977-137">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="14977-137">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="14977-138">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="14977-138">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="14977-139">9</span><span class="sxs-lookup"><span data-stu-id="14977-139">9</span></span>

<span data-ttu-id="14977-140">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="14977-140">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="14977-141">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="14977-141">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="14977-142">10</span><span class="sxs-lookup"><span data-stu-id="14977-142">10</span></span>

<span data-ttu-id="14977-143">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="14977-143">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="14977-144">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="14977-144">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="14977-145">11</span><span class="sxs-lookup"><span data-stu-id="14977-145">11</span></span>

<span data-ttu-id="14977-146">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="14977-146">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="14977-147">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="14977-147">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="14977-148">12</span><span class="sxs-lookup"><span data-stu-id="14977-148">12</span></span>

<span data-ttu-id="14977-149">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="14977-149">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="14977-150">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="14977-150">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="14977-151">13</span><span class="sxs-lookup"><span data-stu-id="14977-151">13</span></span>

<span data-ttu-id="14977-152">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="14977-152">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="14977-153">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="14977-153">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="14977-154">14</span><span class="sxs-lookup"><span data-stu-id="14977-154">14</span></span>

<span data-ttu-id="14977-155">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="14977-155">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="14977-156">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="14977-156">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="14977-157">15</span><span class="sxs-lookup"><span data-stu-id="14977-157">15</span></span>

<span data-ttu-id="14977-158">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="14977-158">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="14977-159">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="14977-159">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="14977-160">16</span><span class="sxs-lookup"><span data-stu-id="14977-160">16</span></span>

<span data-ttu-id="14977-161">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="14977-161">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="14977-162">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="14977-162">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="14977-163">17</span><span class="sxs-lookup"><span data-stu-id="14977-163">17</span></span>

<span data-ttu-id="14977-164">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="14977-164">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="14977-165">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="14977-165">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="14977-166">21</span><span class="sxs-lookup"><span data-stu-id="14977-166">21</span></span>

<span data-ttu-id="14977-167">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="14977-167">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14977-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="14977-168">Remarks</span></span>

<span data-ttu-id="14977-169">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="14977-169">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="14977-170">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="14977-170">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="14977-171">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="14977-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="14977-172">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="14977-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="14977-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14977-173">Requirements</span></span>



| <span data-ttu-id="14977-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="14977-174">Requirement</span></span> | <span data-ttu-id="14977-175">Valore</span><span class="sxs-lookup"><span data-stu-id="14977-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14977-176">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14977-176">Minimum supported client</span></span><br/> | <span data-ttu-id="14977-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14977-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="14977-178">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14977-178">Minimum supported server</span></span><br/> | <span data-ttu-id="14977-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14977-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="14977-180">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="14977-180">Namespace</span></span><br/>                | <span data-ttu-id="14977-181">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="14977-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="14977-182">MOF</span><span class="sxs-lookup"><span data-stu-id="14977-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14977-183"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14977-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="14977-184">DLL</span><span class="sxs-lookup"><span data-stu-id="14977-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14977-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14977-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14977-186">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14977-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14977-187">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="14977-187">**CIM\_LogicalFile**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="14977-188">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="14977-188">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

