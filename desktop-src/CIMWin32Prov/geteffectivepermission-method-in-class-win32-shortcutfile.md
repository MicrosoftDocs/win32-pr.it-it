---
description: Determina se l'utente dispone di tutte le autorizzazioni necessarie specificate nel parametro delle autorizzazioni per l'oggetto file, la directory e la condivisione in cui si trova il file di collegamento, se il file o la directory si trova in una condivisione.
ms.assetid: 36f823c1-fa19-40a1-b750-41e1f73bdf01
ms.tgt_platform: multiple
title: Metodo GetEffectivePermission della classe Win32_ShortcutFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52b57318ac05212304024ead82026d6daf0d8ea4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126492"
---
# <a name="geteffectivepermission-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="81338-103">Metodo GetEffectivePermission della \_ classe ShortcutFile Win32</span><span class="sxs-lookup"><span data-stu-id="81338-103">GetEffectivePermission method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="81338-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetEffectivePermission** determina se l'utente dispone di tutte le autorizzazioni necessarie specificate nel parametro *Permissions* per l'oggetto file, la directory e la condivisione in cui si trova il file di collegamento, se il file o la directory si trova in una condivisione.</span><span class="sxs-lookup"><span data-stu-id="81338-104">The **GetEffectivePermission** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method determines whether the user has all of the required permissions specified in the *Permissions* parameter for the file object, directory, and share where the shortcut file is located, if the file or directory is on a share.</span></span>

<span data-ttu-id="81338-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="81338-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="81338-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="81338-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="81338-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81338-107">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="81338-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="81338-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81338-109">*Autorizzazioni* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81338-109">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81338-110">Bitmap delle autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="81338-110">Bitmap of permissions.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="81338-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**File \_ LEGGERE la \_ directory dell'elenco di file (file) di dati ( \_ \_ Directory)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="81338-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="81338-112">Concede il diritto di leggere i dati dal file.</span><span class="sxs-lookup"><span data-stu-id="81338-112">Grants the right to read data from the file.</span></span> <span data-ttu-id="81338-113">Per una directory, questo valore concede il diritto di elencare il contenuto della directory.</span><span class="sxs-lookup"><span data-stu-id="81338-113">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="81338-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**File \_ Scrivi file di \_ dati (file) \_ Aggiungi \_ file (directory)** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="81338-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="81338-115">Concede il diritto di scrivere i dati nel file.</span><span class="sxs-lookup"><span data-stu-id="81338-115">Grants the right to write data to the file.</span></span> <span data-ttu-id="81338-116">Per una directory, questo valore concede il diritto di creare un file nella directory.</span><span class="sxs-lookup"><span data-stu-id="81338-116">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="81338-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**File \_ ACCODA \_ file di dati (file) \_ Aggiungi \_ sottodirectory (directory)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="81338-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="81338-118">Concede il diritto di accodare i dati al file.</span><span class="sxs-lookup"><span data-stu-id="81338-118">Grants the right to append data to the file.</span></span> <span data-ttu-id="81338-119">Per una directory, questo valore concede il diritto di creare una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="81338-119">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="81338-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**File \_ Leggi \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="81338-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="81338-121">Concede il diritto di leggere gli attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="81338-121">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="81338-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**File \_ Scrivi \_ EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="81338-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="81338-123">Concede il diritto di scrivere attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="81338-123">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>

<span data-ttu-id="81338-124"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**File \_ Attraversamento FILE di esecuzione (file) ( \_ Directory)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="81338-124"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="81338-125">Concede il diritto di eseguire un file.</span><span class="sxs-lookup"><span data-stu-id="81338-125">Grants the right to execute a file.</span></span> <span data-ttu-id="81338-126">Per una directory, la directory può essere attraversata.</span><span class="sxs-lookup"><span data-stu-id="81338-126">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="81338-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**File \_ Elimina \_ elemento figlio (directory)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="81338-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="81338-128">Concede il diritto di eliminare una directory e tutti i file in esso contenuti, anche se i file sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="81338-128">Grants the right to delete a directory and all of the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="81338-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**File \_ Leggi \_ attributi** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="81338-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="81338-130">Concede il diritto di leggere gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="81338-130">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="81338-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**File \_ Scrivi \_ attributi** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="81338-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="81338-132">Concede il diritto di modificare gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="81338-132">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="81338-133"><span id="DELETE"></span><span id="delete"></span>**Elimina** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="81338-133"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="81338-134">Concede l'accesso DELETE.</span><span class="sxs-lookup"><span data-stu-id="81338-134">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="81338-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leggi \_ CONTROLLO** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="81338-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="81338-136">Concede l'accesso in lettura al descrittore di sicurezza e al proprietario.</span><span class="sxs-lookup"><span data-stu-id="81338-136">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="81338-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Scrivi \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="81338-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="81338-138">Concede l'accesso in scrittura all'elenco di controllo di accesso discrezionale (DACL).</span><span class="sxs-lookup"><span data-stu-id="81338-138">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="81338-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Scrivi \_ PROPRIETARIO** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="81338-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="81338-140">Assegna il proprietario della scrittura.</span><span class="sxs-lookup"><span data-stu-id="81338-140">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="81338-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizza** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="81338-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="81338-142">Sincronizza l'accesso e consente a un processo di attendere che un oggetto entri nello stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="81338-142">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81338-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81338-143">Return value</span></span>

<span data-ttu-id="81338-144">Restituisce **true** se l'utente dispone delle autorizzazioni specificate e **false** se l'utente non dispone delle autorizzazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="81338-144">Returns **True** if the user has the specified permissions, and **false** if the user does not have the specified permissions.</span></span>

## <a name="requirements"></a><span data-ttu-id="81338-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81338-145">Requirements</span></span>



| <span data-ttu-id="81338-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="81338-146">Requirement</span></span> | <span data-ttu-id="81338-147">Valore</span><span class="sxs-lookup"><span data-stu-id="81338-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81338-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81338-148">Minimum supported client</span></span><br/> | <span data-ttu-id="81338-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81338-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81338-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81338-150">Minimum supported server</span></span><br/> | <span data-ttu-id="81338-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81338-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81338-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="81338-152">Namespace</span></span><br/>                | <span data-ttu-id="81338-153">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="81338-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81338-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81338-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="81338-155"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="81338-155"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="81338-156">MOF</span><span class="sxs-lookup"><span data-stu-id="81338-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81338-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81338-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81338-158">DLL</span><span class="sxs-lookup"><span data-stu-id="81338-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81338-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81338-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81338-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81338-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="81338-161">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="81338-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="81338-162">**\_ShortcutFile Win32**</span><span class="sxs-lookup"><span data-stu-id="81338-162">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

