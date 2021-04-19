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
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a>Uso di Canvas e interfacce visive di XPS OM

In questo argomento viene descritto come utilizzare le interfacce correlate all'area di disegno dell'API documenti XPS in un modello OM XPS.

| Nome interfaccia                                  | Interfacce figlio logiche                                                                                                                    | Descrizione                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Classe base delle interfacce che definiscono oggetti visivi, ad esempio testo e grafica.<br/> Gli oggetti visivi possono essere raccolti in un'interfaccia [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) .<br/> |
| [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Raccolta di oggetti visivi che possono essere considerati come un singolo oggetto visivo.<br/>                                                                                                                                |
[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) è l'interfaccia di base. gli oggetti visibili di una pagina ereditano da esso. [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) eredita da [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) e consente di raggruppare e agire su molti altri elementi visivi come singolo elemento visivo. Ad esempio, è possibile usare un'interfaccia [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) per creare un banner di pagina che contiene una raccolta di elementi grafici e di testo. Un banner di questo tipo potrebbe contenere un logo, il motto della società e l'indirizzo della società. È possibile inserire tutti questi elementi in [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) di un'interfaccia [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) , quindi applicare una singola trasformazione all'oggetto [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) per ridimensionarla in una pagina specifica. Si tratta di un'operazione molto più semplice rispetto all'elaborazione e all'applicazione di una trasformazione a ogni singolo componente visivo nel banner.

È anche possibile usare un'area di disegno per ridimensionare il contenuto della pagina in base alle dimensioni correnti della pagina. A tale scopo, inserire tutto il contenuto della pagina in un'unica area di disegno, quindi applicare la trasformazione appropriata per adattare l'area di disegno alle dimensioni della pagina corrente. Si tratta di un'operazione molto più semplice rispetto al tentativo di ridimensionare ogni elemento visivo nella raccolta di oggetti visivi nella pagina.

## <a name="move-page-contents-to-a-canvas"></a>Spostare il contenuto della pagina in un'area di disegno

L'esempio di codice seguente sposta il contenuto di una pagina in un'area di disegno.

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

## <a name="related-topics"></a>Argomenti correlati

<dl> 
  Interfaccia <dt>[**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>Interface
  <dt>[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>Interface
  <dt>[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</dl>
