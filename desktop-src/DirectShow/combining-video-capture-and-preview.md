---
description: Combinazione di acquisizione video e anteprima
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Combinazione di acquisizione video e anteprima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d1a3dd3df30bd13aa6fdae7e39894941071df8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481173"
---
# <a name="combining-video-capture-and-preview"></a><span data-ttu-id="01325-103">Combinazione di acquisizione video e anteprima</span><span class="sxs-lookup"><span data-stu-id="01325-103">Combining Video Capture and Preview</span></span>

<span data-ttu-id="01325-104">Le sezioni precedenti descrivono come acquisire video in vari formati di file.</span><span class="sxs-lookup"><span data-stu-id="01325-104">The previous sections describe how to capture video to various file formats.</span></span> <span data-ttu-id="01325-105">La sezione anteprima del [video](previewing-video.md) descrive come compilare un grafico di anteprima in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="01325-105">The section [Previewing Video](previewing-video.md) describes how to build a live preview graph.</span></span> <span data-ttu-id="01325-106">Tuttavia, molte applicazioni devono eseguire entrambe contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="01325-106">However, many applications must do both at once.</span></span> <span data-ttu-id="01325-107">Per compilare un grafo combinato di anteprima e di scrittura di file, è sufficiente effettuare due chiamate a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):</span><span class="sxs-lookup"><span data-stu-id="01325-107">To build a combined preview and file-writing graph, simply make two calls to [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):</span></span>


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



<span data-ttu-id="01325-108">In questo codice, il generatore di grafici di acquisizione nasconde alcuni dettagli:</span><span class="sxs-lookup"><span data-stu-id="01325-108">In this code, the Capture Graph Builder is hiding some details:</span></span>

-   <span data-ttu-id="01325-109">Se il filtro di acquisizione include un pin di anteprima o un PIN della porta video, più un pin di acquisizione, il metodo [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) esegue semplicemente il rendering di entrambi i pin, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="01325-109">If the capture filter has a preview pin or video port pin, plus a capture pin, the [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method simply renders both pins, as shown in the following illustration.</span></span>

    ![Acquisisci e visualizza l'anteprima del grafico](images/vidcap04.png)

-   <span data-ttu-id="01325-111">Se il filtro ha solo un pin di acquisizione, il generatore del grafico di acquisizione usa il filtro [Smart Tee](smart-tee-filter.md) per suddividere il flusso di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="01325-111">If the filter has only a capture pin, the Capture Graph Builder uses the [Smart Tee](smart-tee-filter.md) filter to split the capture stream.</span></span> <span data-ttu-id="01325-112">La figura seguente mostra il grafico con una Smart Tee.</span><span class="sxs-lookup"><span data-stu-id="01325-112">The following illustration shows the graph with a Smart Tee.</span></span>

    ![Acquisisci e visualizza in anteprima il grafico con filtro Smart Tee](images/vidcap05.png)

<span data-ttu-id="01325-114">Il filtro Smart Tee include un pin di acquisizione e un pin di anteprima.</span><span class="sxs-lookup"><span data-stu-id="01325-114">The Smart Tee filter has a capture pin and a preview pin.</span></span> <span data-ttu-id="01325-115">Accetta un solo flusso video dal filtro di acquisizione e lo suddivide in due flussi, uno per l'acquisizione e uno per l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="01325-115">It takes a single video stream from the capture filter and splits it into two streams, one for capture and one for preview.</span></span> <span data-ttu-id="01325-116">Per mantenere la velocità effettiva sul pin di acquisizione, il pin di anteprima Elimina i frame in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="01325-116">To maintain throughput on the capture pin, the preview pin drops frames as needed.</span></span> <span data-ttu-id="01325-117">Elimina inoltre i timestamp di ogni campione prima di distribuirlo, per i motivi illustrati nell'argomento [filtri di acquisizione video DirectShow](directshow-video-capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="01325-117">It also strips the time stamps from each sample before delivering it, for the reasons discussed in the topic [DirectShow Video Capture Filters](directshow-video-capture-filters.md).</span></span>

<span data-ttu-id="01325-118">Sebbene lo Smart Tee suddivida il flusso, non duplica fisicamente i dati del video.</span><span class="sxs-lookup"><span data-stu-id="01325-118">Although the Smart Tee splits the stream, it does not physically duplicate the video data.</span></span> <span data-ttu-id="01325-119">USA invece oggetti di esempio multimediali personalizzati che condividono i buffer.</span><span class="sxs-lookup"><span data-stu-id="01325-119">Instead, it uses custom media sample objects that share the buffers.</span></span> <span data-ttu-id="01325-120">Gli esempi sono contrassegnati come "di sola lettura" per garantire che i filtri downstream non scrivano sui dati.</span><span class="sxs-lookup"><span data-stu-id="01325-120">The samples are marked "read-only" to ensure that downstream filters do not write on the data.</span></span>

<span data-ttu-id="01325-121">Se nel grafico di acquisizione è presente una finestra di anteprima, è possibile che Filter Graph Manager arresti l'intero grafico, incluso il flusso di acquisizione:</span><span class="sxs-lookup"><span data-stu-id="01325-121">If your capture graph has a preview window, several things can cause the Filter Graph Manager to stop the entire graph, including the capture stream:</span></span>

-   <span data-ttu-id="01325-122">Blocco del computer.</span><span class="sxs-lookup"><span data-stu-id="01325-122">Locking the computer.</span></span>
-   <span data-ttu-id="01325-123">Premere CTRL + ALT + CANC in un computer membro di un dominio.</span><span class="sxs-lookup"><span data-stu-id="01325-123">Pressing CTRL+ALT+DELETE on a computer that is a member of a domain.</span></span>
-   <span data-ttu-id="01325-124">Esecuzione di un'applicazione Direct3D a schermo intero, ad esempio un gioco o un screen saver.</span><span class="sxs-lookup"><span data-stu-id="01325-124">Running a full-screen Direct3D application, such as a game or screen saver.</span></span>
-   <span data-ttu-id="01325-125">Cambio di monitor o modifica della risoluzione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="01325-125">Switching monitors or changing the display resolution.</span></span>
-   <span data-ttu-id="01325-126">Esecuzione di un programma che fa in modo che Windows visualizzi una finestra di dialogo controllo dell'account utente (UAC).</span><span class="sxs-lookup"><span data-stu-id="01325-126">Running a program that causes Windows to display a User Account Control (UAC) dialog.</span></span> <span data-ttu-id="01325-127">(Windows Vista o versioni successive).</span><span class="sxs-lookup"><span data-stu-id="01325-127">(Windows Vista or later.)</span></span>
-   <span data-ttu-id="01325-128">Esecuzione di una finestra DOS a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="01325-128">Running a full-screen DOS window.</span></span>

<span data-ttu-id="01325-129">Uno di questi eventi potrebbe interrompere la sessione di acquisizione, causando possibili perdite di dati.</span><span class="sxs-lookup"><span data-stu-id="01325-129">Any of these events might interrupt the capture session, possibly causing data loss.</span></span> <span data-ttu-id="01325-130">(Ecco cosa accade internamente: il renderer video perde le risorse Direct3D o DirectDraw necessarie.</span><span class="sxs-lookup"><span data-stu-id="01325-130">(Here is what happens internally: The video renderer loses the Direct3D or DirectDraw resources that it needs.</span></span> <span data-ttu-id="01325-131">Durante il processo di recupero di tali risorse, il renderer video deve riconnettersi al filtro upstream, causando l'arresto del grafo da parte del gestore del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="01325-131">In the process of recovering those resources, the video renderer must reconnect with the upstream filter, causing the Filter Graph Manager to stop the graph.)</span></span>

<span data-ttu-id="01325-132">Di seguito sono riportate due possibili soluzioni a questo problema:</span><span class="sxs-lookup"><span data-stu-id="01325-132">Two possible solutions to this problem are the following:</span></span>

-   <span data-ttu-id="01325-133">Non includere un flusso di anteprima.</span><span class="sxs-lookup"><span data-stu-id="01325-133">Do not include a preview stream.</span></span> <span data-ttu-id="01325-134">Tuttavia, tenere presente che il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) aggiunge automaticamente una finestra di anteprima quando il dispositivo di acquisizione ha un PIN della porta video.</span><span class="sxs-lookup"><span data-stu-id="01325-134">However, be aware that the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically adds a preview window when the capture device has a video port pin.</span></span> <span data-ttu-id="01325-135">Vedere [pin della porta video nell'acquisizione di file](video-port-pins-in-file-capture.md).</span><span class="sxs-lookup"><span data-stu-id="01325-135">See [Video Port Pins in File Capture](video-port-pins-in-file-capture.md).</span></span>
-   <span data-ttu-id="01325-136">Usare il motore di buffer del flusso per inviare il flusso di anteprima a un grafico in un altro processo.</span><span class="sxs-lookup"><span data-stu-id="01325-136">Use the Stream Buffer Engine to send the preview stream to a graph in another process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01325-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="01325-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01325-138">Acquisizione di video in un file</span><span class="sxs-lookup"><span data-stu-id="01325-138">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



