---
title: Funzione SisRestoredCommonStoreFile (sisbkup. h)
description: Segnala all'architettura SIS che è stato scritto un file di archivio comune.
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- Backup della funzione SisRestoredCommonStoreFile
topic_type:
- apiref
api_name:
- SisRestoredCommonStoreFile
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093ff5f20db42bcafe62ee0ec57d5027abcf9f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963948"
---
# <a name="sisrestoredcommonstorefile-function"></a><span data-ttu-id="e8a02-104">SisRestoredCommonStoreFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="e8a02-104">SisRestoredCommonStoreFile function</span></span>

<span data-ttu-id="e8a02-105">La funzione **SisRestoredCommonStoreFile** segnala all'architettura SIS che è stato scritto un file di archivio comune.</span><span class="sxs-lookup"><span data-stu-id="e8a02-105">The **SisRestoredCommonStoreFile** function reports to the SIS architecture that a common-store file has been written.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a02-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8a02-106">Syntax</span></span>


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a><span data-ttu-id="e8a02-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8a02-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8a02-108">*sisRestoreStructure* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8a02-108">*sisRestoreStructure* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8a02-109">Puntatore a una struttura di ripristino SIS restituita da [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span><span class="sxs-lookup"><span data-stu-id="e8a02-109">Pointer to a SIS restore structure returned from [**SisCreateRestoreStructure**](siscreaterestorestructure.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8a02-110">*commonStoreFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8a02-110">*commonStoreFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8a02-111">Nome del file di archivio comune ripristinato.</span><span class="sxs-lookup"><span data-stu-id="e8a02-111">Name of the restored common-store file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8a02-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8a02-112">Return value</span></span>

<span data-ttu-id="e8a02-113">Questa funzione restituisce **true** se viene completata correttamente e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e8a02-113">This function returns **TRUE** if it completes successfully and **FALSE** otherwise.</span></span> <span data-ttu-id="e8a02-114">Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e8a02-114">Call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get more information about the reason the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8a02-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8a02-115">Remarks</span></span>

<span data-ttu-id="e8a02-116">Questa funzione deve essere chiamata dopo il ripristino di un file di archivio comune.</span><span class="sxs-lookup"><span data-stu-id="e8a02-116">This function should be called after you have restored a common-store file.</span></span> <span data-ttu-id="e8a02-117">Informa l'architettura SIS che è stato scritto un nuovo file di archivio comune, in modo che l'architettura SIS possa eseguire attività di manutenzione interne, ad esempio l'inizializzazione delle strutture di dati interne o la correzione dei collegamenti al file di archivio comune.</span><span class="sxs-lookup"><span data-stu-id="e8a02-117">It notifies the SIS architecture that a new common-store file has been written, so that the SIS architecture can perform internal maintenance tasks such as initializing its internal data structures or fixing the links to the common-store file.</span></span>

<span data-ttu-id="e8a02-118">L'operazione di ripristino dovrebbe ripristinare solo i file di archivio comuni segnalati da [**SisRestoredLink**](sisrestoredlink.md), anche se nel supporto di backup sono presenti file di archivio comuni aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="e8a02-118">Your restore operation should restore only common-store files reported by [**SisRestoredLink**](sisrestoredlink.md), even if there are additional common-store files on the backup media.</span></span> <span data-ttu-id="e8a02-119">L'operazione di ripristino consente di ripristinare i collegamenti SIS e i file di archivio comuni in qualsiasi ordine scelto; Tuttavia, deve chiamare **SisRestoredLink** dopo che il collegamento è stato ripristinato ed è necessario chiamare questa funzione dopo che è stato ripristinato un file di archivio comune.</span><span class="sxs-lookup"><span data-stu-id="e8a02-119">Your restore operation can restore the SIS links and common-store files in any order it chooses; however, it must call **SisRestoredLink** after it restores any link, and it must call this function after it restores any common-store file.</span></span> <span data-ttu-id="e8a02-120">Poiché l'operazione di ripristino non è in grado di identificare i file di archivio comuni che verranno ripristinati fino a quando non vengono segnalati i nomi dei file in seguito al ripristino di un collegamento, l'operazione di ripristino ripristinerà sempre un file di archivio comune dopo che è stato ripristinato almeno un collegamento che vi fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="e8a02-120">Because your restore operation cannot identify which common-store files will be restored until the file names are reported to it as a result of restoring a link, your restore operation will always restore a common-store file after at least one link referring to it is restored.</span></span> <span data-ttu-id="e8a02-121">È tuttavia possibile ripristinare collegamenti SIS aggiuntivi che puntano a tale file di archivio comune.</span><span class="sxs-lookup"><span data-stu-id="e8a02-121">However, you can then restore additional SIS links that point to that common-store file.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8a02-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8a02-122">Requirements</span></span>



| <span data-ttu-id="e8a02-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8a02-123">Requirement</span></span> | <span data-ttu-id="e8a02-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e8a02-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a02-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8a02-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e8a02-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e8a02-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e8a02-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8a02-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e8a02-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8a02-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e8a02-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8a02-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8a02-130"><dt>Sisbkup. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8a02-130"><dt>Sisbkup.h</dt></span></span> </dl>   |
| <span data-ttu-id="e8a02-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="e8a02-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="e8a02-132"><dt>Sisbkup. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8a02-132"><dt>Sisbkup.lib</dt></span></span> </dl> |
| <span data-ttu-id="e8a02-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e8a02-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8a02-134"><dt>Sisbkup.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8a02-134"><dt>Sisbkup.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8a02-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8a02-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a02-136">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="e8a02-136">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)
</dt> <dt>

[<span data-ttu-id="e8a02-137">**SisRestoredLink**</span><span class="sxs-lookup"><span data-stu-id="e8a02-137">**SisRestoredLink**</span></span>](sisrestoredlink.md)
</dt> </dl>

 

