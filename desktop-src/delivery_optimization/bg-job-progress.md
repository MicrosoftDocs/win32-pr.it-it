---
title: Struttura BG_JOB_PROGRESS (Deliveryoptimization. h)
description: La struttura BG_JOB_PROGRESS fornisce informazioni sullo stato di avanzamento correlate al processo, ad esempio il numero di byte e i file trasferiti. Per i processi di caricamento, lo stato di avanzamento si applica al file di caricamento, non al file di risposta.
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- Struttura BG_JOB_PROGRESS
topic_type:
- apiref
api_name:
- BG_JOB_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e45c4a2833f80644ff763fc85a6846f9858fb3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518549"
---
# <a name="bg_job_progress-structure"></a><span data-ttu-id="e44a0-105">Struttura BG_JOB_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="e44a0-105">BG_JOB_PROGRESS structure</span></span>

<span data-ttu-id="e44a0-106">La struttura **BG_JOB_PROGRESS** fornisce informazioni sullo stato di avanzamento correlate al processo, ad esempio il numero di byte e i file trasferiti.</span><span class="sxs-lookup"><span data-stu-id="e44a0-106">The **BG_JOB_PROGRESS** structure provides job-related progress information, such as the number of bytes and files transferred.</span></span> <span data-ttu-id="e44a0-107">Per i processi di caricamento, lo stato di avanzamento si applica al file di caricamento, non al file di risposta.</span><span class="sxs-lookup"><span data-stu-id="e44a0-107">For upload jobs, the progress applies to the upload file, not the reply file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e44a0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e44a0-108">Syntax</span></span>


```C++
typedef struct _BG_JOB_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  ULONG  FilesTotal;
  ULONG  FilesTransferred;
} BG_JOB_PROGRESS;
```



## <a name="members"></a><span data-ttu-id="e44a0-109">Members</span><span class="sxs-lookup"><span data-stu-id="e44a0-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="e44a0-110">**BytesTotal**</span><span class="sxs-lookup"><span data-stu-id="e44a0-110">**BytesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="e44a0-111">Numero totale di byte da trasferire per tutti i file nel processo.</span><span class="sxs-lookup"><span data-stu-id="e44a0-111">Total number of bytes to transfer for all files in the job.</span></span> <span data-ttu-id="e44a0-112">Se il valore è BG_SIZE_UNKNOWN, non è stata determinata la dimensione totale di tutti i file nel processo.</span><span class="sxs-lookup"><span data-stu-id="e44a0-112">If the value is BG_SIZE_UNKNOWN, the total size of all files in the job has not been determined.</span></span> <span data-ttu-id="e44a0-113">DO non imposta questo valore se non è in grado di determinare le dimensioni di uno dei file.</span><span class="sxs-lookup"><span data-stu-id="e44a0-113">DO does not set this value if it cannot determine the size of one of the files.</span></span> <span data-ttu-id="e44a0-114">Se, ad esempio, il file o il server specificato non esiste, non è possibile determinare le dimensioni del file.</span><span class="sxs-lookup"><span data-stu-id="e44a0-114">For example, if the specified file or server does not exist, DO cannot determine the size of the file.</span></span>

<span data-ttu-id="e44a0-115">Se si scaricano gli intervalli dal file, **bytesTotal** include il numero totale di byte che si vuole scaricare dal file.</span><span class="sxs-lookup"><span data-stu-id="e44a0-115">If you are downloading ranges from the file, **BytesTotal** includes the total number of bytes you want to download from the file.</span></span>

</dd> <dt>

<span data-ttu-id="e44a0-116">**Byte trasferiti**</span><span class="sxs-lookup"><span data-stu-id="e44a0-116">**BytesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="e44a0-117">Numero di byte trasferiti.</span><span class="sxs-lookup"><span data-stu-id="e44a0-117">Number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="e44a0-118">**FilesTotal**</span><span class="sxs-lookup"><span data-stu-id="e44a0-118">**FilesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="e44a0-119">Numero totale di file da trasferire per questo processo.</span><span class="sxs-lookup"><span data-stu-id="e44a0-119">Total number of files to transfer for this job.</span></span>

</dd> <dt>

<span data-ttu-id="e44a0-120">**FilesTransferred**</span><span class="sxs-lookup"><span data-stu-id="e44a0-120">**FilesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="e44a0-121">Numero di file trasferiti.</span><span class="sxs-lookup"><span data-stu-id="e44a0-121">Number of files transferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e44a0-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e44a0-122">Requirements</span></span>



| <span data-ttu-id="e44a0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e44a0-123">Requirement</span></span> | <span data-ttu-id="e44a0-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e44a0-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e44a0-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e44a0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e44a0-126">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="e44a0-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e44a0-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e44a0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e44a0-128">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e44a0-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e44a0-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e44a0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e44a0-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="e44a0-130"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e44a0-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e44a0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e44a0-132">**BG_FILE_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="e44a0-132">**BG_FILE_PROGRESS**</span></span>](bg-file-progress.md)
</dt> <dt>

[<span data-ttu-id="e44a0-133">**Metodo ibackgroundcopyjob:: getProgress**</span><span class="sxs-lookup"><span data-stu-id="e44a0-133">**IBackgroundCopyJob::GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





