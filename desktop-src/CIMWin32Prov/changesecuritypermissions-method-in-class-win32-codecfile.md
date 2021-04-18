---
description: Modifica le autorizzazioni di sicurezza per il file di codec logico specificato nel percorso dell'oggetto.
ms.assetid: d7945666-e514-4bfc-81bc-8e98aa90bcf0
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissions della classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b0789164b2bb28b5c3c84e907cf7ae2acb96e01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304445"
---
# <a name="changesecuritypermissions-method-of-the-win32_codecfile-class"></a><span data-ttu-id="5945e-103">Metodo ChangeSecurityPermissions della \_ classe Sqlcfile Win32</span><span class="sxs-lookup"><span data-stu-id="5945e-103">ChangeSecurityPermissions method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="5945e-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** modifica le autorizzazioni di sicurezza per il file di codec logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5945e-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical codec file specified in the object path.</span></span> <span data-ttu-id="5945e-105">Se il file logico è una directory, **ChangeSecurityPermissions** è ricorsivo e modifica le autorizzazioni di sicurezza di tutti i file e le sottodirectory in essa contenuti.</span><span class="sxs-lookup"><span data-stu-id="5945e-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories the directory contains.</span></span> <span data-ttu-id="5945e-106">**ChangeSecurityPermissions** restituisce un valore intero pari a 0 (zero) se le autorizzazioni vengono modificate e un numero diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="5945e-106">**ChangeSecurityPermissions** returns an integer value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<span data-ttu-id="5945e-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="5945e-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5945e-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5945e-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5945e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5945e-109">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="5945e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5945e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5945e-111">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5945e-111">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5945e-112">Espressione che viene risolta in un'istanza di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="5945e-112">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="5945e-113">Questo descrittore contiene nuove autorizzazioni di sicurezza per l'istanza di [**Win32 \_ codecfile**](win32-codecfile.md).</span><span class="sxs-lookup"><span data-stu-id="5945e-113">This descriptor contains new security permissions for the instance of [**Win32\_CodecFile**](win32-codecfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="5945e-114">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5945e-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5945e-115">Privilegio di sicurezza da modificare.</span><span class="sxs-lookup"><span data-stu-id="5945e-115">Security privilege to be modified.</span></span> <span data-ttu-id="5945e-116">Ad esempio, per modificare la sicurezza del proprietario e dell'elenco di controllo di accesso discrezionale (DACL), usare:</span><span class="sxs-lookup"><span data-stu-id="5945e-116">For example, to change the owner and discretionary access control list (DACL) security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="5945e-117">-oppure-</span><span class="sxs-lookup"><span data-stu-id="5945e-117">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="5945e-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del proprietario** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="5945e-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="5945e-119">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="5945e-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="5945e-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="5945e-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="5945e-121">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="5945e-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="5945e-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="5945e-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="5945e-123">Modificare l'elenco di controllo di accesso discrezionale (DACL) del file logico.</span><span class="sxs-lookup"><span data-stu-id="5945e-123">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="5945e-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="5945e-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="5945e-125">Modificare l'elenco di controllo di accesso di sistema (SACL) del file logico.</span><span class="sxs-lookup"><span data-stu-id="5945e-125">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5945e-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5945e-126">Return value</span></span>

<span data-ttu-id="5945e-127">Restituisce un valore pari a 0 (zero) se le autorizzazioni vengono modificate e un numero diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="5945e-127">Returns an value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5945e-128">**Success**</span><span class="sxs-lookup"><span data-stu-id="5945e-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="5945e-129">0</span><span class="sxs-lookup"><span data-stu-id="5945e-129">0</span></span>

<span data-ttu-id="5945e-130">La richiesta ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5945e-130">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="5945e-131">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="5945e-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="5945e-132">2</span><span class="sxs-lookup"><span data-stu-id="5945e-132">2</span></span>

<span data-ttu-id="5945e-133">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="5945e-133">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="5945e-134">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="5945e-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="5945e-135">8</span><span class="sxs-lookup"><span data-stu-id="5945e-135">8</span></span>

<span data-ttu-id="5945e-136">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="5945e-136">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5945e-137">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="5945e-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="5945e-138">9</span><span class="sxs-lookup"><span data-stu-id="5945e-138">9</span></span>

<span data-ttu-id="5945e-139">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="5945e-139">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5945e-140">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="5945e-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="5945e-141">10</span><span class="sxs-lookup"><span data-stu-id="5945e-141">10</span></span>

<span data-ttu-id="5945e-142">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="5945e-142">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5945e-143">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="5945e-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="5945e-144">11</span><span class="sxs-lookup"><span data-stu-id="5945e-144">11</span></span>

<span data-ttu-id="5945e-145">Il file system non è un file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="5945e-145">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="5945e-146">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="5945e-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="5945e-147">12</span><span class="sxs-lookup"><span data-stu-id="5945e-147">12</span></span>

<span data-ttu-id="5945e-148">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="5945e-148">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5945e-149">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="5945e-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="5945e-150">13</span><span class="sxs-lookup"><span data-stu-id="5945e-150">13</span></span>

<span data-ttu-id="5945e-151">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="5945e-151">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5945e-152">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="5945e-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="5945e-153">14</span><span class="sxs-lookup"><span data-stu-id="5945e-153">14</span></span>

<span data-ttu-id="5945e-154">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="5945e-154">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5945e-155">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="5945e-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="5945e-156">15</span><span class="sxs-lookup"><span data-stu-id="5945e-156">15</span></span>

<span data-ttu-id="5945e-157">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="5945e-157">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5945e-158">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="5945e-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="5945e-159">16</span><span class="sxs-lookup"><span data-stu-id="5945e-159">16</span></span>

<span data-ttu-id="5945e-160">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="5945e-160">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5945e-161">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="5945e-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="5945e-162">17</span><span class="sxs-lookup"><span data-stu-id="5945e-162">17</span></span>

<span data-ttu-id="5945e-163">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="5945e-163">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="5945e-164">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="5945e-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5945e-165">21</span><span class="sxs-lookup"><span data-stu-id="5945e-165">21</span></span>

<span data-ttu-id="5945e-166">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="5945e-166">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5945e-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5945e-167">Requirements</span></span>



| <span data-ttu-id="5945e-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="5945e-168">Requirement</span></span> | <span data-ttu-id="5945e-169">Valore</span><span class="sxs-lookup"><span data-stu-id="5945e-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5945e-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5945e-170">Minimum supported client</span></span><br/> | <span data-ttu-id="5945e-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5945e-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5945e-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5945e-172">Minimum supported server</span></span><br/> | <span data-ttu-id="5945e-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5945e-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5945e-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5945e-174">Namespace</span></span><br/>                | <span data-ttu-id="5945e-175">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5945e-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5945e-176">MOF</span><span class="sxs-lookup"><span data-stu-id="5945e-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5945e-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5945e-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5945e-178">DLL</span><span class="sxs-lookup"><span data-stu-id="5945e-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5945e-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5945e-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5945e-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5945e-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="5945e-181">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5945e-181">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5945e-182">**Codecfile Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="5945e-182">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

