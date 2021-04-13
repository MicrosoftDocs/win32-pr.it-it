---
description: Compilazione avanzata della topologia
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Compilazione avanzata della topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4cc061d4e557dda4ccbb81eabc55e8e1b3e33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343336"
---
# <a name="advanced-topology-building"></a><span data-ttu-id="566be-103">Compilazione avanzata della topologia</span><span class="sxs-lookup"><span data-stu-id="566be-103">Advanced Topology Building</span></span>

<span data-ttu-id="566be-104">In questa sezione vengono descritte alcune tecniche avanzate per la creazione di topologie.</span><span class="sxs-lookup"><span data-stu-id="566be-104">This section describes some advanced techniques for building topologies.</span></span> <span data-ttu-id="566be-105">È possibile utilizzare queste tecniche se si desidera un maggiore controllo sulle topologie inviate alla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="566be-105">You can use these techniques if you want more control over the topologies that you send to the Media Session.</span></span>

<span data-ttu-id="566be-106">Poiché queste tecniche sono destinate a scenari che vanno oltre la funzionalità fornita dal caricatore della topologia standard, molti dei dettagli dipendono dai requisiti specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="566be-106">Because these techniques are intended for scenarios that go beyond the functionality provided by the standard topology loader, many of the details will depend on the particular requirements of your application.</span></span> <span data-ttu-id="566be-107">Questa sezione è quindi organizzata in modo più ampio per le sottoattività più piccole, anziché per completare gli scenari end-to-end.</span><span class="sxs-lookup"><span data-stu-id="566be-107">Therefore, this section is organized loosely around smaller subtasks, rather than complete, end-to-end scenarios.</span></span>

<span data-ttu-id="566be-108">L'applicazione di riproduzione tipica segue questa procedura:</span><span class="sxs-lookup"><span data-stu-id="566be-108">The typical playback application follows these steps:</span></span>

1.  <span data-ttu-id="566be-109">L'applicazione compila una topologia parziale e la accoda nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="566be-109">The application builds a partial topology and queues it on the Media Session.</span></span>
2.  <span data-ttu-id="566be-110">La sessione multimediale richiama il caricatore della topologia per risolvere la topologia.</span><span class="sxs-lookup"><span data-stu-id="566be-110">The Media Session invokes the topology loader to resolve the topology.</span></span>

<span data-ttu-id="566be-111">Se si vuole superare le funzionalità del caricatore della topologia, sono disponibili tre approcci generali:</span><span class="sxs-lookup"><span data-stu-id="566be-111">If you want to go beyond the capabilities of the topology loader, there are three general approaches:</span></span>

-   <span data-ttu-id="566be-112">Creare una topologia completa.</span><span class="sxs-lookup"><span data-stu-id="566be-112">Build a complete topology.</span></span> <span data-ttu-id="566be-113">Quando si accoda la topologia nella sessione multimediale, chiamare [**IMFMediaSession:: la topologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) con il \_ flag MFSESSION della topologia \_ NoSolution.</span><span class="sxs-lookup"><span data-stu-id="566be-113">When you queue the topology on the Media Session, call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) with the MFSESSION\_SETTOPOLOGY\_NORESOLUTION flag.</span></span> <span data-ttu-id="566be-114">Questo flag impedisce alla sessione multimediale di tentare di risolvere la topologia.</span><span class="sxs-lookup"><span data-stu-id="566be-114">This flag prevents the Media Session from attempting to resolve the topology.</span></span>

-   <span data-ttu-id="566be-115">Richiamare direttamente il caricatore della topologia per risolvere la topologia.</span><span class="sxs-lookup"><span data-stu-id="566be-115">Directly invoke the topology loader to resolve the topology.</span></span> <span data-ttu-id="566be-116">È quindi possibile modificare la topologia completa prima di accodarla nella sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="566be-116">You can then modify the full topology before queuing it on the Media Session.</span></span>

-   <span data-ttu-id="566be-117">Implementare un caricatore di topologia personalizzato.</span><span class="sxs-lookup"><span data-stu-id="566be-117">Implement a custom topology loader.</span></span> <span data-ttu-id="566be-118">Con questo approccio, viene accodata una topologia parziale, ma la sessione multimediale richiama il caricatore personalizzato invece dell'implementazione di Media Foundation standard.</span><span class="sxs-lookup"><span data-stu-id="566be-118">With this approach, you queue a partial topology, but the Media Session invokes your custom loader instead of the standard Media Foundation implementation.</span></span> <span data-ttu-id="566be-119">Un vantaggio di questo approccio è che è possibile eseguire la compilazione di topologia personalizzata all'interno dell'ambiente protetto.</span><span class="sxs-lookup"><span data-stu-id="566be-119">One advantage of this approach is that you can perform custom topology building inside the protected environment.</span></span> <span data-ttu-id="566be-120">In tal caso, tuttavia, il caricatore della topologia deve essere un componente attendibile.</span><span class="sxs-lookup"><span data-stu-id="566be-120">(In that case, however, the topology loader must be a trusted component.</span></span> <span data-ttu-id="566be-121">Per ulteriori informazioni, vedere [percorso multimediale protetto](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="566be-121">For more information, see [Protected Media Path](protected-media-path.md).)</span></span>

<span data-ttu-id="566be-122">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="566be-122">This section contains the following topics.</span></span>



| <span data-ttu-id="566be-123">Argomento</span><span class="sxs-lookup"><span data-stu-id="566be-123">Topic</span></span>                                                                          | <span data-ttu-id="566be-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="566be-124">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="566be-125">Caricatori topologia personalizzati</span><span class="sxs-lookup"><span data-stu-id="566be-125">Custom Topology Loaders</span></span>](custom-topology-loaders.md)                         | <span data-ttu-id="566be-126">Come fornire un'implementazione personalizzata di [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) per la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="566be-126">How to provide a custom implementation of [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) for the Media Session.</span></span>          |
| [<span data-ttu-id="566be-127">Associazione di nodi di output a sink di supporto</span><span class="sxs-lookup"><span data-stu-id="566be-127">Binding Output Nodes to Media Sinks</span></span>](binding-output-nodes-to-media-sinks.md) | <span data-ttu-id="566be-128">Come preparare i nodi di output in una topologia se si usa il caricatore della topologia al di fuori della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="566be-128">How to prepare the output nodes in a topology if you are using the topology loader outside of the Media Session.</span></span> |
| [<span data-ttu-id="566be-129">Aggiunta di un decodificatore a una topologia</span><span class="sxs-lookup"><span data-stu-id="566be-129">Adding a Decoder to a Topology</span></span>](adding-a-decoder-to-a-topology.md)           | <span data-ttu-id="566be-130">Come selezionare un decodificatore manualmente e aggiungerlo a una topologia.</span><span class="sxs-lookup"><span data-stu-id="566be-130">How to select a decoder manually and add it to a topology.</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="566be-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="566be-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="566be-132">Topologie</span><span class="sxs-lookup"><span data-stu-id="566be-132">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



