---
description: USA i valori impostati nel parametro Permissions per determinare se l'utente dispone delle autorizzazioni specificate impostate nella proprietà AccessMask dell'oggetto Win32 \_ codecfile che rappresenta il file di codec.
ms.assetid: 068dfcaf-037b-4516-b85a-8ba6558ba561
ms.tgt_platform: multiple
title: Metodo GetEffectivePermission della classe Win32_CodecFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc2f24071d5ab864e06686f094707d9111ea07ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877593"
---
# <a name="geteffectivepermission-method-of-the-win32_codecfile-class"></a><span data-ttu-id="40919-103">Metodo GetEffectivePermission della \_ classe Sqlcfile Win32</span><span class="sxs-lookup"><span data-stu-id="40919-103">GetEffectivePermission method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="40919-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) utilizza i valori impostati nel parametro *Permissions* per determinare se l'utente dispone delle autorizzazioni specificate impostate nella proprietà **accessMask** dell'oggetto [**Win32 \_ codecfile**](win32-codecfile.md) che rappresenta il file di codec.</span><span class="sxs-lookup"><span data-stu-id="40919-104">The [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uses the values set in the *Permissions* parameter to determine whether the user has the specified permissions set in the **AccessMask** property of the [**Win32\_CodecFile**](win32-codecfile.md) object that represents the codec file.</span></span> <span data-ttu-id="40919-105">Le autorizzazioni vengono applicate al file, alla directory in cui risiede il file e alla condivisione, se la directory o il file si trova in una condivisione.</span><span class="sxs-lookup"><span data-stu-id="40919-105">The permissions apply to the file, the directory in which the file resides, and the share, if either the directory or the file are in a share.</span></span>

<span data-ttu-id="40919-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="40919-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="40919-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="40919-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="40919-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40919-108">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="40919-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="40919-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40919-110">*Autorizzazioni* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40919-110">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40919-111">Mappa di bit delle autorizzazioni impostate nella proprietà **accessMask** dell'oggetto [**\_ codecfile di Win32**](win32-codecfile.md) .</span><span class="sxs-lookup"><span data-stu-id="40919-111">Bitmap of permissions that are set in the **AccessMask** property of the [**Win32\_CodecFile**](win32-codecfile.md) object.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="40919-112"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**File \_ LEGGERE la \_ directory dell'elenco di file (file) di dati ( \_ \_ Directory)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="40919-112"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="40919-113">Concede il diritto di leggere i dati dal file.</span><span class="sxs-lookup"><span data-stu-id="40919-113">Grants the right to read data from the file.</span></span> <span data-ttu-id="40919-114">Per una directory, questo valore concede il diritto di elencare il contenuto della directory.</span><span class="sxs-lookup"><span data-stu-id="40919-114">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="40919-115"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**File \_ Scrivi file di \_ dati (file) \_ Aggiungi \_ file (directory)** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="40919-115"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="40919-116">Concede il diritto di scrivere i dati nel file.</span><span class="sxs-lookup"><span data-stu-id="40919-116">Grants the right to write data to the file.</span></span> <span data-ttu-id="40919-117">Per una directory, questo valore concede il diritto di creare un file nella directory.</span><span class="sxs-lookup"><span data-stu-id="40919-117">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="40919-118"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**File \_ ACCODA \_ file di dati (file) \_ Aggiungi \_ sottodirectory (directory)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="40919-118"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="40919-119">Concede il diritto di accodare i dati al file.</span><span class="sxs-lookup"><span data-stu-id="40919-119">Grants the right to append data to the file.</span></span> <span data-ttu-id="40919-120">Per una directory, questo valore concede il diritto di creare una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="40919-120">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="40919-121"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**File \_ Leggi \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="40919-121"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="40919-122">Concede il diritto di leggere gli attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="40919-122">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="40919-123"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**File \_ Scrivi \_ EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="40919-123"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="40919-124">Concede il diritto di scrivere attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="40919-124">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="40919-125"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**File \_ Attraversamento FILE di esecuzione (file) ( \_ Directory)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="40919-125"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="40919-126">Concede il diritto di eseguire un file.</span><span class="sxs-lookup"><span data-stu-id="40919-126">Grants the right to execute a file.</span></span> <span data-ttu-id="40919-127">Per una directory, la directory può essere attraversata.</span><span class="sxs-lookup"><span data-stu-id="40919-127">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="40919-128"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**File \_ Elimina \_ elemento figlio (directory)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="40919-128"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="40919-129">Concede il diritto di eliminare una directory e tutti i file in esso contenuti, anche se i file sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="40919-129">Grants the right to delete a directory and all of the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="40919-130"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**File \_ Leggi \_ attributi** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="40919-130"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="40919-131">Concede il diritto di leggere gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="40919-131">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="40919-132"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**File \_ Scrivi \_ attributi** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="40919-132"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="40919-133">Concede il diritto di modificare gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="40919-133">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="40919-134"><span id="DELETE"></span><span id="delete"></span>**Elimina** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="40919-134"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="40919-135">Concede l'accesso DELETE.</span><span class="sxs-lookup"><span data-stu-id="40919-135">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="40919-136"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leggi \_ CONTROLLO** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="40919-136"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="40919-137">Concede l'accesso in lettura al descrittore di sicurezza e al proprietario.</span><span class="sxs-lookup"><span data-stu-id="40919-137">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="40919-138"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Scrivi \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="40919-138"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="40919-139">Concede l'accesso in scrittura all'elenco di controllo di accesso discrezionale (ACL).</span><span class="sxs-lookup"><span data-stu-id="40919-139">Grants write access to the discretionary access control list (ACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="40919-140"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Scrivi \_ PROPRIETARIO** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="40919-140"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="40919-141">Assegna il proprietario della scrittura.</span><span class="sxs-lookup"><span data-stu-id="40919-141">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="40919-142"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizza** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="40919-142"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="40919-143">Sincronizza l'accesso e consente a un processo di attendere che un oggetto entri nello stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="40919-143">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40919-144">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40919-144">Return value</span></span>

<span data-ttu-id="40919-145">Restituisce **true** se il chiamante dispone delle autorizzazioni specificate e **false** quando il chiamante non dispone delle autorizzazioni specificate.</span><span class="sxs-lookup"><span data-stu-id="40919-145">Returns **True** when the caller has the specified permissions, and **false** when the caller does not have the specified permissions.</span></span>

## <a name="requirements"></a><span data-ttu-id="40919-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40919-146">Requirements</span></span>



| <span data-ttu-id="40919-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="40919-147">Requirement</span></span> | <span data-ttu-id="40919-148">Valore</span><span class="sxs-lookup"><span data-stu-id="40919-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40919-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40919-149">Minimum supported client</span></span><br/> | <span data-ttu-id="40919-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40919-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40919-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40919-151">Minimum supported server</span></span><br/> | <span data-ttu-id="40919-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40919-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40919-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="40919-153">Namespace</span></span><br/>                | <span data-ttu-id="40919-154">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="40919-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="40919-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40919-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="40919-156"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="40919-156"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="40919-157">MOF</span><span class="sxs-lookup"><span data-stu-id="40919-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40919-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40919-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="40919-159">DLL</span><span class="sxs-lookup"><span data-stu-id="40919-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40919-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40919-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40919-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40919-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="40919-162">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="40919-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="40919-163">**Codecfile Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="40919-163">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

