---
description: Le classi WMI che rappresentano file o directory, ad esempio Win32 \_ codecfile o CIM \_ DataFile, contengono una proprietà AccessMask.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Costanti dei diritti di accesso a file e directory (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0ddca31034ffde79fa9d9ff902a364cf07e311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324876"
---
# <a name="file-and-directory-access-rights-constants"></a><span data-ttu-id="e7b03-103">Costanti dei diritti di accesso a file e directory</span><span class="sxs-lookup"><span data-stu-id="e7b03-103">File and Directory Access Rights Constants</span></span>

<span data-ttu-id="e7b03-104">Le classi WMI che rappresentano file o directory, ad esempio [**Win32 \_ codecfile**](/windows/desktop/CIMWin32Prov/win32-codecfile) o [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), contengono una proprietà **accessMask** .</span><span class="sxs-lookup"><span data-stu-id="e7b03-104">WMI classes that represent files or directories, such as [**Win32\_CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile) or [**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), contain an **AccessMask** property.</span></span> <span data-ttu-id="e7b03-105">Questa proprietà contiene le impostazioni di bit che specificano i diritti di accesso che un utente o un gruppo deve avere per un accesso o operazioni specifiche sul file.</span><span class="sxs-lookup"><span data-stu-id="e7b03-105">This property contains bit settings that specify the access rights a user or group must have for specific access or operations on the file.</span></span> <span data-ttu-id="e7b03-106">Per ulteriori informazioni, vedere [diritti di accesso e sicurezza dei file](/windows/desktop/FileIO/file-security-and-access-rights) e [modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="e7b03-106">For more information, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="e7b03-107">Le classi di file o directory contenenti una proprietà **accessMask** includono:</span><span class="sxs-lookup"><span data-stu-id="e7b03-107">The file or directory classes which contain an **AccessMask** property include:</span></span>

-   [<span data-ttu-id="e7b03-108">**File di \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="e7b03-108">**CIM\_DataFile**</span></span>](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [<span data-ttu-id="e7b03-109">**\_Directory CIM**</span><span class="sxs-lookup"><span data-stu-id="e7b03-109">**CIM\_Directory**</span></span>](/windows/desktop/CIMWin32Prov/cim-directory)
-   [<span data-ttu-id="e7b03-110">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="e7b03-110">**CIM\_LogicalFile**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [<span data-ttu-id="e7b03-111">**Codecfile Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="e7b03-111">**Win32\_CodecFile**</span></span>](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [<span data-ttu-id="e7b03-112">**\_Directory Win32**</span><span class="sxs-lookup"><span data-stu-id="e7b03-112">**Win32\_Directory**</span></span>](/windows/desktop/CIMWin32Prov/win32-directory)
-   <span data-ttu-id="e7b03-113">[**\_NTEventLogFile Win32**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7b03-113">[**Win32\_NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))</span></span>
-   [<span data-ttu-id="e7b03-114">**\_Condivisione Win32**</span><span class="sxs-lookup"><span data-stu-id="e7b03-114">**Win32\_Share**</span></span>](/windows/desktop/CIMWin32Prov/win32-share)
-   [<span data-ttu-id="e7b03-115">**\_ShortcutFile Win32**</span><span class="sxs-lookup"><span data-stu-id="e7b03-115">**Win32\_ShortcutFile**</span></span>](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

<span data-ttu-id="e7b03-116">Nell'elenco seguente sono elencati i valori dei diritti di accesso a file e directory nella proprietà **accessMask** .</span><span class="sxs-lookup"><span data-stu-id="e7b03-116">The following list lists the values for file and directory access rights in the **AccessMask** property.</span></span> <span data-ttu-id="e7b03-117">Questa proprietà è una bitmap.</span><span class="sxs-lookup"><span data-stu-id="e7b03-117">This property is a bitmap.</span></span>

<dl> <dt>

<span data-ttu-id="e7b03-118"><span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**FILE \_ letti \_ dati**</span><span class="sxs-lookup"><span data-stu-id="e7b03-118"><span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**FILE\_READ\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-119">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="e7b03-119">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-120">Concede il diritto di leggere i dati dal file.</span><span class="sxs-lookup"><span data-stu-id="e7b03-120">Grants the right to read data from the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-121"><span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**\_Directory elenco \_ file**</span><span class="sxs-lookup"><span data-stu-id="e7b03-121"><span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-122">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="e7b03-122">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-123">Concede il diritto di leggere i dati dal file.</span><span class="sxs-lookup"><span data-stu-id="e7b03-123">Grants the right to read data from the file.</span></span> <span data-ttu-id="e7b03-124">Per una directory, questo valore concede il diritto di elencare il contenuto della directory.</span><span class="sxs-lookup"><span data-stu-id="e7b03-124">For a directory, this value grants the right to list the contents of the directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-125"><span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**\_dati di scrittura file \_**</span><span class="sxs-lookup"><span data-stu-id="e7b03-125"><span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**FILE\_WRITE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-126">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="e7b03-126">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-127">Concede il diritto di scrivere i dati nel file.</span><span class="sxs-lookup"><span data-stu-id="e7b03-127">Grants the right to write data to the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-128"><span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**file \_ Aggiungi \_ file**</span><span class="sxs-lookup"><span data-stu-id="e7b03-128"><span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**FILE\_ADD\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-129">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="e7b03-129">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-130">Concede il diritto di scrivere i dati nel file.</span><span class="sxs-lookup"><span data-stu-id="e7b03-130">Grants the right to write data to the file.</span></span> <span data-ttu-id="e7b03-131">Per una directory, questo valore concede il diritto di creare un file nella directory.</span><span class="sxs-lookup"><span data-stu-id="e7b03-131">For a directory, this value grants the right to create a file in the directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-132"><span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**\_dati Accodamento file \_**</span><span class="sxs-lookup"><span data-stu-id="e7b03-132"><span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**FILE\_APPEND\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="e7b03-133">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-134">Concede il diritto di accodare i dati al file.</span><span class="sxs-lookup"><span data-stu-id="e7b03-134">Grants the right to append data to the file.</span></span> <span data-ttu-id="e7b03-135">Per una directory, questo valore concede il diritto di creare una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="e7b03-135">For a directory, this value grants the right to create a subdirectory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-136"><span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**FILE \_ Aggiungi \_ sottodirectory**</span><span class="sxs-lookup"><span data-stu-id="e7b03-136"><span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-137">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="e7b03-137">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-138">Concede il diritto di accodare i dati al file.</span><span class="sxs-lookup"><span data-stu-id="e7b03-138">Grants the right to append data to the file.</span></span> <span data-ttu-id="e7b03-139">Per una directory, questo valore concede il diritto di creare una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="e7b03-139">For a directory, this value grants the right to create a subdirectory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-140"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**\_lettura file \_ EA**</span><span class="sxs-lookup"><span data-stu-id="e7b03-140"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-141">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="e7b03-141">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-142">Concede il diritto di leggere gli attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="e7b03-142">Grants the right to read extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-143"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**\_scrittura file \_ EA**</span><span class="sxs-lookup"><span data-stu-id="e7b03-143"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-144">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="e7b03-144">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-145">Concede il diritto di scrivere attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="e7b03-145">Grants the right to write extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-146"><span id="FILE_EXECUTE"></span><span id="file_execute"></span>**\_esecuzione file**</span><span class="sxs-lookup"><span data-stu-id="e7b03-146"><span id="FILE_EXECUTE"></span><span id="file_execute"></span>**FILE\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-147">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="e7b03-147">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-148">Concede il diritto di eseguire un file.</span><span class="sxs-lookup"><span data-stu-id="e7b03-148">Grants the right to execute a file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-149"><span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**\_attraversamento file**</span><span class="sxs-lookup"><span data-stu-id="e7b03-149"><span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**FILE\_TRAVERSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-150">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="e7b03-150">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-151">Concede il diritto di eseguire un file.</span><span class="sxs-lookup"><span data-stu-id="e7b03-151">Grants the right to execute a file.</span></span> <span data-ttu-id="e7b03-152">Per una directory, la directory può essere attraversata.</span><span class="sxs-lookup"><span data-stu-id="e7b03-152">For a directory, the directory can be traversed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-153"><span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**\_Elimina file \_ figlio**</span><span class="sxs-lookup"><span data-stu-id="e7b03-153"><span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-154">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="e7b03-154">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-155">Concede il diritto di eliminare una directory e tutti i file in esso contenuti (elementi figlio), anche se i file sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e7b03-155">Grants the right to delete a directory and all the files it contains (its children), even if the files are read-only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-156"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**\_attributi di lettura file \_**</span><span class="sxs-lookup"><span data-stu-id="e7b03-156"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-157">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="e7b03-157">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-158">Concede il diritto di leggere gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="e7b03-158">Grants the right to read file attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-159"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**\_attributi di scrittura file \_**</span><span class="sxs-lookup"><span data-stu-id="e7b03-159"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-160">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="e7b03-160">256 (0x100)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-161">Concede il diritto di modificare gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="e7b03-161">Grants the right to change file attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-162"><span id="DELETE"></span><span id="delete"></span>**ELIMINARE**</span><span class="sxs-lookup"><span data-stu-id="e7b03-162"><span id="DELETE"></span><span id="delete"></span>**DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-163">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="e7b03-163">65536 (0x10000)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-164">Concede il diritto di eliminare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e7b03-164">Grants the right to delete the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-165"><span id="READ_CONTROL"></span><span id="read_control"></span>**controllo di lettura \_**</span><span class="sxs-lookup"><span data-stu-id="e7b03-165"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-166">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="e7b03-166">131072 (0x20000)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-167">Concede il diritto di leggere le informazioni nel descrittore di sicurezza per l'oggetto, senza includere le informazioni nell'elenco SACL.</span><span class="sxs-lookup"><span data-stu-id="e7b03-167">Grants the right to read the information in the security descriptor for the object, not including the information in the SACL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-168"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Scrivi \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="e7b03-168"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-169">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="e7b03-169">262144 (0x40000)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-170">Concede il diritto di modificare l'elenco DACL nel descrittore di sicurezza dell'oggetto per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e7b03-170">Grants the right to modify the DACL in the object security descriptor for the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-171"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Scrivi \_ proprietario**</span><span class="sxs-lookup"><span data-stu-id="e7b03-171"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-172">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="e7b03-172">524288 (0x80000)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-173">Concede il diritto di modificare il proprietario nel descrittore di sicurezza per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e7b03-173">Grants the right to change the owner in the security descriptor for the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e7b03-174"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SINCRONIZZARE**</span><span class="sxs-lookup"><span data-stu-id="e7b03-174"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7b03-175">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="e7b03-175">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="e7b03-176">Concede il diritto di utilizzare l'oggetto per la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e7b03-176">Grants the right to use the object for synchronization.</span></span> <span data-ttu-id="e7b03-177">Questo consente a un processo di attendere fino a quando l'oggetto non è in stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="e7b03-177">This enables a process to wait until the object is in signaled state.</span></span> <span data-ttu-id="e7b03-178">Alcuni tipi di oggetto non supportano questo diritto di accesso.</span><span class="sxs-lookup"><span data-stu-id="e7b03-178">Some object types do not support this access right.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7b03-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7b03-179">Requirements</span></span>



| <span data-ttu-id="e7b03-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b03-180">Requirement</span></span> | <span data-ttu-id="e7b03-181">Valore</span><span class="sxs-lookup"><span data-stu-id="e7b03-181">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b03-182">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7b03-182">Header</span></span><br/> | <dl> <span data-ttu-id="e7b03-183"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7b03-183"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7b03-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7b03-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b03-185">Costanti di sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="e7b03-185">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="e7b03-186">Gestione della sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="e7b03-186">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

