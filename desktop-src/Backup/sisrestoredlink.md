---
title: Funzione SisRestoredLink (sisbkup. h)
description: Restituisce i nomi del file o dei file dell'archivio comune a cui fa riferimento il collegamento SIS ripristinato specificato.
ms.assetid: 4eefd975-6055-44c0-93ab-900638948f3e
keywords:
- Backup della funzione SisRestoredLink
topic_type:
- apiref
api_name:
- SisRestoredLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd539d1ad6c203441b2bcd469a7d8f2fe8bdfc7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963947"
---
# <a name="sisrestoredlink-function"></a><span data-ttu-id="af9e4-104">SisRestoredLink (funzione)</span><span class="sxs-lookup"><span data-stu-id="af9e4-104">SisRestoredLink function</span></span>

<span data-ttu-id="af9e4-105">La funzione **SisRestoredLink** restituisce i nomi del file o dei file dell'archivio comune a cui fa riferimento il collegamento SIS ripristinato specificato.</span><span class="sxs-lookup"><span data-stu-id="af9e4-105">The **SisRestoredLink** function returns the names of the common-store file or files pointed to by the specified restored SIS link.</span></span>

## <a name="syntax"></a><span data-ttu-id="af9e4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af9e4-106">Syntax</span></span>


```C++
BOOL SisRestoredLink(
  _In_  PVOID  sisRestoreStructure,
  _In_  PWCHAR restoredFileName,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a><span data-ttu-id="af9e4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="af9e4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af9e4-108">*sisRestoreStructure* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af9e4-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af9e4-109">Puntatore a una struttura di ripristino SIS restituita da [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="af9e4-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="af9e4-110">*restoredFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af9e4-110">*restoredFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af9e4-111">Nome file completo del file di collegamento SIS ripristinato.</span><span class="sxs-lookup"><span data-stu-id="af9e4-111">Fully qualified file name of the restored SIS link file.</span></span>

</dd> <dt>

<span data-ttu-id="af9e4-112">*reparseData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af9e4-112">*reparseData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af9e4-113">Puntatore al contenuto del punto di analisi SIS.</span><span class="sxs-lookup"><span data-stu-id="af9e4-113">Pointer to the contents of the SIS reparse point.</span></span> <span data-ttu-id="af9e4-114">Questo reparse point contiene i dati che descrivono il collegamento SIS ripristinato.</span><span class="sxs-lookup"><span data-stu-id="af9e4-114">This reparse point contains data describing the restored SIS link.</span></span> <span data-ttu-id="af9e4-115">Per recuperare i dati di reparse point per un file, usare il codice di controllo [**FSCTL \_ get \_ reparse \_ Point**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .</span><span class="sxs-lookup"><span data-stu-id="af9e4-115">To retrieve the reparse point data for a file, use the [**FSCTL\_GET\_REPARSE\_POINT**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) control code.</span></span>

</dd> <dt>

<span data-ttu-id="af9e4-116">*reparseDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af9e4-116">*reparseDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af9e4-117">Dimensioni del contenuto del punto di analisi SIS a cui punta *reparseData* in byte.</span><span class="sxs-lookup"><span data-stu-id="af9e4-117">Size of the contents of the SIS reparse point pointed to by *reparseData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="af9e4-118">*countOfCommonStoreFilesToRestore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="af9e4-118">*countOfCommonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af9e4-119">Numero di file elencati nel parametro *commonStoreFilesToRestore* .</span><span class="sxs-lookup"><span data-stu-id="af9e4-119">Number of files listed in the *commonStoreFilesToRestore* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="af9e4-120">*commonStoreFilesToRestore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="af9e4-120">*commonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af9e4-121">Puntatore a una matrice di nomi di file di archivio comuni.</span><span class="sxs-lookup"><span data-stu-id="af9e4-121">Pointer to an array of common-store file names.</span></span> <span data-ttu-id="af9e4-122">Questi file devono essere ripristinati nello stesso momento e nello stesso modo dei file di archivio comuni richiesti da [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span><span class="sxs-lookup"><span data-stu-id="af9e4-122">These files should be restored at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span></span>

<span data-ttu-id="af9e4-123">Se il valore del parametro *countOfCommonStoreFilesToRestore* è diverso da 0, il valore del parametro *commonStoreFilesToRestore* conterrà i nomi dei file dell'archivio comune da ripristinare in seguito al ripristino del collegamento SIS.</span><span class="sxs-lookup"><span data-stu-id="af9e4-123">If the value of the *countOfCommonStoreFilesToRestore* parameter is not 0, the value of the *commonStoreFilesToRestore* parameter will contain the names of the common-store files to be restored as a result of restoring the SIS link.</span></span> <span data-ttu-id="af9e4-124">Se il valore è 0, i file di archivio comuni sono stati restituiti una volta o sono già presenti nel volume.</span><span class="sxs-lookup"><span data-stu-id="af9e4-124">If the value is 0, then either the common-store files have been returned once, or they are already present on the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af9e4-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af9e4-125">Return value</span></span>

<span data-ttu-id="af9e4-126">Questa funzione restituisce **true** se viene completata correttamente e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="af9e4-126">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="af9e4-127">Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="af9e4-127">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="af9e4-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="af9e4-128">Remarks</span></span>

<span data-ttu-id="af9e4-129">È necessario chiamare questa funzione per ogni collegamento SIS che è stato ripristinato.</span><span class="sxs-lookup"><span data-stu-id="af9e4-129">You should call this function for each SIS link that has been restored.</span></span>

<span data-ttu-id="af9e4-130">Questa funzione restituirà ogni file di archivio comune al massimo una volta per ogni operazione di ripristino. qualsiasi tentativo di ripristinare collegamenti SIS aggiuntivi che visualizzano lo stesso file di archivio comune non comporterà la restituzione di un nome file di archivio comune.</span><span class="sxs-lookup"><span data-stu-id="af9e4-130">This function will return each common-store file at most once for each restore operation; any attempt to restore additional SIS links that see the same common-store file will not result in that common-store file name being returned.</span></span>

<span data-ttu-id="af9e4-131">Questa funzione non restituirà un file di archivio comune che non è stato restituito anche in una chiamata a [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) durante l'operazione di backup, supponendo che i dati di reparse SIS archiviati nel supporto non siano danneggiati.</span><span class="sxs-lookup"><span data-stu-id="af9e4-131">This function will not return a common-store file that was not also returned in a call to [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) during the backup operation, assuming that the SIS reparse data stored on the media has not been corrupted.</span></span>

<span data-ttu-id="af9e4-132">Quando si ripristina un collegamento SIS, l'operazione di ripristino deve creare solo il file di tipo sparse appropriato, inizializzare tutti gli intervalli allocati, quindi scrivere i dati di rianalisi SIS esattamente come sono stati letti durante l'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="af9e4-132">When restoring a SIS link, your restore operation should create only the appropriate sparse file, initialize any allocated ranges, and then write the SIS reparse data exactly as it was read during the backup operation.</span></span> <span data-ttu-id="af9e4-133">È fondamentale che l'operazione di ripristino crei file sparse con intervalli non allocati piuttosto che file sparse (o file diversi) inizializzati con zeri.</span><span class="sxs-lookup"><span data-stu-id="af9e4-133">It is crucial that your restore operation create sparse files with unallocated ranges rather than sparse files (or nonsparse files) initialized with zeroes.</span></span>

<span data-ttu-id="af9e4-134">Si noti che questa funzione non identificherà necessariamente il file o i file di archivio comuni corrispondenti a un set di collegamenti SIS nei supporti di backup se tali file o file di archivio comuni sono ancora presenti sul disco.</span><span class="sxs-lookup"><span data-stu-id="af9e4-134">Note that this function will not necessarily identify the common-store file or files corresponding to a set of SIS links on the backup media if those common-store file or files still exist on disk.</span></span> <span data-ttu-id="af9e4-135">Il contenuto del flusso di dati di un file di archivio comune non cambia mai dopo la creazione, quindi, se il file esiste già sul disco, non è necessario ripristinarlo.</span><span class="sxs-lookup"><span data-stu-id="af9e4-135">The contents of a common-store file's data stream never changes once it is created, so if the file already exists on the disk there is no need to restore it.</span></span>

<span data-ttu-id="af9e4-136">I nomi di file di archivio comuni sono univoci a livello globale per garantire l'integrità dell'operazione di ripristino anche se non si verificano nello stesso volume abilitato per SIS a cui è stato eseguito l'accesso all'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="af9e4-136">Common-store file names are globally unique to ensure the integrity of the restore operation even if it does not occur on the same SIS-enabled volume that the backup operation has accessed.</span></span>

## <a name="requirements"></a><span data-ttu-id="af9e4-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af9e4-137">Requirements</span></span>



| <span data-ttu-id="af9e4-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="af9e4-138">Requirement</span></span> | <span data-ttu-id="af9e4-139">Valore</span><span class="sxs-lookup"><span data-stu-id="af9e4-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af9e4-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af9e4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="af9e4-141">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="af9e4-141">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="af9e4-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af9e4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="af9e4-143">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af9e4-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="af9e4-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af9e4-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="af9e4-145"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-145"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="af9e4-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="af9e4-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="af9e4-147"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-147"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="af9e4-148">DLL</span><span class="sxs-lookup"><span data-stu-id="af9e4-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af9e4-149"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af9e4-149"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af9e4-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af9e4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af9e4-151">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="af9e4-151">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="af9e4-152">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="af9e4-152">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> </dl>

 

