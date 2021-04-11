---
description: Acquisisci DV nel file
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: Acquisisci DV nel file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341916"
---
# <a name="capture-dv-to-file"></a><span data-ttu-id="47ad2-103">Acquisisci DV nel file</span><span class="sxs-lookup"><span data-stu-id="47ad2-103">Capture DV to File</span></span>

<span data-ttu-id="47ad2-104">Questa sezione descrive come acquisire video digitali (DV) da una videocamera DV o da un nastro VTR.</span><span class="sxs-lookup"><span data-stu-id="47ad2-104">This section describes how to capture digital video (DV) from a DV camera or from a VTR tape.</span></span>

1.  <span data-ttu-id="47ad2-105">Creare un'istanza del filtro del [driver Msdv](msdv-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="47ad2-105">Create an instance of the [MSDV Driver](msdv-driver.md) filter.</span></span> <span data-ttu-id="47ad2-106">Per altre informazioni, vedere [selezione di un dispositivo di acquisizione](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="47ad2-106">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>
2.  <span data-ttu-id="47ad2-107">Inizializzare il generatore di grafici di acquisizione, come descritto in [informazioni sul generatore di grafici di acquisizione](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="47ad2-107">Initialize the Capture Graph Builder, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
3.  <span data-ttu-id="47ad2-108">Compilare il grafico di acquisizione, a seconda del tipo di file di destinazione:</span><span class="sxs-lookup"><span data-stu-id="47ad2-108">Build the capture graph, depending on the target file type:</span></span>
    -   [<span data-ttu-id="47ad2-109">Acquisire un file DV di tipo 1</span><span class="sxs-lookup"><span data-stu-id="47ad2-109">Capture a Type-1 DV File</span></span>](capture-a-type-1-dv-file.md)
    -   [<span data-ttu-id="47ad2-110">Acquisire un file DV di tipo 2</span><span class="sxs-lookup"><span data-stu-id="47ad2-110">Capture a Type-2 DV File</span></span>](capture-a-type-2-dv-file.md)
    -   [<span data-ttu-id="47ad2-111">Acquisisci DV in RGB non compresso</span><span class="sxs-lookup"><span data-stu-id="47ad2-111">Capture DV to Uncompressed RGB</span></span>](capture-dv-to-uncompressed-rgb.md)
4.  <span data-ttu-id="47ad2-112">Eseguire il grafo.</span><span class="sxs-lookup"><span data-stu-id="47ad2-112">Run the graph.</span></span>

<span data-ttu-id="47ad2-113">L'acquisizione da un nastro VTR funziona esattamente come l'acquisizione di video live dalla fotocamera, ad eccezione del fatto che è necessario riprodurre il nastro, come descritto in [controllo di una videocamera DV](controlling-a-dv-camcorder.md).</span><span class="sxs-lookup"><span data-stu-id="47ad2-113">Capturing from a VTR tape works just like capturing live video from the camera, except that you must play the tape, as described in [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span> <span data-ttu-id="47ad2-114">Per evitare la perdita di frame, eseguire prima il grafo, quindi riprodurre il nastro.</span><span class="sxs-lookup"><span data-stu-id="47ad2-114">To avoid losing any frames, run the graph first, and then play the tape.</span></span> <span data-ttu-id="47ad2-115">Al termine della trasmissione, arrestare prima il nastro e quindi arrestare il grafo.</span><span class="sxs-lookup"><span data-stu-id="47ad2-115">When you are done transmitting, stop the tape first and then stop the graph.</span></span>

> [!Note]  
> <span data-ttu-id="47ad2-116">La videocamera deve essere in modalità VTR.</span><span class="sxs-lookup"><span data-stu-id="47ad2-116">The camcorder must be in VTR mode.</span></span> <span data-ttu-id="47ad2-117">Vedere [modalità dispositivo](device-mode.md).</span><span class="sxs-lookup"><span data-stu-id="47ad2-117">See [Device Mode](device-mode.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="47ad2-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47ad2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47ad2-119">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="47ad2-119">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="47ad2-120">Tipo-1 e file AVI DV di tipo 2</span><span class="sxs-lookup"><span data-stu-id="47ad2-120">Type-1 vs. Type-2 DV AVI Files</span></span>](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[<span data-ttu-id="47ad2-121">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="47ad2-121">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



