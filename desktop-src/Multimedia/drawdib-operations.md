---
title: Operazioni DrawDib
description: Operazioni DrawDib
ms.assetid: 785ad42e-0c77-44a4-b4ef-be2a0ee2b563
keywords:
- DrawDib, informazioni
- DrawDib, accesso
- DrawDib, apertura
- DrawDib, operazioni
- DrawDib, contesto di dispositivo (DC)
- CONTROLLER di dominio (contesto di dispositivo)
- DrawDibOpen (funzione)
- DrawDibClose (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc366287cdf481d70ef03aa82df5ea248673280b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471750"
---
# <a name="drawdib-operations"></a><span data-ttu-id="19f3a-111">Operazioni DrawDib</span><span class="sxs-lookup"><span data-stu-id="19f3a-111">DrawDib Operations</span></span>

<span data-ttu-id="19f3a-112">È possibile accedere all'intero gruppo di funzioni DrawDib usando la funzione [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) .</span><span class="sxs-lookup"><span data-stu-id="19f3a-112">You can access the entire group of DrawDib functions by using the [**DrawDibOpen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) function.</span></span> <span data-ttu-id="19f3a-113">Questa funzione carica la libreria di collegamento dinamico (DLL), alloca le risorse di memoria, crea un contesto di dispositivo DrawDib (DC) e mantiene un conteggio dei riferimenti del numero di controller di dominio inizializzati.</span><span class="sxs-lookup"><span data-stu-id="19f3a-113">This function loads the dynamic-link library (DLL), allocates memory resources, creates a DrawDib device context (DC), and maintains a reference count of the number of DCs that are initialized.</span></span> <span data-ttu-id="19f3a-114">**DrawDibOpen** restituisce anche un handle del nuovo controller di dominio usato con le altre funzioni DrawDib.</span><span class="sxs-lookup"><span data-stu-id="19f3a-114">**DrawDibOpen** also returns a handle of the new DC that you use with the other DrawDib functions.</span></span>

<span data-ttu-id="19f3a-115">È possibile rilasciare un controller di dominio DrawDib al termine dell'uso usando la funzione [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) .</span><span class="sxs-lookup"><span data-stu-id="19f3a-115">You can release a DrawDib DC when you finish using it by using the [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) function.</span></span> <span data-ttu-id="19f3a-116">**DrawDibClose** decrementa anche il conteggio dei riferimenti delle applicazioni che accedono alla dll.</span><span class="sxs-lookup"><span data-stu-id="19f3a-116">**DrawDibClose** also decrements the reference count of the applications accessing the DLL.</span></span> <span data-ttu-id="19f3a-117">La chiamata a **DrawDibClose** deve essere l'ultima funzione DrawDib nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="19f3a-117">The call to **DrawDibClose** should be the last DrawDib function in your application.</span></span>

<span data-ttu-id="19f3a-118">È possibile creare tutti i controller di dominio DrawDib desiderati.</span><span class="sxs-lookup"><span data-stu-id="19f3a-118">You can create as many DrawDib DCs as you want.</span></span> <span data-ttu-id="19f3a-119">È possibile usare più controller di dominio DrawDib per creare diverse bitmap simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="19f3a-119">You can use multiple DrawDib DCs to draw several bitmaps simultaneously.</span></span> <span data-ttu-id="19f3a-120">È anche possibile creare più controller di dominio DrawDib, ognuno con caratteristiche univoche, in modo che l'applicazione possa scegliere e quindi usare il controller di dominio con le impostazioni più appropriate.</span><span class="sxs-lookup"><span data-stu-id="19f3a-120">You can also create multiple DrawDib DCs, each with unique characteristics, so your application can choose and then use the DC with the most appropriate settings.</span></span> <span data-ttu-id="19f3a-121">Ad esempio, è possibile creare due controller di dominio DrawDib in un'applicazione: uno che visualizza un'immagine con la risoluzione normale e l'altro che visualizza una parte ingrandita dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="19f3a-121">For example, you can create two DrawDib DCs in an application: one that displays an image at its normal resolution, and the other that displays an enlarged portion of the image.</span></span>

<span data-ttu-id="19f3a-122">Per un'esecuzione efficiente, le funzioni DrawDib richiedono informazioni sulla scheda di visualizzazione e sul relativo driver.</span><span class="sxs-lookup"><span data-stu-id="19f3a-122">To run efficiently, DrawDib functions require information about the display adapter and its driver.</span></span> <span data-ttu-id="19f3a-123">Il profilo di visualizzazione viene ottenuto eseguendo una serie di test sulla scheda di visualizzazione la prima volta che si accede alla DLL contenente le funzioni DrawDib.</span><span class="sxs-lookup"><span data-stu-id="19f3a-123">The display profile is obtained by running a series of tests on the display adapter the first time the DLL containing the DrawDib functions is accessed.</span></span> <span data-ttu-id="19f3a-124">Le funzioni DrawDib utilizzano queste informazioni per tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="19f3a-124">The DrawDib functions use this information for all applications.</span></span> <span data-ttu-id="19f3a-125">È possibile ripetere questi test quando necessario tramite la funzione [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) .</span><span class="sxs-lookup"><span data-stu-id="19f3a-125">You can repeat these tests when necessary by using the [**DrawDibProfileDisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) function.</span></span>

> [!Note]  
> <span data-ttu-id="19f3a-126">Il recupero e l'archiviazione del profilo di visualizzazione è in genere una singola occorrenza.</span><span class="sxs-lookup"><span data-stu-id="19f3a-126">Retrieving and storing the display profile is typically a one-time occurrence.</span></span> <span data-ttu-id="19f3a-127">Se, tuttavia, le informazioni sul profilo vengono eliminate o nel sistema è installato un altro driver di visualizzazione, DrawDib esegue nuovamente i test.</span><span class="sxs-lookup"><span data-stu-id="19f3a-127">If, however, the profile information is deleted or another display driver is installed in the system, DrawDib reruns the tests.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="19f3a-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="19f3a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19f3a-129">Informazioni sulle funzioni DrawDib</span><span class="sxs-lookup"><span data-stu-id="19f3a-129">About the DrawDib Functions</span></span>](about-the-drawdib-functions.md)
</dt> </dl>

 

 




