---
description: Modifica le autorizzazioni di sicurezza per il file del dispositivo specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo ChangeSecurityPermissions).
ms.assetid: 5ad54470-6961-4c0d-9d2a-d3eaf81d75f4
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissionsEx della classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f2c7261844542f6414052517432c2e8ff3f1194
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127090"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="60c96-103">Metodo ChangeSecurityPermissionsEx della classe CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="60c96-103">ChangeSecurityPermissionsEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="60c96-104">Il metodo **ChangeSecurityPermissionsEx** modifica le autorizzazioni di sicurezza per il file del dispositivo specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md) ).</span><span class="sxs-lookup"><span data-stu-id="60c96-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the device file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-devicefile.md) method).</span></span> <span data-ttu-id="60c96-105">Se il file logico è una directory, questo metodo agisce in modo ricorsivo, modificando le autorizzazioni di sicurezza per tutti i file e le sottodirectory contenute nella directory.</span><span class="sxs-lookup"><span data-stu-id="60c96-105">If the logical file is a directory, then this method acts recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="60c96-106">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="60c96-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60c96-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="60c96-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="60c96-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="60c96-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="60c96-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="60c96-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="60c96-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="60c96-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="60c96-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60c96-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="60c96-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="60c96-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60c96-113">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60c96-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60c96-114">Specifica le informazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="60c96-114">Specifies the security information.</span></span>

> [!Caution]  
> <span data-ttu-id="60c96-115">Un ACL **null** nella struttura [**del \_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede un accesso illimitato.</span><span class="sxs-lookup"><span data-stu-id="60c96-115">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="60c96-116">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60c96-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60c96-117">Privilegi di sicurezza da modificare.</span><span class="sxs-lookup"><span data-stu-id="60c96-117">Security privilege to modify.</span></span> <span data-ttu-id="60c96-118">Per modificare, ad esempio, la sicurezza del proprietario e del DACL, utilizzare</span><span class="sxs-lookup"><span data-stu-id="60c96-118">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="60c96-119">oppure</span><span class="sxs-lookup"><span data-stu-id="60c96-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="60c96-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)</span><span class="sxs-lookup"><span data-stu-id="60c96-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="60c96-121">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="60c96-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="60c96-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)</span><span class="sxs-lookup"><span data-stu-id="60c96-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="60c96-123">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="60c96-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="60c96-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="60c96-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="60c96-125">Modificare l'ACL del file logico.</span><span class="sxs-lookup"><span data-stu-id="60c96-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="60c96-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="60c96-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="60c96-127">Modificare l'ACL di sistema del file logico.</span><span class="sxs-lookup"><span data-stu-id="60c96-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="60c96-128">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="60c96-128">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60c96-129">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="60c96-129">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="60c96-130">Questo parametro è **null** se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="60c96-130">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="60c96-131">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="60c96-131">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="60c96-132">File figlio (o directory) da utilizzare come punto di partenza per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="60c96-132">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="60c96-133">In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="60c96-133">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="60c96-134">Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificati nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="60c96-134">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="60c96-135">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="60c96-135">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="60c96-136">Se è **true**, anche il metodo viene applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ DeviceFile**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="60c96-136">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="60c96-137">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="60c96-137">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60c96-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60c96-138">Return value</span></span>

<span data-ttu-id="60c96-139">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="60c96-139">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="60c96-140">0</span><span class="sxs-lookup"><span data-stu-id="60c96-140">0</span></span>

<span data-ttu-id="60c96-141">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="60c96-141">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60c96-142">2</span><span class="sxs-lookup"><span data-stu-id="60c96-142">2</span></span>

<span data-ttu-id="60c96-143">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="60c96-143">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60c96-144">8</span><span class="sxs-lookup"><span data-stu-id="60c96-144">8</span></span>

<span data-ttu-id="60c96-145">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="60c96-145">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60c96-146">9</span><span class="sxs-lookup"><span data-stu-id="60c96-146">9</span></span>

<span data-ttu-id="60c96-147">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="60c96-147">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60c96-148">10</span><span class="sxs-lookup"><span data-stu-id="60c96-148">10</span></span>

<span data-ttu-id="60c96-149">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="60c96-149">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60c96-150">11</span><span class="sxs-lookup"><span data-stu-id="60c96-150">11</span></span>

<span data-ttu-id="60c96-151">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="60c96-151">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60c96-152">12</span><span class="sxs-lookup"><span data-stu-id="60c96-152">12</span></span>

<span data-ttu-id="60c96-153">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="60c96-153">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60c96-154">13</span><span class="sxs-lookup"><span data-stu-id="60c96-154">13</span></span>

<span data-ttu-id="60c96-155">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="60c96-155">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60c96-156">14</span><span class="sxs-lookup"><span data-stu-id="60c96-156">14</span></span>

<span data-ttu-id="60c96-157">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="60c96-157">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60c96-158">15</span><span class="sxs-lookup"><span data-stu-id="60c96-158">15</span></span>

<span data-ttu-id="60c96-159">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="60c96-159">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60c96-160">16</span><span class="sxs-lookup"><span data-stu-id="60c96-160">16</span></span>

<span data-ttu-id="60c96-161">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="60c96-161">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60c96-162">17</span><span class="sxs-lookup"><span data-stu-id="60c96-162">17</span></span>

<span data-ttu-id="60c96-163">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="60c96-163">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60c96-164">21</span><span class="sxs-lookup"><span data-stu-id="60c96-164">21</span></span>

<span data-ttu-id="60c96-165">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="60c96-165">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60c96-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="60c96-166">Remarks</span></span>

<span data-ttu-id="60c96-167">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="60c96-167">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="60c96-168">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="60c96-168">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="60c96-169">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="60c96-169">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="60c96-170">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="60c96-170">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="60c96-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60c96-171">Requirements</span></span>



| <span data-ttu-id="60c96-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="60c96-172">Requirement</span></span> | <span data-ttu-id="60c96-173">Valore</span><span class="sxs-lookup"><span data-stu-id="60c96-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60c96-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60c96-174">Minimum supported client</span></span><br/> | <span data-ttu-id="60c96-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60c96-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60c96-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60c96-176">Minimum supported server</span></span><br/> | <span data-ttu-id="60c96-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60c96-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60c96-178">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="60c96-178">Namespace</span></span><br/>                | <span data-ttu-id="60c96-179">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="60c96-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60c96-180">MOF</span><span class="sxs-lookup"><span data-stu-id="60c96-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60c96-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60c96-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60c96-182">DLL</span><span class="sxs-lookup"><span data-stu-id="60c96-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60c96-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60c96-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60c96-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60c96-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60c96-185">\_DEVICEFILE CIM</span><span class="sxs-lookup"><span data-stu-id="60c96-185">CIM\_DeviceFile</span></span>](changesecuritypermissionsex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="60c96-186">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="60c96-186">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

