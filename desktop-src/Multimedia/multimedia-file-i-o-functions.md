---
title: Funzioni di I/O di file multimediali
description: Funzioni di I/O di file multimediali
ms.assetid: a5d51906-881f-4fe0-a988-c10776a3b40d
keywords:
- Multimedia di Windows, funzioni di I/O di file
- Multimedia, funzioni di I/O file
- input multimediale, funzioni di I/O di file
- I/O di file multimediali, funzioni
- I/O di file, funzioni
- input e output (I/O), funzioni
- I/O (input e output), funzioni
- informazioni di riferimento sulle funzioni di I/O dei file multimediali
- riferimento I/O file multimediale, funzioni
- riferimento I/O file, funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62b8daf8e84953acebcca9106165f27b350ef2f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516726"
---
# <a name="multimedia-file-io-functions"></a><span data-ttu-id="c2ffd-113">Funzioni di I/O di file multimediali</span><span class="sxs-lookup"><span data-stu-id="c2ffd-113">Multimedia File I/O Functions</span></span>

<span data-ttu-id="c2ffd-114">Le funzioni seguenti vengono usate con l'I/O dei file multimediali.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-114">The following functions are used with multimedia file I/O.</span></span>

-   <span data-ttu-id="c2ffd-115">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c2ffd-115">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span></span>
-   [<span data-ttu-id="c2ffd-116">**mmioAdvance**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-116">**mmioAdvance**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [<span data-ttu-id="c2ffd-117">**mmioAscend**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-117">**mmioAscend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [<span data-ttu-id="c2ffd-118">**mmioClose**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-118">**mmioClose**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [<span data-ttu-id="c2ffd-119">**mmioCreateChunk**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-119">**mmioCreateChunk**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [<span data-ttu-id="c2ffd-120">**mmioDescend**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-120">**mmioDescend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [<span data-ttu-id="c2ffd-121">**mmioFlush**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-121">**mmioFlush**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [<span data-ttu-id="c2ffd-122">**mmioGetInfo**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-122">**mmioGetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   [<span data-ttu-id="c2ffd-123">**mmioInstallIOProc**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-123">**mmioInstallIOProc**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [<span data-ttu-id="c2ffd-124">**mmioOpen**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-124">**mmioOpen**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [<span data-ttu-id="c2ffd-125">**mmioRead**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-125">**mmioRead**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [<span data-ttu-id="c2ffd-126">**mmioRename**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-126">**mmioRename**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [<span data-ttu-id="c2ffd-127">**mmioSeek**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-127">**mmioSeek**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [<span data-ttu-id="c2ffd-128">**mmioSendMessage**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-128">**mmioSendMessage**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)
-   [<span data-ttu-id="c2ffd-129">**mmioSetBuffer**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-129">**mmioSetBuffer**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [<span data-ttu-id="c2ffd-130">**mmioSetInfo**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-130">**mmioSetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)
-   [<span data-ttu-id="c2ffd-131">**mmioStringToFOURCC**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-131">**mmioStringToFOURCC**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)
-   [<span data-ttu-id="c2ffd-132">**mmioWrite**</span><span class="sxs-lookup"><span data-stu-id="c2ffd-132">**mmioWrite**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="related-topics"></a><span data-ttu-id="c2ffd-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c2ffd-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2ffd-134">Riferimento I/O file multimediale</span><span class="sxs-lookup"><span data-stu-id="c2ffd-134">Multimedia File I/O Reference</span></span>](multimedia-file-i-o-reference.md)
</dt> </dl>

 

 