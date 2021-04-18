---
description: Trasmettere DV da un file a un nastro
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Trasmettere DV da un file a un nastro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415a12f0876d3bd8e2a46de58b15f96f3eba3e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316291"
---
# <a name="transmit-dv-from-file-to-tape"></a><span data-ttu-id="d781c-103">Trasmettere DV da un file a un nastro</span><span class="sxs-lookup"><span data-stu-id="d781c-103">Transmit DV from File to Tape</span></span>

<span data-ttu-id="d781c-104">La trasmissione dal file DV AVI al nastro VTR è piuttosto complicata dal fatto che i file possono digitare-1 o digitare-2.</span><span class="sxs-lookup"><span data-stu-id="d781c-104">Transmit from DV AVI file to VTR tape is complicated somewhat by the fact that files can type-1 or type-2.</span></span> <span data-ttu-id="d781c-105">Per trasmettere un file DV su nastro, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d781c-105">To transmit a DV file to tape, do the following:</span></span>

1.  <span data-ttu-id="d781c-106">Creare un'istanza del filtro del [driver Msdv](msdv-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="d781c-106">Create an instance of the [MSDV Driver](msdv-driver.md) filter.</span></span> <span data-ttu-id="d781c-107">Per altre informazioni, vedere [selezione di un dispositivo di acquisizione](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="d781c-107">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>
2.  <span data-ttu-id="d781c-108">Verificare che il dispositivo sia in modalità VTR.</span><span class="sxs-lookup"><span data-stu-id="d781c-108">Make sure the device is in VTR mode.</span></span> <span data-ttu-id="d781c-109">In caso contrario, non sarà possibile trasmettere su nastro. Vedere [modalità dispositivo](device-mode.md).</span><span class="sxs-lookup"><span data-stu-id="d781c-109">Otherwise, you cannot transmit to tape.See [Device Mode](device-mode.md).</span></span>
3.  <span data-ttu-id="d781c-110">Inizializzare il generatore di grafici di acquisizione, come descritto in [informazioni sul generatore di grafici di acquisizione](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="d781c-110">Initialize the Capture Graph Builder, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
4.  <span data-ttu-id="d781c-111">Compilare il grafo.</span><span class="sxs-lookup"><span data-stu-id="d781c-111">Build the graph.</span></span> <span data-ttu-id="d781c-112">La configurazione del grafico dipende dal tipo di file DV:</span><span class="sxs-lookup"><span data-stu-id="d781c-112">The graph configuration depends on the DV file type:</span></span>
    -   [<span data-ttu-id="d781c-113">Trasmissione da un file di tipo 1</span><span class="sxs-lookup"><span data-stu-id="d781c-113">Transmit from Type-1 File</span></span>](transmit-from-type-1-file.md)
    -   [<span data-ttu-id="d781c-114">Trasmissione da un file di tipo 2</span><span class="sxs-lookup"><span data-stu-id="d781c-114">Transmit from Type-2 File</span></span>](transmit-from-type-2-file.md)
5.  <span data-ttu-id="d781c-115">Impostare il dispositivo in modalità di sospensione dei record, come descritto in [controllo di una videocamera DV](controlling-a-dv-camcorder.md).</span><span class="sxs-lookup"><span data-stu-id="d781c-115">Put the device into record-pause mode, as described in [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span>
6.  <span data-ttu-id="d781c-116">Sospendere il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="d781c-116">Pause the filter graph.</span></span> <span data-ttu-id="d781c-117">Mentre il grafico a filtro è sospeso, invia un flusso continuo che ripete il primo frame di video.</span><span class="sxs-lookup"><span data-stu-id="d781c-117">While the filter graph is paused, it sends a continuous stream that repeats the first frame of video.</span></span>
7.  <span data-ttu-id="d781c-118">Per avviare la trasmissione, impostare il dispositivo in modalità registrazione e quindi eseguire il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="d781c-118">To start transmitting, put the device into record mode and then run the filter graph.</span></span> <span data-ttu-id="d781c-119">Il dispositivo richiede una certa quantità di tempo fino a quando l'Head di registrazione non è in grado di registrare, quindi attendere circa due secondi prima di eseguire il grafo.</span><span class="sxs-lookup"><span data-stu-id="d781c-119">It takes the device a certain amount of time until the recording head is able to record, so wait for about two seconds before running the graph.</span></span> <span data-ttu-id="d781c-120">Questo potrebbe comportare alcuni frame duplicati all'inizio del nastro, ma garantisce che non si verifichino perdite di dati.</span><span class="sxs-lookup"><span data-stu-id="d781c-120">This might result in a few duplicated frames at the beginning of the tape, but it ensures that no data is lost.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d781c-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d781c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d781c-122">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d781c-122">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



