---
description: Modifica le autorizzazioni di sicurezza per il file di collegamento logico specificato nel percorso dell'oggetto.
ms.assetid: abd5aec8-4684-4b8d-8fdf-d3a7a5eec103
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissions della classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad2d482e0be93a1abec80fc710a1a43d7873dd99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483501"
---
# <a name="changesecuritypermissions-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="89f23-103">Metodo ChangeSecurityPermissions della \_ classe ShortcutFile Win32</span><span class="sxs-lookup"><span data-stu-id="89f23-103">ChangeSecurityPermissions method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="89f23-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** modifica le autorizzazioni di sicurezza per il file di collegamento logico specificato nel percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="89f23-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical shortcut file specified in the object path.</span></span> <span data-ttu-id="89f23-105">Se il file logico è una directory, **ChangeSecurityPermissions** è ricorsivo e modifica le autorizzazioni di sicurezza di tutti i file e le sottodirectory in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="89f23-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span> <span data-ttu-id="89f23-106">**ChangeSecurityPermissions** restituisce un valore intero pari a 0 (zero) se le autorizzazioni vengono modificate e un numero diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="89f23-106">**ChangeSecurityPermissions** returns an integer value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<span data-ttu-id="89f23-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="89f23-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="89f23-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="89f23-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="89f23-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89f23-109">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="89f23-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="89f23-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89f23-111">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89f23-111">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89f23-112">Espressione che viene risolta in un'istanza di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="89f23-112">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="89f23-113">Questo descrittore contiene nuove autorizzazioni di sicurezza per l'istanza del [**\_ paging Win32**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="89f23-113">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="89f23-114">*Opzione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89f23-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89f23-115">Privilegi di sicurezza effettivi da modificare.</span><span class="sxs-lookup"><span data-stu-id="89f23-115">Actual security privilege to be modified.</span></span> <span data-ttu-id="89f23-116">Per modificare, ad esempio, la sicurezza del proprietario e del DACL, usare:</span><span class="sxs-lookup"><span data-stu-id="89f23-116">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="89f23-117">oppure</span><span class="sxs-lookup"><span data-stu-id="89f23-117">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="89f23-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)</span><span class="sxs-lookup"><span data-stu-id="89f23-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="89f23-119">Modificare il proprietario del file logico.</span><span class="sxs-lookup"><span data-stu-id="89f23-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="89f23-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)</span><span class="sxs-lookup"><span data-stu-id="89f23-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="89f23-121">Modificare il gruppo del file logico.</span><span class="sxs-lookup"><span data-stu-id="89f23-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="89f23-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)</span><span class="sxs-lookup"><span data-stu-id="89f23-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="89f23-123">Modificare l'elenco di controllo di accesso discrezionale (DACL) del file logico.</span><span class="sxs-lookup"><span data-stu-id="89f23-123">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="89f23-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)</span><span class="sxs-lookup"><span data-stu-id="89f23-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="89f23-125">Modificare l'elenco di controllo di accesso di sistema (SACL) del file logico.</span><span class="sxs-lookup"><span data-stu-id="89f23-125">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89f23-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89f23-126">Return value</span></span>

<span data-ttu-id="89f23-127">Restituisce un valore pari a 0 (zero) se le autorizzazioni vengono modificate e un numero diverso per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="89f23-127">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="89f23-128">**Success**</span><span class="sxs-lookup"><span data-stu-id="89f23-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="89f23-129">0</span><span class="sxs-lookup"><span data-stu-id="89f23-129">0</span></span>

<span data-ttu-id="89f23-130">La richiesta ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="89f23-130">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="89f23-131">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="89f23-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="89f23-132">2</span><span class="sxs-lookup"><span data-stu-id="89f23-132">2</span></span>

<span data-ttu-id="89f23-133">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="89f23-133">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="89f23-134">**Errore non specificato**</span><span class="sxs-lookup"><span data-stu-id="89f23-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="89f23-135">8</span><span class="sxs-lookup"><span data-stu-id="89f23-135">8</span></span>

<span data-ttu-id="89f23-136">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="89f23-136">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="89f23-137">**Oggetto non valido**</span><span class="sxs-lookup"><span data-stu-id="89f23-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="89f23-138">9</span><span class="sxs-lookup"><span data-stu-id="89f23-138">9</span></span>

<span data-ttu-id="89f23-139">Il nome specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="89f23-139">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="89f23-140">**Oggetto già esistente**</span><span class="sxs-lookup"><span data-stu-id="89f23-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="89f23-141">10</span><span class="sxs-lookup"><span data-stu-id="89f23-141">10</span></span>

<span data-ttu-id="89f23-142">L'oggetto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="89f23-142">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="89f23-143">**File System non NTFS**</span><span class="sxs-lookup"><span data-stu-id="89f23-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="89f23-144">11</span><span class="sxs-lookup"><span data-stu-id="89f23-144">11</span></span>

<span data-ttu-id="89f23-145">Il file system non è un file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="89f23-145">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="89f23-146">**Piattaforma non NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="89f23-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="89f23-147">12</span><span class="sxs-lookup"><span data-stu-id="89f23-147">12</span></span>

<span data-ttu-id="89f23-148">La piattaforma non è Windows.</span><span class="sxs-lookup"><span data-stu-id="89f23-148">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="89f23-149">**Unità non uguale**</span><span class="sxs-lookup"><span data-stu-id="89f23-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="89f23-150">13</span><span class="sxs-lookup"><span data-stu-id="89f23-150">13</span></span>

<span data-ttu-id="89f23-151">L'unità non è la stessa.</span><span class="sxs-lookup"><span data-stu-id="89f23-151">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="89f23-152">**Directory non vuota**</span><span class="sxs-lookup"><span data-stu-id="89f23-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="89f23-153">14</span><span class="sxs-lookup"><span data-stu-id="89f23-153">14</span></span>

<span data-ttu-id="89f23-154">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="89f23-154">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="89f23-155">**Violazione di condivisione**</span><span class="sxs-lookup"><span data-stu-id="89f23-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="89f23-156">15</span><span class="sxs-lookup"><span data-stu-id="89f23-156">15</span></span>

<span data-ttu-id="89f23-157">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="89f23-157">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="89f23-158">**File di avvio non valido**</span><span class="sxs-lookup"><span data-stu-id="89f23-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="89f23-159">16</span><span class="sxs-lookup"><span data-stu-id="89f23-159">16</span></span>

<span data-ttu-id="89f23-160">Il file di avvio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="89f23-160">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="89f23-161">**Privilegio non mantenuto**</span><span class="sxs-lookup"><span data-stu-id="89f23-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="89f23-162">17</span><span class="sxs-lookup"><span data-stu-id="89f23-162">17</span></span>

<span data-ttu-id="89f23-163">Un privilegio necessario per l'operazione non viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="89f23-163">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="89f23-164">**Parametro non valido**</span><span class="sxs-lookup"><span data-stu-id="89f23-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="89f23-165">21</span><span class="sxs-lookup"><span data-stu-id="89f23-165">21</span></span>

<span data-ttu-id="89f23-166">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="89f23-166">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89f23-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89f23-167">Requirements</span></span>



| <span data-ttu-id="89f23-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="89f23-168">Requirement</span></span> | <span data-ttu-id="89f23-169">Valore</span><span class="sxs-lookup"><span data-stu-id="89f23-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89f23-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89f23-170">Minimum supported client</span></span><br/> | <span data-ttu-id="89f23-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89f23-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89f23-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89f23-172">Minimum supported server</span></span><br/> | <span data-ttu-id="89f23-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89f23-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89f23-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89f23-174">Namespace</span></span><br/>                | <span data-ttu-id="89f23-175">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="89f23-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89f23-176">MOF</span><span class="sxs-lookup"><span data-stu-id="89f23-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89f23-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89f23-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89f23-178">DLL</span><span class="sxs-lookup"><span data-stu-id="89f23-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89f23-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89f23-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89f23-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89f23-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="89f23-181">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="89f23-181">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="89f23-182">**\_ShortcutFile Win32**</span><span class="sxs-lookup"><span data-stu-id="89f23-182">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

