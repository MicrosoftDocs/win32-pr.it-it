---
description: Registrazione delle attività del nodo della topologia
ms.assetid: 853b3900-1214-43b9-bf0e-e45c1159c5f1
title: Registrazione delle attività del nodo della topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ca83d0513b97d053e27388bd0f2a418dfb253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049632"
---
# <a name="logging-topology-node-activities"></a><span data-ttu-id="6c312-103">Registrazione delle attività del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="6c312-103">Logging Topology Node Activities</span></span>

<span data-ttu-id="6c312-104">TopoEdit fornisce l'opzione per la raccolta di informazioni di registrazione per un nodo di trasformazione o un nodo di output di una topologia.</span><span class="sxs-lookup"><span data-stu-id="6c312-104">TopoEdit provides the option for collecting logging information for a transform node or an output node of a topology.</span></span>

## <a name="to-setup-logging"></a><span data-ttu-id="6c312-105">Per configurare la registrazione</span><span class="sxs-lookup"><span data-stu-id="6c312-105">To setup logging</span></span>

1.  <span data-ttu-id="6c312-106">Nel **riquadro topologia** selezionare un nodo di trasformazione o un nodo di output facendo clic su di esso.</span><span class="sxs-lookup"><span data-stu-id="6c312-106">On the **Topology Pane**, select a transform node or an output node by clicking it.</span></span>

2.  <span data-ttu-id="6c312-107">Dal menu **strumenti** fare clic su **Spy nodo selezionato**.</span><span class="sxs-lookup"><span data-stu-id="6c312-107">From the **Tools** menu, click **Spy Selected Node**.</span></span>

<span data-ttu-id="6c312-108">Durante la compilazione della topologia, tutte le chiamate al metodo sul nodo selezionato vengono registrate in un file di testo.</span><span class="sxs-lookup"><span data-stu-id="6c312-108">During topology building, all method calls on the selected node are logged to a text file.</span></span> <span data-ttu-id="6c312-109">Questa operazione viene salvata nella cartella in cui si trova il file multimediale.</span><span class="sxs-lookup"><span data-stu-id="6c312-109">This is saved in the folder where the media file is located.</span></span> <span data-ttu-id="6c312-110">Il file di log viene salvato con il nome del nodo e l'identificatore univoco del nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="6c312-110">The log file is saved with the node name and the unique topology node identifier.</span></span> <span data-ttu-id="6c312-111">In questo modo si garantisce che nessun altro nodo scriva nel log.</span><span class="sxs-lookup"><span data-stu-id="6c312-111">This ensures that no other node writes to the log.</span></span> <span data-ttu-id="6c312-112">Per ottenere l'identificatore a livello di codice, chiamare [**IMFTopologyNode:: GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span><span class="sxs-lookup"><span data-stu-id="6c312-112">To get the identifier programmatically, call [**IMFTopologyNode::GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span></span>

<span data-ttu-id="6c312-113">Di seguito è riportato un Estratto da un file di log.</span><span class="sxs-lookup"><span data-stu-id="6c312-113">The following is an excerpt from a log file.</span></span>

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729720 1 02729760) returns 80004001`

`GetInputCurrentType(0 02C9F4A4) returns c00d6d60`

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729760 1 02729720) returns 80004001`

`SetInputType(0 0012F8D8 0) returns 0`

`--> Arg(2, in) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=WMAudioV8, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=2048, AVG_BYTES_PER_SECOND=12000, BITS_PER_SAMPLE=16, USER_DATA=<BLOB>, {9D62927D-36BE-4CF2-B5C4-A3926E3E8711}=5760, {9D62927F-36BE-4CF2-B5C4-A3926E3E8711}=674,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputCurrentType(0 02C9F4B0) returns c00d6d60`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729640 1 02729720) returns 80004001`

`GetOutputAvailableType(0 0 02C9F4B0) returns 0`

`--> Arg(3, out) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=Float, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=8, AVG_BYTES_PER_SECOND=384000, BITS_PER_SAMPLE=32, ALL_SAMPLES_INDEPENDENT=1, FIXED_SIZE_SAMPLES=1,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputAvailableType(0 1 02C9F4B0) returns 0`

## <a name="related-topics"></a><span data-ttu-id="6c312-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c312-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c312-115">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="6c312-115">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



