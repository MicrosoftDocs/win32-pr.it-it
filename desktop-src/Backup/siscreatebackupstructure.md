---
title: Funzione SisCreateBackupStructure (sisbkup. h)
description: Crea una struttura di backup SIS basata sulle informazioni fornite.
ms.assetid: a8c48961-fa24-4eb6-92cd-1b9bc83cec41
keywords:
- Backup della funzione SisCreateBackupStructure
topic_type:
- apiref
api_name:
- SisCreateBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad432095f9d264e124df1d84070056fc827c625e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475928"
---
# <a name="siscreatebackupstructure-function"></a><span data-ttu-id="8b782-104">SisCreateBackupStructure (funzione)</span><span class="sxs-lookup"><span data-stu-id="8b782-104">SisCreateBackupStructure function</span></span>

<span data-ttu-id="8b782-105">La funzione **SisCreateBackupStructure** crea una struttura di backup SIS basata sulle informazioni fornite.</span><span class="sxs-lookup"><span data-stu-id="8b782-105">The **SisCreateBackupStructure** function creates a SIS backup structure based on the supplied information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b782-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b782-106">Syntax</span></span>


```C++
BOOL SisCreateBackupStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisBackupStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a><span data-ttu-id="8b782-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b782-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b782-108">*volumeRoot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b782-108">*volumeRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b782-109">Nome file della radice del volume, senza la barra rovesciata finale, del volume di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="8b782-109">File name of the volume root, without the trailing backslash, of the volume to be backed up.</span></span> <span data-ttu-id="8b782-110">Ad esempio, specificare "C:" e non "C: \\ ".</span><span class="sxs-lookup"><span data-stu-id="8b782-110">For example, specify "C:" and not "C:\\".</span></span>

</dd> <dt>

<span data-ttu-id="8b782-111">*sisBackupStructure* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b782-111">*sisBackupStructure* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b782-112">Struttura di backup SIS restituita.</span><span class="sxs-lookup"><span data-stu-id="8b782-112">Returned SIS backup structure.</span></span>

</dd> <dt>

<span data-ttu-id="8b782-113">*commonStoreRootPathname* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b782-113">*commonStoreRootPathname* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b782-114">Nome percorso completo dell'archivio comune del volume specificato.</span><span class="sxs-lookup"><span data-stu-id="8b782-114">Fully qualified path name of the specified volume's common store.</span></span> <span data-ttu-id="8b782-115">Ad esempio, "c: \\ SIS Common Store".</span><span class="sxs-lookup"><span data-stu-id="8b782-115">For example, "c:\\SIS Common Store".</span></span>

</dd> <dt>

<span data-ttu-id="8b782-116">*countOfCommonStoreFilesToBackUp* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b782-116">*countOfCommonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b782-117">Numero di file elencati nel parametro *commonStoreFilesToBackUp* .</span><span class="sxs-lookup"><span data-stu-id="8b782-117">Number of files listed in the *commonStoreFilesToBackUp* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8b782-118">*commonStoreFilesToBackUp* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b782-118">*commonStoreFilesToBackUp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b782-119">Puntatore a una matrice di nomi di file che specifica un elenco di file interni utilizzati da SIS per gestire il volume specificato.</span><span class="sxs-lookup"><span data-stu-id="8b782-119">Pointer to an array of file names that specifies a list of internal files used by SIS to manage the specified volume.</span></span> <span data-ttu-id="8b782-120">È necessario eseguire il backup di questi file nello stesso momento e nello stesso modo dei file di archivio comuni richiesti da [ **SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)</span><span class="sxs-lookup"><span data-stu-id="8b782-120">These files should be backed up at the same time and in the same manner as the common-store files requested by [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b782-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b782-121">Return value</span></span>

<span data-ttu-id="8b782-122">Questa funzione restituisce **true** se viene completata correttamente e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8b782-122">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="8b782-123">Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8b782-123">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b782-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b782-124">Remarks</span></span>

<span data-ttu-id="8b782-125">Questa funzione crea una struttura di backup SIS, che viene usata dall'API di backup SIS per creare e gestire un elenco di collegamenti di file nel volume e i file originali a cui puntano i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="8b782-125">This function creates a SIS backup structure, which is used by the SIS backup API to create and maintain a list of the file links on the volume and the original files the links point to.</span></span> <span data-ttu-id="8b782-126">Questa funzione deve essere chiamata una sola volta per ogni volume abilitato per SIS di cui viene eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="8b782-126">This function should be called only once for each SIS-enabled volume being backed up.</span></span> <span data-ttu-id="8b782-127">Tutti i file all'interno del volume specificato devono essere considerati come file di archivio comuni e sottoposti a backup solo se SIS indica che dovrebbero.</span><span class="sxs-lookup"><span data-stu-id="8b782-127">All files within the specified volume should be treated as common-store files and backed up only if SIS indicates that they should.</span></span>

<span data-ttu-id="8b782-128">I parametri *countOfCommonStoreFilesToBackUp* e *commonStoreFilesToBackUp* restituiscono insieme un elenco di file di cui è necessario eseguire il backup indipendentemente dai collegamenti di cui viene eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="8b782-128">The *countOfCommonStoreFilesToBackUp* and *commonStoreFilesToBackUp* parameters together return a list of files that must be backed up regardless of which links are backed up.</span></span>

<span data-ttu-id="8b782-129">Se *countOfCommonStoreFilesToBackUp* è 0, *commonStoreFilesToBackUp* può essere un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="8b782-129">If *countOfCommonStoreFilesToBackUp* is 0, *commonStoreFilesToBackUp* may be a **NULL** pointer.</span></span> <span data-ttu-id="8b782-130">Il valore del parametro *commonStoreFilesToBackUp* deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="8b782-130">The value of the *commonStoreFilesToBackUp* parameter should be ignored.</span></span>

<span data-ttu-id="8b782-131">Al termine dell'operazione di backup, deallocare la memoria utilizzata dalla matrice di stringhe *commonStoreFilesToBackUp* chiamando [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="8b782-131">After the backup operation is complete, deallocate the memory used by the *commonStoreFilesToBackUp* array of strings by calling [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b782-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b782-132">Requirements</span></span>



| <span data-ttu-id="8b782-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b782-133">Requirement</span></span> | <span data-ttu-id="8b782-134">Valore</span><span class="sxs-lookup"><span data-stu-id="8b782-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b782-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b782-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8b782-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8b782-136">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8b782-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b782-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8b782-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8b782-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8b782-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b782-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b782-140"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b782-140"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b782-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="8b782-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b782-142"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b782-142"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="8b782-143">DLL</span><span class="sxs-lookup"><span data-stu-id="8b782-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b782-144"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b782-144"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b782-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b782-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b782-146">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="8b782-146">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="8b782-147">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="8b782-147">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)
</dt> <dt>

[<span data-ttu-id="8b782-148">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="8b782-148">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)
</dt> </dl>

 

