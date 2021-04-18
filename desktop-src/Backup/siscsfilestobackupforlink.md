---
title: Funzione SisCSFilesToBackupForLink (sisbkup. h)
description: Restituisce informazioni che descrivono i file dell'archivio comune a cui punta il collegamento SIS specificato.
ms.assetid: 0580c34e-195a-4a2c-893f-bc339dcc88d7
keywords:
- Backup della funzione SisCSFilesToBackupForLink
topic_type:
- apiref
api_name:
- SisCSFilesToBackupForLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27d4f52728d662f43efed85d662874bd4b008947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301278"
---
# <a name="siscsfilestobackupforlink-function"></a><span data-ttu-id="9bb8c-104">SisCSFilesToBackupForLink (funzione)</span><span class="sxs-lookup"><span data-stu-id="9bb8c-104">SisCSFilesToBackupForLink function</span></span>

<span data-ttu-id="9bb8c-105">La funzione **SisCSFilesToBackupForLink** restituisce informazioni che descrivono i file dell'archivio comune a cui punta il collegamento SIS specificato.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-105">The **SisCSFilesToBackupForLink** function returns information describing the common-store files the specified SIS link points to.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bb8c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9bb8c-106">Syntax</span></span>


```C++
BOOL SisCSFilesToBackupForLink(
  _In_  PVOID  sisBackupStructure,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PVOID  thisFileContext,
  _Out_ PVOID  *matchingFileContext,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a><span data-ttu-id="9bb8c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bb8c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bb8c-108">*sisBackupStructure* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9bb8c-108">*sisBackupStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bb8c-109">Puntatore alla struttura di backup SIS restituita da [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="9bb8c-109">Pointer to the SIS backup structure returned from [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="9bb8c-110">*reparseData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9bb8c-110">*reparseData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bb8c-111">Puntatore al contenuto del punto di analisi SIS.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-111">Pointer to the contents of the SIS reparse point.</span></span> <span data-ttu-id="9bb8c-112">Questo reparse point contiene dati che descrivono un collegamento SIS.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-112">This reparse point contains data describing a SIS link.</span></span> <span data-ttu-id="9bb8c-113">Per recuperare i dati di reparse point per un file, usare il codice di controllo [**FSCTL \_ get \_ reparse \_ Point**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .</span><span class="sxs-lookup"><span data-stu-id="9bb8c-113">To retrieve the reparse point data for a file, use the [**FSCTL\_GET\_REPARSE\_POINT**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) control code.</span></span>

</dd> <dt>

<span data-ttu-id="9bb8c-114">*reparseDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9bb8c-114">*reparseDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bb8c-115">Dimensioni del contenuto del punto di analisi SIS a cui punta *reparseData* in byte.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-115">Size of the contents of the SIS reparse point pointed to by *reparseData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9bb8c-116">*thisFileContext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9bb8c-116">*thisFileContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bb8c-117">Puntatore a una stringa di contesto fornita dall'applicazione di backup che chiama questa funzione.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-117">Pointer to a context string supplied by the backup application calling this function.</span></span> <span data-ttu-id="9bb8c-118">Il contenuto di questa stringa di contenuto è determinato interamente da questa applicazione di backup e non è interpretato dall'API di backup SIS.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-118">The contents of this content string are entirely determined by this backup application and is not interpreted by the SIS Backup API.</span></span> <span data-ttu-id="9bb8c-119">Questo parametro è facoltativo; Se non viene usato, impostare il valore di questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-119">This parameter is optional; if not used, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="9bb8c-120">Il valore di questo parametro non verrà elaborato in questo caso.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-120">The value of this parameter will not be processed in this case.</span></span>

</dd> <dt>

<span data-ttu-id="9bb8c-121">*matchingFileContext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9bb8c-121">*matchingFileContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bb8c-122">Puntatore doppiamente indiretto alla stringa di contesto del collegamento SIS identificato dalle informazioni passate nei primi quattro parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-122">Doubly-indirect pointer to the context string of the SIS link identified by the information passed in the first four parameters of this function.</span></span> <span data-ttu-id="9bb8c-123">Questo parametro è facoltativo; Se non viene specificata una stringa di contesto come valore del parametro *thisFileContext* , impostare il valore di questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-123">This parameter is optional; if a context string is not provided as the value of the *thisFileContext* parameter, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="9bb8c-124">Il valore di questo parametro non verrà elaborato in questo caso.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-124">The value of this parameter will not be processed in this case.</span></span>

</dd> <dt>

<span data-ttu-id="9bb8c-125">*countOfCommonStoreFilesToBackUp* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9bb8c-125">*countOfCommonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bb8c-126">Numero di file elencati nel parametro *commonStoreFilesToBackUp* .</span><span class="sxs-lookup"><span data-stu-id="9bb8c-126">Number of files listed in the *commonStoreFilesToBackUp* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9bb8c-127">*commonStoreFilesToBackUp* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9bb8c-127">*commonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bb8c-128">Puntatore a una matrice di nomi di file.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-128">Pointer to an array of file names.</span></span> <span data-ttu-id="9bb8c-129">È necessario eseguire il backup di questi file nello stesso momento e nello stesso modo dei file di archivio comuni richiesti da [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span><span class="sxs-lookup"><span data-stu-id="9bb8c-129">These files should be backed up at the same time and in the same manner as the common-store files requested by [**SisCreateBackupStructure**](siscreatebackupstructure.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bb8c-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9bb8c-130">Return value</span></span>

<span data-ttu-id="9bb8c-131">Questa funzione restituisce **true** se viene completata correttamente e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-131">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="9bb8c-132">Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-132">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bb8c-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bb8c-133">Remarks</span></span>

<span data-ttu-id="9bb8c-134">L'applicazione di backup deve chiamare questa funzione una sola volta per ogni file di collegamento SIS di cui viene eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-134">The backup application should call this function only once for each SIS link file being backed up.</span></span>

<span data-ttu-id="9bb8c-135">L'applicazione di backup è in grado di identificare un punto di analisi SIS in base al tag, IO \_ reparse \_ tag \_ SIS.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-135">The backup application can identify a SIS reparse point by its tag, IO\_REPARSE\_TAG\_SIS.</span></span> <span data-ttu-id="9bb8c-136">Questo tag è definito in Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-136">This tag is defined in Winnt.h.</span></span>

<span data-ttu-id="9bb8c-137">Se questo punto di analisi identificato dal valore del parametro *reparseData* descrive la prima istanza di un file di cui eseguire il backup, la funzione restituirà **null** come valore del parametro *matchingFileContext* e inizializza il valore della matrice *commonStoreFilesToBackUp* di stringhe con i nomi del file o dei file di archivio comuni di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-137">If this reparse point identified by the value of the *reparseData* parameter describes the first instance of a file to be backed up, this function will return **NULL** as the value of the *matchingFileContext* parameter, and initialize the value of the *commonStoreFilesToBackUp* array of strings with the names of the common-store file or files to be backed up.</span></span> <span data-ttu-id="9bb8c-138">In caso contrario, questa funzione imposterà il valore del parametro *matchingFileContext* sulla stringa di contesto corrispondente alla prima istanza del file specificato e imposterà il valore del parametro *countOfCommonStoreFilesToBackUp* su 0.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-138">Otherwise, this function will set the value of the *matchingFileContext* parameter to the context string corresponding to the first instance of the specified file and set the value of the *countOfCommonStoreFilesToBackUp* parameter to 0.</span></span> <span data-ttu-id="9bb8c-139">Se sono presenti più file di archivio comuni che corrispondono al collegamento specificato, il valore del parametro *thisFileContext* sarà la stringa di contesto corrispondente al primo file di archivio comune restituito nella matrice, ovvero commonStoreFilesToBackUp \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="9bb8c-139">If there are multiple common-store files corresponding to the specified link, the value of the *thisFileContext* parameter will be the context string corresponding to the first common-store file returned in the array that is, commonStoreFilesToBackUp\[0\].</span></span>

<span data-ttu-id="9bb8c-140">La versione corrente di questa funzione restituirà al massimo un file di archivio comune, ma è possibile che nelle versioni future un solo collegamento possa essere supportato da diversi file di archivio comuni, ad esempio uno per ogni flusso del file, in modo che l'applicazione di backup debba supportare più file in ogni chiamata a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-140">The current version of this function will return at most one common-store file, but it is possible that in future versions a single link may be backed by several common-store files for example, one for each stream in the file so your backup application should support multiple files in each call to this function.</span></span> <span data-ttu-id="9bb8c-141">In ogni caso, ogni file di archivio comune verrà restituito al massimo una volta per ogni passaggio di backup.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-141">In any case, each common-store file will be returned at most once for each backup pass.</span></span>

<span data-ttu-id="9bb8c-142">L'applicazione di backup deve eseguire il backup o il ripristino del file o dei file dell'archivio comune identificato dal nome file o dai nomi file restituiti nel parametro *commonStoreFilesToBackUp* .</span><span class="sxs-lookup"><span data-stu-id="9bb8c-142">Your backup application should back up or restore the common-store file or files identified by the file name or file names returned in the *commonStoreFilesToBackUp* parameter.</span></span> <span data-ttu-id="9bb8c-143">Indipendentemente dal fatto che esista un file di archivio comune corrispondente, l'applicazione di backup deve eseguire il backup del file di collegamento SIS così come esiste sul disco, ad esempio, come un reparse point e un file sparse e probabilmente senza intervalli compilati.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-143">Regardless of whether there is a corresponding common-store file, your backup application should back up the SIS link file as it exists on the disk for example, as a reparse point and a sparse file, and most likely with no ranges filled in.</span></span> <span data-ttu-id="9bb8c-144">L'applicazione di backup può eseguire il backup o ripristinare immediatamente il file o i file dell'archivio comune, posticiparne il backup o combinarli in modo necessario.</span><span class="sxs-lookup"><span data-stu-id="9bb8c-144">Your backup application may back up or restore the common-store file or files immediately, postpone backing them up, or mix them together as necessary.</span></span>

<span data-ttu-id="9bb8c-145">Al termine dell'operazione di backup, deallocare la memoria utilizzata dalla matrice di stringhe *commonStoreFilesToBackUp* chiamando [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9bb8c-145">After the backup operation is complete, deallocate the memory used by the *commonStoreFilesToBackUp* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9bb8c-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bb8c-146">Requirements</span></span>



| <span data-ttu-id="9bb8c-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bb8c-147">Requirement</span></span> | <span data-ttu-id="9bb8c-148">Valore</span><span class="sxs-lookup"><span data-stu-id="9bb8c-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bb8c-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bb8c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="9bb8c-150">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9bb8c-150">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9bb8c-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bb8c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="9bb8c-152">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9bb8c-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9bb8c-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bb8c-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bb8c-154"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bb8c-154"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="9bb8c-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="9bb8c-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="9bb8c-156"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bb8c-156"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="9bb8c-157">DLL</span><span class="sxs-lookup"><span data-stu-id="9bb8c-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bb8c-158"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bb8c-158"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bb8c-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bb8c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bb8c-160">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="9bb8c-160">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> <dt>

[<span data-ttu-id="9bb8c-161">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="9bb8c-161">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> </dl>

 

