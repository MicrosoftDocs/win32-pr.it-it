---
description: Aggiunta di nodi di output con TopoEdit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Aggiunta di nodi di output con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dc30631332e8138b35e4bbc0ccde75ec9b0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306760"
---
# <a name="adding-output-nodes-with-topoedit"></a><span data-ttu-id="784d8-103">Aggiunta di nodi di output con TopoEdit</span><span class="sxs-lookup"><span data-stu-id="784d8-103">Adding Output Nodes with TopoEdit</span></span>

<span data-ttu-id="784d8-104">In una topologia un nodo di output rappresenta un sink multimediale che riceve i dati multimediali da un nodo di trasformazione e li presenta per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="784d8-104">In a topology, an output node represents a media sink that receives media data from a transform node and presents it for playback.</span></span> <span data-ttu-id="784d8-105">Il tipo di nodo di output dipende dal tipo di supporto del nodo di origine.</span><span class="sxs-lookup"><span data-stu-id="784d8-105">The type of output node depends on the media type of the source node.</span></span>

<span data-ttu-id="784d8-106">Nella tabella seguente viene illustrato il comando menu/barra degli strumenti per aggiungere un nodo di output alla topologia.</span><span class="sxs-lookup"><span data-stu-id="784d8-106">The following table shows the menu/toolbar command for adding an output node to the topology.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="784d8-107">Tipo di supporto di origine</span><span class="sxs-lookup"><span data-stu-id="784d8-107">Source media type</span></span></th>
<th><span data-ttu-id="784d8-108">Comando menu/barra degli strumenti</span><span class="sxs-lookup"><span data-stu-id="784d8-108">Menu/Toolbar Command</span></span></th>
<th><span data-ttu-id="784d8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="784d8-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="784d8-110">Flusso audio</span><span class="sxs-lookup"><span data-stu-id="784d8-110">Audio stream</span></span></td>
<td><span data-ttu-id="784d8-111">Scegliere <strong>Aggiungi SAR</strong>dal menu <strong>topologia</strong> .</span><span class="sxs-lookup"><span data-stu-id="784d8-111">On the <strong>Topology</strong> menu, click <strong>Add SAR</strong>.</span></span></td>
<td><span data-ttu-id="784d8-112">Crea un nodo di output per il renderer di streaming audio (SAR) che riproduce un flusso audio tramite un dispositivo audio, ad esempio una scheda audio.</span><span class="sxs-lookup"><span data-stu-id="784d8-112">Creates an output node for the Streaming Audio Renderer (SAR) that plays an audio stream through an audio device such as a sound card.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="784d8-113">Flusso video</span><span class="sxs-lookup"><span data-stu-id="784d8-113">Video stream</span></span></td>
<td><span data-ttu-id="784d8-114">Nel menu <strong>topologia</strong> fare clic su <strong>Aggiungi EVR</strong>.</span><span class="sxs-lookup"><span data-stu-id="784d8-114">On the <strong>Topology</strong> menu, click <strong>Add EVR</strong>.</span></span></td>
<td><span data-ttu-id="784d8-115">Crea un nodo di output per il renderer video avanzato (EVR) che Visualizza i frame per un flusso video.</span><span class="sxs-lookup"><span data-stu-id="784d8-115">Creates an output node for the enhanced video renderer (EVR) that displays frames for a video stream.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="784d8-116">Sink di supporti personalizzati</span><span class="sxs-lookup"><span data-stu-id="784d8-116">Custom media sink</span></span></td>
<td><ol>
<li><span data-ttu-id="784d8-117">Scegliere <strong>Aggiungi sink personalizzato</strong>dal menu <strong>topologia</strong> .</span><span class="sxs-lookup"><span data-stu-id="784d8-117">On the <strong>Topology</strong> menu, click <strong>Add Custom Sink</strong>.</span></span><br/> <span data-ttu-id="784d8-118">Verrà visualizzata la finestra di dialogo <strong>GUID personalizzato di input</strong> .</span><span class="sxs-lookup"><span data-stu-id="784d8-118">The <strong>Input Custom GUID</strong> dialog box opens.</span></span><br/></li>
<li><p><span data-ttu-id="784d8-119">Nel campo <strong>GUID:</strong> immettere il GUID del sink personalizzato che si desidera aggiungere alla topologia.</span><span class="sxs-lookup"><span data-stu-id="784d8-119">In the <strong>GUID:</strong> field, enter the GUID of your custom sink that you want to add to the topology.</span></span><br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="784d8-120">TopoEdit prevede il GUID nel formato &quot; {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} &quot; .</span><span class="sxs-lookup"><span data-stu-id="784d8-120">TopoEdit expects the GUID in the format &quot;{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}&quot;.</span></span> <span data-ttu-id="784d8-121">In caso contrario, non sarà possibile aggiungere il nodo e verrà visualizzato un &quot; messaggio di errore GUID non valido &quot; .</span><span class="sxs-lookup"><span data-stu-id="784d8-121">Otherwise, it fails to add the node and displays an &quot;Invalid GUID&quot; error message.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="784d8-122">Fare clic su <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="784d8-122">Click <strong>OK</strong>.</span></span><br/></li>
</ol></td>
<td><span data-ttu-id="784d8-123">Crea un nodo di output per il sink di flusso per un'origine multimediale personalizzata.</span><span class="sxs-lookup"><span data-stu-id="784d8-123">Creates an output node for the stream sink for a custom media source.</span></span><br/> <span data-ttu-id="784d8-124">Il sink personalizzato deve supportare <strong>CoCreateInstance</strong> , in modo che il sink possa essere specificato con un CLSID.</span><span class="sxs-lookup"><span data-stu-id="784d8-124">The custom sink must support <strong>CoCreateInstance</strong> so that the sink can be specified with a CLSID.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="784d8-125">TopoEdit crea il nodo di output specificato.</span><span class="sxs-lookup"><span data-stu-id="784d8-125">TopoEdit creates the specified output node.</span></span> <span data-ttu-id="784d8-126">Il **riquadro topologia** Mostra il nodo output come una casella verde che mostra il nome del sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="784d8-126">The **Topology Pane** shows the output node as a green box that shows the name of the stream sink.</span></span>

<span data-ttu-id="784d8-127">Per informazioni sull'aggiunta di nodi di output a livello di codice usando le API di Media Foundation, vedere [creazione di nodi di output](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="784d8-127">For information about adding output nodes programmatically by using Media Foundation APIs, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="784d8-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="784d8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="784d8-129">Compilazione di topologie tramite TopoEdit</span><span class="sxs-lookup"><span data-stu-id="784d8-129">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="784d8-130">Renderer audio di streaming</span><span class="sxs-lookup"><span data-stu-id="784d8-130">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> <dt>

[<span data-ttu-id="784d8-131">Renderer video migliorato</span><span class="sxs-lookup"><span data-stu-id="784d8-131">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="784d8-132">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="784d8-132">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 




