---
description: È possibile modificare i grafici audio in qualsiasi momento per aggiungere o rimuovere voci o interi sottografici.
ms.assetid: b2f9ec6a-4b5b-e618-759b-d7dbc0d97ac4
title: 'Procedura: Aggiungere o rimuovere dinamicamente voci da un grafico audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb26150b5614ec53e4cc4de5af74e9a14ee2a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129767"
---
# <a name="how-to-dynamically-add-or-remove-voices-from-an-audio-graph"></a><span data-ttu-id="920df-103">Procedura: Aggiungere o rimuovere dinamicamente voci da un grafico audio</span><span class="sxs-lookup"><span data-stu-id="920df-103">How to: Dynamically Add or Remove Voices From an Audio Graph</span></span>

<span data-ttu-id="920df-104">È possibile modificare i grafici audio in qualsiasi momento per aggiungere o rimuovere voci o interi sottografici.</span><span class="sxs-lookup"><span data-stu-id="920df-104">You can change audio graphs at any time to add or remove voices or entire subgraphs.</span></span> <span data-ttu-id="920df-105">Questo argomento illustra come aggiungere o rimuovere submix Voices da un grafo creato seguendo i passaggi in [procedura: creare un grafico di elaborazione audio di base](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="920df-105">This topic shows you how to add or remove submix voices from a graph that has been created following the steps in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span> <span data-ttu-id="920df-106">Una singola voce può inviare l'output a diverse voci o a una lungo catena di voci.</span><span class="sxs-lookup"><span data-stu-id="920df-106">A single voice can send its output to several voices or to a long chain of voices.</span></span> <span data-ttu-id="920df-107">La rimozione o l'aggiunta di una singola voce può avere un effetto grande su un grafico audio.</span><span class="sxs-lookup"><span data-stu-id="920df-107">Removing or adding a single voice can have a large effect on an audio graph.</span></span>

## <a name="to-dynamically-change-an-audio-graph"></a><span data-ttu-id="920df-108">Per modificare dinamicamente un grafico audio</span><span class="sxs-lookup"><span data-stu-id="920df-108">To dynamically change an audio graph</span></span>

<span data-ttu-id="920df-109">L'aggiunta e la rimozione di voci da un grafo audio è molto simile all'aggiunta o alla rimozione di nodi da un grafico o un elenco collegato a un solo collegamento.</span><span class="sxs-lookup"><span data-stu-id="920df-109">Adding and removing voices from an audio graph is very similar to adding or removing nodes from a single-linked list or graph.</span></span>

-   <span data-ttu-id="920df-110">Per aggiungere una voce o un sottografico a un grafico audio</span><span class="sxs-lookup"><span data-stu-id="920df-110">To add a voice or subgraph to an audio graph</span></span>

    <span data-ttu-id="920df-111">Impostare l'output di una voce nel grafico, ovvero la voce padre, sulla voce da aggiungere tramite la funzione [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) .</span><span class="sxs-lookup"><span data-stu-id="920df-111">Set the output of a voice in the graph, the parent voice, to the voice to be added using the [**SetOutputVoices**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputvoices) function.</span></span> <span data-ttu-id="920df-112">Impostare l'output della nuova voce sull'elemento figlio originale della voce padre.</span><span class="sxs-lookup"><span data-stu-id="920df-112">Set the output of the new voice to the original child of the parent voice.</span></span>

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pNewVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    send.pOutputVoice = pChildVoice;
    pNewVoice->SetOutputVoices(&sendlist);
    ```

    

-   <span data-ttu-id="920df-113">Per rimuovere una voce o un sottografico da un grafico audio</span><span class="sxs-lookup"><span data-stu-id="920df-113">To remove a voice or subgraph from an audio graph</span></span>

    <span data-ttu-id="920df-114">Impostare la voce di output dell'elemento padre della voce da rimuovere al figlio della voce da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="920df-114">Set the output voice of the parent of the voice being removed to the child of the voice being removed.</span></span> <span data-ttu-id="920df-115">Se la voce da rimuovere si trova alla fine del grafico, è necessario modificare la voce padre in modo che punti alla voce Master.</span><span class="sxs-lookup"><span data-stu-id="920df-115">If the voice being removed is at the end of the graph, the parent voice should be changed to point to the master voice.</span></span>

    ```
    XAUDIO2_SEND_DESCRIPTOR send = {0, pChildVoice};
    XAUDIO2_VOICE_SENDS sendlist = {1, &send};
    pParentVoice->SetOutputVoices(&sendlist);
    ```

    

<span data-ttu-id="920df-116">Si noti che per chiarezza ogni elemento padre ha solo un elemento figlio in questi esempi.</span><span class="sxs-lookup"><span data-stu-id="920df-116">Note that for clarity each parent only has one child in these examples.</span></span> <span data-ttu-id="920df-117">Se un nodo padre ha più elementi figlio, il relativo oggetto Send includerà una matrice di voci anziché un puntatore a una sola voce.</span><span class="sxs-lookup"><span data-stu-id="920df-117">If a parent node has multiple children, its sendlist will contain an array of voices instead of a pointer to just one voice.</span></span>

## <a name="related-topics"></a><span data-ttu-id="920df-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="920df-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="920df-119">Grafici audio</span><span class="sxs-lookup"><span data-stu-id="920df-119">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="920df-120">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="920df-120">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="920df-121">Procedura: Creare un grafico di elaborazione audio di base</span><span class="sxs-lookup"><span data-stu-id="920df-121">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="920df-122">Procedura: Usare voci di missaggio secondario</span><span class="sxs-lookup"><span data-stu-id="920df-122">How to: Use Submix Voices</span></span>](how-to--use-submix-voices.md)
</dt> <dt>

[<span data-ttu-id="920df-123">Procedura: Creare una catena di effetti</span><span class="sxs-lookup"><span data-stu-id="920df-123">How to: Create an Effect Chain</span></span>](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 
