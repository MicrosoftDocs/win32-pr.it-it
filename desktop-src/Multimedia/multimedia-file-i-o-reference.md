---
title: Riferimento I/O file multimediale
description: Riferimento I/O file multimediale
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Windows Multimedia, riferimento I/O file
- Multimedia, riferimento I/O file
- input multimediale, riferimento I/O file
- I/O file multimediale, informazioni di riferimento
- I/O di file, riferimento
- input e output (I/O), riferimento
- I/O (input e output), riferimento
- informazioni di riferimento per l'I/O del file multimediale, informazioni
- riferimento I/O file multimediale, informazioni
- riferimento I/O file, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f833b7fb6677e064c19897e276d3961038cfc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724818"
---
# <a name="multimedia-file-io-reference"></a><span data-ttu-id="91412-113">Riferimento I/O file multimediale</span><span class="sxs-lookup"><span data-stu-id="91412-113">Multimedia File I/O Reference</span></span>

<span data-ttu-id="91412-114">Questa sezione descrive le funzioni, le macro, i messaggi e le strutture associati all'input e all'output del file multimediale.</span><span class="sxs-lookup"><span data-stu-id="91412-114">This section describes the functions, macros, messages, and structures associated with multimedia file input and output.</span></span> <span data-ttu-id="91412-115">Questi elementi vengono raggruppati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="91412-115">These elements are grouped as follows.</span></span>

## <a name="basic-io"></a><span data-ttu-id="91412-116">I/O di base</span><span class="sxs-lookup"><span data-stu-id="91412-116">Basic I/O</span></span>

-   [<span data-ttu-id="91412-117">**mmioClose**</span><span class="sxs-lookup"><span data-stu-id="91412-117">**mmioClose**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [<span data-ttu-id="91412-118">**mmioOpen**</span><span class="sxs-lookup"><span data-stu-id="91412-118">**mmioOpen**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [<span data-ttu-id="91412-119">**mmioRead**</span><span class="sxs-lookup"><span data-stu-id="91412-119">**mmioRead**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [<span data-ttu-id="91412-120">**mmioRename**</span><span class="sxs-lookup"><span data-stu-id="91412-120">**mmioRename**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [<span data-ttu-id="91412-121">**mmioSeek**</span><span class="sxs-lookup"><span data-stu-id="91412-121">**mmioSeek**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [<span data-ttu-id="91412-122">**mmioWrite**</span><span class="sxs-lookup"><span data-stu-id="91412-122">**mmioWrite**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="buffered-io"></a><span data-ttu-id="91412-123">I/O memorizzato nel buffer</span><span class="sxs-lookup"><span data-stu-id="91412-123">Buffered I/O</span></span>

-   [<span data-ttu-id="91412-124">**mmioAdvance**</span><span class="sxs-lookup"><span data-stu-id="91412-124">**mmioAdvance**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [<span data-ttu-id="91412-125">**mmioFlush**</span><span class="sxs-lookup"><span data-stu-id="91412-125">**mmioFlush**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [<span data-ttu-id="91412-126">**mmioGetInfo**</span><span class="sxs-lookup"><span data-stu-id="91412-126">**mmioGetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   <span data-ttu-id="91412-127">[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91412-127">[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))</span></span>
-   [<span data-ttu-id="91412-128">**mmioSetBuffer**</span><span class="sxs-lookup"><span data-stu-id="91412-128">**mmioSetBuffer**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [<span data-ttu-id="91412-129">**mmioSetInfo**</span><span class="sxs-lookup"><span data-stu-id="91412-129">**mmioSetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)

## <a name="riff-io"></a><span data-ttu-id="91412-130">I/O RIFF</span><span class="sxs-lookup"><span data-stu-id="91412-130">RIFF I/O</span></span>

-   [<span data-ttu-id="91412-131">**mmioAscend**</span><span class="sxs-lookup"><span data-stu-id="91412-131">**mmioAscend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [<span data-ttu-id="91412-132">**MMCKINFO**</span><span class="sxs-lookup"><span data-stu-id="91412-132">**MMCKINFO**</span></span>](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [<span data-ttu-id="91412-133">**mmioCreateChunk**</span><span class="sxs-lookup"><span data-stu-id="91412-133">**mmioCreateChunk**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [<span data-ttu-id="91412-134">**mmioDescend**</span><span class="sxs-lookup"><span data-stu-id="91412-134">**mmioDescend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [<span data-ttu-id="91412-135">**mmioFOURCC**</span><span class="sxs-lookup"><span data-stu-id="91412-135">**mmioFOURCC**</span></span>](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [<span data-ttu-id="91412-136">**mmioStringToFOURCC**</span><span class="sxs-lookup"><span data-stu-id="91412-136">**mmioStringToFOURCC**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a><span data-ttu-id="91412-137">Procedure di I/O personalizzate</span><span class="sxs-lookup"><span data-stu-id="91412-137">Custom I/O Procedures</span></span>

-   <span data-ttu-id="91412-138">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91412-138">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span></span>
-   [<span data-ttu-id="91412-139">**mmioInstallIOProc**</span><span class="sxs-lookup"><span data-stu-id="91412-139">**mmioInstallIOProc**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [<span data-ttu-id="91412-140">**chiusura di MMIOM \_**</span><span class="sxs-lookup"><span data-stu-id="91412-140">**MMIOM\_CLOSE**</span></span>](mmiom-close.md)
-   [<span data-ttu-id="91412-141">**MMIOM \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="91412-141">**MMIOM\_OPEN**</span></span>](mmiom-open.md)
-   [<span data-ttu-id="91412-142">**MMIOM di \_ lettura**</span><span class="sxs-lookup"><span data-stu-id="91412-142">**MMIOM\_READ**</span></span>](mmiom-read.md)
-   [<span data-ttu-id="91412-143">**ridenominazione MMIOM \_**</span><span class="sxs-lookup"><span data-stu-id="91412-143">**MMIOM\_RENAME**</span></span>](mmiom-rename.md)
-   [<span data-ttu-id="91412-144">**MMIOM \_ Seek**</span><span class="sxs-lookup"><span data-stu-id="91412-144">**MMIOM\_SEEK**</span></span>](mmiom-seek.md)
-   [<span data-ttu-id="91412-145">**\_scrittura MMIOM**</span><span class="sxs-lookup"><span data-stu-id="91412-145">**MMIOM\_WRITE**</span></span>](mmiom-write.md)
-   [<span data-ttu-id="91412-146">**\_WRITEFLUSH MMIOM**</span><span class="sxs-lookup"><span data-stu-id="91412-146">**MMIOM\_WRITEFLUSH**</span></span>](mmiom-writeflush.md)
-   [<span data-ttu-id="91412-147">**mmioSendMessage**</span><span class="sxs-lookup"><span data-stu-id="91412-147">**mmioSendMessage**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a><span data-ttu-id="91412-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91412-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91412-149">I/O file multimediale</span><span class="sxs-lookup"><span data-stu-id="91412-149">Multimedia File I/O</span></span>](multimedia-file-i-o.md)
</dt> </dl>

 

 