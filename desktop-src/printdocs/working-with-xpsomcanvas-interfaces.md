---
title: Canvas e interfacce visive di XPS OM
description: In questo argomento viene descritto come utilizzare le interfacce correlate all'area di disegno dell'API documenti XPS in un modello OM XPS.
ms.assetid: 368b8c47-9803-42ee-a3a8-681bf55315ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8bd15333c2786801900b09b32eb6cd59121af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313534"
---
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a><span data-ttu-id="13cc9-103">Uso di Canvas e interfacce visive di XPS OM</span><span class="sxs-lookup"><span data-stu-id="13cc9-103">Working with XPS OM Canvas and Visual Interfaces</span></span>

<span data-ttu-id="13cc9-104">In questo argomento viene descritto come utilizzare le interfacce correlate all'area di disegno dell'API documenti XPS in un modello OM XPS.</span><span class="sxs-lookup"><span data-stu-id="13cc9-104">This topic describes how to use the canvas-related interfaces of the XPS Document API in an XPS OM.</span></span>

| <span data-ttu-id="13cc9-105">Nome interfaccia</span><span class="sxs-lookup"><span data-stu-id="13cc9-105">Interface name</span></span>                                  | <span data-ttu-id="13cc9-106">Interfacce figlio logiche</span><span class="sxs-lookup"><span data-stu-id="13cc9-106">Logical child interfaces</span></span>                                                                                                                    | <span data-ttu-id="13cc9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13cc9-107">Description</span></span>                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13cc9-108">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="13cc9-108">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [<span data-ttu-id="13cc9-109">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="13cc9-109">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="13cc9-110">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="13cc9-110">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="13cc9-111">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="13cc9-111">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | <span data-ttu-id="13cc9-112">Classe base delle interfacce che definiscono oggetti visivi, ad esempio testo e grafica.</span><span class="sxs-lookup"><span data-stu-id="13cc9-112">The base class of the interfaces that define visual objects, such as text and graphics.</span></span><br/> <span data-ttu-id="13cc9-113">Gli oggetti visivi possono essere raccolti in un'interfaccia [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) .</span><span class="sxs-lookup"><span data-stu-id="13cc9-113">Visual objects can be collected in an [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) interface.</span></span><br/> |
| [<span data-ttu-id="13cc9-114">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="13cc9-114">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [<span data-ttu-id="13cc9-115">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="13cc9-115">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="13cc9-116">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="13cc9-116">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="13cc9-117">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="13cc9-117">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | <span data-ttu-id="13cc9-118">Raccolta di oggetti visivi che possono essere considerati come un singolo oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="13cc9-118">A collection of visual objects that can be treated as a single visual object.</span></span><br/>                                                                                                                                |
<span data-ttu-id="13cc9-119">[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) è l'interfaccia di base. gli oggetti visibili di una pagina ereditano da esso.</span><span class="sxs-lookup"><span data-stu-id="13cc9-119">[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) is the base interface; the visible objects of a page inherit from it.</span></span> <span data-ttu-id="13cc9-120">[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) eredita da [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) e consente di raggruppare e agire su molti altri elementi visivi come singolo elemento visivo.</span><span class="sxs-lookup"><span data-stu-id="13cc9-120">[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) inherits from [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) and enables many other visual elements to be grouped and acted upon as a single visual element.</span></span> <span data-ttu-id="13cc9-121">Ad esempio, è possibile usare un'interfaccia [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) per creare un banner di pagina che contiene una raccolta di elementi grafici e di testo.</span><span class="sxs-lookup"><span data-stu-id="13cc9-121">For example, you could use an [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) interface to create a page banner that contains a collection of text and graphical elements.</span></span> <span data-ttu-id="13cc9-122">Un banner di questo tipo potrebbe contenere un logo, il motto della società e l'indirizzo della società.</span><span class="sxs-lookup"><span data-stu-id="13cc9-122">Such a banner might contain a logo, the company slogan, and the company address.</span></span> <span data-ttu-id="13cc9-123">È possibile inserire tutti questi elementi in [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) di un'interfaccia [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) , quindi applicare una singola trasformazione all'oggetto [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) per ridimensionarla in una pagina specifica.</span><span class="sxs-lookup"><span data-stu-id="13cc9-123">You could place all these elements into the [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) of an [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) interface, and then apply a single transform to the [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) object to resize it to a particular page.</span></span> <span data-ttu-id="13cc9-124">Si tratta di un'operazione molto più semplice rispetto all'elaborazione e all'applicazione di una trasformazione a ogni singolo componente visivo nel banner.</span><span class="sxs-lookup"><span data-stu-id="13cc9-124">This is much simpler than computing and applying a transform to each individual visual component in the banner.</span></span>

<span data-ttu-id="13cc9-125">È anche possibile usare un'area di disegno per ridimensionare il contenuto della pagina in base alle dimensioni correnti della pagina.</span><span class="sxs-lookup"><span data-stu-id="13cc9-125">You can also use a canvas to resize the page contents to fit the current page size.</span></span> <span data-ttu-id="13cc9-126">A tale scopo, inserire tutto il contenuto della pagina in un'unica area di disegno, quindi applicare la trasformazione appropriata per adattare l'area di disegno alle dimensioni della pagina corrente.</span><span class="sxs-lookup"><span data-stu-id="13cc9-126">To accomplish this, place all contents of the page into a single canvas, then apply the appropriate transform to fit the canvas to the current page size.</span></span> <span data-ttu-id="13cc9-127">Si tratta di un'operazione molto più semplice rispetto al tentativo di ridimensionare ogni elemento visivo nella raccolta di oggetti visivi nella pagina.</span><span class="sxs-lookup"><span data-stu-id="13cc9-127">This is also much simpler than trying to resize each visual element in the collection of visuals in the page.</span></span>

## <a name="move-page-contents-to-a-canvas"></a><span data-ttu-id="13cc9-128">Spostare il contenuto della pagina in un'area di disegno</span><span class="sxs-lookup"><span data-stu-id="13cc9-128">Move page contents to a canvas</span></span>

<span data-ttu-id="13cc9-129">L'esempio di codice seguente sposta il contenuto di una pagina in un'area di disegno.</span><span class="sxs-lookup"><span data-stu-id="13cc9-129">The following code example moves the contents of a page to a canvas.</span></span>

```C++
    HRESULT                   hr = S_OK;

    IXpsOMVisualCollection    *pageVisuals;
    IXpsOMVisualCollection    *canvasVisuals;
    IXpsOMVisual              *oneVisual;
    IXpsOMCanvas              *newPageCanvas;

    UINT32 numVisuals = 0;
    UINT32 thisVisual;

    // get the page's visual collection
    // and how many objects it contains
    hr = page->GetVisuals( &pageVisuals );
    hr = pageVisuals->GetCount ( &numVisuals );

    // create the new canvas object and
    // its (empty) visual collection
    hr = xpsFactory->CreateCanvas ( &newPageCanvas );
    hr = newPageCanvas->GetVisuals ( &canvasVisuals );

    // go through the page's list of visual objects,
    //  move each one from the page's list to the canvas' list
    //  release the local pointer
    //  remove it from the page's collection
    thisVisual = 0;
    while (thisVisual < numVisuals) {
        hr = pageVisuals->GetAt (0, &oneVisual);
        hr = canvasVisuals->Append (oneVisual);
        hr = pageVisuals->RemoveAt (0);
        thisVisual++;
    }
    // the page's visual collection should be empty
    hr = pageVisuals->GetCount (&numVisuals);
    _ASSERT (0 == numVisuals);

    // add the new canvas to the page's visual collection
    pageVisuals->Append ( newPageCanvas );

```

## <a name="related-topics"></a><span data-ttu-id="13cc9-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13cc9-130">Related topics</span></span>

<dl> 
  <span data-ttu-id="13cc9-131">Interfaccia <dt>[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>Interface
  <dt>[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>Interface
  <dt>[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</span><span class="sxs-lookup"><span data-stu-id="13cc9-131"><dt>[**IXpsOMCanvas Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>
  <dt>[**IXpsOMVisual Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>
  <dt>[**IXpsOMVisualCollection Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</span></span></dl>
