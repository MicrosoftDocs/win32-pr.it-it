---
description: Tablet PC include la tecnologia per il riconoscimento dell'input penna più comunemente sotto forma di grafia.
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: Informazioni sul riconoscimento della grafia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff794f018cd0019a5013bacf8b9edfbe45018d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319578"
---
# <a name="about-handwriting-recognition"></a><span data-ttu-id="b6303-103">Informazioni sul riconoscimento della grafia</span><span class="sxs-lookup"><span data-stu-id="b6303-103">About Handwriting Recognition</span></span>

<span data-ttu-id="b6303-104">Tablet PC include la tecnologia per il riconoscimento dell'input penna più comunemente sotto forma di grafia.</span><span class="sxs-lookup"><span data-stu-id="b6303-104">Tablet PC includes technology for recognizing ink input that is most commonly in the form of handwriting.</span></span> <span data-ttu-id="b6303-105">Il modulo software che fornisce il riconoscimento è denominato riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="b6303-105">The software module that provides the recognition is called a recognizer.</span></span> <span data-ttu-id="b6303-106">Un riconoscimento riconosce una lingua, un gruppo di linguaggi correlati o una classe di oggetti correlati, ad esempio note musicali, movimenti di sistema o forme geometriche.</span><span class="sxs-lookup"><span data-stu-id="b6303-106">A recognizer recognizes one language, a group of related languages, or a class of related objects such as musical notes, system gestures, or geometric shapes.</span></span> <span data-ttu-id="b6303-107">È possibile aggiungere in modo dinamico i riconoscitori al sistema dei servizi Ink.</span><span class="sxs-lookup"><span data-stu-id="b6303-107">You can dynamically add recognizers to the ink services system.</span></span>

## <a name="recognition-steps"></a><span data-ttu-id="b6303-108">Procedura di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="b6303-108">Recognition Steps</span></span>

<span data-ttu-id="b6303-109">Il riconoscimento viene gestito tramite l'utilizzo di un contesto di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="b6303-109">Recognition is handled through the use of a recognizer context.</span></span> <span data-ttu-id="b6303-110">Il riconoscimento è costituito da quattro passaggi di base:</span><span class="sxs-lookup"><span data-stu-id="b6303-110">Recognition consists of four basic steps:</span></span>

1.  <span data-ttu-id="b6303-111">Configurazione dei vincoli di riconoscimento:</span><span class="sxs-lookup"><span data-stu-id="b6303-111">Setting up the recognition constraints by:</span></span>
    -   <span data-ttu-id="b6303-112">Selezione del riconoscimento e della modalità di input (vincoli geometrici).</span><span class="sxs-lookup"><span data-stu-id="b6303-112">Selecting the recognizer and input mode (geometric constraints).</span></span>
    -   <span data-ttu-id="b6303-113">Impostazione dei vincoli della lingua.</span><span class="sxs-lookup"><span data-stu-id="b6303-113">Setting the language constraints.</span></span> <span data-ttu-id="b6303-114">Ad esempio, è possibile limitare l'input ai caratteri alfanumerici oppure è possibile passare gli schemi per facilitare il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="b6303-114">For example, you can restrict input to alphanumeric characters or you can pass schemas to assist the recognizer.</span></span>
2.  <span data-ttu-id="b6303-115">Invio dell'input penna al riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="b6303-115">Sending ink to the recognizer.</span></span>
3.  <span data-ttu-id="b6303-116">Elaborazione dell'input (riconoscimento).</span><span class="sxs-lookup"><span data-stu-id="b6303-116">Processing the input (recognizing).</span></span>
4.  <span data-ttu-id="b6303-117">Restituzione dei risultati del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="b6303-117">Returning the results of the recognition.</span></span>

<span data-ttu-id="b6303-118">I passaggi 2 e 3 possono essere ripetuti in un ciclo oppure tutti i tratti di input penna possono essere aggiunti all'input penna prima del tentativo di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="b6303-118">Steps 2 and 3 may be repeated in a loop, or all of the ink strokes may be added to the ink before recognition is attempted.</span></span>

## <a name="samples-and-related-topics"></a><span data-ttu-id="b6303-119">Esempi e argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b6303-119">Samples and Related Topics</span></span>

<span data-ttu-id="b6303-120">Nell' [esempio Advanced Recognition](advanced-recognition-sample.md) viene illustrato come utilizzare i riconoscitori con oggetti [**Ink**](inkdisp-class.md) per eseguire il riconoscimento dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="b6303-120">[Advanced Recognition Sample](advanced-recognition-sample.md) demonstrates how to use recognizers with [**Ink**](inkdisp-class.md) objects to perform ink recognition.</span></span>

<span data-ttu-id="b6303-121">Il [modello di esempio della DLL di riconoscimento](recognizer-dll-sample-template.md) contiene un modello per la creazione di una dll del riconoscitore.</span><span class="sxs-lookup"><span data-stu-id="b6303-121">[Recognizer DLL Sample Template](recognizer-dll-sample-template.md) contains a template for creating a recognizer DLL.</span></span> <span data-ttu-id="b6303-122">Il modello contiene funzioni per la registrazione e l'annullamento della registrazione del server, nonché scheletri per le funzioni di riconoscimento primarie.</span><span class="sxs-lookup"><span data-stu-id="b6303-122">The template contains functions for registering and unregistering the server, as well as skeletons for primary recognizer functions.</span></span>

<span data-ttu-id="b6303-123">Nelle sezioni seguenti vengono descritti i concetti di base della tecnologia di riconoscimento dei Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="b6303-123">The following sections describe the basic concepts behind the Tablet PC recognition technology.</span></span> <span data-ttu-id="b6303-124">Per informazioni dettagliate sulla creazione di riconoscitori personalizzati, vedere [creazione di un riconoscimento](creating-a-recognizer.md).</span><span class="sxs-lookup"><span data-stu-id="b6303-124">For detailed information about creating custom recognizers, see [Creating a Recognizer](creating-a-recognizer.md).</span></span>

-   [<span data-ttu-id="b6303-125">Riconoscitori di testo</span><span class="sxs-lookup"><span data-stu-id="b6303-125">Text Recognizers</span></span>](text-recognizers.md)
-   [<span data-ttu-id="b6303-126">Riconoscitori di oggetti</span><span class="sxs-lookup"><span data-stu-id="b6303-126">Object Recognizers</span></span>](object-recognizers.md)
-   [<span data-ttu-id="b6303-127">Uso della raccolta Recognizers</span><span class="sxs-lookup"><span data-stu-id="b6303-127">Using the Recognizers Collection</span></span>](using-the-recognizers-collection.md)
-   [<span data-ttu-id="b6303-128">Contesto di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="b6303-128">Recognizer Context</span></span>](recognizer-context.md)
-   [<span data-ttu-id="b6303-129">Segmenti di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="b6303-129">Recognition Segments</span></span>](recognition-segments.md)
-   [<span data-ttu-id="b6303-130">Riconoscimento del testo angolato</span><span class="sxs-lookup"><span data-stu-id="b6303-130">Recognition of Angled Text</span></span>](recognition-of-angled-text.md)
-   [<span data-ttu-id="b6303-131">Supporto per il riordinamento del tratto del riconoscimento</span><span class="sxs-lookup"><span data-stu-id="b6303-131">Recognizer Stroke Reordering Support</span></span>](recognizer-stroke-reordering-support.md)
-   [<span data-ttu-id="b6303-132">Dizionari e factoids</span><span class="sxs-lookup"><span data-stu-id="b6303-132">Dictionaries and Factoids</span></span>](dictionaries-and-factoids.md)
-   <span data-ttu-id="b6303-133">[Proprietà confidenza \[ sul riconoscimento\]](confidence-property--about-recognition.md)</span><span class="sxs-lookup"><span data-stu-id="b6303-133">[Confidence Property \[About Recognition\]](confidence-property--about-recognition.md)</span></span>
-   [<span data-ttu-id="b6303-134">Glifi alternativi</span><span class="sxs-lookup"><span data-stu-id="b6303-134">Alternates</span></span>](alternates.md)
-   [<span data-ttu-id="b6303-135">Segmenti di input penna e alternative</span><span class="sxs-lookup"><span data-stu-id="b6303-135">Ink Segments and Alternates</span></span>](ink-segments-and-alternates.md)

 

 



