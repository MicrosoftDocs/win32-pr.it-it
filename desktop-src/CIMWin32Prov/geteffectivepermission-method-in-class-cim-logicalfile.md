---
description: Determina se il chiamante dispone delle autorizzazioni aggregate sull'oggetto CIM \_ LogicalFile e della condivisione in cui risiede il file o la directory, come specificato dall'argomento Permissions.
ms.assetid: 7b6845df-2427-44a8-bd91-9a4ba65caa51
ms.tgt_platform: multiple
title: Metodo GetEffectivePermission della classe CIM_LogicalFile (aclui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cc578436c5d116e202911d2bb68edf7369564a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126498"
---
# <a name="geteffectivepermission-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="75ed9-103">Metodo GetEffectivePermission della classe CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="75ed9-103">GetEffectivePermission method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="75ed9-104">Il metodo **GetEffectivePermission** determina se il chiamante dispone delle autorizzazioni aggregate per l'oggetto [**CIM \_ LogicalFile**](cim-logicalfile.md) e della condivisione in cui risiede il file o la directory, come specificato dall'argomento *Permissions* .</span><span class="sxs-lookup"><span data-stu-id="75ed9-104">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_LogicalFile**](cim-logicalfile.md) object, and the share on which the file or directory resides, as specified by the *Permissions* argument.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75ed9-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="75ed9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="75ed9-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="75ed9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="75ed9-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="75ed9-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="75ed9-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="75ed9-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="75ed9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75ed9-109">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="75ed9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="75ed9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75ed9-111">*Autorizzazioni* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75ed9-111">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75ed9-112">Elenco delle autorizzazioni di cui l'utente può richiedere informazioni.</span><span class="sxs-lookup"><span data-stu-id="75ed9-112">List of permissions that the user can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="75ed9-113"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**File \_ LETTURA \_ dati (file) o \_ Directory elenco file \_ (directory)** (1)</span><span class="sxs-lookup"><span data-stu-id="75ed9-113"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="75ed9-114">Concede il diritto di leggere i dati dal file.</span><span class="sxs-lookup"><span data-stu-id="75ed9-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="75ed9-115">Per una directory, questo valore concede il diritto di elencare il contenuto della directory.</span><span class="sxs-lookup"><span data-stu-id="75ed9-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="75ed9-116"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**File \_ SCRITTURA di \_ dati (file) o file di \_ aggiunta \_ (directory)** (2)</span><span class="sxs-lookup"><span data-stu-id="75ed9-116"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="75ed9-117">Concede il diritto di scrivere i dati nel file.</span><span class="sxs-lookup"><span data-stu-id="75ed9-117">Grants the right to write data to the file.</span></span> <span data-ttu-id="75ed9-118">Per una directory, questo valore concede il diritto di creare un file nella directory.</span><span class="sxs-lookup"><span data-stu-id="75ed9-118">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="75ed9-119"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**File \_ ACCODA \_ dati (file) o \_ Aggiungi \_ sottodirectory (directory)** (4)</span><span class="sxs-lookup"><span data-stu-id="75ed9-119"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="75ed9-120">Concede il diritto di accodare i dati al file.</span><span class="sxs-lookup"><span data-stu-id="75ed9-120">Grants the right to append data to the file.</span></span> <span data-ttu-id="75ed9-121">Per una directory, questo valore concede il diritto di creare una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="75ed9-121">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="75ed9-122"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**File \_ Leggi \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="75ed9-122"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="75ed9-123">Concede il diritto di leggere gli attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="75ed9-123">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="75ed9-124"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**File \_ Scrivi \_ EA** (16)</span><span class="sxs-lookup"><span data-stu-id="75ed9-124"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="75ed9-125">Concede il diritto di scrivere attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="75ed9-125">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="75ed9-126"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**File \_ ESECUZIONE (file) o \_ attraversamento file (directory)** (32)</span><span class="sxs-lookup"><span data-stu-id="75ed9-126"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="75ed9-127">Concede il diritto di eseguire un file.</span><span class="sxs-lookup"><span data-stu-id="75ed9-127">Grants the right to execute a file.</span></span> <span data-ttu-id="75ed9-128">Per una directory, la directory può essere attraversata.</span><span class="sxs-lookup"><span data-stu-id="75ed9-128">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="75ed9-129"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**File \_ Elimina \_ elemento figlio (directory)** (64)</span><span class="sxs-lookup"><span data-stu-id="75ed9-129"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="75ed9-130">Concede il diritto di eliminare una directory e tutti i file in esso contenuti, anche se i file sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="75ed9-130">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="75ed9-131"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**File \_ Leggi \_ attributi** (128)</span><span class="sxs-lookup"><span data-stu-id="75ed9-131"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="75ed9-132">Concede il diritto di leggere gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="75ed9-132">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="75ed9-133"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**File \_ Scrivi \_ attributi** (256)</span><span class="sxs-lookup"><span data-stu-id="75ed9-133"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="75ed9-134">Concede il diritto di modificare gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="75ed9-134">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="75ed9-135"><span id="DELETE"></span><span id="delete"></span>**Elimina** (65536)</span><span class="sxs-lookup"><span data-stu-id="75ed9-135"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="75ed9-136">Concede l'accesso DELETE.</span><span class="sxs-lookup"><span data-stu-id="75ed9-136">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="75ed9-137"><span id="READ_CONTROL"></span><span id="read_control"></span>**Leggi \_ CONTROLLO** (131072)</span><span class="sxs-lookup"><span data-stu-id="75ed9-137"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="75ed9-138">Concede l'accesso in lettura al descrittore di sicurezza e al proprietario.</span><span class="sxs-lookup"><span data-stu-id="75ed9-138">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="75ed9-139"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Scrivi \_ Applicazione livello dati** (262144)</span><span class="sxs-lookup"><span data-stu-id="75ed9-139"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="75ed9-140">Concede l'accesso in scrittura all'ACL discrezionale.</span><span class="sxs-lookup"><span data-stu-id="75ed9-140">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="75ed9-141"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Scrivi \_ PROPRIETARIO** (524288)</span><span class="sxs-lookup"><span data-stu-id="75ed9-141"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="75ed9-142">Assegna il proprietario della scrittura.</span><span class="sxs-lookup"><span data-stu-id="75ed9-142">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="75ed9-143"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizza** (1048576)</span><span class="sxs-lookup"><span data-stu-id="75ed9-143"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="75ed9-144">Sincronizza l'accesso e consente a un processo di attendere che un oggetto entri nello stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="75ed9-144">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75ed9-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75ed9-145">Return value</span></span>

<span data-ttu-id="75ed9-146">Restituisce **true** se la chiamata dispone dell'autorizzazione necessaria. in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="75ed9-146">Returns **True** if the call has the necessary permission; otherwise, it returns **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="75ed9-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="75ed9-147">Remarks</span></span>

<span data-ttu-id="75ed9-148">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="75ed9-148">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="75ed9-149">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="75ed9-149">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="75ed9-150">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="75ed9-150">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="75ed9-151">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="75ed9-151">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="75ed9-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75ed9-152">Requirements</span></span>



| <span data-ttu-id="75ed9-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="75ed9-153">Requirement</span></span> | <span data-ttu-id="75ed9-154">Valore</span><span class="sxs-lookup"><span data-stu-id="75ed9-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75ed9-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75ed9-155">Minimum supported client</span></span><br/> | <span data-ttu-id="75ed9-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75ed9-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75ed9-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75ed9-157">Minimum supported server</span></span><br/> | <span data-ttu-id="75ed9-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75ed9-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75ed9-159">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="75ed9-159">Namespace</span></span><br/>                | <span data-ttu-id="75ed9-160">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="75ed9-160">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="75ed9-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75ed9-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="75ed9-162"><dt>Aclui. h</dt></span><span class="sxs-lookup"><span data-stu-id="75ed9-162"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="75ed9-163">MOF</span><span class="sxs-lookup"><span data-stu-id="75ed9-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75ed9-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75ed9-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="75ed9-165">DLL</span><span class="sxs-lookup"><span data-stu-id="75ed9-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75ed9-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75ed9-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75ed9-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75ed9-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ed9-168">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="75ed9-168">**CIM\_LogicalFile**</span></span>](geteffectivepermission-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="75ed9-169">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="75ed9-169">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

