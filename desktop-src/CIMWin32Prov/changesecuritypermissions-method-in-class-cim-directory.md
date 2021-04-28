---
description: "Metodo ChangeSecurityPermissions della classe CIM_Directory: modifica le autorizzazioni di sicurezza per il file di voce di directory logica specificato nel percorso dell'oggetto."
ms.assetid: d3caeec1-fecc-4463-9349-d82869c11927
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissions della classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 389ed5b7b0a43981c5eeb3d66a73bd19cbd99d88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091069"
---
# <a name="changesecuritypermissions-method-of-the-cim_directory-class"></a><span data-ttu-id="b5d68-103">Metodo ChangeSecurityPermissions della classe Directory CIM \_</span><span class="sxs-lookup"><span data-stu-id="b5d68-103">ChangeSecurityPermissions method of the CIM\_Directory class</span></span>

<span data-ttu-id="b5d68-104">Il **metodo ChangeSecurityPermissions** modifica le autorizzazioni di sicurezza per il file di voce di directory logica specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b5d68-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="b5d68-105">Se il file logico è una directory, questo metodo agirà in modo ricorsivo, modificando le autorizzazioni di sicurezza per tutti i file e le sottodirectory contenuti nella directory.</span><span class="sxs-lookup"><span data-stu-id="b5d68-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="b5d68-106">Questo metodo viene ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5d68-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5d68-107">Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model) sono le classi padre su cui vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="b5d68-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b5d68-108">WMI attualmente supporta solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b5d68-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b5d68-109">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b5d68-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b5d68-110">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b5d68-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b5d68-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5d68-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="b5d68-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5d68-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5d68-113">*Descrittore di sicurezza* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b5d68-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d68-114">Specifica le informazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b5d68-114">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="b5d68-115">Un **elenco di** controllo di accesso (ACL) NULL nella struttura SECURITY [**\_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede l'accesso illimitato.</span><span class="sxs-lookup"><span data-stu-id="b5d68-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="b5d68-116">*Opzione* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b5d68-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5d68-117">Privilegio di sicurezza da modificare.</span><span class="sxs-lookup"><span data-stu-id="b5d68-117">Security privilege to modify.</span></span> <span data-ttu-id="b5d68-118">Ad esempio, per modificare il proprietario e la sicurezza DACL, usare:</span><span class="sxs-lookup"><span data-stu-id="b5d68-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="b5d68-119">oppure</span><span class="sxs-lookup"><span data-stu-id="b5d68-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="b5d68-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**MODIFICA \_ INFORMAZIONI \_ DI SICUREZZA DEL \_ PROPRIETARIO** (1)</span><span class="sxs-lookup"><span data-stu-id="b5d68-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b5d68-121">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="b5d68-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="b5d68-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**MODIFICA \_ INFORMAZIONI \_ SULLA SICUREZZA DEL \_ GRUPPO** (2)</span><span class="sxs-lookup"><span data-stu-id="b5d68-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b5d68-123">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="b5d68-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="b5d68-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**MODIFICA \_ INFORMAZIONI DI \_ SICUREZZA DACL \_** (4)</span><span class="sxs-lookup"><span data-stu-id="b5d68-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b5d68-125">Modificare l'ACL del file logico.</span><span class="sxs-lookup"><span data-stu-id="b5d68-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="b5d68-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**MODIFICA \_ INFORMAZIONI DI \_ SICUREZZA SACL \_** (8)</span><span class="sxs-lookup"><span data-stu-id="b5d68-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b5d68-127">Modificare l'ACL di sistema del file logico.</span><span class="sxs-lookup"><span data-stu-id="b5d68-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5d68-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5d68-128">Return value</span></span>

<span data-ttu-id="b5d68-129">Restituisce il valore 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="b5d68-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="b5d68-130">0</span><span class="sxs-lookup"><span data-stu-id="b5d68-130">0</span></span>

<span data-ttu-id="b5d68-131">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b5d68-131">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b5d68-132">2</span><span class="sxs-lookup"><span data-stu-id="b5d68-132">2</span></span>

<span data-ttu-id="b5d68-133">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="b5d68-133">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b5d68-134">8</span><span class="sxs-lookup"><span data-stu-id="b5d68-134">8</span></span>

<span data-ttu-id="b5d68-135">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="b5d68-135">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b5d68-136">9</span><span class="sxs-lookup"><span data-stu-id="b5d68-136">9</span></span>

<span data-ttu-id="b5d68-137">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="b5d68-137">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b5d68-138">10</span><span class="sxs-lookup"><span data-stu-id="b5d68-138">10</span></span>

<span data-ttu-id="b5d68-139">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="b5d68-139">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b5d68-140">11</span><span class="sxs-lookup"><span data-stu-id="b5d68-140">11</span></span>

<span data-ttu-id="b5d68-141">File system non NTFS.</span><span class="sxs-lookup"><span data-stu-id="b5d68-141">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b5d68-142">12</span><span class="sxs-lookup"><span data-stu-id="b5d68-142">12</span></span>

<span data-ttu-id="b5d68-143">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="b5d68-143">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b5d68-144">13</span><span class="sxs-lookup"><span data-stu-id="b5d68-144">13</span></span>

<span data-ttu-id="b5d68-145">Unità non uguale.</span><span class="sxs-lookup"><span data-stu-id="b5d68-145">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b5d68-146">14</span><span class="sxs-lookup"><span data-stu-id="b5d68-146">14</span></span>

<span data-ttu-id="b5d68-147">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="b5d68-147">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b5d68-148">15</span><span class="sxs-lookup"><span data-stu-id="b5d68-148">15</span></span>

<span data-ttu-id="b5d68-149">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="b5d68-149">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b5d68-150">16</span><span class="sxs-lookup"><span data-stu-id="b5d68-150">16</span></span>

<span data-ttu-id="b5d68-151">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="b5d68-151">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b5d68-152">17</span><span class="sxs-lookup"><span data-stu-id="b5d68-152">17</span></span>

<span data-ttu-id="b5d68-153">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="b5d68-153">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b5d68-154">21</span><span class="sxs-lookup"><span data-stu-id="b5d68-154">21</span></span>

<span data-ttu-id="b5d68-155">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="b5d68-155">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5d68-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5d68-156">Remarks</span></span>

<span data-ttu-id="b5d68-157">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="b5d68-157">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b5d68-158">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="b5d68-158">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b5d68-159">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="b5d68-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b5d68-160">Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="b5d68-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d68-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5d68-161">Requirements</span></span>



| <span data-ttu-id="b5d68-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5d68-162">Requirement</span></span> | <span data-ttu-id="b5d68-163">Valore</span><span class="sxs-lookup"><span data-stu-id="b5d68-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d68-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5d68-164">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d68-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5d68-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5d68-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5d68-166">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d68-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5d68-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5d68-168">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b5d68-168">Namespace</span></span><br/>                | <span data-ttu-id="b5d68-169">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b5d68-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b5d68-170">MOF</span><span class="sxs-lookup"><span data-stu-id="b5d68-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5d68-171"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5d68-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5d68-172">DLL</span><span class="sxs-lookup"><span data-stu-id="b5d68-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5d68-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5d68-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5d68-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5d68-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d68-175">CIM \_ Directory</span><span class="sxs-lookup"><span data-stu-id="b5d68-175">CIM\_Directory</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="b5d68-176">**CIM \_ Directory**</span><span class="sxs-lookup"><span data-stu-id="b5d68-176">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

