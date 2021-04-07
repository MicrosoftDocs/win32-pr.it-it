---
description: Modifica le autorizzazioni di sicurezza per il file di voce della directory logica specificato nel percorso dell'oggetto.
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
ms.openlocfilehash: 2bf767dc45907a90354b2c00fb30c6b31ce6d09a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748626"
---
# <a name="changesecuritypermissions-method-of-the-cim_directory-class"></a><span data-ttu-id="a3321-103">Metodo ChangeSecurityPermissions della classe di \_ directory CIM</span><span class="sxs-lookup"><span data-stu-id="a3321-103">ChangeSecurityPermissions method of the CIM\_Directory class</span></span>

<span data-ttu-id="a3321-104">Il metodo **ChangeSecurityPermissions** modifica le autorizzazioni di sicurezza per il file di voce della directory logica specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a3321-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="a3321-105">Se il file logico è una directory, questo metodo agirà in modo ricorsivo, modificando le autorizzazioni di sicurezza per tutti i file e le sottodirectory presenti nella directory.</span><span class="sxs-lookup"><span data-stu-id="a3321-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="a3321-106">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="a3321-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a3321-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a3321-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a3321-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a3321-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a3321-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a3321-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a3321-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a3321-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3321-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3321-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="a3321-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3321-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3321-113">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3321-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3321-114">Specifica le informazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a3321-114">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="a3321-115">Un elenco di controllo di accesso (ACL) **null** nella struttura del [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede un accesso illimitato.</span><span class="sxs-lookup"><span data-stu-id="a3321-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="a3321-116">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3321-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3321-117">Privilegi di sicurezza da modificare.</span><span class="sxs-lookup"><span data-stu-id="a3321-117">Security privilege to modify.</span></span> <span data-ttu-id="a3321-118">Per modificare, ad esempio, la sicurezza del proprietario e del DACL, usare:</span><span class="sxs-lookup"><span data-stu-id="a3321-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="a3321-119">oppure</span><span class="sxs-lookup"><span data-stu-id="a3321-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="a3321-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)</span><span class="sxs-lookup"><span data-stu-id="a3321-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a3321-121">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="a3321-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="a3321-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)</span><span class="sxs-lookup"><span data-stu-id="a3321-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a3321-123">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="a3321-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="a3321-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="a3321-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a3321-125">Modificare l'ACL del file logico.</span><span class="sxs-lookup"><span data-stu-id="a3321-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="a3321-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="a3321-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a3321-127">Modificare l'ACL di sistema del file logico.</span><span class="sxs-lookup"><span data-stu-id="a3321-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3321-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3321-128">Return value</span></span>

<span data-ttu-id="a3321-129">Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="a3321-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="a3321-130">0</span><span class="sxs-lookup"><span data-stu-id="a3321-130">0</span></span>

<span data-ttu-id="a3321-131">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a3321-131">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a3321-132">2</span><span class="sxs-lookup"><span data-stu-id="a3321-132">2</span></span>

<span data-ttu-id="a3321-133">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="a3321-133">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a3321-134">8</span><span class="sxs-lookup"><span data-stu-id="a3321-134">8</span></span>

<span data-ttu-id="a3321-135">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="a3321-135">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a3321-136">9</span><span class="sxs-lookup"><span data-stu-id="a3321-136">9</span></span>

<span data-ttu-id="a3321-137">Oggetto non valido.</span><span class="sxs-lookup"><span data-stu-id="a3321-137">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a3321-138">10</span><span class="sxs-lookup"><span data-stu-id="a3321-138">10</span></span>

<span data-ttu-id="a3321-139">Oggetto già esistente.</span><span class="sxs-lookup"><span data-stu-id="a3321-139">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a3321-140">11</span><span class="sxs-lookup"><span data-stu-id="a3321-140">11</span></span>

<span data-ttu-id="a3321-141">File System non NTFS.</span><span class="sxs-lookup"><span data-stu-id="a3321-141">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a3321-142">12</span><span class="sxs-lookup"><span data-stu-id="a3321-142">12</span></span>

<span data-ttu-id="a3321-143">Piattaforma non Windows.</span><span class="sxs-lookup"><span data-stu-id="a3321-143">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a3321-144">13</span><span class="sxs-lookup"><span data-stu-id="a3321-144">13</span></span>

<span data-ttu-id="a3321-145">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="a3321-145">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a3321-146">14</span><span class="sxs-lookup"><span data-stu-id="a3321-146">14</span></span>

<span data-ttu-id="a3321-147">Directory non vuota.</span><span class="sxs-lookup"><span data-stu-id="a3321-147">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a3321-148">15</span><span class="sxs-lookup"><span data-stu-id="a3321-148">15</span></span>

<span data-ttu-id="a3321-149">Violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="a3321-149">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a3321-150">16</span><span class="sxs-lookup"><span data-stu-id="a3321-150">16</span></span>

<span data-ttu-id="a3321-151">File di avvio non valido.</span><span class="sxs-lookup"><span data-stu-id="a3321-151">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a3321-152">17</span><span class="sxs-lookup"><span data-stu-id="a3321-152">17</span></span>

<span data-ttu-id="a3321-153">Privilegio non mantenuto.</span><span class="sxs-lookup"><span data-stu-id="a3321-153">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="a3321-154">21</span><span class="sxs-lookup"><span data-stu-id="a3321-154">21</span></span>

<span data-ttu-id="a3321-155">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="a3321-155">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3321-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3321-156">Remarks</span></span>

<span data-ttu-id="a3321-157">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="a3321-157">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a3321-158">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="a3321-158">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a3321-159">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a3321-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a3321-160">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a3321-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3321-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3321-161">Requirements</span></span>



| <span data-ttu-id="a3321-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3321-162">Requirement</span></span> | <span data-ttu-id="a3321-163">Valore</span><span class="sxs-lookup"><span data-stu-id="a3321-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3321-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3321-164">Minimum supported client</span></span><br/> | <span data-ttu-id="a3321-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3321-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3321-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3321-166">Minimum supported server</span></span><br/> | <span data-ttu-id="a3321-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3321-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3321-168">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a3321-168">Namespace</span></span><br/>                | <span data-ttu-id="a3321-169">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a3321-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a3321-170">MOF</span><span class="sxs-lookup"><span data-stu-id="a3321-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3321-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3321-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3321-172">DLL</span><span class="sxs-lookup"><span data-stu-id="a3321-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3321-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3321-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3321-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3321-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3321-175">\_Directory CIM</span><span class="sxs-lookup"><span data-stu-id="a3321-175">CIM\_Directory</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="a3321-176">**\_Directory CIM**</span><span class="sxs-lookup"><span data-stu-id="a3321-176">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

