---
description: Modifica le autorizzazioni di sicurezza per il file di paging logico specificato nel percorso dell'oggetto.
ms.assetid: 3abdfa1d-49d8-4676-b7a5-3be528938ec4
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissions della classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc30d8780f7c0573b9a63ff83f16ad46b9d2a70f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966192"
---
# <a name="changesecuritypermissions-method-of-the-win32_pagefile-class"></a><span data-ttu-id="11ba4-103">Metodo ChangeSecurityPermissions della classe di \_ paging Win32</span><span class="sxs-lookup"><span data-stu-id="11ba4-103">ChangeSecurityPermissions method of the Win32\_PageFile class</span></span>

<span data-ttu-id="11ba4-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** modifica le autorizzazioni di sicurezza per il file di paging logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="11ba4-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical paging file specified in the object path.</span></span> <span data-ttu-id="11ba4-105">Se il file logico è una directory, **ChangeSecurityPermissions** è ricorsivo e modifica le autorizzazioni di sicurezza di tutti i file e le sottodirectory in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="11ba4-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="11ba4-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="11ba4-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="11ba4-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="11ba4-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="11ba4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11ba4-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="11ba4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="11ba4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11ba4-110">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11ba4-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-111">Espressione che viene risolta in un'istanza di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="11ba4-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="11ba4-112">Questo descrittore contiene nuove autorizzazioni di sicurezza per l'istanza del [**\_ paging Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="11ba4-112">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="11ba4-113">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11ba4-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-114">Privilegio di sicurezza da modificare.</span><span class="sxs-lookup"><span data-stu-id="11ba4-114">Security privilege to be modified.</span></span> <span data-ttu-id="11ba4-115">Ad esempio, per modificare la sicurezza del proprietario e dell'elenco di controllo di accesso discrezionale (DACL), usare:</span><span class="sxs-lookup"><span data-stu-id="11ba4-115">For example, to change the owner and discretionary access control list (DACL) security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="11ba4-116">-oppure-</span><span class="sxs-lookup"><span data-stu-id="11ba4-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="11ba4-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)</span><span class="sxs-lookup"><span data-stu-id="11ba4-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="11ba4-118">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="11ba4-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="11ba4-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)</span><span class="sxs-lookup"><span data-stu-id="11ba4-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="11ba4-120">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="11ba4-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="11ba4-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="11ba4-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="11ba4-122">Modificare l'elenco DACL del file logico.</span><span class="sxs-lookup"><span data-stu-id="11ba4-122">Change the DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="11ba4-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="11ba4-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="11ba4-124">Modificare l'elenco di controllo di accesso di sistema (SACL) del file logico.</span><span class="sxs-lookup"><span data-stu-id="11ba4-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11ba4-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11ba4-125">Return value</span></span>

<span data-ttu-id="11ba4-126">Restituisce un valore pari a 0 (zero) se le autorizzazioni vengono modificate e un numero diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="11ba4-126">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="11ba4-127">**Success**</span><span class="sxs-lookup"><span data-stu-id="11ba4-127">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-128">0</span><span class="sxs-lookup"><span data-stu-id="11ba4-128">0</span></span>

<span data-ttu-id="11ba4-129">La richiesta ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="11ba4-129">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="11ba4-130">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="11ba4-130">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-131">2</span><span class="sxs-lookup"><span data-stu-id="11ba4-131">2</span></span>

<span data-ttu-id="11ba4-132">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="11ba4-132">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="11ba4-133">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="11ba4-133">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-134">8</span><span class="sxs-lookup"><span data-stu-id="11ba4-134">8</span></span>

<span data-ttu-id="11ba4-135">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="11ba4-135">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="11ba4-136">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="11ba4-136">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-137">9</span><span class="sxs-lookup"><span data-stu-id="11ba4-137">9</span></span>

<span data-ttu-id="11ba4-138">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="11ba4-138">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="11ba4-139">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="11ba4-139">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-140">10</span><span class="sxs-lookup"><span data-stu-id="11ba4-140">10</span></span>

<span data-ttu-id="11ba4-141">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="11ba4-141">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="11ba4-142">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="11ba4-142">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-143">11</span><span class="sxs-lookup"><span data-stu-id="11ba4-143">11</span></span>

<span data-ttu-id="11ba4-144">Il file system non è un file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="11ba4-144">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="11ba4-145">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="11ba4-145">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-146">12</span><span class="sxs-lookup"><span data-stu-id="11ba4-146">12</span></span>

<span data-ttu-id="11ba4-147">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="11ba4-147">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="11ba4-148">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="11ba4-148">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-149">13</span><span class="sxs-lookup"><span data-stu-id="11ba4-149">13</span></span>

<span data-ttu-id="11ba4-150">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="11ba4-150">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="11ba4-151">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="11ba4-151">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-152">14</span><span class="sxs-lookup"><span data-stu-id="11ba4-152">14</span></span>

<span data-ttu-id="11ba4-153">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="11ba4-153">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="11ba4-154">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="11ba4-154">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-155">15</span><span class="sxs-lookup"><span data-stu-id="11ba4-155">15</span></span>

<span data-ttu-id="11ba4-156">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="11ba4-156">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="11ba4-157">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="11ba4-157">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-158">16</span><span class="sxs-lookup"><span data-stu-id="11ba4-158">16</span></span>

<span data-ttu-id="11ba4-159">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="11ba4-159">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="11ba4-160">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="11ba4-160">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-161">17</span><span class="sxs-lookup"><span data-stu-id="11ba4-161">17</span></span>

<span data-ttu-id="11ba4-162">Un privilegio necessario per l'operazione è mancante.</span><span class="sxs-lookup"><span data-stu-id="11ba4-162">A privilege required for the operation is missing.</span></span>

</dd> <dt>

<span data-ttu-id="11ba4-163">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="11ba4-163">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="11ba4-164">21</span><span class="sxs-lookup"><span data-stu-id="11ba4-164">21</span></span>

<span data-ttu-id="11ba4-165">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="11ba4-165">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11ba4-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11ba4-166">Requirements</span></span>



| <span data-ttu-id="11ba4-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="11ba4-167">Requirement</span></span> | <span data-ttu-id="11ba4-168">Valore</span><span class="sxs-lookup"><span data-stu-id="11ba4-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11ba4-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11ba4-169">Minimum supported client</span></span><br/> | <span data-ttu-id="11ba4-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11ba4-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="11ba4-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11ba4-171">Minimum supported server</span></span><br/> | <span data-ttu-id="11ba4-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11ba4-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="11ba4-173">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="11ba4-173">Namespace</span></span><br/>                | <span data-ttu-id="11ba4-174">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="11ba4-174">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="11ba4-175">MOF</span><span class="sxs-lookup"><span data-stu-id="11ba4-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11ba4-176"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11ba4-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="11ba4-177">DLL</span><span class="sxs-lookup"><span data-stu-id="11ba4-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11ba4-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11ba4-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11ba4-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11ba4-179">See also</span></span>

<dl> <dt>

<span data-ttu-id="11ba4-180">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="11ba4-180">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="11ba4-181">**\_Pagefile Win32**</span><span class="sxs-lookup"><span data-stu-id="11ba4-181">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

