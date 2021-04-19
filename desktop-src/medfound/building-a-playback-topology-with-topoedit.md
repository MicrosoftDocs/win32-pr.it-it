---
description: Compilazione di una topologia di riproduzione con TopoEdit
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: Compilazione di una topologia di riproduzione con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f942984b3ba56ef1288566cee80e7d30026de155
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320211"
---
# <a name="building-a-playback-topology-with-topoedit"></a><span data-ttu-id="40e59-103">Compilazione di una topologia di riproduzione con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="40e59-103">Building a Playback Topology with TopoEdit</span></span>

<span data-ttu-id="40e59-104">TopoEdit può compilare una topologia di riproduzione per un file multimediale locale aggiungendo e connettendo automaticamente i nodi di origine, trasformazione e output.</span><span class="sxs-lookup"><span data-stu-id="40e59-104">TopoEdit can build a playback topology for a local media file by automatically adding and connecting the source, transform, and output nodes.</span></span> <span data-ttu-id="40e59-105">TopoEdit non risolve automaticamente la topologia.</span><span class="sxs-lookup"><span data-stu-id="40e59-105">TopoEdit does not automatically resolve the topology.</span></span> <span data-ttu-id="40e59-106">Per riprodurre la topologia, risolverla e quindi usare i controlli di trasporto.</span><span class="sxs-lookup"><span data-stu-id="40e59-106">To play the topology, resolve it and then use the transport controls.</span></span>

## <a name="to-build-and-play-a-topology-for-a-media-file"></a><span data-ttu-id="40e59-107">Per compilare e riprodurre una topologia per un file multimediale</span><span class="sxs-lookup"><span data-stu-id="40e59-107">To build and play a topology for a media file</span></span>

1.  <span data-ttu-id="40e59-108">Scegliere **file di rendering** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="40e59-108">On the **File** menu, click **Render File**.</span></span>

    <span data-ttu-id="40e59-109">Verrà visualizzata la finestra di dialogo **Seleziona origine multimediale** .</span><span class="sxs-lookup"><span data-stu-id="40e59-109">This opens the **Select Media Source** dialog box.</span></span>

2.  <span data-ttu-id="40e59-110">Passare alla cartella in cui si trova il file multimediale.</span><span class="sxs-lookup"><span data-stu-id="40e59-110">Navigate to the folder where the media file is located.</span></span>
3.  <span data-ttu-id="40e59-111">Nel campo **nome file:** immettere il nome del file.</span><span class="sxs-lookup"><span data-stu-id="40e59-111">In the **File name:** field, enter the name of the file.</span></span>
4.  <span data-ttu-id="40e59-112">Fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="40e59-112">Click **Open**.</span></span>

    <span data-ttu-id="40e59-113">Il **riquadro topologia** Mostra la topologia connessa.</span><span class="sxs-lookup"><span data-stu-id="40e59-113">The **Topology Pane** shows the connected topology.</span></span> <span data-ttu-id="40e59-114">Internamente, TopoEdit esegue le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="40e59-114">Internally, TopoEdit performs the following tasks:</span></span>

    -   <span data-ttu-id="40e59-115">Enumera i flussi nel file multimediale e crea i nodi di origine.</span><span class="sxs-lookup"><span data-stu-id="40e59-115">Enumerates the streams in the media file and creates the source nodes.</span></span>
    -   <span data-ttu-id="40e59-116">A seconda del tipo di supporto dei nodi di origine, aggiunge i nodi di trasformazione, ad esempio i decodificatori.</span><span class="sxs-lookup"><span data-stu-id="40e59-116">Depending on the media type of the source nodes, adds transform nodes, such as decoders.</span></span>
    -   <span data-ttu-id="40e59-117">Consente di aggiungere il sink di streaming audio renderer (SAR) per il flusso audio e il sink EVR (Enhanced video renderer) per il flusso video.</span><span class="sxs-lookup"><span data-stu-id="40e59-117">Adds the Streaming Audio Renderer (SAR) sink for audio stream and the enhanced video renderer (EVR) sink for the video stream.</span></span>
    -   <span data-ttu-id="40e59-118">Connette gli input del nodo e gli output del nodo.</span><span class="sxs-lookup"><span data-stu-id="40e59-118">Connects the node inputs and the node outputs.</span></span>

5.  <span data-ttu-id="40e59-119">Scegliere **Risolvi topologia** dal menu **topologia** .</span><span class="sxs-lookup"><span data-stu-id="40e59-119">On the **Topology** menu, click **Resolve Topology**.</span></span>
6.  <span data-ttu-id="40e59-120">Fare clic sul pulsante **Riproduci** sulla barra degli strumenti per riprodurre la topologia.</span><span class="sxs-lookup"><span data-stu-id="40e59-120">Click the **Play** button on the toolbar to play the topology.</span></span> La figura seguente mostra il pulsante **Riproduci** :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: .

## <a name="related-topics"></a><span data-ttu-id="40e59-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40e59-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40e59-123">Controlli di riproduzione in TopoEdit</span><span class="sxs-lookup"><span data-stu-id="40e59-123">Playback Controls in TopoEdit</span></span>](playback-controls-in-topoedit.md)
</dt> <dt>

[<span data-ttu-id="40e59-124">Risoluzione di una topologia con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="40e59-124">Resolving a Topology with TopoEdit</span></span>](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[<span data-ttu-id="40e59-125">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="40e59-125">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



