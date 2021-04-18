---
description: Determina se il chiamante dispone delle autorizzazioni aggregate per l' \_ oggetto DataFile del file CIM e della condivisione in cui risiede il file o la directory, come specificato dall'argomento di autorizzazione. Questo metodo viene ereditato da \_ LOGICALFILE CIM.
ms.assetid: 57eadc2e-36ef-4d3c-932f-6f7fafb2b9a4
ms.tgt_platform: multiple
title: Metodo GetEffectivePermission della classe CIM_DataFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 109e4953b310f9465c4523a9e80ca401c225f885
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304686"
---
# <a name="geteffectivepermission-method-of-the-cim_datafile-class"></a><span data-ttu-id="34538-104">Metodo GetEffectivePermission della classe del file di \_ DataFile CIM</span><span class="sxs-lookup"><span data-stu-id="34538-104">GetEffectivePermission method of the CIM\_DataFile class</span></span>

<span data-ttu-id="34538-105">Il metodo **GetEffectivePermission** determina se il chiamante dispone delle autorizzazioni aggregate per l' [**oggetto \_ DataFile**](cim-datafile.md) del file CIM e della condivisione in cui risiede il file o la directory, come specificato dall'argomento di **autorizzazione** .</span><span class="sxs-lookup"><span data-stu-id="34538-105">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_DataFile**](cim-datafile.md) object, and the share on which the file or directory resides, as specified by the **Permission** argument.</span></span> <span data-ttu-id="34538-106">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="34538-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34538-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="34538-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="34538-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="34538-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="34538-109">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="34538-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="34538-110">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="34538-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="34538-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34538-111">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="34538-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="34538-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34538-113">*Autorizzazioni* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34538-113">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34538-114">Elenco delle autorizzazioni di cui il chiamante può richiedere informazioni.</span><span class="sxs-lookup"><span data-stu-id="34538-114">List of permissions that the caller can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="34538-115"><span id="FILE_READ_DATA__file_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**File \_ LEGGERE la \_ directory dell'elenco di file (file) di dati ( \_ \_ Directory)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="34538-115"><span id="FILE_READ_DATA__file_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file)FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="34538-116">Concede il diritto di leggere i dati dal file.</span><span class="sxs-lookup"><span data-stu-id="34538-116">Grants the right to read data from the file.</span></span> <span data-ttu-id="34538-117">Per una directory, questo valore concede il diritto di elencare il contenuto della directory.</span><span class="sxs-lookup"><span data-stu-id="34538-117">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="34538-118"><span id="FILE_WRITE_DATA__file_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE_FILE_ADD_FILE__DIRECTORY_"></span>**File \_ Scrivi file di \_ dati (file) \_ Aggiungi \_ file (directory)** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="34538-118"><span id="FILE_WRITE_DATA__file_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file)FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="34538-119">Concede il diritto di scrivere i dati nel file.</span><span class="sxs-lookup"><span data-stu-id="34538-119">Grants the right to write data to the file.</span></span> <span data-ttu-id="34538-120">Per una directory, questo valore concede il diritto di creare un file nella directory.</span><span class="sxs-lookup"><span data-stu-id="34538-120">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="34538-121"><span id="FILE_APPEND_DATA__file_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**File \_ ACCODA \_ file di dati (file) \_ Aggiungi \_ sottodirectory (directory)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="34538-121"><span id="FILE_APPEND_DATA__file_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file)FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="34538-122">Concede il diritto di accodare i dati al file.</span><span class="sxs-lookup"><span data-stu-id="34538-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="34538-123">Per una directory, questo valore concede il diritto di creare una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="34538-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="34538-124"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**File \_ Leggi \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="34538-124"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="34538-125">Concede il diritto di leggere gli attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="34538-125">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="34538-126"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**File \_ Scrivi \_ EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="34538-126"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="34538-127">Concede il diritto di scrivere attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="34538-127">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file_FILE_TRAVERSE__directory_"></span><span id="file_execute__file_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="34538-128"><span id="FILE_EXECUTE__file_FILE_TRAVERSE__directory_"></span><span id="file_execute__file_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE_FILE_TRAVERSE__DIRECTORY_"></span>**File \_ Attraversamento FILE di esecuzione (file) ( \_ Directory)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="34538-128"><span id="FILE_EXECUTE__file_FILE_TRAVERSE__directory_"></span><span id="file_execute__file_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file)FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="34538-129">Concede il diritto di eseguire un file.</span><span class="sxs-lookup"><span data-stu-id="34538-129">Grants the right to execute a file.</span></span> <span data-ttu-id="34538-130">Per una directory, la directory può essere attraversata.</span><span class="sxs-lookup"><span data-stu-id="34538-130">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="34538-131"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**File \_ Elimina \_ elemento figlio (directory)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="34538-131"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="34538-132">Concede il diritto di eliminare una directory e tutti i file in esso contenuti, anche se i file sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="34538-132">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="34538-133"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**File \_ Leggi \_ attributi** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="34538-133"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="34538-134">Concede il diritto di leggere gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="34538-134">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="34538-135"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**File \_ Scrivi \_ attributi** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="34538-135"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="34538-136">Concede il diritto di modificare gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="34538-136">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="34538-137"><span id="DELETE"></span><span id="delete"></span>**Elimina** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="34538-137"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="34538-138">Concede l'accesso DELETE.</span><span class="sxs-lookup"><span data-stu-id="34538-138">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="34538-139"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leggi \_ CONTROLLO** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="34538-139"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="34538-140">Concede l'accesso in lettura al descrittore di sicurezza e al proprietario.</span><span class="sxs-lookup"><span data-stu-id="34538-140">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="34538-141"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Scrivi \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="34538-141"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="34538-142">Concede l'accesso in scrittura all'ACL discrezionale.</span><span class="sxs-lookup"><span data-stu-id="34538-142">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="34538-143"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Scrivi \_ PROPRIETARIO** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="34538-143"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="34538-144">Assegna il proprietario della scrittura.</span><span class="sxs-lookup"><span data-stu-id="34538-144">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="34538-145"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizza** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="34538-145"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="34538-146">Sincronizza l'accesso e consente a un processo di attendere che un oggetto entri nello stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="34538-146">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34538-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34538-147">Return value</span></span>

<span data-ttu-id="34538-148">Restituisce **true** se la chiamata dispone dell'autorizzazione necessaria. in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="34538-148">Returns **True** if the call has the necessary permission; otherwise, it returns **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="34538-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="34538-149">Remarks</span></span>

<span data-ttu-id="34538-150">Il metodo **GetEffectivePermission** nel file di [**\_ DataFile CIM**](cim-datafile.md) viene implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="34538-150">The **GetEffectivePermission** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="34538-151">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="34538-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="34538-152">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="34538-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="34538-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34538-153">Requirements</span></span>



| <span data-ttu-id="34538-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="34538-154">Requirement</span></span> | <span data-ttu-id="34538-155">Valore</span><span class="sxs-lookup"><span data-stu-id="34538-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34538-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34538-156">Minimum supported client</span></span><br/> | <span data-ttu-id="34538-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34538-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="34538-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34538-158">Minimum supported server</span></span><br/> | <span data-ttu-id="34538-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34538-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="34538-160">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="34538-160">Namespace</span></span><br/>                | <span data-ttu-id="34538-161">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="34538-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="34538-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34538-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="34538-163"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="34538-163"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="34538-164">MOF</span><span class="sxs-lookup"><span data-stu-id="34538-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34538-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34538-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="34538-166">DLL</span><span class="sxs-lookup"><span data-stu-id="34538-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34538-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34538-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34538-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34538-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34538-169">File di \_ DataFile CIM</span><span class="sxs-lookup"><span data-stu-id="34538-169">CIM\_DataFile</span></span>](geteffectivepermission-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="34538-170">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="34538-170">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="34538-171">Attività WMI: file e cartelle</span><span class="sxs-lookup"><span data-stu-id="34538-171">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="34538-172">**Costanti dei diritti di accesso a file e directory**</span><span class="sxs-lookup"><span data-stu-id="34538-172">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

