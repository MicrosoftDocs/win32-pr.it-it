---
title: Funzione SisCreateRestoreStructure (sisbkup. h)
description: Crea una struttura di ripristino SIS basata sulle informazioni fornite.
ms.assetid: acdd4258-813d-42af-a2e1-e59a1426f86c
keywords:
- Backup della funzione SisCreateRestoreStructure
topic_type:
- apiref
api_name:
- SisCreateRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b83ebcdd609b00fdec19666a6915926692a2048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873534"
---
# <a name="siscreaterestorestructure-function"></a><span data-ttu-id="b4ea7-104">SisCreateRestoreStructure (funzione)</span><span class="sxs-lookup"><span data-stu-id="b4ea7-104">SisCreateRestoreStructure function</span></span>

<span data-ttu-id="b4ea7-105">La funzione **SisCreateRestoreStructure** crea una struttura di ripristino SIS basata sulle informazioni fornite.</span><span class="sxs-lookup"><span data-stu-id="b4ea7-105">The **SisCreateRestoreStructure** function creates a SIS restore structure based on the supplied information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4ea7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4ea7-106">Syntax</span></span>


```C++
BOOL SisCreateRestoreStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisRestoreStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a><span data-ttu-id="b4ea7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4ea7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4ea7-108">*volumeRoot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4ea7-108">*volumeRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4ea7-109">Nome file della radice del volume, senza la barra rovesciata finale, del volume di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="b4ea7-109">File name of the volume root, without the trailing backslash, of the volume to be backed up.</span></span> <span data-ttu-id="b4ea7-110">Ad esempio, specificare "C:" e non "C: \\ ".</span><span class="sxs-lookup"><span data-stu-id="b4ea7-110">For example, specify "C:" and not "C:\\".</span></span> <span data-ttu-id="b4ea7-111">Il volume non può essere il volume di sistema o di avvio.</span><span class="sxs-lookup"><span data-stu-id="b4ea7-111">The volume cannot be the system or boot volume.</span></span>

</dd> <dt>

<span data-ttu-id="b4ea7-112">*sisRestoreStructure* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b4ea7-112">*sisRestoreStructure* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4ea7-113">Struttura di ripristino SIS restituita.</span><span class="sxs-lookup"><span data-stu-id="b4ea7-113">Returned SIS restore structure.</span></span> <span data-ttu-id="b4ea7-114">Questa struttura deve essere considerata opaca dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="b4ea7-114">This structure should be treated as opaque by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="b4ea7-115">*commonStoreRootPathname* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b4ea7-115">*commonStoreRootPathname* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4ea7-116">Nome percorso completo dell'archivio comune del volume specificato.</span><span class="sxs-lookup"><span data-stu-id="b4ea7-116">Fully qualified path name of the specified volume's common store.</span></span> <span data-ttu-id="b4ea7-117">Ad esempio, "c: \\ SIS Common Store".</span><span class="sxs-lookup"><span data-stu-id="b4ea7-117">For example, "c:\\SIS Common Store".</span></span>

</dd> <dt>

<span data-ttu-id="b4ea7-118">*countOfCommonStoreFilesToRestore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b4ea7-118">*countOfCommonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4ea7-119">Numero di file elencati nel parametro *commonStoreFilesToRestore* .</span><span class="sxs-lookup"><span data-stu-id="b4ea7-119">Number of files listed in the *commonStoreFilesToRestore* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b4ea7-120">*commonStoreFilesToRestore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b4ea7-120">*commonStoreFilesToRestore* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4ea7-121">Puntatore a una matrice di nomi di file che specifica l'elenco di file interni utilizzati da SIS per gestire il volume specificato.</span><span class="sxs-lookup"><span data-stu-id="b4ea7-121">Pointer to an array of file names that specifies the list of internal files used by SIS to manage the specified volume.</span></span> <span data-ttu-id="b4ea7-122">Questi file devono essere ripristinati nello stesso momento e nello stesso modo dei file di archivio comuni richiesti da [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span><span class="sxs-lookup"><span data-stu-id="b4ea7-122">These files should be restored at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4ea7-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4ea7-123">Return value</span></span>

<span data-ttu-id="b4ea7-124">Questa funzione restituisce **true** se viene completata correttamente e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b4ea7-124">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="b4ea7-125">Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b4ea7-125">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4ea7-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4ea7-126">Remarks</span></span>

<span data-ttu-id="b4ea7-127">Questa funzione stabilisce l'ambiente di ripristino nel volume specificato nel modo in cui [**SisCreateBackupStructure**](siscreatebackupstructure.md) stabilisce l'ambiente di backup nel volume specificato.</span><span class="sxs-lookup"><span data-stu-id="b4ea7-127">This function establishes the restore environment on the specified volume in the way that [**SisCreateBackupStructure**](siscreatebackupstructure.md) establishes the backup environment on the specified volume.</span></span>

<span data-ttu-id="b4ea7-128">Si noti che questa funzione non identificherà necessariamente il file o i file di archivio comuni corrispondenti a un set di collegamenti SIS nei supporti di backup se tali file o file di archivio comuni sono ancora presenti sul disco.</span><span class="sxs-lookup"><span data-stu-id="b4ea7-128">Note that this function will not necessarily identify the common-store file or files corresponding to a set of SIS links on the backup media if those common store file or files still exist on disk.</span></span> <span data-ttu-id="b4ea7-129">Il contenuto del flusso di dati di un file di archivio comune non cambia mai dopo la creazione, quindi, se il file esiste già sul disco, non è necessario ripristinarlo.</span><span class="sxs-lookup"><span data-stu-id="b4ea7-129">The contents of a common-store file's data stream never change once it is created, so if the file already exists on the disk there is no need to restore it.</span></span>

<span data-ttu-id="b4ea7-130">I nomi di file di archivio comuni sono univoci a livello globale per garantire l'integrità dell'operazione di ripristino anche se non si verificano nello stesso volume abilitato per SIS a cui è stato eseguito l'accesso all'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="b4ea7-130">Common-store file names are globally unique to ensure the integrity of the restore operation even if it does not occur on the same SIS-enabled volume that the backup operation has accessed.</span></span>

<span data-ttu-id="b4ea7-131">Al termine dell'operazione di ripristino, deallocare la memoria utilizzata dalla matrice di stringhe *commonStoreFilesToRestore* chiamando [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b4ea7-131">After the restore operation is complete, deallocate the memory used by the *commonStoreFilesToRestore* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4ea7-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4ea7-132">Requirements</span></span>



| <span data-ttu-id="b4ea7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4ea7-133">Requirement</span></span> | <span data-ttu-id="b4ea7-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b4ea7-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ea7-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4ea7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b4ea7-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b4ea7-136">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b4ea7-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4ea7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b4ea7-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b4ea7-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b4ea7-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4ea7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4ea7-140"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4ea7-140"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4ea7-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="b4ea7-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4ea7-142"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4ea7-142"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="b4ea7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b4ea7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4ea7-144"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4ea7-144"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4ea7-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4ea7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4ea7-146">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="b4ea7-146">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)
</dt> <dt>

[<span data-ttu-id="b4ea7-147">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="b4ea7-147">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="b4ea7-148">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="b4ea7-148">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> <dt>

[<span data-ttu-id="b4ea7-149">**SisFreeBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="b4ea7-149">**SisFreeBackupStructure**</span></span>](sisfreebackupstructure.md)
</dt> </dl>

 

