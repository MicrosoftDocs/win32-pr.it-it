---
description: Determina se il chiamante dispone delle autorizzazioni aggregate sull'oggetto CIM \_ DeviceFile e della condivisione in cui risiede il file o la directory, come specificato dall'argomento di autorizzazione.
ms.assetid: e566f1f6-773e-4ecb-8145-369afaad0f99
ms.tgt_platform: multiple
title: Metodo GetEffectivePermission della classe CIM_DeviceFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4b74c489c41b3da83f0e009526af225fd7de889
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126504"
---
# <a name="geteffectivepermission-method-of-the-cim_devicefile-class"></a><span data-ttu-id="1ecc1-103">Metodo GetEffectivePermission della classe CIM \_ DeviceFile</span><span class="sxs-lookup"><span data-stu-id="1ecc1-103">GetEffectivePermission method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="1ecc1-104">Il metodo **GetEffectivePermission** determina se il chiamante dispone delle autorizzazioni aggregate per l'oggetto [**CIM \_ DeviceFile**](cim-devicefile.md) e della condivisione in cui risiede il file o la directory, come specificato dall'argomento di **autorizzazione** .</span><span class="sxs-lookup"><span data-stu-id="1ecc1-104">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_DeviceFile**](cim-devicefile.md) object, and the share on which the file or directory resides, as specified by the **Permission** argument.</span></span> <span data-ttu-id="1ecc1-105">Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="1ecc1-105">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ecc1-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1ecc1-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1ecc1-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1ecc1-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="1ecc1-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1ecc1-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1ecc1-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1ecc1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ecc1-110">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="1ecc1-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ecc1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ecc1-112">*Autorizzazioni* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ecc1-112">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ecc1-113">Elenco delle autorizzazioni di cui il chiamante può richiedere informazioni.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-113">List of permissions that the caller can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="1ecc1-114"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**File \_ LEGGERE la \_ directory dell'elenco di file (file) di dati ( \_ \_ Directory)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="1ecc1-114"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="1ecc1-115">Concede il diritto di leggere i dati dal file.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-115">Grants the right to read data from the file.</span></span> <span data-ttu-id="1ecc1-116">Per una directory, questo valore concede il diritto di elencare il contenuto della directory.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-116">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="1ecc1-117"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**File \_ Scrivi file di \_ dati (file) \_ Aggiungi \_ file (directory)** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="1ecc1-117"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="1ecc1-118">Concede il diritto di scrivere i dati nel file.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-118">Grants the right to write data to the file.</span></span> <span data-ttu-id="1ecc1-119">Per una directory, questo valore concede il diritto di creare un file nella directory.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-119">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="1ecc1-120"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**File \_ ACCODA \_ file di dati (file) \_ Aggiungi \_ sottodirectory (directory)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="1ecc1-120"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="1ecc1-121">Concede il diritto di accodare i dati al file.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-121">Grants the right to append data to the file.</span></span> <span data-ttu-id="1ecc1-122">Per una directory, questo valore concede il diritto di creare una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-122">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="1ecc1-123"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**File \_ Leggi \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="1ecc1-123"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="1ecc1-124">Concede il diritto di leggere gli attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-124">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="1ecc1-125"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**File \_ Scrivi \_ EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="1ecc1-125"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="1ecc1-126">Concede il diritto di scrivere attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-126">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>

<span data-ttu-id="1ecc1-127"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**File \_ Attraversamento FILE di esecuzione (file) ( \_ Directory)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="1ecc1-127"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="1ecc1-128">Concede il diritto di eseguire un file.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-128">Grants the right to execute a file.</span></span> <span data-ttu-id="1ecc1-129">Per una directory, la directory può essere attraversata.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-129">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="1ecc1-130"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**File \_ Elimina \_ elemento figlio (directory)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="1ecc1-130"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="1ecc1-131">Concede il diritto di eliminare una directory e tutti i file in esso contenuti, anche se i file sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-131">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="1ecc1-132"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**File \_ Leggi \_ attributi** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="1ecc1-132"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="1ecc1-133">Concede il diritto di leggere gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-133">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="1ecc1-134"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**File \_ Scrivi \_ attributi** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="1ecc1-134"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="1ecc1-135">Concede il diritto di modificare gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-135">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="1ecc1-136"><span id="DELETE"></span><span id="delete"></span>**Elimina** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="1ecc1-136"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="1ecc1-137">Concede l'accesso DELETE.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-137">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="1ecc1-138"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leggi \_ CONTROLLO** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="1ecc1-138"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="1ecc1-139">Concede l'accesso in lettura al descrittore di sicurezza e al proprietario.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-139">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="1ecc1-140"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Scrivi \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="1ecc1-140"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="1ecc1-141">Concede l'accesso in scrittura all'ACL discrezionale.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-141">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="1ecc1-142"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Scrivi \_ PROPRIETARIO** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="1ecc1-142"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="1ecc1-143">Assegna il proprietario della scrittura.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-143">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="1ecc1-144"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizza** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="1ecc1-144"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="1ecc1-145">Sincronizza l'accesso e consente a un processo di attendere che un oggetto entri nello stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-145">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ecc1-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ecc1-146">Return value</span></span>

<span data-ttu-id="1ecc1-147">Restituisce **true** se la chiamata dispone dell'autorizzazione necessaria. in caso contrario, restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-147">Returns **True** if the call has the necessary permission; otherwise, it returns **True**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ecc1-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ecc1-148">Remarks</span></span>

<span data-ttu-id="1ecc1-149">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1ecc1-150">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1ecc1-151">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1ecc1-152">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="1ecc1-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ecc1-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ecc1-153">Requirements</span></span>



| <span data-ttu-id="1ecc1-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ecc1-154">Requirement</span></span> | <span data-ttu-id="1ecc1-155">Valore</span><span class="sxs-lookup"><span data-stu-id="1ecc1-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ecc1-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ecc1-156">Minimum supported client</span></span><br/> | <span data-ttu-id="1ecc1-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ecc1-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1ecc1-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ecc1-158">Minimum supported server</span></span><br/> | <span data-ttu-id="1ecc1-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ecc1-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1ecc1-160">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1ecc1-160">Namespace</span></span><br/>                | <span data-ttu-id="1ecc1-161">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1ecc1-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1ecc1-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ecc1-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ecc1-163"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ecc1-163"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="1ecc1-164">MOF</span><span class="sxs-lookup"><span data-stu-id="1ecc1-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ecc1-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ecc1-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ecc1-166">DLL</span><span class="sxs-lookup"><span data-stu-id="1ecc1-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ecc1-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ecc1-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ecc1-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ecc1-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ecc1-169">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="1ecc1-169">**CIM\_DeviceFile**</span></span>](geteffectivepermission-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="1ecc1-170">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="1ecc1-170">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

