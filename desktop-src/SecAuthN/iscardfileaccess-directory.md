---
description: Il metodo Directory recupera un elenco di file del tipo specificato dalla directory corrente.
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: ISCardFileAccess::D Metodo irectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Directory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 74293d4fa97a61133739cac75f17eaffed6e52b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880693"
---
# <a name="iscardfileaccessdirectory-method"></a><span data-ttu-id="66d0d-103">ISCardFileAccess::D Metodo irectory</span><span class="sxs-lookup"><span data-stu-id="66d0d-103">ISCardFileAccess::Directory method</span></span>

<span data-ttu-id="66d0d-104">\[Il metodo **directory** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="66d0d-104">\[The **Directory** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="66d0d-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="66d0d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="66d0d-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="66d0d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="66d0d-107">Il metodo **directory** recupera un elenco di file del tipo specificato dalla directory corrente.</span><span class="sxs-lookup"><span data-stu-id="66d0d-107">The **Directory** method retrieves a list of files of the specified type from the current directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="66d0d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66d0d-108">Syntax</span></span>


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a><span data-ttu-id="66d0d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="66d0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66d0d-110">*FileType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66d0d-110">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66d0d-111">Tipo di file di [*Smart Card*](../secgloss/s-gly.md) da elencare.</span><span class="sxs-lookup"><span data-stu-id="66d0d-111">Type of [*smart card*](../secgloss/s-gly.md) files to list.</span></span>



| <span data-ttu-id="66d0d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="66d0d-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="66d0d-113">Significato</span><span class="sxs-lookup"><span data-stu-id="66d0d-113">Meaning</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <span data-ttu-id="66d0d-114"><dt>**\_directory di tipi SC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d0d-114"><dt>**SC\_TYPE\_DIRECTORIES**</dt></span></span> </dl>           | <span data-ttu-id="66d0d-115">Elencare solo i file di directory.</span><span class="sxs-lookup"><span data-stu-id="66d0d-115">List directory files only.</span></span><br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <span data-ttu-id="66d0d-116"><dt>**\_file di tipo SC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d0d-116"><dt>**SC\_TYPE\_FILES**</dt></span></span> </dl>                             | <span data-ttu-id="66d0d-117">Elencare solo i file elementari.</span><span class="sxs-lookup"><span data-stu-id="66d0d-117">List elementary files only.</span></span><br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <span data-ttu-id="66d0d-118"><dt>**SC \_ digitare \_ tutti \_ i file**</dt></span><span class="sxs-lookup"><span data-stu-id="66d0d-118"><dt>**SC\_TYPE\_ALL\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="66d0d-119">Elencare sia la directory che i file elementari.</span><span class="sxs-lookup"><span data-stu-id="66d0d-119">List both directory and elementary files.</span></span><br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <span data-ttu-id="66d0d-120"><dt>**\_file di \_ directory di tipo SC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="66d0d-120"><dt>**SC\_TYPE\_DIRECTORY\_FILE**</dt></span></span> </dl> | <span data-ttu-id="66d0d-121">File di directory.</span><span class="sxs-lookup"><span data-stu-id="66d0d-121">Directory file.</span></span><br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <span data-ttu-id="66d0d-122"><dt>**SC \_ - \_ tipo \_ EF trasparente**</dt></span><span class="sxs-lookup"><span data-stu-id="66d0d-122"><dt>**SC\_TYPE\_TRANSPARENT\_EF**</dt></span></span> </dl> | <span data-ttu-id="66d0d-123">File elementare trasparente.</span><span class="sxs-lookup"><span data-stu-id="66d0d-123">Transparent elementary file.</span></span><br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <span data-ttu-id="66d0d-124"><dt>**\_tipo SC \_ fisso \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="66d0d-124"><dt>**SC\_TYPE\_FIXED\_EF**</dt></span></span> </dl>                   | <span data-ttu-id="66d0d-125">File elementare fisso lineare.</span><span class="sxs-lookup"><span data-stu-id="66d0d-125">Linear fixed elementary file.</span></span><br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <span data-ttu-id="66d0d-126"><dt>**SC \_ tipo \_ ciclico \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="66d0d-126"><dt>**SC\_TYPE\_CYCLIC\_EF**</dt></span></span> </dl>                | <span data-ttu-id="66d0d-127">File elementare ciclico.</span><span class="sxs-lookup"><span data-stu-id="66d0d-127">Cyclic elementary file.</span></span><br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <span data-ttu-id="66d0d-128"><dt>**\_variabile di tipo SC \_ \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="66d0d-128"><dt>**SC\_TYPE\_VARIABLE\_EF**</dt></span></span> </dl>          | <span data-ttu-id="66d0d-129">File elementare della variabile lineare.</span><span class="sxs-lookup"><span data-stu-id="66d0d-129">Linear variable elementary file.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="66d0d-130">*ppFileList* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="66d0d-130">*ppFileList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66d0d-131">Matrice di BSTR che rappresenta l'elenco di file che corrispondono all'identificatore in *FileType*.</span><span class="sxs-lookup"><span data-stu-id="66d0d-131">Array of BSTRs representing the list of files matching the specifier in *fileType*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66d0d-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66d0d-132">Return value</span></span>

<span data-ttu-id="66d0d-133">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="66d0d-133">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="66d0d-134">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="66d0d-134">Return code</span></span>                                                                                   | <span data-ttu-id="66d0d-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66d0d-135">Description</span></span>                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="66d0d-136"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="66d0d-136"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="66d0d-137">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="66d0d-137">Operation was completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="66d0d-138"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="66d0d-138"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="66d0d-139">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="66d0d-139">Invalid parameter.</span></span><br/>                             |
| <dl> <span data-ttu-id="66d0d-140"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="66d0d-140"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="66d0d-141">L'interfaccia non ha implementato questo metodo.</span><span class="sxs-lookup"><span data-stu-id="66d0d-141">The interface has not implemented this method.</span></span><br/> |
| <dl> <span data-ttu-id="66d0d-142"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="66d0d-142"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="66d0d-143">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="66d0d-143">Out of memory.</span></span><br/>                                 |
| <dl> <span data-ttu-id="66d0d-144"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="66d0d-144"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="66d0d-145">È stato passato un puntatore non valido per *ppFileList*.</span><span class="sxs-lookup"><span data-stu-id="66d0d-145">A bad pointer was passed in for *ppFileList*.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="66d0d-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="66d0d-146">Remarks</span></span>

<span data-ttu-id="66d0d-147">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="66d0d-147">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="66d0d-148">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="66d0d-148">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="66d0d-149">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="66d0d-149">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66d0d-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66d0d-150">Requirements</span></span>



| <span data-ttu-id="66d0d-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="66d0d-151">Requirement</span></span> | <span data-ttu-id="66d0d-152">Valore</span><span class="sxs-lookup"><span data-stu-id="66d0d-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="66d0d-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66d0d-153">Minimum supported client</span></span><br/> | <span data-ttu-id="66d0d-154">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="66d0d-154">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="66d0d-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66d0d-155">Minimum supported server</span></span><br/> | <span data-ttu-id="66d0d-156">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="66d0d-156">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="66d0d-157">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="66d0d-157">End of client support</span></span><br/>    | <span data-ttu-id="66d0d-158">Windows XP</span><span class="sxs-lookup"><span data-stu-id="66d0d-158">Windows XP</span></span><br/>                                |
| <span data-ttu-id="66d0d-159">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="66d0d-159">End of server support</span></span><br/>    | <span data-ttu-id="66d0d-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="66d0d-160">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="66d0d-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66d0d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d0d-162">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="66d0d-162">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
