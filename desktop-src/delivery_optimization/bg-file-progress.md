---
title: Struttura BG_FILE_PROGRESS (Deliveryoptimization. h)
description: La struttura BG_FILE_PROGRESS fornisce informazioni sullo stato di avanzamento correlate ai file, ad esempio il numero di byte trasferiti.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- Struttura BG_FILE_PROGRESS
topic_type:
- apiref
api_name:
- BG_FILE_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93507b8aeefa9c0ea16f70f67e221ecc4218427f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742866"
---
# <a name="bg_file_progress-structure"></a><span data-ttu-id="f9fb2-104">Struttura BG_FILE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="f9fb2-104">BG_FILE_PROGRESS structure</span></span>

<span data-ttu-id="f9fb2-105">La struttura **BG_FILE_PROGRESS** fornisce informazioni sullo stato di avanzamento correlate ai file, ad esempio il numero di byte trasferiti.</span><span class="sxs-lookup"><span data-stu-id="f9fb2-105">The **BG_FILE_PROGRESS** structure provides file-related progress information, such as the number of bytes transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9fb2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9fb2-106">Syntax</span></span>


```C++
typedef struct _BG_FILE_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  BOOL   Completed;
} BG_FILE_PROGRESS;
```



## <a name="members"></a><span data-ttu-id="f9fb2-107">Members</span><span class="sxs-lookup"><span data-stu-id="f9fb2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9fb2-108">**BytesTotal**</span><span class="sxs-lookup"><span data-stu-id="f9fb2-108">**BytesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="f9fb2-109">Dimensioni del file, in byte.</span><span class="sxs-lookup"><span data-stu-id="f9fb2-109">Size of the file in bytes.</span></span> <span data-ttu-id="f9fb2-110">Se non è in grado di determinare le dimensioni del file (ad esempio, se il file o il server non esiste), il valore viene DO_UNKNOWN_FILE_SIZE.</span><span class="sxs-lookup"><span data-stu-id="f9fb2-110">If DO cannot determine the size of the file (for example, if the file or server does not exist), the value is DO_UNKNOWN_FILE_SIZE.</span></span>

<span data-ttu-id="f9fb2-111">Se si scaricano intervalli da un file, **bytesTotal** riflette il numero totale di byte che si vuole scaricare dal file.</span><span class="sxs-lookup"><span data-stu-id="f9fb2-111">If you are downloading ranges from a file, **BytesTotal** reflects the total number of bytes you want to download from the file.</span></span>

</dd> <dt>

<span data-ttu-id="f9fb2-112">**Byte trasferiti**</span><span class="sxs-lookup"><span data-stu-id="f9fb2-112">**BytesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="f9fb2-113">Numero di byte trasferiti.</span><span class="sxs-lookup"><span data-stu-id="f9fb2-113">Number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="f9fb2-114">**Operazione completata**</span><span class="sxs-lookup"><span data-stu-id="f9fb2-114">**Completed**</span></span>
</dt> <dd>

<span data-ttu-id="f9fb2-115">Per i download, il valore è **true** se il file è disponibile per l'utente; in caso contrario, il valore è **false**.</span><span class="sxs-lookup"><span data-stu-id="f9fb2-115">For downloads, the value is **TRUE** if the file is available to the user; otherwise, the value is **FALSE**.</span></span> <span data-ttu-id="f9fb2-116">I file sono disponibili per l'utente dopo la chiamata al metodo [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="f9fb2-116">Files are available to the user after calling the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span> <span data-ttu-id="f9fb2-117">Se il metodo **complete** genera un errore temporaneo, i file elaborati prima dell'errore sono disponibili per l'utente. gli altri non lo sono.</span><span class="sxs-lookup"><span data-stu-id="f9fb2-117">If the **Complete** method generates a transient error, those files processed before the error occurred are available to the user; the others are not.</span></span> <span data-ttu-id="f9fb2-118">Utilizzare il membro **completato** per determinare se il file è disponibile per l'utente quando il **completamento** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f9fb2-118">Use the **Completed** member to determine if the file is available to the user when **Complete** fails.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9fb2-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9fb2-119">Remarks</span></span>

<span data-ttu-id="f9fb2-120">Per determinare se il file è stato trasferito, è possibile:</span><span class="sxs-lookup"><span data-stu-id="f9fb2-120">To determine if DO transferred the file, you can:</span></span>

-   <span data-ttu-id="f9fb2-121">Confrontare **byte trasferiti** con **bytesTotal**.</span><span class="sxs-lookup"><span data-stu-id="f9fb2-121">Compare **BytesTransferred** to **BytesTotal**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9fb2-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9fb2-122">Requirements</span></span>



| <span data-ttu-id="f9fb2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9fb2-123">Requirement</span></span> | <span data-ttu-id="f9fb2-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f9fb2-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9fb2-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9fb2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f9fb2-126">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9fb2-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f9fb2-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9fb2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f9fb2-128">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f9fb2-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f9fb2-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9fb2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9fb2-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9fb2-130"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9fb2-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9fb2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9fb2-132">**BG_JOB_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="f9fb2-132">**BG_JOB_PROGRESS**</span></span>](bg-job-progress.md)
</dt> <dt>

[<span data-ttu-id="f9fb2-133">**IBackgroundCopyFile:: getProgress**</span><span class="sxs-lookup"><span data-stu-id="f9fb2-133">**IBackgroundCopyFile::GetProgress**</span></span>](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





