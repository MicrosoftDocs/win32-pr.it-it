---
description: Digitare-1 rispetto a
ms.assetid: 3f1cf981-f678-46a6-9784-ffb389438b6d
title: Tipo-1 e file AVI DV di tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000b81e94e25749b5590287145a88a28280e16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967691"
---
# <a name="type-1-vs-type-2-dv-avi-files"></a><span data-ttu-id="99f3d-103">Tipo-1 e file AVI DV di tipo 2</span><span class="sxs-lookup"><span data-stu-id="99f3d-103">Type-1 vs. Type-2 DV AVI Files</span></span>

<span data-ttu-id="99f3d-104">Le fotocamere DV producono audio-video con interfoliazione ogni frame di video contiene anche le informazioni audio.</span><span class="sxs-lookup"><span data-stu-id="99f3d-104">DV cameras produce interleaved audio-video; each frame of video also contains the audio information.</span></span> <span data-ttu-id="99f3d-105">Se si salvano i dati DV in un file AVI, è possibile scegliere:</span><span class="sxs-lookup"><span data-stu-id="99f3d-105">If you save DV data to an AVI file, you have a choice:</span></span>

-   <span data-ttu-id="99f3d-106">Archiviare i dati con interfoliazione come un flusso nel file AVI.</span><span class="sxs-lookup"><span data-stu-id="99f3d-106">Store the interleaved data as one stream in the AVI file.</span></span> <span data-ttu-id="99f3d-107">Questa operazione è nota come file di tipo 1.</span><span class="sxs-lookup"><span data-stu-id="99f3d-107">This is known as a type-1 file.</span></span>
-   <span data-ttu-id="99f3d-108">Suddividere i dati con interfoliazione in flussi audio e video distinti.</span><span class="sxs-lookup"><span data-stu-id="99f3d-108">Split the interleaved data into separate audio and video streams.</span></span> <span data-ttu-id="99f3d-109">Questa operazione è nota come file di tipo 2.</span><span class="sxs-lookup"><span data-stu-id="99f3d-109">This is known as a type-2 file.</span></span>

<span data-ttu-id="99f3d-110">Per l'acquisizione video, in cui la velocità effettiva massima è cruciale, è preferibile usare un file di tipo 1, perché i file di tipo 2 contengono dati audio ridondanti.</span><span class="sxs-lookup"><span data-stu-id="99f3d-110">For video capture, where maximum throughput is crucial, it is better to use a type-1 file, because type-2 files carry redundant audio data.</span></span> <span data-ttu-id="99f3d-111">Il flusso video contiene ancora i dati audio.</span><span class="sxs-lookup"><span data-stu-id="99f3d-111">(The video stream still has the audio data.</span></span> <span data-ttu-id="99f3d-112">L'audio è semplicemente nascosto etichettando il flusso come video. Inoltre, la scrittura di un file di tipo 2 richiede un tempo di elaborazione aggiuntivo per suddividere il flusso con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="99f3d-112">The audio is simply hidden by labeling the stream as video.) Also, writing a type-2 file requires some additional processor time to split the interleaved stream.</span></span>

<span data-ttu-id="99f3d-113">D'altra parte, i file di tipo 1 risultano meno efficienti per la modifica in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="99f3d-113">On the other hand, type-1 files are less efficient for real-time editing.</span></span> <span data-ttu-id="99f3d-114">L'applicazione deve estrarre l'audio dal flusso con interfoliazione, apportare le modifiche ed eseguire di nuovo l'interfoliazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="99f3d-114">The application must extract the audio from the interleaved stream, make the edits, and interleave the data again.</span></span> <span data-ttu-id="99f3d-115">Inoltre, il formato di tipo-1 non è compatibile con Microsoft® video for Windows® (VFW).</span><span class="sxs-lookup"><span data-stu-id="99f3d-115">Also, the type-1 format is not compatible with Microsoft® Video for Windows® (VFW).</span></span> <span data-ttu-id="99f3d-116">DirectShow è in grado di gestire entrambi i tipi di file.</span><span class="sxs-lookup"><span data-stu-id="99f3d-116">DirectShow can handle both types of files.</span></span>

<span data-ttu-id="99f3d-117">Un file di tipo 2 può essere convertito nel tipo-1 usando il filtro [muxer DV](dv-muxer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="99f3d-117">A type-2 file can be converted to type-1 using the [DV Muxer](dv-muxer-filter.md) filter.</span></span> <span data-ttu-id="99f3d-118">Un file di tipo 1 può essere convertito nel tipo-2 usando il filtro della [barra di divisione DV](dv-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="99f3d-118">A type-1 file can be converted to type-2 using the [DV Splitter](dv-splitter-filter.md) filter.</span></span> <span data-ttu-id="99f3d-119">Il diagramma seguente illustra la differenza tra i due formati.</span><span class="sxs-lookup"><span data-stu-id="99f3d-119">The following diagram illustrates the difference between the two formats.</span></span>

![conversione tra Type-1 e Type-2 DV](images/dv-filters3.png)

## <a name="related-topics"></a><span data-ttu-id="99f3d-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99f3d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99f3d-122">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="99f3d-122">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="99f3d-123">Dati DV nel formato di file AVI</span><span class="sxs-lookup"><span data-stu-id="99f3d-123">DV Data in the AVI File Format</span></span>](dv-data-in-the-avi-file-format.md)
</dt> </dl>

 

 



