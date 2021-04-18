---
description: Modifica le autorizzazioni di sicurezza per il file di voce della directory logica specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo ChangeSecurityPermissions e viene ereditato da CIM \_ LogicalFile).
ms.assetid: 5c1f66ba-9aa1-47ca-8fcf-7663782544cd
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissionsEx della classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2d8ddf4c6ffdbd016db1e8c08d89f2dd6476ccf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304786"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_directory-class"></a><span data-ttu-id="300ae-103">Metodo ChangeSecurityPermissionsEx della classe di \_ directory CIM</span><span class="sxs-lookup"><span data-stu-id="300ae-103">ChangeSecurityPermissionsEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="300ae-104">Il metodo **ChangeSecurityPermissionsEx** modifica le autorizzazioni di sicurezza per il file di voce della directory logica specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md) ed è ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md)).</span><span class="sxs-lookup"><span data-stu-id="300ae-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical directory entry file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md)).</span></span> <span data-ttu-id="300ae-105">Se il file logico è una directory, questo metodo agirà in modo ricorsivo, modificando le autorizzazioni di sicurezza per tutti i file e le sottodirectory presenti nella directory.</span><span class="sxs-lookup"><span data-stu-id="300ae-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="300ae-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="300ae-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="300ae-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="300ae-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="300ae-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="300ae-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="300ae-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="300ae-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="300ae-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="300ae-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="300ae-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="300ae-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="300ae-112">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="300ae-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="300ae-113">Specifica le informazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="300ae-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="300ae-114">Un ACL **null** nella struttura [**del \_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede un accesso illimitato.</span><span class="sxs-lookup"><span data-stu-id="300ae-114">A **NULL** ACL in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="300ae-115">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="300ae-115">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="300ae-116">Privilegi di sicurezza da modificare.</span><span class="sxs-lookup"><span data-stu-id="300ae-116">Security privilege to modify.</span></span> <span data-ttu-id="300ae-117">Per modificare, ad esempio, la sicurezza del proprietario e del DACL, utilizzare</span><span class="sxs-lookup"><span data-stu-id="300ae-117">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="300ae-118">oppure</span><span class="sxs-lookup"><span data-stu-id="300ae-118">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="300ae-119"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)</span><span class="sxs-lookup"><span data-stu-id="300ae-119"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="300ae-120">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="300ae-120">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="300ae-121"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)</span><span class="sxs-lookup"><span data-stu-id="300ae-121"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="300ae-122">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="300ae-122">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="300ae-123"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="300ae-123"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="300ae-124">Modificare l'ACL del file logico.</span><span class="sxs-lookup"><span data-stu-id="300ae-124">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="300ae-125"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="300ae-125"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="300ae-126">Modificare l'ACL di sistema del file logico.</span><span class="sxs-lookup"><span data-stu-id="300ae-126">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="300ae-127">*StopFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="300ae-127">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="300ae-128">Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="300ae-128">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="300ae-129">Se il metodo ha esito positivo, il valore di questo parametro è **null** .</span><span class="sxs-lookup"><span data-stu-id="300ae-129">This parameter has a value of **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="300ae-130">*StartFileName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="300ae-130">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="300ae-131">Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo.</span><span class="sxs-lookup"><span data-stu-id="300ae-131">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="300ae-132">In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="300ae-132">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="300ae-133">Se il valore del parametro è **null**, l'operazione viene eseguita nel file o nella directory specificata nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="300ae-133">If the parameter value is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="300ae-134">*Ricorsivo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="300ae-134">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="300ae-135">Se è **true**, anche il metodo viene applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza di [**\_ directory CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="300ae-135">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="300ae-136">Per le istanze di file, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="300ae-136">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="300ae-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="300ae-137">Return value</span></span>

<span data-ttu-id="300ae-138">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="300ae-138">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="300ae-139">0</span><span class="sxs-lookup"><span data-stu-id="300ae-139">0</span></span>

<span data-ttu-id="300ae-140">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="300ae-140">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="300ae-141">2</span><span class="sxs-lookup"><span data-stu-id="300ae-141">2</span></span>

<span data-ttu-id="300ae-142">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="300ae-142">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="300ae-143">8</span><span class="sxs-lookup"><span data-stu-id="300ae-143">8</span></span>

<span data-ttu-id="300ae-144">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="300ae-144">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="300ae-145">9</span><span class="sxs-lookup"><span data-stu-id="300ae-145">9</span></span>

<span data-ttu-id="300ae-146">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="300ae-146">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="300ae-147">10</span><span class="sxs-lookup"><span data-stu-id="300ae-147">10</span></span>

<span data-ttu-id="300ae-148">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="300ae-148">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="300ae-149">11</span><span class="sxs-lookup"><span data-stu-id="300ae-149">11</span></span>

<span data-ttu-id="300ae-150">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="300ae-150">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="300ae-151">12</span><span class="sxs-lookup"><span data-stu-id="300ae-151">12</span></span>

<span data-ttu-id="300ae-152">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="300ae-152">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="300ae-153">13</span><span class="sxs-lookup"><span data-stu-id="300ae-153">13</span></span>

<span data-ttu-id="300ae-154">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="300ae-154">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="300ae-155">14</span><span class="sxs-lookup"><span data-stu-id="300ae-155">14</span></span>

<span data-ttu-id="300ae-156">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="300ae-156">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="300ae-157">15</span><span class="sxs-lookup"><span data-stu-id="300ae-157">15</span></span>

<span data-ttu-id="300ae-158">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="300ae-158">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="300ae-159">16</span><span class="sxs-lookup"><span data-stu-id="300ae-159">16</span></span>

<span data-ttu-id="300ae-160">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="300ae-160">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="300ae-161">17</span><span class="sxs-lookup"><span data-stu-id="300ae-161">17</span></span>

<span data-ttu-id="300ae-162">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="300ae-162">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="300ae-163">21</span><span class="sxs-lookup"><span data-stu-id="300ae-163">21</span></span>

<span data-ttu-id="300ae-164">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="300ae-164">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="300ae-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="300ae-165">Remarks</span></span>

<span data-ttu-id="300ae-166">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="300ae-166">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="300ae-167">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="300ae-167">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="300ae-168">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="300ae-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="300ae-169">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="300ae-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="300ae-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="300ae-170">Requirements</span></span>



| <span data-ttu-id="300ae-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="300ae-171">Requirement</span></span> | <span data-ttu-id="300ae-172">Valore</span><span class="sxs-lookup"><span data-stu-id="300ae-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="300ae-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="300ae-173">Minimum supported client</span></span><br/> | <span data-ttu-id="300ae-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="300ae-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="300ae-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="300ae-175">Minimum supported server</span></span><br/> | <span data-ttu-id="300ae-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="300ae-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="300ae-177">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="300ae-177">Namespace</span></span><br/>                | <span data-ttu-id="300ae-178">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="300ae-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="300ae-179">MOF</span><span class="sxs-lookup"><span data-stu-id="300ae-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="300ae-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="300ae-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="300ae-181">DLL</span><span class="sxs-lookup"><span data-stu-id="300ae-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="300ae-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="300ae-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="300ae-183">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="300ae-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="300ae-184">\_Directory CIM</span><span class="sxs-lookup"><span data-stu-id="300ae-184">CIM\_Directory</span></span>](changesecuritypermissionsex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="300ae-185">**\_Directory CIM**</span><span class="sxs-lookup"><span data-stu-id="300ae-185">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

