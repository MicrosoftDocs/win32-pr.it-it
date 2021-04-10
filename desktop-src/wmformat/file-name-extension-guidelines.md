---
title: Linee guida sull'estensione del nome file
description: Linee guida sull'estensione del nome file
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- Windows Media Format SDK, estensioni di file
- ASF (Advanced Systems Format), estensioni di file
- ASF (Advanced Systems Format), estensioni di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bed1fb59379644711a3954dc5eb82707e0e42f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955424"
---
# <a name="file-name-extension-guidelines"></a><span data-ttu-id="74b91-106">Linee guida sull'estensione del nome file</span><span class="sxs-lookup"><span data-stu-id="74b91-106">File Name Extension Guidelines</span></span>

<span data-ttu-id="74b91-107">Un'estensione di file fornisce un fornitore di software indipendente con informazioni sui requisiti di rendering di un'applicazione che utilizza l'estensione specifica.</span><span class="sxs-lookup"><span data-stu-id="74b91-107">A file name extension provides an independent software vendor with information about the rendering requirements of an application that uses that particular extension.</span></span>

<span data-ttu-id="74b91-108">L'estensione del nome di file che è necessario usare per un file creato da un'applicazione basata su Windows Media Format SDK è determinata dal tipo di contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="74b91-108">The file name extension you must use for a file created by an application based on the Windows Media Format SDK is determined by the type of content in the file.</span></span> <span data-ttu-id="74b91-109">Usare la logica seguente per determinare l'estensione del nome di file che è necessario usare.</span><span class="sxs-lookup"><span data-stu-id="74b91-109">Use the following logic to determine the file name extension you must use.</span></span>

<span data-ttu-id="74b91-110">Se il file contiene flussi codificati con codec di terze parti o dati non compressi non supportati (inclusi dati arbitrari), il file deve utilizzare l'estensione ASF.</span><span class="sxs-lookup"><span data-stu-id="74b91-110">If the file contains any streams encoded with third-party codecs or any unsupported uncompressed data (including arbitrary data), the file must use the .asf extension.</span></span>

<span data-ttu-id="74b91-111">Se il file non contiene flussi non supportati e contiene uno o più flussi video non compressi o codificati con qualsiasi codec video Windows Media, il file deve usare l'estensione. wmv.</span><span class="sxs-lookup"><span data-stu-id="74b91-111">If the file contains no unsupported streams and contains one or more video streams either uncompressed or encoded with any Windows Media video codec, the file must use the .wmv extension.</span></span> <span data-ttu-id="74b91-112">Questi file possono includere anche flussi audio PCM, flussi audio codificati con qualsiasi codec audio Windows Media, flussi di script e flussi Web.</span><span class="sxs-lookup"><span data-stu-id="74b91-112">These files may also include PCM audio streams, audio streams encoded with any Windows Media audio codec, script streams, and Web streams.</span></span>

<span data-ttu-id="74b91-113">Se il file non contiene flussi non supportati e nessun flusso video supportato e contiene uno o più flussi audio decompressi PCM o codificati con qualsiasi codec audio Windows Media, il file deve utilizzare l'estensione WMA.</span><span class="sxs-lookup"><span data-stu-id="74b91-113">If the file contains no unsupported streams and no supported video streams, and contains one or more audio streams either uncompressed PCM or encoded with any Windows Media audio codec, the file must use the .wma extension.</span></span> <span data-ttu-id="74b91-114">Questi file possono contenere anche flussi di script e flussi Web.</span><span class="sxs-lookup"><span data-stu-id="74b91-114">These files may also contain script streams, and Web streams.</span></span>

<span data-ttu-id="74b91-115">Se il file contiene solo flussi che non sono audio né video, è necessario usare l'estensione ASF.</span><span class="sxs-lookup"><span data-stu-id="74b91-115">If the file contains only streams that are neither audio nor video, it must use the .asf extension.</span></span>

<span data-ttu-id="74b91-116">I tipi di video non compressi supportati includono RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU e YVU9.</span><span class="sxs-lookup"><span data-stu-id="74b91-116">Supported uncompressed video types include RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU, and YVU9.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74b91-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="74b91-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74b91-118">**Considerazioni sui progetti**</span><span class="sxs-lookup"><span data-stu-id="74b91-118">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




